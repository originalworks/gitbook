# Integrations and flow of funds



<figure><img src="../.gitbook/assets/Original Works Protocol Design - Royalty Pool (private royalty splits) (1).jpg" alt=""><figcaption></figcaption></figure>

Here's how the rights holder verification and payout flow works, including the compliance checks:

1. Statement Processing

* DSP reports get converted from USD to USDC
* Pool generates statements using Merkle tree data
* Each rights holder sees only their share per asset

2. Claim Initiation

* Rights holder reviews their statement (0x1ab = $x, 0x2cd = $y)
* Submits claim with proof of ownership
* Can specify new private receiving address

3. Compliance Checks

* Pool administrator verifies KYC status
* Applies any required tax withholding
* Handles territory-specific compliance
* Updates payout amount accordingly

4. Payment Distribution

* Pool releases net USDC after withholding
* Rights holder receives funds at specified address
* Can offramp to USD via bank/card
* Gets cryptographic proof of correct payment amount

The system maintains privacy throughout - rights holders can verify their correct share while withholding details remain confidential and splits stay private.
