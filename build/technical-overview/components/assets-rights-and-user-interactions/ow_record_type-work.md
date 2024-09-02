# OW\_Record\_type: Work

A `DataProvider` registering **Works** on Original works must include the `MusicalWorkid` identifier, composed of an ISWC as the key value (alongside `Territory` and `rightType`.  Any `Resource` identifier (i.e. ISRC)  will be treated as metadata, but will not override the `Resource` identifier submitted by the in registration of the **`Recording`**.\
\
A **Work** that has not bee registered as an OW\_Record (i.e. it was merely specified as metadata in the registration of an `OW_Record_type:Recording`) _cannot_ have any associated **`Deals`**


{% tabs %}
{% tab title="DDEX Works example" %}
```json
<ResourceDetailsByTerritory>
    <TerritoryCode>Worldwide</TerritoryCode>
    <MusicalWorkId>
        <ISWC>T-123.456.789.Z</ISWC>
    </MusicalWorkId>
</ResourceDetailsByTerritory>
```
{% endtab %}
{% endtabs %}