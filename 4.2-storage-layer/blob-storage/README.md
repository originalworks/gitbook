# Blob Storage

Storage of protocol data is completely decentralized. Protocol stores data on two places:

* Blockchain
* IPFS

IPFS data is additionally secured by Filecoin deals to guarantee availability and increase decentralization.

On IPFS we store one folder per Blob (an live example is [here](https://bafybeicc3kvcgna6nwfyngrlslkckzj6urpz2bh3x4nnyclb6r4mi2qwda.ipfs.w3s.link/)) with the following structure:
* `blob` cotnains the blob itself and relevang metadata
* `json` contains all json files of the original DDEX messages sent by OWEN
* `images` contains all images referenced in the json files

This allows:
* Protocol is not linked to any specific provider or service
* Anybody can verify on what specific servers the IPFS data is stored (usually between 5 and 10)
* Anybody can verify when the filecoin deals for each file expires
* Anybody can extend the filecoin deals that secure the data of the protocol

