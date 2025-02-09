# Stakeholders Diagram

**Technical Implementation by Stakeholder:**

Rights Administrators (Distributors/Publishers):

* Run OWEN client to process standard industry messages
* Generate zero-knowledge proofs of valid submissions
* Submit data to blockchain through blob storage (EIP-4844)
* Operate Royalty Pools for stablecoin deposits
* Maintain Merkle trees of rights splits
* Process rights holder claims with privacy preservation
* Define claim Claim requirements (regulatory and compliance oversight)

Validators:

* Listen for Royalty Admin submissions on the network
* Verify zero-knowledge proofs of message validity
* Generate subgraph indices of verified assets
* Submit validation proofs through KZG commitments
* Maintain distributed storage of complete metadata
* Secure the minting of ERC1155 royalty contract tokens

Rights Holders:

* Receive ERC1155 royalty contract tokens representing revenue rights
* Hold tokens in separate wallets from claim addresses
* Generate proofs of ownership for royalty claims
* Claim stablecoin payments to new addresses
* Optionally transfer rights through token transfers

Smart Contracts:

* Manage ERC1155 token minting and transfers
* Process royalty claims with privacy preservation
* Verify proof submissions from validators
* Handle stablecoin deposits and withdrawals
* Maintain protocol security parameters
* Enable automated split payments

The separation between rights registration (secured by validators) and royalty distribution (managed by Royalty Admins) ensures both decentralized security and efficient operations, while the use of privacy-preserving mechanisms protects sensitive business relationships throughout the process.

```mermaid

flowchart TB
    subgraph RoyaltyAdmin["Royalty Admin Layer"]
        input1["DDEX.ERN or CWR Files"]
        input3["Royalty Payouts"]
        
        subgraph RoyaltyClient["Royalty Pool Client"]
            merkle["Merkle Tree Split Information"]
            pool["Royalty Pool USDC Balance"]
        end

        input3 --> pool
    end

    subgraph OWEN["OWEN Processing"]
        parse["XML Parser"]
        convert["JSON output"]
        check["Validation Checks"]
        passed{"passed"}
        kill["kill process"]
        generate["Generate ISCC (optional)"]
        ipfs["IPFS Storage"]
    
        parse --> convert
        convert --> check
        check --> passed
        passed -->|No| kill
        passed -->|Yes| generate
        generate --> ipfs
    end

    subgraph Storage["Distributed Storage"]
        ipfsStore["IPFS Stores BLOBs"]
        blobContract["Blockchain Transaction - BLOB 18-day retention - Commitment mapping - Payment provider registry"]
    end

    subgraph ValidatorNetwork["L1 Validator Network"]
        digest1["Digest BLOB Message"]
        extract["Extract Key Data"]
        zkproof["Generate ZK Proof"]
        commit["Private Inputs BLOB KZG\nCommitment"]
        output["Output Parsed Messages"]
        digest2["Secondary Validator\nDigest BLOB Message"]
    end

    subgraph Index["Indexing Layer"]
        registry["Registry of DDEX Relations"]
        metadata["Index of registered Asset Metadata"]
    end

    subgraph RightsClaims["Rights Holder Claims"]
        voucher["Voucher Wallet ERC1155 Tokens"]
        claim["Claim Process Proof of Ownership - Σ[royalties] - Private 0x"]
        payout["Payout Wallet - New address per claim"]
    end

    input1 --> OWEN
    OWEN --> Storage
    Storage --> ValidatorNetwork
    ValidatorNetwork --> Index
    
    merkle --> pool
    pool --> claim
    voucher --> claim
    claim --> payout
    
    style RoyaltyAdmin fill:#f5f5f5
    style OWEN fill:#e1f5fe
    style Storage fill:#fff3e0
    style ValidatorNetwork fill:#e8f5e9
    style Index fill:#f3e5f5
    style RightsClaims fill:#e1bee7


```
