# Error Handling

Owen encounters two types of errors: fatal errors, which cause the process to terminate, and recoverable errors, which affect individual messages but allow processing to continue.

## Fatal Errors (Process-Terminating)
These errors will cause Owen to shut down:

**Configuration Error** – Occurs during startup if required environment variables are missing.

**RPC Error** – Arises when there is an issue with the RPC provider, such as failure to retrieve blockchain data or insufficient wallet funds for blockchain operations.

**Versioning Error** – Occurs if the image ID used by Owen is not accepted by the Sequencer contract, preventing transactions that would otherwise be rejected.

**Input Error** – Happens when input files are not correctly organized.

## Recoverable Errors (Message-Specific)
These errors affect individual messages but do not stop processing. Affected messages will be marked as rejected, logged, and excluded from the blob:

**Validation Error** – Occurs when a message fails validation.

**Input Error** – Happens if a message is in the wrong format or is missing.

**Media Processing Error** – Occurs when an audio or image file cannot be processed.

**IPFS Error** – Arises if a media file cannot be uploaded to IPFS.
