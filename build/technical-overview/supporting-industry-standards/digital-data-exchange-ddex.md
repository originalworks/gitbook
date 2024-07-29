---
description: List of ERN, MWN, MWL, RDR and CDM messages used by the protocol.
---

# Digital Data Exchange (DDEX)

\<insert DDEX exerpt>

### DDEX Messages supported by on OWN:

1. **Electronic Release Notification (ERN) Messages**: These messages are used to communicate information about new releases, including metadata about the sound recordings (ISRCs) and the associated musical works (ISWCs). Key messages include:
   * **NewReleaseMessage**: Communicates details about a new release, including metadata for individual sound recordings and musical works.
   * **DealNotificationMessage**: Communicates the commercial terms (deals) associated with the release, specifying usage rights and conditions.
2. **Musical Work Right Share Notification (MWN) Messages**: These messages communicate information about the ownership shares of musical works. This is crucial for linking ISRCs to ISWCs and understanding the rights associated with each work.
   * **MusicalWorkShareNotification**: Provides details on the shares of musical works, including the percentages owned by different parties.
3. **Musical Work Licensing (MWL) Messages**: These messages are used for managing licenses and deals for musical works.
   * **MusicalWorkLicenseRequest**: Requests a license for a musical work.
   * **MusicalWorkLicenseMessage**: Communicates the terms and conditions of the license for a musical work.
4. **Recording Data and Rights (RDR) Messages**: These messages handle the notification of rights and claims related to sound recordings.
   * **DeclarationOfSoundRecordingRightsClaim**: Communicates the rights claims for sound recordings.
   * **RevokeSoundRecordingRightsClaim**: Communicates the revocation of rights claims.
5. **Claim Detail Message (CDM) Suite**: This suite of messages is used to provide detailed claims and invoices related to the exploitation of musical works and sound recordings. It ensures the financial aspects are correctly managed and communicated.
   * **ClaimDetailMessage**: Provides detailed claims and invoice information.
   * **ClaimDetailDiscrepancyNotification**: Communicates discrepancies found in claim details.
6. **Digital Sales Reporting (DSR) Messages**: These messages report sales and usage data for sound recordings and musical works.
   * **SalesReportMessage**: Provides sales and usage data, including the ISRCs and the revenues generated.

#### Example Workflow

1. **Release Notification**: Use `NewReleaseMessage` (ERN) to announce a new release, including ISRCs and their metadata.
2. **Share Notification**: Use `MusicalWorkShareNotification` (MWN) to communicate the shares of the ISWCs associated with the release.
3. **Licensing**: Use `MusicalWorkLicenseRequest` (MWL) and `MusicalWorkLicenseMessage` (MWL)to manage licenses for the musical works.
4. **Rights Management**: Use `DeclarationOfSoundRecordingRightsClaim` (RDR) and `RevokeSoundRecordingRightsClaim (RDR)` to manage rights claims for sound recordings.
5. **Sales Reporting**: Use `SalesReportMessage` (DSR) to report sales and usage data, linking ISRCs to revenues.
6. **Claim Details**: Use `ClaimDetailMessage` (CDM)to provide detailed claims and manage discrepancies with `ClaimDetailDiscrepancyNotification`.

