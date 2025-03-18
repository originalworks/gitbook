# Versioning and ImageID

## Adapting to Evolving Standards

The Protocol processes DDEX messages and ensures that all processed messages comply with a specific standard. However, standards evolve over time, requiring updates to the validation mechanisms.

## RiscZero Guest Code and ImageID

- DDEX messages are validated using **RiscZero guest code**, which generates a **ZK proof** that is verified on-chain.
- The on-chain verification process relies on a specific **ImageID**, which corresponds to a unique version of the RiscZero guest code.
- **Modifying the guest code results in a new ImageID**, meaning that whenever a DDEX standard is updated, the ImageID must also be updated in the smart contract.

## Upgrade Mechanism

To ensure a smooth transition between standards, The Protocol follows a **gradual upgrade process**:

1. **Communication Phase**

   - Any upcoming standard upgrade will be announced, providing time for participants to adapt.

2. **Temporary Dual Standard Acceptance**

   - The Protocol will temporarily accept **both the current and previous standards** to allow for a seamless transition.

3. **Phased Decommissioning of the Previous Standard**
   - The `DdexSequencer` will first **stop accepting new BLOBs** that conform to the previous standard.
   - Once all BLOBs from the previous standard are dequeued, the `DdexSequencer` will **stop accepting proofs** from validators using the previous standard.

This upgrade mechanism ensures that changes to the DDEX standard are implemented efficiently while minimizing disruptions to Data Providers and Validators.
