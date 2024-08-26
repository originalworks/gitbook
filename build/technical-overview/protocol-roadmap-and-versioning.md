# Protocol Roadmap and Versioning

Original Works has evolved from being a vision starting 6 years ago, into a reality, by evolving alongside the industries need to manage fractional payments at scale, while remaining efficient and equitable. These challenges are getting ever more complicated with the advent of AI content, and continuous growth in monetizable UGC-based IP. \
\
To date we have deployed multiple case studies and pilots with partners along the music supply chain, and currently V0.1 is live in production, and available via revaltor labs.\
\
The documentation presented in this gitbook covers all planned features to be deployed on our testnet and later replace the contracts, which are currently deployed on our public mainnet contracts. \


**(phase 1:) POC - V0.1**\
Today [Revelator](https://www.revelator.com/) is the first digital distributor, which has implemented Royalty Tokens and is onboarding the first labels and artists, using on-chain payment for more transparent payments, protection against native currency devaluation and to access royalty advances.&#x20;

This version assumes the ISRC reported by the data provider is accurate, and does not deal with any conflicting claims.

**(phase 2:) Proof of Record - V0.2.1**\
Replying on Blob storage, ZK proofs we are able to upgrade our data model and advance towards a decentralized registry, providing provenance and several layers to mitigate fraud or conflicting registrations. This upgrade will also provide audio fingerprinting, and enable DDEX transmission.

Existing Royalty Tokens can simply swap their current identifiers (i.e. ISRC) with the new decentralized OW record.

**(phase 3:) Private Licenses - V0.2.3**

Based on the infrastructure completed in phase 2, phase 3 will allow any payment providers to register private licensing deals of any OW record, while retaining any level of privacy that is desired. Using ZK proofs, $OWN validators will be able to provide proofs to queries about it (i.e will this license be valid in 6 months). this will allow any IP license to be tokenized on-chain&#x20;

**(phase 4: Private Royalty Splits) - V0.2.5**

Merkle tree royalty pools

**(phase 5: Public Launch) V1.0**\
$OWN Staking and launch of decentralized validator network on mainnet&#x20;
