# $OWN Tokenomics

### Token Model

The **$OWN** Utility Token is used to pay fees to the Original Works protocol and between protocol users, as well as govern the OWN Protocol.&#x20;

The core reason for the existance of the $OWN token is to incentivize the protocol participants to act in the common good of the OWN Protocol. The music industry is fragmented among many players whose incentives do not always align. This includes: artists and rights holders, record labels, distributors, publishers, music fans, investors and developers. An ecosystem that is greater than the sum of its parts will grow the pie for everyone, creating a more collaborative industry, benefiting all participants. The $OWN token assists this alignment of interests by ensuring that network participants are rewarded for the work they contribute to the protocol:

* Music distributors act as Royalty admin, bridging cash flow from traditional music rails to web3. They are the bridge and Royalty admin of cash flows. In return for this service they receive a new revenue stream in the form of fees and new business opportunities, such as cash advances and being able to provide sophisticated data models around music assets.
* Publishers and Music associations act as Data Providers around relevant music records, ensuring that Royalty Tokens have the correct data associated with their rights. This creates value for artists as they will now be able to license their music rights more easily and receive advances from more participants. Data Providers receive fees from `rightsholders` in return for the data they provide.
* Artists and `rightsholders` elect to tokenize music assets into Royalty Tokens and be paid on chain, bridging their cash flow from web2 to web3. This enables them to gain access to a new world of financial products, such as DeFi, and new communities to incentivize fans, such as royalty splits. They agree to pay fees to their Payment and Data Provider oRoyalty admins in return for these new opportunities.&#x20;
* Developers, fans and entrepreneurs can create new products to interact with Royalty Token music assets, whether in fan engagement or financial products. They can elect to use unique data provided by Data Providers or private data revealed by `rightsholders` (if they so choose) and in return pay these participants for this data.&#x20;

The $OWN token enables mechanisms of rewards (fees paid to service providers) and slashing (punishments for misbehavior) for the different actors ensuring that they perform properly.

### Slashing

Royalty admins who are found to be fraudulent actors can expect to have their stake penalized, the size of the slash amount depends on the type of network fault. Fraudulent behavior by Payment Providers includes:

* Not transmitting funds on chain to a relevant RT in a timely fashion, despite receiving the funds from DSPs or other rights management companies/participants, because of:
  * Internal mismanagement of funds - 1% slashing penalty of staked amount for each two week delay in payment.
  * The artist requests the Royalty admin to resume payments off-chain and the Royalty admin does this without checking whether the RT royalty flow is committed to another party, such as being part of a Defi contract (i.e it is being used as collateral) - 10% slashing penalty of staked amount.
* Providing an asset fact sheet that is incorrect or unavailable:
  * Misreporting asset revenue history in the RT prospectus - 5% slashing penalty of staked amount.
  * Misreporting known claims and red flags - 5% slashing penalty of staked amount.
  * Not ensuring the liveness of the asset fact sheet - 2% slashing penalty of staked amount.

It’s important to note that Royalty admins are only slashed for things under their direct control. They do not get slashed for events or data that are not, this includes a DSP not transmitting payments in a timely fashion or if they manage distribution for an artist who commits fraud and misrepresents data or cash flow for their music.

#### Cool down period

Royalty admins who wish to leave the protocol can unstake their $OWN six months after they stop being a Royalty Admin. The music industry has long payment periods, therefore a longer cool down period is needed so that fraud nodes can submit relevant fraud proofs if needed. During this period rewards continue to accrue and governance position is weighted as normal.&#x20;

\
