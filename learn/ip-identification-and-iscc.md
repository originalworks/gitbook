# IP Identification and ISCC

The mission to accelerate royalty payments across the creative industries is the main mission of the Original Works protocol, and as such providing a unique and precise descriptor for each individual revenue stream of a given IP asset is crucial in order to settle payments with minimum friction or policing.

{% hint style="success" %}
By integrating with Original Works (simply transmitting DDEX ERN messages to the protocol) **every single asset recorded on the registry automatically receives a unique ISCC code and including audio fingerprint hash**. This added value is free out-of-the box for any publisher, distributor or royalty society who want to better ensure the authenticity of their records and avoid conflicting claims in the future.
{% endhint %}

Today assets in the music industry are described using International Standard Codes; ISRC (International Standard Record Code) defined specifically to describe sound recordings (Phonograph), and ISWC (International Standard Work Code) defined specifically to describe musical works (Composition and lyrics)

The only way to capture these identifiers when ingesting a message or transaction regarding an IP asset is by relying on the meta data provided with the file. Many times the same phonograph (master recording) is distributed by ISRC issuers with different codes, and there is no simple way to match ISRCs with media files or ISWCs. Other times, the information is simply missing or a wrong code was entered by error.

ISCC is a new international standard, allowing anyone to create a unique code that is derived from the media itself and ensures a unique audio fingerprint (unique hash) is attached to it so no other identical file could be created, and even more so,  in the case of edited or similar recordings, they will each get unique ISCC codes, but their metadata will preserve the link to the other assets and provide direct links to the different ISCC codes with similarity scores.

Original Works has integrated the generation of ISCC meaning that each Original Works Record will receive an ISCC code. This is to ensure the unicity of each asset recorded, but the ISCC code and accompanying audio fingerprint is a valuable asset for data providers and can be used beyond the bounds of the Original Works protocol.&#x20;

