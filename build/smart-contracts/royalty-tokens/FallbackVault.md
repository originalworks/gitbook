
<h2>Fallback Vault</h2>

<pre><code class="language-solidity">// SPDX-License-Identifier: MIT

pragma solidity ^0.8.4;

import '@openzeppelin/contracts-upgradeable/security/ReentrancyGuardUpgradeable.sol';
import '@openzeppelin/contracts-upgradeable/access/OwnableUpgradeable.sol';
import '@openzeppelin/contracts-upgradeable/utils/introspection/ERC165Upgradeable.sol';
import '@openzeppelin/contracts-upgradeable/proxy/utils/UUPSUpgradeable.sol';
import '@original-works/contracts-shared/contracts/CallHelpers/CallHelpers.sol';
import './interfaces/IFallbackVault.sol';

contract FallbackVault is
    IFallbackVault,
    ReentrancyGuardUpgradeable,
    OwnableUpgradeable,
    ERC165Upgradeable,
    UUPSUpgradeable
{
    mapping(address => uint256) public balances;

    event Withdrawn(address _user, uint256 _amount);

    /// @custom:oz-upgrades-unsafe-allow constructor
    constructor() {
        _disableInitializers();
    }

    function initialize() public initializer {
        __ReentrancyGuard_init();
        __Ownable_init();
        __ERC165_init();
    }

    function withdrawFor(address user, uint256 gasLimit) external {
        _withdraw(user, user, gasLimit);
    }

    function withdraw(address receiver, uint256 gasLimit) external {
        _withdraw(msg.sender, receiver, gasLimit);
    }

    function _withdraw(
        address user,
        address receiver,
        uint256 gasLimit
    ) internal nonReentrant {
        uint256 amount = balances[user];
        require(amount > 0, 'FallbackVault: no funds to withdraw');
        balances[user] = 0;
        bool success;
        bytes memory response;
        if (gasLimit != 0) {
            (success, response) = receiver.call{value: amount, gas: gasLimit}(
                ''
            );
        } else {
            (success, response) = receiver.call{value: amount}('');
        }

        if (!success) {
            string memory message = CallHelpers.getRevertMsg(response);
            revert(message);
        }

        emit Withdrawn(user, amount);
    }

    function registerIncomingFunds(address user) external payable {
        balances[user] += msg.value;
    }

    function supportsInterface(
        bytes4 interfaceId
    ) public view virtual override(ERC165Upgradeable) returns (bool) {
        return
            interfaceId == type(IFallbackVault).interfaceId ||
            super.supportsInterface(interfaceId);
    }

    function _authorizeUpgrade(address) internal override onlyOwner {}

    receive() external payable {}
}
</code></pre>