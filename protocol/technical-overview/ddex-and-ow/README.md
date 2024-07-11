---
description: Original Works protocol uses the DDEX standard
---

# DDEX and OW

[DDEX](https://ddex.net/) is a standards setting organisation focused on the creation of digital value chain standards to make the exchange of data and information across the music industry more efficient.

#### DDEX has multiple standards that are used by the Original Works Protocol:

1. **ERN** focuses heavily on the lifecycle of releases, including metadata, deals, and takedown messages, which are specific to the distribution and management of digital releases.
2. **MWN** is centered around the notification and licensing of musical work shares, emphasizing the identification and licensing shares of musical works.
3. **RDR-N** deals with the declaration and management of rights claims related to sound recordings, with a focus on the exchange of rights claims and sales reporting.
4. **CDM** provides detailed mechanisms for communicating claims and discrepancies related to sales/usage reports, with a strong emphasis on financial and royalty claims.

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



Some critical compoments for the OW protocol are available on only some of the standards and others are available in several of them. Below is a table summarizing:



<table><thead><tr><th>No.</th><th width="330">Component</th><th width="84">ERN</th><th width="77">MWN</th><th width="83">RDR-N</th><th>CDM</th></tr></thead><tbody><tr><td>1</td><td>NewReleaseMessage</td><td>Yes</td><td>No</td><td>No</td><td>No</td></tr><tr><td>2</td><td>Takedown Messages</td><td>Yes</td><td>No</td><td>No</td><td>No</td></tr><tr><td>3</td><td>Release Types</td><td>Yes</td><td>No</td><td>No</td><td>No</td></tr><tr><td>4</td><td>Release Profiles</td><td>Yes</td><td>No</td><td>No</td><td>No</td></tr><tr><td>5</td><td>Statement of Truth</td><td>Yes</td><td>No</td><td>No</td><td>No</td></tr><tr><td>6</td><td>Rights Controller</td><td>Yes</td><td>Yes</td><td>Yes</td><td>Yes</td></tr><tr><td>7</td><td>Commercial Model Type</td><td>Yes</td><td>No</td><td>Yes</td><td>Yes</td></tr><tr><td>8</td><td>Usage Type</td><td>Yes</td><td>Yes</td><td>Yes</td><td>Yes</td></tr><tr><td>9</td><td>Rights Type</td><td>Yes</td><td>Yes</td><td>Yes</td><td>Yes</td></tr><tr><td>10</td><td>MusicalWorkShare-Request</td><td>No</td><td>Yes</td><td>No</td><td>No</td></tr><tr><td>11</td><td>MusicalWorkShare-Notification</td><td>No</td><td>Yes</td><td>No</td><td>No</td></tr><tr><td>12</td><td>Licensing Share</td><td>No</td><td>Yes</td><td>No</td><td>No</td></tr><tr><td>13</td><td>Hub-Centric Approach</td><td>No</td><td>Yes</td><td>No</td><td>No</td></tr><tr><td>14</td><td>Rights Share</td><td>No</td><td>Yes</td><td>No</td><td>Yes</td></tr><tr><td>15</td><td>DeclarationOfSound-RecordingRightsClaim-Message</td><td>No</td><td>No</td><td>Yes</td><td>No</td></tr><tr><td>16</td><td>RevokeSoundRecording-RightsClaimMessage</td><td>No</td><td>No</td><td>Yes</td><td>No</td></tr><tr><td>17</td><td>RightsClaimStatus-UpdateMessage</td><td>No</td><td>No</td><td>Yes</td><td>No</td></tr><tr><td>18</td><td>SalesReportMessage</td><td>No</td><td>No</td><td>Yes</td><td>No</td></tr><tr><td>19</td><td>ManifestMessage</td><td>No</td><td>No</td><td>Yes</td><td>No</td></tr><tr><td>20</td><td>Claim Detail Message</td><td>No</td><td>No</td><td>No</td><td>Yes</td></tr><tr><td>21</td><td>Claim Detail Discrepancy Notification</td><td>No</td><td>No</td><td>No</td><td>Yes</td></tr><tr><td>22</td><td>Correction or Update of a Claim Detail Message (CDMCor)</td><td>No</td><td>No</td><td>No</td><td>Yes</td></tr><tr><td>23</td><td>Invoice Details</td><td>No</td><td>No</td><td>No</td><td>Yes</td></tr><tr><td>24</td><td>Choreography</td><td>No</td><td>No</td><td>No</td><td>Yes</td></tr><tr><td>25</td><td>Release</td><td>Yes</td><td>No</td><td>Yes</td><td>Yes</td></tr><tr><td>26</td><td>Resource</td><td>Yes</td><td>No</td><td>Yes</td><td>Yes</td></tr><tr><td>27</td><td>Sales/Usage Report Message</td><td>Yes</td><td>No</td><td>Yes</td><td>Yes</td></tr><tr><td>28</td><td>Profile</td><td>Yes</td><td>Yes</td><td>Yes</td><td>Yes</td></tr><tr><td>29</td><td>Delimiter</td><td>Yes</td><td>Yes</td><td>Yes</td><td>Yes</td></tr><tr><td>30</td><td>Block</td><td>Yes</td><td>Yes</td><td>Yes</td><td>Yes</td></tr></tbody></table>

