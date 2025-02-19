# Table of contents

## Quick Start

* [About Original Works](README.md)
* [Rights and Royalties On Chain](quick-start/rights-and-royalties-on-chain.md)
* [Use cases](introduction/use-cases.md)

## 1. Introduction

* [Protocol Overview](introduction/protocol-overview.md)
* [Problem Statement](introduction/problem-statement.md)
* [Key Benefits](introduction/key-benefits.md)
* [Solution Architecture](introduction/solution-architecture.md)
* [User Flow](1.-introduction/user-flow.md)
* [Stakeholder Roles](introduction/stakeholders.md)
* [Stakeholders Diagram](resources/main-flow.md)

## 2.1 Royalty Admins

* [Definition and Requirements](oracles/definition.md)
* [Royalty Admin Benefits](oracles/benifits.md)
* [Types of Royalty Admins](oracles/types.md)
  * [Royalty Administrators](oracles/distributors-and-publishers.md)
  * [Data Providers](oracles/data-and-payment-providers.md)
* [Onboarding Process](oracles/onboarding.md)
* [Staking Requirements](oracles/staking.md)
* [Service Provider Responsibilities](oracles/responsibilities.md)
* [Economic Incentives](oracles/economics.md)
* [Compliance Requirements](oracles/compliance.md)

## 2.2 Validators

* [Network Role and Importance](validator/validator-role.md)
* [Validation Process](resources/validator_flow.md)
  * [BLOB Message Processing](validator/blob-processing.md)
  * [ZK Proof Generation](validator/zkproof.md)
* [Reward Mechanism](validator/rewards.md)
* [Slashing Conditions](validator/slashing.md)
* [Best Practices](validator/best-practices.md)
* [Network Participation Rules](2.2-validators/network-participation-rules.md)

## 2.3 Rights Holders

* [Role Definition](2.3-rights-holders/role-definition.md)
* [Asset Registration Process](2.3-rights-holders/asset-registration-process.md)
* [Rights Management](2.3-rights-holders/rights-management.md)
* [Royalty Claims Process](2.3-rights-holders/royalty-claims-process.md)
* [Privacy Features](2.3-rights-holders/privacy-features.md)
* [Available Tools and Interfaces](2.3-rights-holders/available-tools-and-interfaces.md)

## 3.1 Royalty Pools

* [Operating an Original Works Royalty Pool](3.1-royalty-pools/pool-structure.md)
* [Integrations and flow of funds](3.1-royalty-pools/integrations-and-flow-of-funds.md)
* [USDC Integration](3.1-royalty-pools/usdc-integration.md)
* [Balance Management](3.1-royalty-pools/balance-management.md)
* [Historical State Tracking](3.1-royalty-pools/historical-state-tracking.md)

## 3.2 Privacy Architecture

* [Merkle Tree Implementation](3.2-privacy-architecture/merkle-tree-implementation.md)
* [Split Information Storage](3.2-privacy-architecture/split-information-storage.md)
* [Proof Generation](3.2-privacy-architecture/proof-generation.md)
* [Data Access Controls](3.2-privacy-architecture/data-access-controls.md)

## 3.3 Claims Process

* [Voucher Token System](3.3-claims-process/voucher-token-system.md)
* [Proof of Ownership](3.3-claims-process/proof-of-ownership.md)
* [Payment Processing](3.3-claims-process/payment-processing.md)
* [New Address Generation](3.3-claims-process/new-address-generation.md)

## 3.4 Compliance Framework

* [KYC Integration](3.4-compliance-framework/kyc-integration.md)
* [Tax Withholding](3.4-compliance-framework/tax-withholding.md)
* [Regulatory Reporting](3.4-compliance-framework/regulatory-reporting.md)
* [Audit Trail](3.4-compliance-framework/audit-trail.md)

## 4.1 OWEN Client

* [What is OWEN?](4.1-owen-client/what-is-owen.md)
* [Why is OWEN needed to enable Royalty Tokenization?](4.1-owen-client/why-is-owen-crucial-to-enable-royalty-tokenization.md)
* [Installation Requirements](4.1-owen-client/installation-requirements.md)
* [Configuration Options](4.1-owen-client/configuration-options.md)
* [XML Processing](4.1-owen-client/xml-processing/README.md)
  * [DDEX.ERN Support](4.1-owen-client/xml-processing/ddex.ern-support.md)
  * [CWR Support](4.1-owen-client/xml-processing/cwr-support.md)
