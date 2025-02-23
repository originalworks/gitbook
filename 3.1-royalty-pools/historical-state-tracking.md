The Royalty Pool maintains a complete history of all rights and payments through a system of Merkle trees, ensuring both accessibility and immutability of historical data.

## Tamper-Proof Record Keeping

Each update to rights splits or payment distributions creates a new state in the Merkle tree, while preserving previous states. This creates an immutable chain of records where:
- Each state links cryptographically to its predecessor
- Historical records cannot be altered
- All changes are verifiable
- Previous states remain accessible

## Verifiable Income History

Rights holders can generate proofs of their historical earnings to access financial services like royalty advances. For example:

```
Income Verification Process:
1. Rights holder requests proof of earnings
2. Royalty Pool generates proof showing:
   - Total earnings over specified period
   - Verification of source (Royalty Admin)
   - Confirmation of completed payments
   - Integrity of historical records
3. Smart contracts verify the proof
4. Lending pools can immediately process advance requests
```

## Practical Application

A rights holder seeking an advance can prove their income history without revealing sensitive details:
- Submit transaction to Royalty Pool requesting proof
- Specify time period (e.g., "last 12 months")
- Set minimum earnings threshold
- Generate zero-knowledge proof of earnings

The Royalty Pool produces a verifiable proof that the rights holder's earnings met the specified criteria, unlocking immediate access to advance funding while maintaining privacy of specific earnings details.

This system enables new financial opportunities for rights holders while ensuring the integrity of historical records and protecting sensitive business information.
# Historical State Tracking

