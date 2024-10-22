
<h2>Fee Manager</h2>

<pre><code class="language-solidity">// SPDX-License-Identifier: Unlicensed
pragma solidity ^0.8.13;
import '@openzeppelin/contracts-upgradeable/access/OwnableUpgradeable.sol';
import '@openzeppelin/contracts-upgradeable/token/ERC20/IERC20Upgradeable.sol';
import '@openzeppelin/contracts-upgradeable/token/ERC20/utils/SafeERC20Upgradeable.sol';
import '@openzeppelin/contracts-upgradeable/utils/introspection/ERC165Upgradeable.sol';
import '@openzeppelin/contracts-upgradeable/proxy/utils/UUPSUpgradeable.sol';
import './interfaces/IPaymentFeeSource.sol';
import './interfaces/ICreationFeeSource.sol';
import './interfaces/IFeeManager.sol';

contract FeeManager is
    IFeeManager,
    OwnableUpgradeable,
    UUPSUpgradeable,
    ERC165Upgradeable
{
    using SafeERC20Upgradeable for IERC20Upgradeable;

    // STORAGE

    uint256 public creationFee;
    uint256 public paymentFee;
    uint256 public paymentFeeDenominator;

    // EVENTS

    event CreationFeeChanged(uint256 creationFee);
    event PaymentFeeChanged(uint256 paymentFee);

    // INIT

    /// @custom:oz-upgrades-unsafe-allow constructor
    constructor() {
        _disableInitializers();
    }

    function initialize(
        uint256 initialCreationFee,
        uint256 initialPaymentFee
    ) public initializer {
        paymentFeeDenominator = 10 ** 18;
        __Ownable_init();
        setPaymentFee(initialPaymentFee);
        setCreationFee(initialCreationFee);
        emit CreationFeeChanged(initialCreationFee);
        emit PaymentFeeChanged(initialPaymentFee);
    }

    // GETTER

    function getFees()
        external
        view
        returns (
            uint256 _creationFee,
            uint256 _paymentFee,
            uint256 _paymentFeeDenominator
        )
    {
        return (creationFee, paymentFee, paymentFeeDenominator);
    }

    function owner()
        public
        view
        override(IFeeManager, OwnableUpgradeable)
        returns (address)
    {
        return OwnableUpgradeable.owner();
    }

    // SETTERS

    function setCreationFee(uint256 newFee) public onlyOwner {
        creationFee = newFee;
        emit CreationFeeChanged(newFee);
    }

    function setPaymentFee(uint256 newFee) public onlyOwner {
        require(
            newFee <= paymentFeeDenominator,
            'FeeManager: Payment fee greater than 100%'
        );
        paymentFee = newFee;
        emit PaymentFeeChanged(newFee);
    }

    // LOGIC

    function collectCreationFee(ICreationFeeSource from) public onlyOwner {
        from.collectFee();
    }

    function collectPaymentFee(
        IPaymentFeeSource from,
        address currency
    ) public onlyOwner {
        from.collectFee(currency);
    }

    function withdrawNativeCoins(address to) public onlyOwner {
        (bool success, ) = to.call{value: address(this).balance}('');
        if (!success) {
            revert('FeeManager: withdrawing native coins failed');
        }
    }

    function withdrawERC20(
        address payable to,
        IERC20Upgradeable token
    ) public onlyOwner {
        token.safeTransfer(to, token.balanceOf(address(this)));
    }

    function supportsInterface(
        bytes4 interfaceId
    ) public view virtual override(ERC165Upgradeable) returns (bool) {
        return
            interfaceId == type(IFeeManager).interfaceId ||
            super.supportsInterface(interfaceId);
    }

    function _authorizeUpgrade(address) internal override onlyOwner {}

    receive() external payable {}
}
</code></pre>