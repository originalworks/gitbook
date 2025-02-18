---
description: >-
  OWEN can run on your local environment or be hosted on your cloud
  infrastructure.
---

# Configuration Options

### **This github guide will walk you through deploying a DDEX processing pipeline on your AWS account.**&#x20;

#### The architecture consists of:

* An S3 bucket (`ddex-messages-prod`) for uploading DDEX files.
* A Lambda function (`sendDdexToSQS`) to process uploaded files.
* An SQS FIFO queue (`OwenInputQueue.fifo`) to manage zip file delivery.
* A Lambda function (`Owen`) to process the zip files from the queue.

#### To read the full guide see our github entry for the latest version:

[https://github.com/originalworks/protocol-core/tree/master/owen/aws](https://github.com/originalworks/protocol-core/tree/master/owen/aws)
