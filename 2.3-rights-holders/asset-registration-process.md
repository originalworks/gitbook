# Asset Registration Process

### Standard Asset Registration Process

Rights Holders register their assets through Royalty Admins who:

* Submit standard industry formats (DDEX.ERN/CWR)
* Register rights and splits
* Generate verifiable proofs
* Issue ERC1155 voucher tokens

Rights Holders receive vouchers representing their right to collect royalties, while actual split percentages remain private.

### Early Authentication Process (Direct registration for independent creators).

Creators can establish verifiable proof of their work before formal distribution through Original Works' early authentication system.

{% stepper %}
{% step %}
### **Initial Submission**

* Upload audio file
* Provide basic metadata
* Sign submission with creator's key
* Generate ISCC fingerprint
{% endstep %}

{% step %}
### ISCC Generation&#x20;

In this step the protocol captures the audio submitted by the creator and a code is generated using the [ISCC audio fingerprinting algorithm](https://iscc.codes/) &#x20;

```
ISCC Components:
- Content-Code: Audio fingerprint
- Meta-Code: Essential metadata hash
- Data-Code: Technical metadata
- Instance-Code: File hash
```
{% endstep %}

{% step %}
### Blockchain Registration

When the work is later registered through a Royalty Admin, the protocol can verify:

1. Original timestamp
2. Creator's signature
3. Audio fingerprint match
4. Unaltered metadata

This creates an immutable chain of custody from creation to formal registration, helping creators protect their rights and prove authenticity.

#### Example Use Case:

```
1. Creator generates ISCC: 2024-01-15
2. Signs and registers proof
3. Distributes through label: 2024-03-01
4. Label registers rights
5. Protocol verifies original proof
6. Creation timestamp maintained
```
{% endstep %}
{% endstepper %}

