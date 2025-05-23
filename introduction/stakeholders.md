# Stakeholder Roles

## **Technical Implementation by Stakeholder**

<details>

<summary>Rights and Royalty Administrators (Distributors/Publishers/CMOs)</summary>

* Run the [OWEN](https://docs.original.works/original-works/4.1-owen-client/what-is-owen) client to process standard industry messages
* Generate zero-knowledge proofs of valid submissions
* Submit data to blockchain through blob storage (EIP-4844)
* Operate Royalty Pools for stablecoin deposits
* Maintain Merkle trees of rights splits
* Process rights holder claims with privacy preservation
* Define claim Claim requirements (regulatory and compliance oversight)
* More details available in the [Technical Setup](https://docs.original.works/original-works/7.1-integration-rights-and-royalty-admins/technical-setup)
* latest code and instalation guidelines available on [Github](https://github.com/originalworks/protocol-core/tree/master/owen)

</details>

<details>

<summary>Validators</summary>

* Listen for Royalty Admin submissions on the network
* Verify zero-knowledge proofs of message validity
* Generate subgraph indices of verified assets
* Submit validation proofs through KZG commitments
* Maintain distributed storage of complete metadata
* Secure the minting of ERC1155 royalty contract tokens
* More details available in the [Technical Documentation](https://docs.original.works/original-works/7.2-validator-setup/technical-requirements)
* latest code and instalation guidelines available on [Github](https://github.com/originalworks/protocol-core/tree/master/validator_node)

</details>

<details>

<summary>Rights Holders</summary>

* Hold tokens in separate wallets from claim addresses
* Generate proofs of ownership for royalty claims
* Claim stablecoin payments to new addresses
* Optionally transfer rights through token transfers

</details>

<details>

<summary>Smart Contracts</summary>

* Process royalty claims with privacy preservation
* Verify proof submissions from validators
* Handle stablecoin deposits and withdrawals
* Maintain protocol security parameters
* Enable automated split payments

</details>

{% hint style="info" %}
The separation between rights registration (secured by validators) and royalty distribution (managed by Royalty Admins) ensures both decentralized security and efficient operations, while the use of privacy-preserving mechanisms protects sensitive business relationships throughout the process.
{% endhint %}



