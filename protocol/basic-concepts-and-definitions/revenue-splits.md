# Revenue Splits

Any [**Royalty asset**](royalty-assets-and-royalty-tokens.md) or [**Royalty License**](royalty-licenses.md) allocates shares of incoming payments to different wallet addresses; With Royalty Assets, this is based on a list of token holders that may change hands, while with Royalty Licenses, the contract will list a fixed list of beneficiaries. \
While these two contracts may be chained, [**RL**](royalty-licenses.md) will always be payed out first in the order of maturity and the [**RA**](royalty-assets-and-royalty-tokens.md) (default split) will either be paid directly or at the end of the license calculations. Original Works [**Validators**](original-works-validators.md) ensure that all conditional contract logic is air tight before minting each additional license.

Original Works relayers ensure that revenue also flows between blockchains and in case an asset is minted on one chain, but paid from another chain, they are able to aggregate and execute efficient batch settlement transactions ensuring [**Payment Providers**](verified-payment-providers.md) are able to transmit a single payment order per asset without the hassle of bridges.&#x20;

All revenue paid by verified [**Payment Providers** ](verified-payment-providers.md)will first be fulfilled by any business logic governed by the license and only then send any "un-categorized" payments to the [**Royalty Asset** ](royalty-assets-and-royalty-tokens.md)0x address of the same [**IP Asset**](ip-assets.md) that is being monetized.&#x20;

**Claiming Splits**

In order to execute a Split (i.e. transmit the transaction that claims a single toekn holder's funds from the contract to their individual wallet) gas needs to be paid to the blockchain, and additional terms might need to be met, which are determined by the [**Payment Provider**](verified-payment-providers.md)

* Splits to Royalty Token Holders my be claimed automatically by the Payment Provider&#x20;
* Splits may be claimed by Royalty Token holders using the protocol Explorer
* Splits my be claimed by any network Relayer collecting fees for transaction aggregation
