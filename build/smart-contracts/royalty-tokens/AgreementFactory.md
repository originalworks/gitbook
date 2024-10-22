
<h2>Agreement Factory</h2>

<pre><code class="language-solidity">// SPDX-License-Identifier: Unlicensed
pragma solidity ^0.8.13;

import '@openzeppelin/contracts-upgradeable/access/OwnableUpgradeable.sol';
import '@openzeppelin/contracts-upgradeable/proxy/utils/Initializable.sol';
import '@openzeppelin/contracts-upgradeable/utils/AddressUpgradeable.sol';
import '@openzeppelin/contracts-upgradeable/utils/introspection/ERC165CheckerUpgradeable.sol';
import '@openzeppelin/contracts-upgradeable/proxy/utils/UUPSUpgradeable.sol';
import './AgreementProxy.sol';
import '../interfaces/IFeeManager.sol';
import '../interfaces/ILendingContract.sol';
import '../interfaces/IAgreementRelationsRegistry.sol';
import '../interfaces/IAgreementERC20.sol';
import '../interfaces/IAgreementERC1155.sol';
import '../interfaces/IHolder.sol';
import '../interfaces/ISplitCurrencyListManager.sol';
import '../interfaces/IFallbackVault.sol';
import '../interfaces/ICreationFeeSource.sol';
import '../interfaces/INamespaceRegistry.sol';

