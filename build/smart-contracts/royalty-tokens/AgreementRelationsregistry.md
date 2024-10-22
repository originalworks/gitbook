
<h2>Agreement Relations registry</h2>

<pre><code class="language-solidity">// SPDX-License-Identifier: Unlicensed
pragma solidity ^0.8.13;

import '@openzeppelin/contracts-upgradeable/utils/introspection/ERC165Upgradeable.sol';
import './interfaces/IAgreementRelationsRegistry.sol';

contract AgreementRelationsRegistry is
    IAgreementRelationsRegistry,
    ERC165Upgradeable
{
    mapping(address => address[]) private childParentRelations;

    function registerChildParentRelation(address parent) external {
        _checkForCircularDependency(msg.sender, parent);
        childParentRelations[msg.sender].push(parent);
    }

    function removeChildParentRelation(address parent) external {
        for (uint256 i = 0; i < childParentRelations[msg.sender].length; i++) {
            if (childParentRelations[msg.sender][i] == parent) {
                childParentRelations[msg.sender][i] = childParentRelations[
                    msg.sender
                ][childParentRelations[msg.sender].length - 1];
                childParentRelations[msg.sender].pop();
            }
        }
    }

    function _checkForCircularDependency(
        address child,
        address parent
    ) private view {
        address[] memory grandParents = childParentRelations[parent];
        for (uint256 i = 0; i < grandParents.length; i++) {
            if (grandParents[i] == child) {
                revert(
                    'AgreementRelationsRegistry: Circular dependency not allowed'
                );
            } else {
                _checkForCircularDependency(child, grandParents[i]);
            }
        }
    }

    function supportsInterface(
        bytes4 interfaceId
    ) public view virtual override(ERC165Upgradeable) returns (bool) {
        return
            interfaceId == type(IAgreementRelationsRegistry).interfaceId ||
            super.supportsInterface(interfaceId);
    }
}
</code></pre>