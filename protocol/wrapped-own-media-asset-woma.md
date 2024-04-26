# Wrapped OWN Media Asset (wOMA)

An OMA includes all the core building blocks for on-chain integration and use, however, music IP assets are complex and royalty streams fluctuate and have many nuances. We introduce the wrapped OMA, a protocol wrapper contract that provides additional functionality and data for third-party participants or DeFi protocols to fully interact with an OMA.

A wOMA adds several aspects to an OMA:&#x20;

* Designated wallet addresses that supersede the OMA owner. This ensures that if the OMA is used as collateral, the appropriate account will receive the royalty payments.
* A time period for the wOMA's existence.&#x20;
* An OWN Protocol risk factor and suggested discount rate, calculated by using the advanced analytics of a DP and the time period of the wOMA.&#x20;
* Percentage of the OMAs payment flow that the artist wants to lock up in the wOMA. This enables partial and fractional use of the OMA.&#x20;
* wOMA termination details, which include terms for the legitimate termination of the wOMA (for example payment of the specified royalty payment amount) or early termination should the artist choose including an early termination fee.&#x20;

The additional aspects that a wOMA  adds to an OMA, enable the OMA to become a fully functioning financial asset, granting artists control over their royalty streams and investors assurances and data to make appropriate financial decision
