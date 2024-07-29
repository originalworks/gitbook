# Licenses



{% hint style="info" %}
Objects/entities in`CodeFormat` are proposed official naming conventions adopted from the Dedx ERN structure. Objects/entities in **bold** have no formal naming convention yet.
{% endhint %}

### **License**

A License is agreement granted to a `RightsHolder` to exercise one or more of the usage rights, described as `RightsCoverage` that can be granted by a `PaymentProvider` in relation to a specific registered **`Creation`** in specific territories, time periods, and`RightsCoverage` types.

`RightsHolder` - is the Party that holds the rights in respect of some or all rights in one or more **`Creation`**

**`PaymentProviderRoles`** related to a **`Creation`**:

* `RightsController` **-** The `DataProvider` in charge of registering the asset, keeping the on-chain records available and providing verifiable proofs about the asset on-demand. As long as the **`Creation`** has not been tokenized by the `RightsHolder`(s), then the `RightsController` remains the `admin` and acts as their on-chain representative. It is typically an enterprise like a music distributor or publishing admin that controls rights in one or more Creations in respect of some or all rights for specific territories, time periods,`RightsCoverage` types.
* `RightsAdministrator` - The administrator assigned by the Rights Controller in charge with administering the rights off-chain;\\
* `RightsCoverage`:
  * `MakeAvailableRight`: The right to distribute and make a work available to the public.
  * `MechanicalRight`: The right to record and distribute a work on a carrier. (applicable for ISWC assets only)
  * `PerformingRight`: The right to perform a work.
  * `PrintRight`: The right to make a visual copy of a work and distribute it.
  * `ReproductionRight`: The right to make a physical reproduction of a work.
    * `SynchronizationRight`: The right to include a work in timed relation with other works for making an audiovisual or multimedia creation.
  * `UserDefined`: Complying with the DDEX

### **License uniqueness and data availability**

Only one combination of `RightsCoverage` + **`Region`** with overlapping active dates can be issued for any giver **`Creation`** may be valid

{% hint style="info" %}
**bold** fields are compulsory. _italic_ fields are optional.
{% endhint %}

**bold** fields are compulsory. _italic_ fields are optional.

#### Public data

* **`License creator`**
* **`License signature`**
* **`Reference to Creation ID`**
* **`Right coverage`**
* **`Region (ISO 3166)`**
* **`startDate`**
* _`CID to private data of license`_
* _`Blockchain`_
* _`Contract`_

#### Private Data

* **`CID to public data`**
* **`sharePercentage`** - _what percentage of the revenue of this the rights licensed is collected by this specific license_
* **`revenueSource`** _- array of all known (non-exclusive) platforms exercising this license_
* _`RightsCoverage`_ _- how the IP is consumed - ad based streams, ad-free radio, etc…_
* _`FactSheet`_ - custom JSON that may be private or public
* \*`Agreement` \*- optional link to a URL hosted copy of the PDF/DOC of the agreement

#### **Data that can be added as private or public**

* **`RightsHolder`** - A Party that holds the rights in respect of some or all rights in one or more `Creation` in specific territories, time periods, `RightsCoverage` types, and types
* **`RightsController`** - The `DataProvider` in charge of registering the asset, keeping the on-chain records available and providing verifiable proofs about the asset on-demand. As long as the `Creation` has not been tokenized by the `RightsHolder`(s), then the `RightsController` remains the `admin` and acts as their on-chain representative. It is typically an enterprise like a music distributor or publishing admin that controls rights in one or more Creations in respect of some or all rights for specific territories, time periods,`RightsCoverage` types.
* `RightsAdministrator` - The administrator assigned by the Rights Controller in charge with administering the rights off-chain;\\
* `RightsCoverage`:
  * `MakeAvailableRight`: The right to distribute and make a work available to the public.
  * `MechanicalRight`: The right to record and distribute a work on a carrier. (applicable for ISWC assets only)
  * `PerformingRight`: The right to perform a work.
  * `PrintRight`: The right to make a visual copy of a work and distribute it.
  * `ReproductionRight`: The right to make a physical reproduction of a work.
    * `SynchronizationRight`: The right to include a work in timed relation with other works for making an audiovisual or multimedia creation.
  * `UserDefined`: Complying with the DDEX
