---
description: Blob storage sequencing for storing
---

# Structuring records on IPFS

Since IPFS records of XML data strucutres cannot be parsed on-chain, there must be a method to parse the data off-chain and provide subgraph with a schema against which it can create queries.&#x20;

In order to keep the protocol decentralized, this process must be done in a transparent manner and is outsourced to "validator" smart contracts that anyone can track, and/or deploy and take part in the validation process to earn $OWN.

Data providers register new DDEX messages by sending a DDEX-compliant XML file to the Protocol's core smart contract, called the Sequencer, as a blob along with a processing fee. \
\
The blob, enabled by EIP-4844, allows for cost-effective temporary storage of large data chunks on the blockchain. Multiple DDEX XML files can be batched in a single blob to optimize costs further. Validators then pick up the blob to check message validity:

* If a message fails validation, the validator generates a zk-proof to demonstrate the invalidity and submits it to the Sequencer, resulting in the slashing of the data provider's staked funds.
* If the messages are valid, the validator creates a zk-proof confirming validity and collects the processing fee.

Finally, the validator sends the zk-proof and messages back to the Sequencer, which validates the proof and registers the messages in the Protocol's subgraph. This process ensures secure and cost-effective data registration and validation within the Protocol.
