# Installation Requirements

**To run OWEN on Holesky, you'll need four things:**

1. **RPC endpoint URL**: This should point to the Holesky blockchain network. You can get one for free from most RPC providers like Alchemy, Chainstack, QuickNode, etc.
2. **IPFS client**: in the current implementation, we support two solutions:
   * **Pinata's JWT Token**: You can get one for free here: [Pinata](https://pinata.cloud/) / [API keys](https://docs.pinata.cloud/account-management/api-keys)
   * **IPFS Kubo client endpoint URL with exposed** [**API V0**](https://docs.ipfs.tech/reference/kubo/rpc/): For testing purposes, you can run it locally with the following Bash command from the project root folder: `docker compose -f ./docker/run-local.yml up ipfs`. For production environments, you should run a full version on your server or in the cloud.
3. **Private key of your wallet** with funds on Holesky testnet
4. **Folder with your DDEX messages in xml format**: Each message should be in a separate subfolder and include an image file. You can use our test files from the `owen/tests/msg_one` and `owen/tests/msg_two` folders, but remember to change some values because the Protocol prevents sending identical BLOBs twice.
