## Solution Architecture


Original Works addresses the music industry's challenges through a layered architecture that combines proven industry standards with innovative blockchain technology. At its core, the protocol transforms traditional music industry data formats (DDEX.ERN and CWR) into on-chain assets while preserving privacy and maintaining compliance with existing systems.

Consider how a typical music release works today: A distributor submits standardized XML files to streaming platforms, containing essential metadata about songs, artists, and rights holders. Original Works enhances this process through the OWEN (Original Work Electronic Notification) client, which processes these same XML files but adds a crucial layer of blockchain verification. When a distributor submits a release, OWEN:

- Parses the XML data and extracts key identifiers (ISRC, ISWC)
- Generates a unique audio fingerprint (ISCC) from the content upon request - This is optional only if the audio file is delivered with the DDEX package.
- Stores the original file in blob storage with an 18-day retention period
- Posts a the actual file (xml and jpg) to IPFS for permanent accessibility
- Submits a blockchain transaction linking all these elements to the registered asset

This process creates an immutable, verifiable record of the release while maintaining the privacy of sensitive business information; The protocol's validator network then: 

- Picks up on the blockchain transaction
- Recalculates the transaction details, with the pinned IPFS data as the input source
- Verifies these submissions and generates their corresponding ZK proofs. 
- This process repeats for any update to the registered asset. 

Anyone in the world can then check the proof against the pinned data, ensuring a fully available audit trail of the public records, and verified data integrity without accessing the confidential details of rights and royalties.

After the decentralized registration process validates the asset, Oracles can proceed with royalty tokenization through an innovative privacy-preserving system. Instead of storing split and revenue data directly on-chain, where it would be publicly visible, the protocol employs a specialized data structure called a Merkle Tree. This tree functions like a sophisticated filing cabinet that only the Oracle can access fully, while allowing individual rights holders to prove and claim their specific portions without revealing their ownership percentages to anyone.

### Why Merkle Trees?

Think of it like a redacted document where each rights holder can only see their own information: When claiming royalties, a rights holder presents their voucher token (similar to showing ID to pick up a package), and the system generates a cryptographic proof that verifies their specific share of the royalties without exposing anyone else's information. This proof confirms both their right to claim and the exact amount they're owed, while keeping the overall split structure and individual percentages completely confidential. The system maintains this privacy even as it processes and distributes payments, ensuring that sensitive business relationships remain protected.
