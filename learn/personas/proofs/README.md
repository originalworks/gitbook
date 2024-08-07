# Original Works Validators

Original Works accepts [DDEX and CWR messages](../../../build/technical-overview/supporting-industry-standards/) as the main interface for existing service providers along music supply chais. In order to validate the format of the messages is correct, and that the claim of registration does not conflict any other record (provided by a different service provider or even on a different chain) someone must parse and structure the data that can be indexed by subgraph.&#x20;

Original works may process this on its own "validator" contract in a transparent way (by submitting ZK proof for each new record) so anyone can validate it, and anyone can run a validator by staking $OWN, competing for a chance to validate incoming records and earning new $OWN tokens.

[Data Providers](../../../protocol/personas/data-providers.md) may be verified or unverified, but beyond the simple verification that requires some level of trust in the Original Works foundation, additional steps are required to ensure the protocol is truly decentralized; This involves [staking  $OWN](broken-reference). If their stake falls below a certain threshold, they are restricted from registering new messages until they replenish their stake. \
\
A decentralized network of validators can ensure this mechanism is open, trustless and verifiable.
