## Split data is stored and managed by Royalty Admins off-chain using Merkle trees for superior privace and data integrity:

- Splits are never exposed on-chain
- Only hashed commitments are published
- Each asset has its own Merkle tree
- Updates maintain audit trail without revealing values# Split Information Storage
- Selective disclosure support

### Layered Data Management:

**Private Layer (Royalty Admin)**

- Complete split information
- Full payment history
- Rights holder details
- Merkle tree management

**Public Layer (Blockchain)**

- Asset identifiers
- Hash commitments
- Proof verifications
- Registry updates

#### Storage Implementation:

- Each asset maintains its own Merkle tree
- Updates create new tree states
- Historical records are preserved
- Only commitments published on-chain
- Full data secured off-chain
- Access controlled by Royalty Admin

```mermaid
flowchart TB
    subgraph RoyaltyAdmin["Royalty Admin Layer"]
        splits["Split Data"]
        tree["Merkle Tree"]
        hash["Hash Generator"]
    end

    splits --> hash
    hash --> tree

    subgraph Storage["Storage Layer"]
        commit["On-chain Commitment"]
        private["Private Storage"]
    end

    tree --> commit
    tree --> private

    style RoyaltyAdmin fill:#e1f5fe
    style Storage fill:#f3e5f5
```
