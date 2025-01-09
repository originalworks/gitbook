# Original Works Protocol Documentation

## 1. Introduction

Original Works is a decentralized protocol designed to enhance and streamline the music industry's rights management and royalty distribution system. By leveraging blockchain technology, zero-knowledge proofs, and innovative privacy-preserving mechanisms, the protocol enables efficient synchronization of global music IP records while creating new opportunities for rights holders to manage and monetize their assets.

The protocol's foundational principle is evolution, not revolution. Original Works does not aim to replace the existing music industry supply chain or require artists and fans to change how they engage with music. Instead, it provides a secure and efficient layer for existing industry participants to streamline their operations, reduce costs, and offer enhanced services to rights holders. By building upon established industry practices and infrastructure, the protocol enables traditional music industry service providers to leverage blockchain technology while maintaining their essential role in the ecosystem.

## Protocol Overview

The digital transformation of the music industry has created an unprecedented opportunity. Music consumption has shifted almost entirely to streaming platforms, generating digital-native cashflows that should be ideal for automated processing and distribution. However, these streams of revenue remain trapped in opaque, siloed systems that rely on outdated reconciliation methods and manual synchronization processes. By bringing royalty and IP data on-chain, Original Works creates a foundation for a new economic layer built on top of music rights—an uncorrelated asset class that generates billions of dollars annually in global revenue.

With decades of experience in the music industry, we understand that most artists prefer to focus on their creative work rather than becoming entrepreneurs. They rely on service providers to handle the complex business aspects of their careers. Original Works acknowledges this reality by enabling existing music distributors and publishers to serve as network oracles. These service providers can participate in the protocol by running our client software and staking tokens, while maintaining their current business operations and relationships with artists. This approach preserves the valuable role of industry professionals while introducing greater efficiency and transparency to their services.


## Problem Statement

The current state of royalty management in the music industry presents significant challenges that disproportionately affect creators and rights holders. Global settlement of royalties remains prohibitively expensive and operationally complex, particularly in developing countries that export substantial amounts of music content. The lack of transparency in royalty calculations and distributions creates an illiquid market for music rights, limiting opportunities for creators to leverage their assets effectively.

Most artists and their teams lack the expertise and resources to navigate the intricate landscape of music rights monetization. Consequently, they often find themselves surrendering significant ownership and control to administrators who manage their cashflows. These administrative relationships frequently lead to long-term contractual obligations that keep artists in cycles of debt and dependency, unable to fully capitalize on their creative work.

By enabling on-chain identification and authentication of intellectual property, Original Works creates a foundation for automated split payments, royalty advances, and innovative financing solutions. These capabilities rely on smart contracts and economic incentives rather than traditional administrative control. As a result, artists at any scale can access sophisticated financial services and rights management tools without sacrificing their autonomy or ownership rights. This democratization of access represents a fundamental shift in how creators can manage and monetize their intellectual property while maintaining control of their musical work.


## Key Benefits

The Original Works protocol delivers immediate, practical benefits to all participants in the music ecosystem:

For Rights Holders:
- Privacy-Preserving Claims: Rights holders need only present their ERC1155 voucher tokens to claim royalties, while their ownership percentages and earnings remain completely hidden from the blockchain. By generating new claiming addresses for each transaction, the protocol ensures that payment patterns cannot be tracked or analyzed by external observers.
- Stable Value Distribution: Royalties are distributed in stable coins, protecting rights holders from cryptocurrency volatility while enabling automated, trustless distribution through smart contracts. This combines the efficiency of blockchain technology with the stability of traditional currency, ensuring predictable income streams.
- Capital Efficiency: Verified on-chain rights can be used as collateral for DeFi services

For Music Service Providers:
- Reduced Operating Costs: Automated reconciliation and settlement reduce administrative overhead
- Enhanced Services: Providers can offer new financial products backed by verified rights data
- Business Continuity: Integration requires minimal changes to existing operations

For the Industry:
- Global Accessibility: Standardized protocol enables participation from any jurisdiction
- Market Efficiency: Transparent, verifiable rights data creates liquid markets for music assets
- Innovation Platform: Open protocol enables new services built on verified rights data


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

Think of it like a redacted document where each rights holder can only see their own information: When claiming royalties, a rights holder presents their voucher token (similar to showing ID to pick up a package), and the system generates a cryptographic proof that verifies their specific share of the royalties without exposing anyone else's information. This proof confirms both their right to claim and the exact amount they're owed, while keeping the overall split structure and individual percentages completely confidential. The system maintains this privacy even as it processes and distributes payments, ensuring that sensitive business relationships remain protected.
