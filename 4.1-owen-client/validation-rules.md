# Validation Rules

Files ingested by Owen need to comply with Ddex's Electronic Release Notification (ERN) v4.3 standard (http://service.ddex.net/xml/ern/43). 

In addition, Protocol adds some extra validation rules:
- ResourceList:SoundRecording:ResourceRightsController:RightSharePercentage is between 0 an 100. Never negative or above 100,
- PartyList:Party:Affiliation:Type must be of type "MusicLicensingCompany"
- PartyList:Party:Affiliation:RightType has to include "MakeAvailableRight",
- ISRC is specified for each SoundRecording - SoundRecording:SoundRecordingEdition:ResourceId:{ISRC} and every ISRC within SoundRecording is unique. Also checks the format: `^[A-Za-z]{2}\w{3}\d{7}$`.  
- SoundRecording: ResourceList:SoundRecording:ResourceRightsController:RightsControlType: has to include either "RightsAdministrator" or "RightsController".
- ResourceList:SoundRecording:ResourceRightsController:TerritoryOfRightsDelegation is required
- ResourceList:SoundRecording:ResourceRightsController:DelegatedUsageRights:UseType has to include one of "Stream", "PermanentDownload", "ConditionalDownload", "TetheredDownload"
