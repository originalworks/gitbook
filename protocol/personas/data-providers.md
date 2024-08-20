# Data Providers

`DataProviders` are businesses in charge of any part of the music supply chain, and provide services to `RightsHolders`. As such, they are the permitted "Persona" with the role of creating new records in the Original Works Registry, and provide factual information about the assets they administer. As a sort of oracle to the network, `DataProviders` compete on Original Works to provide on metrics like cost, data integration, Integrations with payment providers, access to liquidity, ease of governance and delegation, etc.

\
Data Providers can be any of the following :&#x20;

* Digital Streaming Platform (DSP)&#x20;
* Record Labels&#x20;
* Distributors
* Copyright Societies
* Performing Rights Organizations
* Collective Management Organizations
* Participating financial Institutions & Lenders
* DeFi Protocols

> Traditionally "Oracles" provide protocols with off-chain data, but in those cases they are unbiased 3rd parties to the protocol; Therefore the term `DataProviders` seems more appropriate to describe music supply-chain admins and rights controllers, as they will require to maintain a stake of $OWN tokens and protocol validators will validate their incoming messages and transactions.

Music royalty revenue is not a traditional form of cash flow; each asset has multiple payment sources and terms, that are represented by different service providers in different jurisdictions, and therefore there is no straightforward way to accurately price a license to collect royalties from a given asset in a specific jurisdiction; If the license and underlying terms are not made public - _and they never are_ - it can be very hard to estimate or predict its future earnings and forecast future flows.\
\
Original Works solves this issue in two features available to Data Providers

1. **Creating an Original Works Record - Asset, Rights and Territory Registration** Allowing these existing service providers to publicly claim control over the share of control over assets and rights they manage in a given territory, while keeping all the underlying data about the licenses, rights holders or revenue completely private. These records are agnostic, hosting the data and international identifiers in IPFS, while the structured data required for the protocol can reside on any chain that chooses to index datapoints about these assets.
2. **Royalty Tokenization** - Licenses that have no conflicting claims can be tokenized, informing the to receive any royalty income while private sensitive information can remain off-chain. ZK proofs can be easily produced by Data Providers (at each of the rights holders' request). These proofs can validate one's earnings and his respective share against the DSP report, without revealing other members' holdings, and can be exposed to DeFi contracts with specific details about earnings or other private contract terms.\
   \
   \*In order to access Royalty Tokenization - Data Providers must assume the role of Payment Providers (see next article) and add additional stake.

This coupling of private data with immutable records ensures the full transparency and provenance about the Data Provider's managed assets and rights holders. It can then be securely and privately shared in the market by any rights holder or manager. Enabling secure access to the underlying cashflows on chain will create numerous new business opportunities for these traditional music service providers, and offer better rights/financial management tools for their customers. &#x20;
