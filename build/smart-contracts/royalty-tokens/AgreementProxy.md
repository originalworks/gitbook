
<h2>Agreement Proxy</h2>

<pre><code class="language-solidity">// SPDX-License-Identifier: Unlicensed
pragma solidity ^0.8.13;

import '@openzeppelin/contracts/proxy/Proxy.sol';
import '@openzeppelin/contracts/utils/StorageSlot.sol';
import '@openzeppelin/contracts/utils/Address.sol';
import '../interfaces/IAgreementProxy.sol';

contract AgreementProxy is Proxy, IAgreementProxy {
    bytes32 internal constant _IMPLEMENTATION_SLOT =
        0x360894a13ba1a3210667c828492db98dca3e2076cc3735a920a3ca505d382bbc;

    event Upgraded(address implementation);

    constructor(address initialImplementation, bytes memory data) {
        _upgradeToAndCall(initialImplementation, data);
    }

    function upgradeTo(address newImplementation) public {
        require(
            msg.sender == address(this),
            'Proxy: Can only be upgraded by itself'
        );
        require(
            Address.isContract(newImplementation),
            'ERC1967: new implementation is not a contract'
        );
        _setImplementation(newImplementation);
        emit Upgraded(newImplementation);
    }

    function _implementation() internal view override returns (address) {
        return StorageSlot.getAddressSlot(_IMPLEMENTATION_SLOT).value;
    }

    function _setImplementation(address newImplementation) private {
        require(
            Address.isContract(newImplementation),
            'ERC1967: new implementation is not a contract'
        );
        StorageSlot
            .getAddressSlot(_IMPLEMENTATION_SLOT)
            .value = newImplementation;
    }

    function _upgradeToAndCall(
        address newImplementation,
        bytes memory data
    ) internal {
        _setImplementation(newImplementation);
        if (data.length > 0) {
            Address.functionDelegateCall(newImplementation, data);
        }
    }
}
</code></pre>