# Data Providers

`DataProviders` are businesses in charge of any part of the music supply chain, and provide services to `Rights Holders`. As such, they are the permitted "Persona" to create new records in the Original Works Registry, and provide factual information about the assets they administer. As a sort of oracle to the network, `DataProviders` compete on Original Works to provide on metrics like cost, data integration, offramp solutions, access to liquidity, ease of governance and delegation, etc..&#x20;

\
Data Providers can be any of the following :&#x20;

* Digital Streaming Providers (DSP)&#x20;
* Record Labels&#x20;
* Distributors
* Copyright Societies
* Performing Rights Organizations
* Collective Management Organizations
* Participating financial Institutions & Lenders
* DeFi Protocols

> Traditionally "Oracles" provide protocols with off-chain data, but in those cases they are unbiased 3rd parties to the protocol; Therefore the term `DataProviders` seems more appropriate to describe music supply-chain admins and rights controllers, as they may be in conflict of interest to other protocol users.&#x20;

Music royalty streams are not a traditional form of cash flow; each asset has multiple payment sources and terms, that are represented by different service providers in different jurisdictions, and therefore there is no straightforward way to evaluate a specific `License` to collect royalties from a given asset; If the `License` and underlying asset is not tokenized _and_ made public, it can be very hard to estimate or predict its future earnings and forecast future flows.

`DataProviders` ("DP"s) are ecosystem players in the OWN protocol who have the ability to register an asset on chain, keeping it private, while securely and privately making any proof request accessible to permitted wallets and contracts.&#x20;

In order to methodologically ensure data integrity and availability, `DataProviders` on Original Works can submit Zero Knowledge Proofs - Verifiable Credentials about private and immutable records on assets, ownership, licenses, revenue and payments.

Proofs are validated by `Validators`, but will initially be outsourced to Chainlink Functions to ensure decentralization.\
Alternatively, if potential purchasers/lenders/collaborators can receive provable statements originating from a public immutable registry they can begin to mark assets to market and price music IP.&#x20;

### Verified Data Providers

To provide Trust and Safety and to ensure lawful implementation of IP and royalties management, while keeping the protocol permissionless and accessible, the Original Works Foundation will verify and validate any interested Data Provider. The "Verified" blue check ensures that the public key signing the creation or interaction with an asset or license is done by a verified music supply chain company

As a permissionless protocol, anyone can call the registry contract and enter records. Trusted parties in developing countries, lacking royalties Infrastructure for example can use the protocol and validate keys directly amongst themselves, even if the Original Works protocol is unable to do so at first. They will have to bare the cost of doing so and will contribute to the diversity of the . If at any point, assets they have registered are claimed by a Verified`Data Provider`  The foundation will have to validate and verify the claims against the records of each lawful owner in any jurisdiction.&#x20;

> As our stated mission is to increase access to liquidity for the global music market, we will work towards increasing the amount of available Verified Data Providers and incentivize both on chain records and tokenization through grant programs and developer support.

### Data Provider Roles&#x20;

These are the different Data Provider Roles a DataProvider persona can assume in the protocol:

**`DataProviderRole`**: A type of role played by a Data Provider.

* `CopyrightController` - The `DataProvider` in charge of registering the asset, keeping the on-chain records available and providing verifiable proofs about the asset on-demand. As long as the IP Asset has not been tokenized by the `CopyrightHolder`(s), then the `copyrightController` remains the `admin` and acts as their on-chain representative.
* `RightsController` **-** The `DataProvider` in charge of registering a license, keeping the on-chain records available and providing verifiable proofs about the license on-demand. As long as the IP Asset has not been tokenized by the `RightHolder`(s), then the `RightsController` remains the `admin` and acts as their on-chain representative. \
  It is typically an enterprise like a music distributor or publishing admin that controls rights in one or more Creations in respect of some or all rights for specific territories, time periods,`RightsCoverage` types.
* `rightsAdministrator` - The administrator assigned by the Rights Controller in charge with administering the rights on-chain and off-chain;

### Data Channels:

As the `rightsAdministrator`or `RightsController DataProviders` can submit custom messages and attestations (As a tr
