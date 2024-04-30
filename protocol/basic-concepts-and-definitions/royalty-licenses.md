# Royalty Licenses

A Royalty License is a smart contract that is minted against any commercial agreement that requires additional split or payment other than a straight-forward splits.\
This can be used for tax withholding, ad-hoc licensing deals or any unique combination of business terms, that needs to be applied - superseding the "default" revenue split govern by the holders of [**Royalty Tokens**](royalty-assets-and-royalty-tokens.md)**.** \
\
Royalty Licenses are different from RTs as they are not based on Token distribution, but rather a JSON file representing the business terms and payment logic of the binding agreement; It has a list of payees, contractual terms and conditions, and is governed by the issuing [**IP Asset Smart Contract**](ip-assets.md).\


* Licenses do not have token holders, and are not transferrable as they are governed by off-chain agreements.&#x20;
* Licenses also have fixed terms and conditions, whereas Royalty Assets only represent the default split of any income paid.
* Royalty payments flowing on the Original Works Protocol will firstly look for any license that is directing payments based on **any set of instructions** before applying they apply splits.&#x20;
* Normally the [Royalty Asset ](royalty-assets-and-royalty-tokens.md)0x addresses, governed by the same [IP Asset](ip-assets.md) will be a party to this License, but not necessarily.
* Royalty License payments are executed using the OW native [Revenue Splits](revenue-splits.md) mechanism.
* Licenses can address business specific terms like payment to agents, 3rd parties, tax withholding, reimbursement, payable advances or any other business logic.
