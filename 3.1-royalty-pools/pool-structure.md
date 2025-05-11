---
description: Privacy-preserving royalty distribution system works
---

<figure><img src="../.gitbook/assets/resources/pool_design.jpg" alt=""><figcaption></figcaption></figure>

# Operating an Original Works Royalty Pool

The `Royalty Pool` is a local database, run by OWEN client users who are also royalty administrators (collect and distribute royalty payments). This database is unique as it provides a "receipt" that proves each royalty split without revealing the remaining splits. It also allows the royalty admin to set the terms for transfer of splits or withdrawal of royalties to comply with regulations or any requirements from copyright holders.

### The key benefits of the Original Works Royalty Pools:

* Maintain your existing contracts and splits system
* OWEN automatically records rights to your Royalty Pool — both clients run locally or on your hosted setup
* Complete privacy of commercial relationships
* Full compliance with industry standards
* Cutting out intermediaries and increasing the revenue margin

### How it Works:

1. Any asset that has been successfully registered via the Original Works validator network can be tokenized, by registering the splits on your own hosted Royalty Pool
   * Royalty Pools use [Merkle Tree storage](https://docs.alchemy.com/docs/merkle-trees-in-blockchains). Think of it like a secure filing cabinet — it always uses the latest version of splits for calculations, but keeps the individual percentages private. Each asset has it's own "tree" representing its current splits state and its evolution. The pool generates statements showing each rights holder only their portion of each asset's revenue.
2. Once the pool recorded the splits, each rights holder is issued a voucher that unlocks his current split at any given moment.
3. Rights Holders can then use this voucher to claim royalties, transfer splits, prove income to 3rd parties and verify their splits.
