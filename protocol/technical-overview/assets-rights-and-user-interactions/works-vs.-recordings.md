---
description: Disambiguating between Publishing and Master Royalties
---

# Works vs. Recordings



{% hint style="info" %}
Objects/entities in`CodeFormat` are proposed official naming conventions adopted from the Dedx ERN structure. Objects/entities in **`bold`** have no formal naming convention yet.&#x20;
{% endhint %}

### **Musical works and Recordings.**&#x20;

A musical work is monetized via two different IP ownership schemes, with each governed, administered and controlled by different parties in different regions, with different applicable rights.&#x20;

1. A Musical Work - The intellectual property representing an abstract work that can be musically preformed recorded, synced, etc.. It is usually controlled under various rights covered in the owners' publishing agreement, when registered with Royalty Societies across the globe. Usually unregistered rights are not collected - or worst - collected but never paid out.
2. A Muscial Recording - The ownership rights to the "master track" recording of a specific Musical Work, or not. It is usually covered under a single distributor or agent monetizing the streaming, sync or other rights applicable to recordings.&#x20;

Assets on Original Works are defined as **`Creations`** allowing us o conform to existing standars.&#x20;

We will support two&#x20;

**`Creation:`** a type of media or IP asset that is being monetized&#x20;

* **`CreationType`**
  * **`Release`**
    * `(optional)`**`ReleaseType`**\

  * **`Resource`**
    * **`ResourceType`**
      * **`SoundRecording`**

In the future we will unlock additional asset types:

* **`CreationType`**
  * <mark style="background-color:purple;">**MusicalWork (unreleased music)**</mark>
* **`Resource`**
  * **`ResourceType`**
    * **`SoundRecording`**
    * <mark style="background-color:purple;">(any acceptable Ddex descriptor)</mark>

### Original Works Assets

A musical work is identified on the Original Works ecosystem by its 0x address and the protocol ensures it has a unique `RevenueSource` by validating the combination of it's international identifier `ISWC` /`ISRC` and its unique combination of public and private terms.&#x20;

A **`CreationType`** can be added by anyone by pinning the record to a local IPFS node and transmitting the CID to the protocol. This ensures an immutable record of a fully-private registration  is generated and can be made public

This musical asset has a given number of lawful owners at any given time. The owners are usually represented by an administrating company, such as a publishing admin and may have several royalty societies representing their collection rights in different teritorries. These representatives act as the network "Oracles" in a sense as they provide records and attestations about the "Real World {music} Asset" and may become a verified `DataProvider` to the protocol, using their public address to interact with the protocol. Assets registered by a verified data provider will have a "verified" status.

Personas related to a `Creation`:&#x20;

* `CopyrightClaimant` - A Party listed as copyright owner at the time of registration.
* `CopyrightHolder` - A Party to whom copyright has been granted or transferred.\
  \
  Both users can be listed as the current legal owner(s) of the underlying IP. \
  If the asset is tokenized then then these users become the `admins` and all actions triggered on-chain by the `CopyrightController` will need the collective owner's on-chain approval.
* `CopyrightController` - The `DataProvider` in charge of registering the asset, keeping the on-chain records available and providing verifiable proofs about the asset on-demand. As long as the IP Asset has not been tokenized by the `CopyrightHolder`(s), then the `copyrightController` remains the `admin` and acts as their on-chain representative.

###
