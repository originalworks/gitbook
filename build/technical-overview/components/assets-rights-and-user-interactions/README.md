# Assets, Rights and User interactions

{% hint style="info" %}
In This section we will cover the basic building blocks of the protocol (**`Creations`** and **`Licenses`**), which represent the the "real-world asset" and related "cashflos" respectively, and how they relate to the different Personas and User Roles.
{% endhint %}

## System Components

<table><thead><tr><th width="145">Component</th><th width="244">Description</th><th width="164">Unique Key</th><th width="119">Conditions</th><th width="108">Who Creates?</th><th>Wo Approves</th></tr></thead><tbody><tr><td>MusicalWork</td><td>A Musical Work</td><td><a data-footnote-ref href="#user-content-fn-1">ISWC</a></td><td></td><td></td><td></td></tr><tr><td>Sound Recording</td><td>A Recording (typically of a Musical Work)</td><td>ISRC</td><td></td><td></td><td></td></tr><tr><td>Release</td><td>A product containing one or more Sound Recordings </td><td>UPC</td><td></td><td></td><td></td></tr><tr><td>UserDefined</td><td>A custom reference to unique intellectual property, media resource or 0x address</td><td></td><td></td><td></td><td></td></tr><tr><td><a data-footnote-ref href="#user-content-fn-2">RightsRegistered</a></td><td>A single entry in the OW Registry database</td><td>Creation+RightType+<strong>Territory</strong></td><td></td><td></td><td></td></tr><tr><td>Territory</td><td>ISO 3166-1, ISO 3166-2</td><td></td><td></td><td></td><td></td></tr><tr><td>Deal</td><td></td><td>RightsRegistered</td><td></td><td></td><td></td></tr><tr><td>RightShare</td><td></td><td></td><td></td><td></td><td></td></tr><tr><td>RightsCoverage</td><td>A type of right to make use of the Creation under a License</td><td>A fixed list of rights covered will be maintained by the Foundation</td><td></td><td></td><td></td></tr><tr><td>Proof</td><td>A validation that a statement about an asset is true.</td><td>--</td><td></td><td></td><td></td></tr><tr><td>Creation Tokens</td><td>Governance tokens allowing the RightsHolders of a</td><td>--</td><td></td><td></td><td></td></tr><tr><td>Royalty Tokens</td><td></td><td>--</td><td></td><td></td><td></td></tr><tr><td>$OWN Token</td><td></td><td></td><td></td><td></td><td></td></tr></tbody></table>

## Protocol Users

|                   |   |   |
| ----------------- | - | - |
| Rights Holders    |   |   |
| Copyright Holders |   |   |
| Data Providers    |   |   |
| Payment Providers |   |   |
| Validators        |   |   |
| Relayers          |   |   |

* Creation
  * release
    * license
      * rights
  * work
    * license
      * rights

[^1]: The OW foundation will add more Creation types and global identifiers as part of its roadmap

[^2]: Proposed naming convention for the registration of a single entry in the OW DB
