---
description: Disambiguating between Publishing and Master Royalties
---

# Musical Works, Recordings and UserDefined IP Assets

{% hint style="info" %}
Objects/entities in`CodeFormat` are proposed official naming conventions adopted from the DDEX ERN structure. Objects/entities in **`bold`** have no formal naming convention yet.
{% endhint %}

### **Musical works and Recordings.**

A musical creation is monetized via two different IP ownership schemes, with each governed, administered and controlled by different parties in different regions, with different applicable rights.

1. A Musical Work - The intellectual property representing an abstract work that can be musically performed recorded, synced, etc.. It is usually controlled under various rights covered in the owners' publishing agreement, when registered with Royalty Societies across the globe. Usually unregistered rights are not collected - or worst - collected but never paid out.
2. A Sound Recording - The ownership rights to the "master track" recording (or phonograph) of a specific Musical Work, or with now related Music Work. It is usually covered under a single distributor or agent monetizing the streaming, sync or other rights applicable to recordings.\
   Performance rights from recordings are often collected by PROs and are still invoiced by societies, and not digitally collected.

Assets on Original Works are defined as `OW Records` - A unique proof of a unique record referencing either a Recording or Work:

1. `OW_Record_type:Recording`&#x20;
2. `OW_Record_type:Musical Work`

Both assets must be delivered in the context of a **`Release`**, and the OW protocol will alert of any conflicting registrations thath take place in the same territory, for the same record.

Releases continue one or many Resouces with can be of many types (`ResorceType`):

- **SoundRecording**: Digital audio file, such as a song, spoken word recording, or other audio content.
- **MusicalWork**: Underlying composition, including music and lyrics, associated with a sound recording.
- **ImageResource**: Visual assets associated with a release.
- **Video**: Audiovisual content associated with a release.
- **Text**: Textual content related to the release.
- **Lyrics**: A specific type of Text that represents the lyrics of a song.
- **Label**: Graphical elements or logos associated with the record label.
- **DigitalBooklet**: Document resource that provides additional information or content related to a release.
- **InteractiveMenu**: Interactive elements that could be part of a multimedia release.
- **Document**: Additional documents associated with a release.
- **Software**: Digital applications or interactive media associated with a release.
- **OtherResource**: Any other digital asset that doesn’t fall into the standard categories.

### Original Works Assets and Governance

A musical work is identified on the Original Works ecosystem by its 0x address and the protocol ensures it has a unique `RevenueSource` by validating the combination of it's international identifier `ISWC` /`ISRC` and its unique combination of public and private terms.

An `OW_Records` can be added by anyone by pinning the record to a local IPFS node and transmitting the CID to the protocol. This ensures an immutable record of a fully-private registration is generated and can be made public

This musical asset has a given number of lawful owners at any given time. The owners are usually represented by an administrating company, such as a publishing admin and may have several royalty societies representing their collection rights in different territories. These representatives act as the network "Oracles" in a sense as they provide records and attestations about the "Real World {music} Asset" and may become a verified `DataProvider` to the protocol, using their public address to interact with the protocol. Assets registered by a verified data provider will have a "verified" status.

Personas related to an OW\_Record:

* `CopyrightClaimant` - A Party listed as copyright owner at the time of registration.
* `CopyrightHolder` - A Party to whom copyright has been granted or transferred.\
  \
  Both users can be listed as the current legal owner(s) of the underlying IP.\
  If the asset is tokenized then then these users become the `admins` and all actions triggered on-chain by the **`CopyrightController`** will need the collective owner's on-chain approval.
* `CopyrightController` - The `DataProvider` in charge of registering the asset, keeping the on-chain records available and providing verifiable proofs about the asset on-demand. As long as the IP Asset has not been tokenized by the `CopyrightHolder`(s), then the `copyrightController` remains the `admin` and acts as their on-chain representative.
