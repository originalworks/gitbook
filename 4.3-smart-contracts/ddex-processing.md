# DDEX Message Processing

## Overview

DDEX message processing in The Protocol is managed by the `DdexSequencer` smart contract. The process consists of two main steps: **enqueueing** (handled by Data Providers) and **dequeueing** (handled by Validators).

## Enqueue: Submitting DDEX Messages

1. **Data Providers** use the **OWEN client** to send transactions to the `DdexSequencer` calling smart contract function: `submitNewBlob(bytes32 _imageId, bytes memory, _commitment, bytes32 _blobSha2)`.
2. Each transaction includes a **BLOB** containing encoded **DDEX messages**.
3. For every BLOB submitted, its **ID is enqueued** and stored in the order it arrives (**First In, First Out**).

## Dequeue: Validating and Removing Messages

1. **Validators** operate a `validator node`, software that retrieves the BLOB submitted by a Data Provider.
2. Inside a **RiscZero zkVM**, the node executes code to validate each DDEX message within the BLOB.
3. The validator node generates a **ZK proof** of the BLOB’s validity or invalidity.
4. The **ZK proof** is submitted to `DdexSequencer` smart contract by calling `submitProof(bytes32 _imageId, bytes memory _journal, bytes calldata _seal, string memory _cid)`, This **dequeues** the BLOB.
5. A BLOB can be dequeued by submitting:
   - **Proof of validity** → The BLOB is confirmed as valid.
   - **Proof of invalidity** → The BLOB is flagged as invalid, triggering the **slashing mechanism** (covered in the next chapter).
