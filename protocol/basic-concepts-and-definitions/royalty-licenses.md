---
description: >-
  Royalty Licenses are commercial agreements granting rights to generate,
  collect and distribute revenue from usage of the underlying intelectual
  property of an IP Asset
---

# Royalty Licenses

A Royalty License is a smart contract that is minted against any commercial agreement that requires additional split or payment other than a straight-forward splits.\
This can be used for tax withholding, ad-hoc licensing deals or any unique combination of business terms, that needs to be applied. Like [**Royalty Assets**](royalty-assets-and-royalty-tokens.md)**,** The Original Works protocol ensures that royalties from verified [**Payment Providers**](verified-payment-provider.md) are paid to the Royalty Licenses of an [**IP Asset**](ip-assets.md);

> IP Assets have a one-to-many relationship with Royalty Licenses:
>
> * **Each License can be associated with only one IP Asset**
> * **Each IP Asset can have multiple Royalty Licenses**

Royalty Licenses are different from RTs as they are not based on Token distribution, but rather a set of instructions representing the business terms and payment logic of the binding agreement; It has a list of payees, contractual terms and conditions, and is governed by the issuing [**IP Asset Smart Contract**](ip-assets.md).

**Conditional Logic and Contract Chaining:** \
Allowing the complex aspect of music licensing to exist gracefully on-chain, Royalty Licenses always supersede the "default" revenue split, which is governed by the holders of [**Royalty Tokens**](royalty-assets-and-royalty-tokens.md)**.**&#x20;

The [**Registry**](decentralized-right-registry.md) allows for each rights holder to verify and authenticate their payment shares from all associated assets

* Licenses do not have token holders, and are not transferrable as they are governed by off-chain agreements.&#x20;
* Licenses also have fixed terms and conditions, whereas Royalty Assets only represent the default
* Royalty payments flowing on the Original Works Protocol will firstly look for any license that is directing payments based on **any set of instructions** before applying they apply splits.&#x20;
* Normally the [Royalty Asset ](royalty-assets-and-royalty-tokens.md)0x addresses, governed by the same [IP Asset](ip-assets.md) will be a party to this License, but not necessarily.
* Royalty License payments are executed using the OW native [Revenue Splits](revenue-splits.md) mechanism.
* Licenses can address business specific terms like payment to agents, 3rd parties, tax withholding, reimbursement, payable advances or any other business logic.
