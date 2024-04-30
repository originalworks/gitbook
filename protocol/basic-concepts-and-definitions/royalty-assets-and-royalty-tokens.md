---
description: Royalty Assets are the default mechanism for an IP Asset to be monetized.
---

# Royalty assets and Royalty Tokens

**Royalty Asset (RA)** \
The rights To Collect Revenue from a Work or Performance: A smart contract representing the right to collect revenue from any **IP Asset**. The rights holders of the **IP Asset** may approve the minting of a **Royalty Asset** (RA). \
\
When this smart contract is minted, each rights holder receives a portion of **Royalty Tokens** that represent their pro-rated split of any revenue deposited. The Original Works protocol ensures that royalties from verified [**Payment Providers**](verified-payment-providers.md) are paid to the Royalty Assets.

> IP Assets have a one-to-one relationship with Royalty Assets:\
>
>
> * **Each Royalty Asset can be associated with only one IP Asset**
> * **Each IP Asset can have only one single Royalty Asset at any given time**

**Royalty Tokens (RT):** \
Each **RA** is composed of individual **Royalty Tokens**; Each **Royalty Token** (RT) represents the smallest divisible default royalty split. All payments made to a **RA** contract are split across all **RT** holders; These tokens are transferable and fungible.

* **Royalty Token** settlement is executed using the OW native [Revenue Splits mechanism](revenue-splits.md).
* While Royalty Assets can be minted on any chain supported by the Original Works Protocol, a **Revenue Asset**, and therefor all underlying **Royalty Tokens** will always exist on the same chain under a single contract\
  \
