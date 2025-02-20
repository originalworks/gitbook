# Frequently Asked Questions

### 1. What is Original Works Protocol?
Original Works is a decentralized protocol that enables music industry participants to register rights, manage royalties, and process payments while maintaining privacy and reducing costs. It works alongside existing industry infrastructure rather than replacing it.

### 2. How does Original Works integrate with existing music industry systems?
The protocol accepts standard industry formats (DDEX.ERN and CWR) through the [OWEN](https://docs.original.works/original-works/4.1-owen-client/what-is-owen) client, requiring minimal changes to existing workflows. Music distributors and publishers can continue using their current systems while gaining blockchain benefits.
You can trace the actual processing and verification of these public Electronic Release Notifications live on production in our testnet implementation [here](https://holesky.etherscan.io/address/0x09A5a916b7a37C035E268A9EefCD182cC9cA51E3)

### 3. What's the difference between Rights Administrators and Validators?
Rights and Royalty Administrators are music industry participants (distributors, publishers) who submit rights data to the network. Validators are independent network participants who verify these submissions and maintain the network's integrity. This separation ensures decentralized verification of rights registration.

### 4. How does the protocol maintain privacy while ensuring transparency?
The protocol uses zero-knowledge proofs and Merkle trees to enable rights holders to verify their earnings without exposing sensitive information like split percentages or total pool amounts. Each payment comes with cryptographic proof of correctness.

### 5. Why does Original Works use USDC for payments?
USDC is a regulated stablecoin that maintains a 1:1 value with USD while enabling instant, global transfers at lower costs. It's widely accepted by financial institutions and provides the stability of traditional currency with the efficiency of blockchain technology.

### 6. What are the technical requirements for running OWEN?
[OWEN](https://docs.original.works/original-works/4.1-owen-client/what-is-owen) requires minimal infrastructure (approximately $50/month hosting) and can be deployed on existing cloud or local systems. It's provided as a pre-compiled, open-source solution that accepts standard industry formats.

### 7. How does the Royalty Pool system work?
Royalty Pools allow administrators to deposit bulk payments and automatically generate statements based on registered splits. Rights holders can claim their earnings with privacy-preserving proofs and receive payments to new addresses each time.

### 8. Can rights holders get advances against their royalties?
Yes, the protocol enables rights holders to access advances based on verified streaming revenue. Unlike traditional advances, these don't require giving up ownership rights and use transparent, smart contract-based repayment from future earnings.

### 9. How does the protocol handle compliance and regulations?
Royalty Pool administrators can implement KYC checks and tax withholding as needed. The system integrates with regulated payment providers like Bridge (Stripe) for compliant fiat on/off ramps.

### 10. What happens to historical rights data?
All rights registration data is stored on distributed storage systems (IPFS/SWARM) for complete auditability, while current state information is maintained on-chain for efficient access. The validator network ensures data availability and integrity.

### 11. What are the requirements to become a validator?
Validators need to run a node with minimum specifications of 8+ core processor, 16GB RAM, For GPU mode: Nvidia GPU with at least 4GB VRAM (optional but recommended) and 100Mbps stable network connection. They must also stake protocol tokens and maintain high availability for network operations.

### 12. How do validators earn rewards?
Validators earn rewards for:

- Successfully validating rights registrations
- Maintaining data availability
- Providing proof generation services
- Contributing to network security. The reward structure ensures sustainable operations while incentivizing honest behavior.

### 13. How do rights holders claim their royalties?
Rights holders receive statements showing their earnings per asset. They can submit claims for multiple statements at once, optionally generating new addresses for each claim. After passing any required compliance checks, payments are automatically processed to their specified address.

### 14. Can rights holders verify they're receiving the correct amount?
Yes. Each payment comes with a cryptographic proof that verifies the payment amount matches their registered split percentage. This allows rights holders to confirm they're receiving the correct share without seeing other participants' splits or total pool amounts.

### 15. What happens if a validator goes offline?
The network is designed to be resilient to individual validator downtime. Multiple validators process each submission, ensuring continuous operation. However, extended downtime may result in reduced rewards or potential slashing of staked tokens.

### 16. How are royalty splits managed privately?
Splits are stored in Merkle trees managed by Royalty Pool administrators. When revenue is assigned to an asset, the system automatically calculates individual shares based on the current tree state. Rights holders can only see and verify their own percentage.

### 17. What happens when rights splits change?
Rights Holders can update the Merkle tree (splits database) of a release by prooving they hold a valid Voucher of the asset by submitting a transaction with new split information. The state is updated on the local setup of the Royalty Admin so the next time royalties are deposited they are split according to the latest state. All future payments will use the updated splits, while historical payments remain verifiable based on the splits that were active at the time of payment. For new 0x addresses to cliam royalies successfully, the Royalty Admin may impose any verifications or identifications necessary.

