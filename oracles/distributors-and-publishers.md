# Royalty Administrators

Royalty Administrators are the gateway to the existing music industry, managing rights registration and royalty distribution. Initially permissioned, the service will transition to permissionless once tokenomics and staking are introduced.

### **Music Distributors**

**Traditional Industry Role:**

* Deliver music to digital streaming platforms (Spotify, Apple Music, etc.)
* Collect and process master recording royalties
* Generate and manage ISRC codes
* Handle digital asset delivery and metadata
* Maintain relationships with artists and record labels

**Protocol Royalty Admin Duties:**

* Submit DDEX.ERN messages through [OWEN](https://github.com/originalworks/protocol-core/tree/master/owen) for new releases
* Tokenize master recording rights using protocol standards
* Operate [Royalty Pools](https://docs.original.works/original-works/3.1-royalty-pools) for master recording earnings
* Provide verifiable proof of streaming revenues
* Maintain accurate play counts and revenue allocation
* Enable automated royalty splits through smart contracts

### **Publishers**

**Traditional Industry Role:**

* Register and protect musical compositions
* Collect sync and mechanical royalties
* Handle songwriter/composer relationships
* Manage or outsource territorial rights
* Interface with collection societies worldwide

**Protocol Royalty Admin Duties:**

* Submit CWR (Common Works Registration) data through [OWEN](https://github.com/originalworks/protocol-core/tree/master/owen)
* Tokenize publishing rights using protocol standards
* Operate [Royalty Pools](https://docs.original.works/original-works/3.1-royalty-pools) for publishing royalties they are responsible for collecting
* Process territorial rights claims
* Enable automated writer share distributions
* Provide verifiable proof of performance royalties

### **Collective Management Organizations (CMOs)**

**Traditional Industry Role:**

* Collect and distribute performance royalties
* Manage blanket licenses for territories
* Monitor music usage across venues
* Process international royalty claims
* Interface with other CMOs globally

**Protocol Royalty Admin Duties:**

* Operate dedicated [Royalty Pools](https://docs.original.works/original-works/3.1-royalty-pools/)
* Receive publisher delegations for payment processing
* Distribute royalties based on publisher-registered splits
* Process CWR data transmitted through [OWEN](https://github.com/originalworks/protocol-core/tree/master/owen)
* Manage territorial collection rights
* Provide verifiable proof of collections and distributions

**Combined Service Providers**

Some organizations provide both distribution and publishing services. In these cases, they can:

* Operate as both types of Royalty Admins
* Maintain separate [Royalty Pools](https://docs.original.works/original-works/3.1-royalty-pools/) for different rights types
* Process both DDEX.ERN and CWR through a single [OWEN](https://github.com/originalworks/protocol-core/tree/master/owen) installation
* Provide comprehensive rights management on the protocol
