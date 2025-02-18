---
description: >-
  Here's how any Distributor or Publisher can integrate with Original Works
  through our three-step process, designed to complement existing industry
  workflows
---

# Technical Setup

<figure><img src="../.gitbook/assets/Original Works Protocol Design - Frame 34 (2).jpg" alt=""><figcaption></figcaption></figure>



1. **Release Management**: OWEN accepts standard DDEX/CWR formats because we believe blockchain adoption shouldn't require changing established industry practices. Your existing release notification system remains unchanged while gaining blockchain benefits.
   * Submit DDEX/CWR notifications as usual&#x20;
   * **Integration**: Run OWEN on your local/hosted setup
     * OWEN client processes these automatically
     * Validated by Original Works Network on Gnosis chain
     * Full audit trail maintained on IPFS/SWARM
     * Full installation guide on github:
       * [https://github.com/originalworks/protocol-core/tree/master/owen](https://github.com/originalworks/protocol-core/tree/master/owen)
       * Script to check all dependencies: [https://github.com/originalworks/protocol-core/blob/master/owen/owen.sh](https://github.com/originalworks/protocol-core/blob/master/owen/owen.sh) \

2. **Rights Registration**: Distributors and Publishers have sophisticated rights management systems. Rather than replacing these, we provide a simple interface to record rights information while maintaining your operational control.
   * Use your existing admin system for licenses and splits
     * **Integration**: Register rights through a local API socket linking you Royalty Pool client with your instance of **OWEN** or using standard formats (DDEX/CWR)
     * Each asset is mapped to a uniquely identifiable asset, in the Original Works tamper-proof and verifiable Registry\

3. **Royalty Distribution**: By partnering with regulated payment providers like Bridge (a Stripe company), we ensure compliance while reducing settlement costs. The batch payment system minimizes operational overhead while maintaining privacy. USDC is the currency we pay out, which is also fully regulated and widely adopted by financial institutions&#x20;
   * **Integration**: Deposit total royalties through Bridge/Stripe (or other) 3rd party
     * Assign revenue per asset - assign deposit per track based on consumption reports
     * Splits and statements generated automatically and parked in pool.
     * Rights holders claim through compliance-verified process
     * Support for anonymous withdrawal addresses

