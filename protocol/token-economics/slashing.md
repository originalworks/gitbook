# Slashing

Oracles who are found to be fraudulent actors can expect to have their stake slashed, the size of the slash amount depends on the type of network fault.&#x20;

These faults include:&#x20;

*   Not transmitting funds on chain to a relevant OMA in a timely fashion, despite receiving the funds from DSPs or other rights management companies/participants, because of:&#x20;

    * Internal mismanagement of funds - 1% slashing penalty of staked amount.&#x20;
    * The artist requests the oracle to resume payments off-chain and the oracle does this without checking whether the OMA’s royalty flow is committed to another party, such as being part of a wOMA (i.e it is being used as collateral) - 10% slashing penalty of staked amount.&#x20;


* Providing an asset fact sheet that is incorrect or unavailable:&#x20;
  * Misreporting asset revenue history - 5% slashing penalty of staked amount.&#x20;
  * Misreporting known claims and red flags - 5% slashing penalty of staked amount.&#x20;
  * Not ensuring the liveness of the asset fact sheet - 2% slashing penalty of staked amount.&#x20;

It’s important to note that oracles do not get slashed for events or data that is not under their control. This includes a DSP not transmitting payments in a timely fashion or if they manage distribution for an artist who commits fraud and misrepresents data or cash flow for their music. An oracle can only be slashed for things under their control.
