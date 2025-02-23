# Balance Management

The Royalty Pool balance management system enables efficient bulk deposits and automated statement generation for rights holders while maintaining privacy of splits.

### Administrative Flow

1. **Bulk Deposit**

```
Input: Total royalty amount in USD
Process:
- Bridge converts USD to USDC
- USDC deposited to pool contract
- Balance update verified
```

2. **Revenue Assignment**

```
Input: Asset revenue data
{
  asset_id: amount,
  period: timestamp,
  source: platform
}
Process:
- Local API validates pool balance
- Assigns revenue to Merkle trees
- Updates asset states
```

3. **Statement Generation**

```
For each Merkle tree:
- Read current splits
- Calculate individual shares
- Generate proofs
- Create rights holder statements
```

### Statement Structure

```
Statement {
  rightsholder_id: string,
  assets: [{
    asset_id: string,
    amount: number,
    proof: bytes,
    period: timestamp
  }],
  total: number
}
```

### Implementation Requirements

* Configure a secure API locally between OWEN and Merkle tree service
* Integration to existing statement and KYC flows
* Statement distribution system
