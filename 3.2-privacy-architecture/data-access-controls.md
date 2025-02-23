## Data Access Controls

### Access to sensitive information is strictly controlled:

- Royalty Admins manage their own trees and impose any controls or restrictions related to roylaty claims.
- Rights holders see only their shares and recieve cryptographic proof of their payout rate with each payment.
- Validators verify and secure public release notifications and associated assets.
- Public data limited to essential Metadata, assigned Identifiers and Royalty Admin.
- Access to private data is controlled by admin and rights-holder but always linked to a an independently-verifiable public redord.

```mermaid
flowchart TB
    subgraph Access["Access Layers"]
        direction TB
        L1["Public Layer"]
        L2["Validator Layer"]
        L3["Admin Layer"]
        L4["Private Layer"]
    end

    subgraph Data["Data Types"]
        D1["Asset Metadata"]
        D2["Proofs & Commits"]
        D3["Split Info"]
        D4["Payment Data"]
    end

    L1 --> D1
    L2 --> D2
    L3 --> D3
    L4 --> D4

    style L1 fill:#e1f5fe
    style L2 fill:#e8f5e9
    style L3 fill:#fff3e0
    style L4 fill:#f3e5f5
```
