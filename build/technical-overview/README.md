---
description: Providing a Tech-Stack to on-ramp the existing music IP infrastructure.
---

# Technical Overview

### Design Principals

First and foremost, Original Works is designed to serve IP rights holders.\
The vast majority of global IP is monetized and administered by multiple service providers across different territories who are essentially appointed data gate-keepers and fraud detectors enabling IP holders to claim royalties. Therefore, the technical design of Original Works is intended to make their work easier, reward them for being transparent, efficient and empower their IP holders to have direct custody on their creative IP.

#### Permissionless Infrastructure Coupled with Verified Credentials&#x20;

Original Works is designed as a permissionless protocol as any IP holder or rights controller can stake $OWN to claim IP records, issue licenses and monetize them on-chain. This will allow trusted parties to use our public rails for IP registration and monetization - rights holders may validate the signatures of statements and royalty payments but will still require they trust their data providers with the data brought on-chain.\
At the same time, our mission statement is to empower IP holders and their service providers to eliminate un-matching of royalty reports, conflicting claims, fraudulent activity and other anomalies that in the music and streaming industry. To mitigate against those risks, the Original Works foundation will verify rights controllers and expose their public 0x address so anyone can verify their signature. This will allow the protocol to differentiate between verified data and payment providers.

#### Additional design principals:

* **Decentralization**: The protocol uses a combination of distributed storage and public blockchain infrastructure to ensure data is stored in a decentralized and verifiable manner, eliminating single points of failure and disincentivizing fraud.
* **Immutability**: Once recorded, data cannot be altered, ensuring the integrity of rights and ownership records.
* **Industry Standards Adoption:** Original Works ingests the most common digital messages to record IP, such as DDEX and CWR and may automatically generate ISCC codes for each record added to the protocol
* **Accessibility:** The permissionless infrastructure allows for anyone to register assets and licenses - Protocol users will immediately know if they are interacting with a verified music supply chain service provider (a verified `DataProvider)` indicating that they need to verify and trust the issuing account.
* **Balancing Privacy and Transparency**: Using several developments in cryptography and adoption by public blockchains, it is now feasible and economical to provide full turnkey solution for programmable-royalties on-chain with full privacy and immutability. Several solutions can be adopted to solve different problems&#x20;
* **Permissionless and verifiable:** verified `DataProviders` vare vetted service providers and protocol/token stakeholders, and unverified `DataProviders`can effectively launch on-chain distribution, simply by having trusted counterparties authenticate their keys.
* **Automation**: Smart contracts automate the execution of agreements, such as royalty payments against validated claims based on predefined conditions.
* **Enforcement**: Smart contracts enforce the terms of agreements without the need for intermediaries, which enables royalty collateralization at a fracture of what is would cost traditionally.

#### Tokenization

* **Self Custody (Digital Assets)**: Royalties[^1] and/or IP rights are recorded on merkle trees, ensuring complete privacy, while still allowing IP rights holders to be prove their ownership and traded on the blockchain&#x20;
* **Fractional Ownership**: Tokenization enables fractional _ownership of IP_ **or** _right to collect revenue_, allowing multiple parties to hold stakes in a single asset.
* **RWA:** We consider the underlying assets and cashflows tokenized by the Original Works Protocol to be Real World Assets as Original Works is the only protocol that supports the complex recording of multiple cashflows, licenses and administrative oversight over the same IP.

#### Zero Knowledge Proofs and Network Validators

* **Verifiable Credentials**: Using Original Works, rights holders (or their administrators) can submit verifiable credentials that a certain fact about an asset, entity, license or payment is true or not, without knowing the any other fact about the data itself. This provides two fundamental advantages: (i) **Rights Holders** can leverage their IP while protecting their privacy without relying on intermediaries, and (ii) **Service Providers** can monetize their data without any additional effort, while continuing to safeguard the rights and privacy of their customers
* **Cross-chain permissionless record keeping**: As generating verifiable proofs about privately stored data is computationally intensive and requires specialized software, Original Works has integrated Risk0 Network and allows anyone who is permitted to by the rights holder to generate proofs. At the first phase, we are leveraging&#x20;



[^1]: Revenue collected from exercising the right to distribute, perform, reproduce, etc..
