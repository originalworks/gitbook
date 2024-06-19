# Data Channels

Data channels: Official protocol oracles are able to provide attestations about registered assets via D`ataChannels`. These may be private or public and provide immutable record of any datapoint or statement about an asset and the public signature of the message signer. Anyone can setup a data channel and message the OWN protocol with information about a registered asset, but only verified `DataProvider` signatures should be considered to be a verified data source, and are legally accountable for the information they provide. The protocol tokenomics incentivize data providers to provide accurate information on time and penalizes underperformance. \
\
Data channels may include conditional chaining logic, historic financial data, fraud clearance, rights registration or any other records.



#### Data Management

The `DataChannel` is owned by a data provider and creates an immutable record trail of statements, updates, off-chain information about any asset in the protocol - obviously statements about the assets registered by the same party should bee more trustworthy, but data channels are designed to be permissionless as they cannot trigger any native protocol action.

At the end of the day, disputes can only be settled in court, but having immutable proof of **who** claimed **what**, **when** and based on **which** datapoints, making a copyright claim or ensuring an asset isn't automatically taken down by content ID networks if it may have a license on chain becomes much more feasible



### Submitting statements via Data Channels

#### Private vs. public data

Each message must reference a few fields in the header to map the message to a specific unique asset (`Creation` or  `license`), the `DataProvider`'s signature and a `url` pointing to a JSON file containing the message.  Among these indicators, the header may contain information about the message format so partners can easily parse it.&#x20;

The json document can be any of the 4 options below, depending on the nature of the data and the business requirements; each `DataProvider` is free to customize their data structure, availability  and privacy policy.

1. an IPFS document
2. a static web page
3. a dynamic web page
4. a Merkel root pointing to authentication of off-chain data

#### Metadata Schema

As a design principle, the protocol adapts music-industry message standards and has no intention of creating any new web3-specific standard. \`

We have designed the protocol namespaces to match DDEX ERN messages and recommend entrenching the usage of DDEX 4+ as a standard electronic notifications for releases, but as a permissionless protocol we allow transmission of any JSON object in reference to minted assets and licenses. \
Any counterparty that is expected to parse this data should be able to identify the format, first and foremost.

#### Suggested mandatory fields

* **Identifiers**: Unique ID for each **Asset** (**musical work** or **recording)** or **License**. Assets and licenses may be tokenized or not. These are the first primitives the protocol will define&#x20;
* **Creator Information**: Details of the artist(s) and rights holders.
* **Ownership Records**: Private Information on the ownership
* **Usage Rights:** Private Information on licensing agreements, rights coveraed and teritory
* **Licenses:** Licensing agreements, exercizng&#x20;
* **Usage Data**: Records of how and where an asset is used.

#### Segregating data channels

We propose the usage of multiple `DataChannels` per `DataProvider`so the data will be strucutred easiliy and insights can easily be derived; Some examples of specific `DataChannels` managed by a single enterprise coul be:

* **Initial Registration**: Recording the original rights holder.
* **Asset Financial prospectus:** authenticated off-chain financial records
* **Asset Analytics:** Revenue and consumption trends, patterns and insights
* **Transfers**: Documenting off-chain changes in ownership and licensing.
* **Disputes**: Mechanism for resolving disputes over ownership or rights.

