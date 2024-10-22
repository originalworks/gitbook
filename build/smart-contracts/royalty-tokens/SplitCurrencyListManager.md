
<h2>Split Currency List Manager</h2>

<pre><code class="language-solidity">// SPDX-License-Identifier: Unlicensed
pragma solidity ^0.8.13;
import '@openzeppelin/contracts-upgradeable/access/OwnableUpgradeable.sol';
import '@openzeppelin/contracts-upgradeable/proxy/utils/UUPSUpgradeable.sol';
import '@openzeppelin/contracts-upgradeable/utils/introspection/ERC165Upgradeable.sol';
import '@openzeppelin/contracts-upgradeable/token/ERC20/extensions/IERC20MetadataUpgradeable.sol';
import './interfaces/ISplitCurrencyListManager.sol';

contract SplitCurrencyListManager is
    OwnableUpgradeable,
    ISplitCurrencyListManager,
    ERC165Upgradeable,
    UUPSUpgradeable
{
    mapping(address => bool) public currencyMap;
    address[] private currencyArray;
    address public lendingCurrency;

    event CurrencyAdded(
        address currencyAddress,
        string symbol,
        string name,
        uint8 decimals
    );
    event CurrencyRemoved(address currencyAddress);
    event LendingCurrencyChanged(
        address newLendingCurrency,
        address oldLendingCurrency
    );

    /// @custom:oz-upgrades-unsafe-allow constructor
    constructor() {
        _disableInitializers();
    }

    function initialize(
        address[] memory initialList,
        address _lendingCurrency
    ) public initializer {
        __Ownable_init();
        __UUPSUpgradeable_init();
        __ERC165_init();
        setLendingCurrency(_lendingCurrency);

        currencyMap[address(0)] = true;
        currencyArray.push(address(0));
        emit CurrencyAdded(address(0), '', 'native coin', 0);

        for (uint i = 0; i < initialList.length; i++) {
            addCurrency(initialList[i]);
        }
    }

    function getCurrencyArray() external view returns (address[] memory) {
        return currencyArray;
    }

    function addCurrency(address currency) public onlyOwner {
        require(
            currencyMap[currency] == false,
            'SplitCurrencyListManager: currency already listed'
        );
        currencyMap[currency] = true;
        currencyArray.push(currency);

        string memory symbol = IERC20MetadataUpgradeable(currency).symbol();
        string memory name = IERC20MetadataUpgradeable(currency).name();
        uint8 decimals = IERC20MetadataUpgradeable(currency).decimals();

        emit CurrencyAdded(currency, symbol, name, decimals);
    }

    function removeCurrency(address currency) external onlyOwner {
        require(
            currencyMap[currency] == true,
            'SplitCurrencyListManager: currency not listed'
        );
        require(
            currency != address(0),
            'SplitCurrencyListManager: can not remove native coin address'
        );
        require(
            currency != lendingCurrency,
            'SplitCurrencyListManager: can not remove lending token address'
        );
        currencyMap[currency] = false;
        for (uint i = 0; i < currencyArray.length; i++) {
            if (currency == currencyArray[i]) {
                currencyArray[i] = currencyArray[currencyArray.length - 1];
                currencyArray.pop();
            }
        }

        emit CurrencyRemoved(currency);
    }

    function setLendingCurrency(address newLendingCurrency) public onlyOwner {
        require(
            newLendingCurrency != lendingCurrency,
            'SplitCurrencyListManager: lending currency already in use'
        );
        address oldLendingCurrency = lendingCurrency;
        lendingCurrency = newLendingCurrency;
        if (currencyMap[newLendingCurrency] == false) {
            addCurrency(newLendingCurrency);
        }
        emit LendingCurrencyChanged(newLendingCurrency, oldLendingCurrency);
    }

    function supportsInterface(
        bytes4 interfaceId
    ) public view virtual override(ERC165Upgradeable) returns (bool) {
        return
            interfaceId == type(ISplitCurrencyListManager).interfaceId ||
            super.supportsInterface(interfaceId);
    }

    function _authorizeUpgrade(address) internal override onlyOwner {}
}
</code></pre>