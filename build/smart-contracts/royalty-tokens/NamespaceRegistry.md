
<h2>Namespace Registry</h2>

<pre><code class="language-solidity">// SPDX-License-Identifier: Unlicensed
pragma solidity ^0.8.13;

import '@openzeppelin/contracts-upgradeable/proxy/utils/UUPSUpgradeable.sol';
import '@openzeppelin/contracts-upgradeable/utils/introspection/ERC165Upgradeable.sol';
import '@openzeppelin/contracts-upgradeable/access/OwnableUpgradeable.sol';
import './interfaces/INamespaceRegistry.sol';

contract NamespaceRegistry is
    INamespaceRegistry,
    OwnableUpgradeable,
    ERC165Upgradeable,
    UUPSUpgradeable
{
    event NamespaceEdited(address[] forAddresses, string[] newNamespaces);

    mapping(address => string) public namespaces;

    /// @custom:oz-upgrades-unsafe-allow constructor
    constructor() {
        _disableInitializers();
    }

    function initialize() public initializer {
        __Ownable_init();
    }

    function setNamespaceForAddresses(
        address[] memory addressesArray,
        string[] memory _namespaces
    ) public onlyOwner {
        require(
            addressesArray.length == _namespaces.length &&
                _namespaces.length > 0,
            'NamespaceRegistry: wrong input'
        );
        for (uint i = 0; i < addressesArray.length; i++) {
            namespaces[addressesArray[i]] = _namespaces[i];
        }
        emit NamespaceEdited(addressesArray, _namespaces);
    }

    function getNamespaceForAddress(
        address addressToCheck
    ) public view returns (string memory) {
        if (
            keccak256(abi.encodePacked(namespaces[addressToCheck])) ==
            keccak256(abi.encodePacked(''))
        ) {
            return 'UNKNOWN:';
        } else {
            return string.concat(namespaces[addressToCheck], ':');
        }
    }

    function canEditURI(
        string memory uri,
        address sender
    ) public view returns (bool) {
        bytes memory bytesUri = bytes(uri);
        uint256 namespaceLength;
        for (uint i = 0; i < bytesUri.length; i++) {
            if (
                keccak256(abi.encodePacked(bytesUri[i])) ==
                keccak256(abi.encodePacked(':'))
            ) {
                namespaceLength = i;
                break;
            }
        }

        if (namespaceLength == 0) {
            return false;
        }

        bytes memory uriNamespaceBytes = new bytes(namespaceLength);
        for (uint i = 0; i < namespaceLength; i++) {
            uriNamespaceBytes[i] = bytesUri[i];
        }

        string memory uriNamespace = string(uriNamespaceBytes);

        if (
            keccak256(abi.encodePacked(uriNamespace)) ==
            keccak256(abi.encodePacked(namespaces[sender]))
        ) {
            return true;
        } else {
            return false;
        }
    }

    function supportsInterface(
        bytes4 interfaceId
    ) public view virtual override(ERC165Upgradeable) returns (bool) {
        return
            interfaceId == type(INamespaceRegistry).interfaceId ||
            super.supportsInterface(interfaceId);
    }

    function _authorizeUpgrade(address) internal override onlyOwner {}
}
</code></pre>