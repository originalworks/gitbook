---
description: List of terms used in the protocol and in the DDEX standard.
---

# Glossary

#### Common Terms Across DDEX Standards

1. **Licensor**: A party that grants a license in respect of rights in one or more creations (e.g., Musical Works, Sound Recordings) to one or more Licensees. The Licensor may also be the Rights Controller, Rights Administrator, or Rights Holder.
2. **Licensee**: A party that is granted a license in respect of rights in one or more creations by a Licensor. The Licensee may be a human being or other legal person or corporate entity.
3. **Release**: An abstract entity representing a bundle of one or more resources compiled by an issuer. Resources in releases are typically sound recordings or music audiovisual recordings.
4. **Resource**: A digital fixation of an expression of an abstract work (such as a sound recording, video, image, software, or text). Resources are individual assets that make up a Release.
5. **Sales/Usage Report Message**: A message created in accordance with DDEX standards to report sales and usage data.
6. **Block**: A group of records in a message that communicates information that belongs intrinsically together. Blocks contain the same Block Identifier and Record Identifier.
7. **Delimiter**: Characters used to separate data elements within a record (e.g., tabs, pipes).
8. **Profile**: A subset of a DDEX standard that defines how to use the capabilities of the standard in a specific commercial context.

#### Specific Terms and Their Usage in Different Standards

**Electronic Release Notification (ERN)**

* **NewReleaseMessage**: Communicates metadata about a new release including descriptive metadata, deals, and other necessary information.
* **Takedowns**: Messages sent to remove a release from distribution.
* **Deal**: Information about the terms under which a release is made available (e.g., pricing, allowed types of usage).

**Musical Work Right Share Notification (MWN)**

* **MusicalWorkShare-Request**: A request message to identify the owners of shares in a musical work.
* **MusicalWorkShare-Notification**: A notification message that informs about the share owners and their respective shares in a musical work.
* **Licensing Share**: The share of a musical work that can be licensed by a specific publisher or entity.

**Recording Data and Rights Notification (RDR-N)**

* **DeclarationOfSound-RecordingRightsClaim-Message**: A message for declaring rights claims or mandates related to sound recordings.
* **RevokeSoundRecording-RightsClaimMessage**: A message to revoke previously declared rights claims.
* **RightsClaimStatus-UpdateMessage**: A message to update the status of a rights claim.
* **SalesReportMessage**: Provides sales and usage figures for sound recordings.

**Claim Detail Message (CDM)**

* **Claim Detail Message**: A format for a response to a sales/usage report that sets out the claim each owner/administrator is making in respect of musical works identified in the report.
* **Claim Detail Discrepancy Notification**: A message to signal discrepancies in the claim detail messages.
* **Correction or Update of a Claim Detail Message (CDMCor)**: A message format used to correct previously sent claim detail messages.
* **Invoice Details**: Details of the financial claims being made by a licensor against a licensee based on usage data.

####