* [Validation Rules](4.1-owen-client/validation-rules.md)
* [ISCC Generation](4.1-owen-client/iscc-generation.md)
* [Error Handling](4.1-owen-client/error-handling.md)

## 4.2 Storage Layer

* [IPFS Implementation](4.2-storage-layer/ipfs-implementation.md)
* [Blob Storage](4.2-storage-layer/blob-storage/README.md)
  * [EIP-4844 Integration](4.2-storage-layer/blob-storage/eip-4844-integration.md)
  * [Retention Policies](4.2-storage-layer/blob-storage/retention-policies.md)
* [Data Availability](4.2-storage-layer/data-availability.md)
* [Network Redundancy](4.2-storage-layer/network-redundancy.md)

## 4.3 Smart Contracts

* [Contract Architecture](resources/token-factory-contract-interaction-flow.md)
* [Function Specifications](4.3-smart-contracts/function-specifications.md)
* [State Management](4.3-smart-contracts/state-management.md)
* [Access Controls](4.3-smart-contracts/access-controls.md)
* [Upgrade Mechanisms](4.3-smart-contracts/upgrade-mechanisms.md)

## 4.4 Network Infrastructure

* [Node Requirements](4.4-network-infrastructure/node-requirements.md)
* [Network Topology](4.4-network-infrastructure/network-topology.md)
* [Communication Protocols](4.4-network-infrastructure/communication-protocols.md)
* [Performance Optimization](4.4-network-infrastructure/performance-optimization.md)

## 5.1 Industry Standards

* [ISRC Integration](5.1-industry-standards/isrc-integration.md)
* [ISWC Implementation](5.1-industry-standards/iswc-implementation.md)
* [ISCC Generation](5.1-industry-standards/iscc-generation.md)
* [Metadata Standards](5.1-industry-standards/metadata-standards.md)

## 5.2 Protocol Standards

* [Asset Identification](5.2-protocol-standards/asset-identification.md)
* [Rights Documentation](5.2-protocol-standards/rights-documentation.md)
* [Payment References](5.2-protocol-standards/payment-references.md)
* [Version Control](5.2-protocol-standards/version-control.md)

## 6.1 Token Economics

* [Utility Token Design](6.1-token-economics/utility-token-design.md)
* [Staking Mechanism](6.1-token-economics/staking-mechanism.md)
* [Fee Structure](6.1-token-economics/fee-structure.md)
* [Reward Distribution](6.1-token-economics/reward-distribution.md)

## 6.2 Market Dynamics

* [Price Discovery](6.2-market-dynamics/price-discovery.md)
* [Liquidity Mechanisms](6.2-market-dynamics/liquidity-mechanisms.md)
* [Risk Management](6.2-market-dynamics/risk-management.md)
* [Market Making](6.2-market-dynamics/market-making.md)

## 6.3 Incentive Alignment

* [Oracle Incentives](6.3-incentive-alignment/oracle-incentives.md)
* [Validator Rewards](6.3-incentive-alignment/validator-rewards.md)
* [Network Growth](6.3-incentive-alignment/network-growth.md)
* [Sustainability](6.3-incentive-alignment/sustainability.md)

## 7.1 Integration: Rights and Royalty Admins

* [Technical Setup](7.1-integration-rights-and-royalty-admins/technical-setup.md)
* [Commercial Requirements](7.1-integration-rights-and-royalty-admins/commercial-requirements.md)
* [Data Parsing](7.1-integration-rights-and-royalty-admins/api-documentation.md)
* [Security Requirements](7.1-integration-rights-and-royalty-admins/security-requirements.md)
* [Best Practices](7.1-integration-rights-and-royalty-admins/best-practices.md)

## 7.2 Validator Setup

* [Hardware Requirements](validator/technical-requirements.md)
* [Software Installation](7.2-validator-setup/software-installation.md)
* [Network Configuration](7.2-validator-setup/network-configuration.md)
* [Performance Monitoring](7.2-validator-setup/performance-monitoring.md)

## 7.3 Rights Holder Interface

