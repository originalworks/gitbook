# Token Economics

### Token Model

The **$OWN** Utility Token is used to pay fees to the Original Works protocol and between protocol users. While the assets tokenized using the Original Works protocol represent rights to receive revenue or govern an IP-backed asset, The $OWN Utility token is used to facilitate permissionless payments and splits to rights holders, incentivise `PaymentProviders` - the $OWN token activity should capture the economic value in securing, monetizing and paying music assets, reward early adaptors and as part of the mission statement, also incentivize artists to drive direct engagement from their fans.

**Data and Payment Providers** (or any independent web3 payor) will have to Pay fees in $OWN tokens to use the protocol's , but a significant amount of tokens are preserved to onboard the existing music industry on-chain, so the early years of the protocol adoption should come at no cost to them.

Independent labels and artists who are interested in self-custody and can connect their own database to the original Original Works stack, may act as a `DataProvider`s and apply for the Original Works affiliate program.

Additionally, as a Public Good, we believe that any excess value created by $OWN that is not used by the Foundation to continue governing the protocol and invest in its development should flow back to the artists

#### Those same network participants will also earn fees in $OWN for their signatures and payment orders:

* `Data Providers` can earn passive income every time their data is monetized by rights holders and validators.
  * **Verify the registration and enforce privacy settings of $IP assets**
* `Payment Providers` can chose if they want to invest in native web3 integration and retain all fees, or post payment to network relayers, who can batch transactions efficiently and sweep up fees.
  * **Control the Creation of and Privacy settings of licenses**
  * **Mint Royalty Tokens**
  * **Execute on-chain payments for licenses created**

`Relayers` and `Validators` are the open layer above the trusted representatives of rights holders (Service Providers). The protocol allows for any web 3 builder or node operator to become a Validator or Relayer and earn $OWN:

* preserve the data integrity across multiple chains
* prevent double entries of international IP identification codes
* Validate ZK proofs declared about licenses, financials and or/ownership data of an asset
* prevent conflicting payment logic
  * **share percentage** - _what percentage of the revenue of this the rights licensed is collected by this specific license_
  * **revenue source** _- the platform, which monetized the asset_
  * **rights type** _- how the IP is consumed - ad based streams, ad-free radio, etc…_
  * **jurisdiction** \*\*- _Country ISO_
  * **term** - _start and end date_
* provide last mile settlement by batching payments and optimizing gas on splits
* providing cross-chain payment bridges for multi-chain settlement

Additionally, **builders and researches** can earn $OWN by contributing to the public git repository, namely in areas of efficient privacy designs and data-availability optimization schemes.

**The main technical requirements for a Royalty Asset smart contract are:**

* To receive royalties from one or more unique license(s), which are (each) tied to a unique asset, minted on the Original Works Protocol.
* To split those royalty payments to all the token holders of the Royalty Asset contract (Royalty Tokens)
  * If the Payment Provider does not cover the gas for all split claims, the protocol should incentivize relayers to pick those up (in exchange for a share of the payment fee)
* To enable the collection of descriptors about payments made to the Royalty Asset contract
* For UX purposes any payment made from a web3 source to the address of a Royalty Asset’s 0x address should be claimable by its rights holders.
  * Adding a custom url or namespace (like ENS) so anyone can send money to a “song”

`Rights Holders` Will earn $OWN tokens for minting $IP Assets

### Incentivizing Direct Fan Engagement&#x20;

### Stake for Yield to cover gas + excess interest

<figure><img src="../.gitbook/assets/Web 3 Planning - Frame 13.jpg" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="160">Action</th><th width="146">Who requests</th><th width="156">who approves</th><th width="159">who pays</th><th>who gets paid</th></tr></thead><tbody><tr><td>Register an Asset</td><td>Rights Holder</td><td>Data Provider</td><td>Data Provider, Protocol Reserves</td><td>Rights Holders</td></tr><tr><td>Register a License</td><td>Payment Provider</td><td>Validator</td><td></td><td></td></tr><tr><td>Verify a fact about an Asset</td><td>Inquirer (anyone)</td><td>Rights Holder</td><td>Inquirer</td><td>Data Provider</td></tr><tr><td></td><td></td><td></td><td></td><td></td></tr></tbody></table>
