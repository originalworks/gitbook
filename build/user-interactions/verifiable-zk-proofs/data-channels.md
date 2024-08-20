# Using Data Channels

### Submitting statements via Data Channels

#### Private vs. public data

Each message must reference a few fields in the header to map the message to a specific unique asset (`Creation` or `license`), the `DataProvider`'s signature and a `url` pointing to a JSON file containing the message. Among these indicators, the header may contain information about the message format so partners can easily parse it.

The json document can be any of the 4 options below, depending on the nature of the data and the business requirements; each `DataProvider` is free to customize their data structure, availability and privacy policy.

1. an IPFS document
2. a static web page
3. a dynamic web page
4. a Merkel root pointing to authentication of off-chain data

#### Metadata Schema

As a design principle, the protocol adapts music-industry message standards and has no intention of creating any new web3-specific standard. \`

We have designed the protocol namespaces to match DDEX ERN messages and recommend entrenching the usage of DDEX 4+ as a standard electronic notifications for releases, but as a permissionless protocol we allow transmission of any JSON object in reference to minted assets and licenses.\
Any counterparty that is expected to parse this data should be able to identify the format, first and foremost.

#### Suggested mandatory fields

* **Identifiers**: Unique ID for each **Asset** (**musical work** or **recording)** or **License**. Assets and licenses may be tokenized or not. These are the first primitives the protocol will define
* **Creator Information**: Details of the artist(s) and rights holders.
* **Ownership Records**: Private Information on the ownership
* **Usage Rights:** Private Information on licensing agreements, rights coveraed and territory
* **Licenses:** Licensing agreements, exercizng
* **Usage Data**: Records of how and where an asset is used.

#### Segregating data channels

We propose the usage of multiple `DataChannels` per `DataProvider`so the data will be structured easily and insights can easily be derived; Some examples of specific `DataChannels` managed by a single enterprise could be:

* **Initial Registration**: Recording the original rights holder.
* **Asset Financial prospectus:** authenticated off-chain financial records
* **Asset Analytics:** Revenue and consumption trends, patterns and insights
* **Transfers**: Documenting off-chain changes in ownership and licensing.
* **Disputes**: Mechanism for resolving disputes over ownership or rights.