* [Wallet Setup](7.3-rights-holder-interface/wallet-setup.md)
* [Asset Registration](7.3-rights-holder-interface/asset-registration.md)
* [Rights Management](7.3-rights-holder-interface/rights-management.md)
* [Payment Configuration](7.3-rights-holder-interface/payment-configuration.md)

## 8.1 Protocol Updates

* [Proposal Process](8.1-protocol-updates/proposal-process.md)
* [Voting Mechanism](8.1-protocol-updates/voting-mechanism.md)
* [Implementation Process](8.1-protocol-updates/implementation-process.md)
* [Emergency Procedures](8.1-protocol-updates/emergency-procedures.md)

## 8.2 Community Participation

* [Decision Making](8.2-community-participation/decision-making.md)
* [Discussion Forums](8.2-community-participation/discussion-forums.md)
* [Improvement Proposals](8.2-community-participation/improvement-proposals.md)
* [Conflict Resolution](8.2-community-participation/conflict-resolution.md)

## 9.1 Network Security

* [Threat Models](9.1-network-security/threat-models.md)
* [Attack Vectors](9.1-network-security/attack-vectors.md)
* [Mitigation Strategies](9.1-network-security/mitigation-strategies.md)
* [Incident Response](9.1-network-security/incident-response.md)

## 9.2 Smart Contract Security

* [Audit Process](9.2-smart-contract-security/audit-process.md)
* [Known Vulnerabilities](9.2-smart-contract-security/known-vulnerabilities.md)
* [Security Best Practices](9.2-smart-contract-security/security-best-practices.md)
* [Update Procedures](9.2-smart-contract-security/update-procedures.md)

## 9.3 Privacy Protection

* [Data Encryption](9.3-privacy-protection/data-encryption.md)
* [Access Controls](9.3-privacy-protection/access-controls.md)
* [Information Flow](9.3-privacy-protection/information-flow.md)
* [Privacy Guarantees](9.3-privacy-protection/privacy-guarantees.md)

## 10.1 API Reference

* [Endpoints](10.1-api-reference/endpoints.md)
* [Request/Response Formats](10.1-api-reference/request-response-formats.md)
* [Authentication](10.1-api-reference/authentication.md)
* [Rate Limiting](10.1-api-reference/rate-limiting.md)

## 10.2 Smart Contract Interface

* [Function Signatures](10.2-smart-contract-interface/function-signatures.md)
* [Event Logs](10.2-smart-contract-interface/event-logs.md)
* [Error Codes](10.2-smart-contract-interface/error-codes.md)
* [Gas Optimization](10.2-smart-contract-interface/gas-optimization.md)

## 10.3 Data Schemas

* [XML Formats](10.3-data-schemas/xml-formats.md)
* [JSON Structures](10.3-data-schemas/json-structures.md)
* [Merkle Tree Format](10.3-data-schemas/merkle-tree-format.md)
* [Proof Formats](10.3-data-schemas/proof-formats.md)

## 11.1 Privacy Design

* [Zero-Knowledge Proofs](11.1-privacy-design/zero-knowledge-proofs.md)
* [Merkle Tree Privacy](11.1-privacy-design/merkle-tree-privacy.md)
* [Transaction Privacy](11.1-privacy-design/transaction-privacy.md)
* [Data Minimization](11.1-privacy-design/data-minimization.md)

## 11.2 Compliance

* [GDPR Compliance](11.2-compliance/gdpr-compliance.md)
* [Data Protection](11.2-compliance/data-protection.md)
* [Rights Management](11.2-compliance/rights-management.md)
* [Audit Requirements](11.2-compliance/audit-requirements.md)

## 12.1 Glossary

* [Technical Terms](12.1-glossary/technical-terms.md)
* [Industry Terms](12.1-glossary/industry-terms.md)
* [Protocol-Specific Terms](12.1-glossary/protocol-specific-terms.md)

## 12.2 FAQs

* [Common Questions](12.2-faqs/common-questions.md)
* [Troubleshooting](12.2-faqs/troubleshooting.md)
* [Best Practices](12.2-faqs/best-practices.md)

## 12.3 Reference Material

* [Code Examples](12.3-reference-material/code-examples.md)
* [Implementation Guides](12.3-reference-material/implementation-guides.md)
* [External Resources](12.3-reference-material/external-resources.md)
