# OW\_Record type: Recording

A `DataProvider` registering **`Recordings`** on Original works must include the `SoundRecordingId`, which is composed by the ISRC and the ISCC of the recording.
\
A **Recording** that has not bee registered as an OW\_Record (i.e. it was merely specified as metadata in the registration of an `OW_Record_type:Work`) _cannot_ have any associated **`Deals`**

{% tabs %}
{% tab title="DDEX Recording example" %}
```json
<SoundRecordingId> 
    <ISRC>US1234567890</ISRC>
    <ISCC>ISCC:KEC37BNSAEG5UGZOQGP4RB4J4SOOPSLAIL74KIXPQWGN3PZIILZ2YPI</ISCC>
</SoundRecordingId>
```
{% endtab %}
{% endtabs %}