# Integrations and flow of funds



<figure><img src="../.gitbook/assets/Original Works Protocol Design - Royalty Pool (private royalty splits) (1).jpg" alt=""><figcaption></figcaption></figure>

Here's how the rights holder verification and payout flow works, including the compliance checks:

1. Statement Processing
   * DSP reports get converted from USD to USDC
   * Pool generates statements using Merkle tree data
   * Each rights holder sees only their share per asset\

2. Claim Initiation
   * Rights holder reviews their statement
   * Submits claim with proof of ownership
   * Can specify new private receiving address\

3.  Compliance Checks

    * Pool administrator verifies KYC status
    * Applies any required tax withholding
    * The pool handles territory-specific compliance based payout amount accordingly


4. Payment Distribution
   * Pool releases net USDC after withholding
   * Rights holder receives funds at specified address
   * Can offramp to USD via bank/card
   * Gets cryptographic proof of correct payment amount

\--

**The system maintains privacy throughout - rights holders can verify their correct share while withholding details remain confidential and splits stay private:**

When Royalty Admins receive consumption reports from DSPs, instead of calculating individual payments, they simply deposit the total revenue into thier own Royalty Pool and assign amounts per asset. The pool then automatically calculates each rights holder's share based on the pre-registered splits stored in its Merkle tree.

Rights holders can then submit claims for multiple statements at once. When they do, the system automatically generates a new receiving address tied to their existing account. This means each withdrawal goes to a fresh address, making it impossible to track payment patterns.

Most importantly, each claim comes with a cryptographic proof that verifies they received the correct percentage of each asset's revenue. This proof confirms their payment is accurate without revealing anything about other rights holders or the total pool amount. It's like getting a redacted bank statement where you can only see your own transactions but can mathematically verify they're correct.

So while you maintain control of royalty deposits and compliance checks, rights holders get privacy and verifiable accuracy for their earnings. The entire process remains compliant since all claims must pass KYC/AML checks before approval.
