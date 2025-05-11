# Integrations and flow of funds

***

## Integrations and flow of funds

The system maintains privacy throughout - rights holders can verify their correct share while withholding details remain confidential and splits stay private.

<figure><img src="../.gitbook/resources/pool_design.jpg" alt=""><figcaption></figcaption></figure>

Here's how the rights holder verification and payout flow works, including the compliance checks:

{% stepper %}
{% step %}
**Statement Processing**

* DSP reports get converted from USD to USDC by the Royalty Admin using a third party service
* Pool generates statements using Merkle tree data
* Each rights holder sees only their share per asset\\
{% endstep %}

{% step %}
**Claim Initiation**

* Rights holder reviews their statement
* Submits claim with proof of ownership
* Can specify new private receiving address
{% endstep %}

{% step %}
**Compliance Checks**

* Pool administrator verifies KYC status
* Applies any required tax withholding
* The pool handles territory-specific compliance based payout amount accordingly
{% endstep %}

{% step %}
**Payment Distribution**

* Pool releases net USDC after withholding
* Rights holder receives funds at specified address
* Can offramp to USD via bank/card
* Gets cryptographic proof of correct payment amount
{% endstep %}
{% endstepper %}

### Why this flow combines the best solution in each category for Royalty Admins

**Efficiency:** When Royalty Admins receive consumption reports from DSPs, instead of calculating individual payments, they simply deposit the total revenue into their own Royalty Pool and assign amounts per asset. The pool then automatically calculates each rights holder's share based on the pre-registered splits stored in its [Merkle tree](https://docs.alchemy.com/docs/merkle-trees-in-blockchains).

**Privacy:** Rights holders can then submit claims for multiple statements at once. When they do, the system automatically generates a new receiving address tied to their existing account. This means each withdrawal goes to a fresh address, making it impossible to track payment patterns.

**Verifiability:** Most importantly, each claim comes with a cryptographic proof that verifies they received the correct percentage of each asset's revenue. This proof confirms their payment is accurate without revealing anything about other rights holders or the total pool amount. It's like getting a redacted bank statement where you can only see your own transactions but can mathematically verify they're correct.

**Compliance:** The entire process remains compliant since all claims must pass KYC/AML checks before approval. So while you maintain control of royalty deposits and compliance checks, rights holders get privacy and verifiable accuracy for their earnings.