contract AgreementFactory is
    Initializable,
    OwnableUpgradeable,
    IHolder,
    ICreationFeeSource,
    UUPSUpgradeable
{
    using ERC165CheckerUpgradeable for address;

    IFeeManager private feeManager;
    address private lendingContract; // unused legacy parameter
    address private splitCurrencyListManager;
    address private agreementRelationsRegistry;
    address private agreementERC20Implementation;
    address private agreementERC1155Implementation;
    address private fallbackVault;
    address private namespaceRegistry;

    event AgreementCreated(
        address agreementAddress,
        address agreementImplementation
    );
    event AgreementImplementationChanged(
        address agreementImplementation,
        TokenStandard tokenStandard
    );

    event InitialRevenueStreamURISet(
        address agreementAddress,
        string[] addedUris,
        address addedByAccount
    );

    enum TokenStandard {
        ERC20,
        ERC1155
    }

    struct ICreateBatchERC20 {
        string _dataHash;
        Holder[] holders;
        string[] partialRevenueStreamURIs;
    }

    struct ICreateBatchERC1155 {
        string _dataHash;
        Holder[] holders;
        string[] partialRevenueStreamURIs;
        string contractURI;
    }

    /// @custom:oz-upgrades-unsafe-allow constructor
    constructor() {
        _disableInitializers();
    }

    function initialize(
        address _agreementERC20Implementation,
        address _agreementERC1155Implementation,
        address _feeManager,
        address _agreementRelationsRegistry,
        address _splitCurrencyListManager,
        address _fallbackVault,
        address _namespaceRegistry
    ) public initializer {
        require(
            _feeManager.supportsInterface(type(IFeeManager).interfaceId),
            'AgreementFactory: Wrong interface at FeeManager address'
        );
        require(
            _agreementRelationsRegistry.supportsInterface(
                type(IAgreementRelationsRegistry).interfaceId
            ),
            'AgreementFactory: Wrong interface at AgreementRelationsRegistry address'
        );
        require(
            _splitCurrencyListManager.supportsInterface(
                type(ISplitCurrencyListManager).interfaceId
            ),
            'AgreementFactory: Wrong interface at SplitCurrencyListManager address'
        );
        require(
            _fallbackVault.supportsInterface(type(IFallbackVault).interfaceId),
            'AgreementFactory: Wrong interface at FallbackVault address'
        );
        require(
            _namespaceRegistry.supportsInterface(
                type(INamespaceRegistry).interfaceId
            ),
            'AgreementFactory: Wrong interface at NamespaceRegistry address'
        );

        __Ownable_init();
        setAgreementImplementation(
            _agreementERC20Implementation,
            TokenStandard.ERC20
        );
        setAgreementImplementation(
            _agreementERC1155Implementation,
            TokenStandard.ERC1155
        );
        feeManager = IFeeManager(_feeManager);
        agreementRelationsRegistry = _agreementRelationsRegistry;
        splitCurrencyListManager = _splitCurrencyListManager;
        fallbackVault = _fallbackVault;
        namespaceRegistry = _namespaceRegistry;
    }

    function setNamespaceRegistryAddress(address newAddress) public onlyOwner {
        namespaceRegistry = newAddress;
    }

    function getAgreementImplementations()
        public
        view
        returns (address agreementERC20, address agreementERC1155)
    {
        return (agreementERC20Implementation, agreementERC1155Implementation);
    }

    function setAgreementImplementation(
        address newImplementation,
        TokenStandard tokenStandard
    ) public onlyOwner {
        require(
            newImplementation != address(0),
            'AgreementFactory: agreement address cannot be 0'
        );
        require(
            AddressUpgradeable.isContract(newImplementation),
            'AgreementFactory: agreement implementation must be a contract'
        );
        if (tokenStandard == TokenStandard.ERC20) {
            agreementERC20Implementation = newImplementation;
        } else {
            agreementERC1155Implementation = newImplementation;
        }
        emit AgreementImplementationChanged(newImplementation, tokenStandard);
    }

    function createERC20(
        string memory _dataHash,
        Holder[] memory holders,
        string[] memory partialRevenueStreamURIs
    ) public payable {
        (uint256 creationFee, , ) = feeManager.getFees();
        require(msg.value >= creationFee, 'AgreementFactory: Insufficient fee');

        string[] memory revenueStreamURIs = getCompleteRevenueStreamURIs(
            partialRevenueStreamURIs
        );
        bytes memory data = abi.encodeWithSelector(
            IAgreementERC20.initialize.selector,
            _dataHash,
            holders,
            splitCurrencyListManager,
            feeManager,
            agreementRelationsRegistry,
            fallbackVault,
            namespaceRegistry,
            revenueStreamURIs
        );

        AgreementProxy agreement = new AgreementProxy(
            agreementERC20Implementation,
            data
        );
        emit AgreementCreated(address(agreement), agreementERC20Implementation);
        emit InitialRevenueStreamURISet(
            address(agreement),
            revenueStreamURIs,
            msg.sender
        );
    }

    function createBatchERC20(ICreateBatchERC20[] memory input) public payable {
        (uint256 creationFee, , ) = feeManager.getFees();
        require(
            msg.value >= creationFee * input.length,
            'AgreementFactory: Insufficient fee'
        );

        for (uint i = 0; i < input.length; i++) {
            string[] memory revenueStreamURIs = getCompleteRevenueStreamURIs(
                input[i].partialRevenueStreamURIs
            );
            bytes memory data = abi.encodeWithSelector(
                IAgreementERC20.initialize.selector,
                input[i]._dataHash,
                input[i].holders,
                splitCurrencyListManager,
                feeManager,
                agreementRelationsRegistry,
                fallbackVault,
                namespaceRegistry,
                revenueStreamURIs
            );

            AgreementProxy agreement = new AgreementProxy(
                agreementERC20Implementation,
                data
            );
            emit AgreementCreated(
                address(agreement),
                agreementERC20Implementation
            );
            emit InitialRevenueStreamURISet(
                address(agreement),
                revenueStreamURIs,
                msg.sender
            );
        }
    }

    function createERC1155(
        string memory _dataHash,
        Holder[] memory holders,
        string memory contractURI,
        string[] memory partialRevenueStreamURIs
    ) public payable {
        (uint256 creationFee, , ) = feeManager.getFees();
        require(msg.value >= creationFee, 'AgreementFactory: Insufficient fee');
        string[] memory revenueStreamURIs = getCompleteRevenueStreamURIs(
            partialRevenueStreamURIs
        );
        bytes memory data = abi.encodeWithSelector(
            IAgreementERC1155.initialize.selector,
            contractURI,
            _dataHash,
            holders,
            splitCurrencyListManager,
            feeManager,
            agreementRelationsRegistry,
            fallbackVault,
            namespaceRegistry,
            revenueStreamURIs
        );

        AgreementProxy agreement = new AgreementProxy(
            agreementERC1155Implementation,
            data
        );
        emit AgreementCreated(
            address(agreement),
            agreementERC1155Implementation
        );
        emit InitialRevenueStreamURISet(
            address(agreement),
            revenueStreamURIs,
            msg.sender
        );
    }

    function createBatchERC1155(
        ICreateBatchERC1155[] memory input
    ) public payable {
        (uint256 creationFee, , ) = feeManager.getFees();
        require(
            msg.value >= creationFee * input.length,
            'AgreementFactory: Insufficient fee'
        );

        for (uint i = 0; i < input.length; i++) {
            string[] memory revenueStreamURIs = getCompleteRevenueStreamURIs(
                input[i].partialRevenueStreamURIs
            );
            bytes memory data = abi.encodeWithSelector(
                IAgreementERC1155.initialize.selector,
                input[i].contractURI,
                input[i]._dataHash,
                input[i].holders,
                splitCurrencyListManager,
                feeManager,
                agreementRelationsRegistry,
                fallbackVault,
                namespaceRegistry,
                revenueStreamURIs
            );

            AgreementProxy agreement = new AgreementProxy(
                agreementERC1155Implementation,
                data
            );
            emit AgreementCreated(
                address(agreement),
                agreementERC1155Implementation
            );
            emit InitialRevenueStreamURISet(
                address(agreement),
                revenueStreamURIs,
                msg.sender
            );
        }
    }

    function getCompleteRevenueStreamURIs(
        string[] memory partialRevenueStreamURIs
    ) private view returns (string[] memory) {
        if (partialRevenueStreamURIs.length == 0) {
            return new string[](0);
        }
        string memory namespace = INamespaceRegistry(namespaceRegistry)
            .getNamespaceForAddress(msg.sender);

        string[] memory revenueStreamURIs = new string[](
            partialRevenueStreamURIs.length
        );
        for (uint i = 0; i < partialRevenueStreamURIs.length; i++) {
            revenueStreamURIs[i] = string.concat(
                namespace,
                partialRevenueStreamURIs[i]
            );
        }

        return revenueStreamURIs;
    }

    function collectFee() external {
        require(
            msg.sender == address(feeManager),
            'AgreementFactory: Only FeeManager can collect fee'
        );
        address payable feeManagerAddr = payable(address(feeManager));
        feeManagerAddr.transfer(address(this).balance);
        emit FeeCollected(address(this).balance, address(0));
    }

    function _authorizeUpgrade(address) internal override onlyOwner {}
}
</code></pre>