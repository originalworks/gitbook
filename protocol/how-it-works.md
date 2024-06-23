# How it Works

### Registering Musical Works, Recordings and licenses on chain

`DataProviders` upload specific information about each asset (`Release` or `SoundRecording`, identified by their global ISWC and ISRC records respectively) to a private IPFS node, and submit a message to the protocol, with a proof of registration, revealing _only_ the **asset identifier** (ISRC or ISWC), **`RightsCoverage[]`**, and **`Region`**.&#x20;

The protocol then validates that no proof of record with conflicting _public_ terms (unique combination of asset, specific right, region) has been registered.&#x20;

This message constitutes the `RegisteredRights` - a unique record, granting the `DataProvider` signing the registration message the sole[^1] authority to issue `Licenses` under the `RegisteredRights`.&#x20;

`Licenses` are issued against any real world agreement, that captures it's rights holders exercise of rights in a business construct - such as a distribution or royalty collection contract.

### Tokenizing Royalty Payments

Rights holders may elect to register their assets on-chain in order to anonymously and privately record and collect their royalties on chain, unlocking liquidity and making it easy to grant access to their royalty data; In order to do so, they will need to distribute their music with one of the Protocol `PaymentProviders`. All `PaymentProviders` are also `DataProviders` and if they&#x20;

### Automating Royalty Payments to Rights Holders

### Getting a Royalty Advance form and DeFi Lending Pool

<figure><img src="../.gitbook/assets/Web 3 Planning - Frame 13 (3).jpg" alt=""><figcaption></figcaption></figure>



[^1]: In v1.2 Data providers will be able to tokenize their assets and give rights holders full custody and governance over the assets
