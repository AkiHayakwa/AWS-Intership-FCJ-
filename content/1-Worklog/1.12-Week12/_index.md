---
title: "Week 12 Worklog"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 1.12. </b> "
---
{{% notice warning %}} 
⚠️ **Note:** The following information is for reference purposes only. Please **do not copy verbatim** for your own report, including this warning.
{{% /notice %}}


### Week 12 Objectives:

* Review and consolidate understanding of all AWS services used in the **CloudBrief** project.
* Redraw and refine the system workflow diagram to accurately reflect the current architecture.
* Identify any gaps or improvements in the existing architecture and documentation.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                                                                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------------------------------------------------------- |
| 2   | - **Re-research AWS services used in CloudBrief project:** <br>&emsp; + **EC2** (`t4g.small` ARM64): Instance lifecycle, Auto Scaling, Security Groups, IAM Role attachment <br>&emsp; + **Amazon S3**: Static hosting, bucket policy, versioning, lifecycle rules <br>&emsp; + **Amazon SQS**: Queue types (Standard vs FIFO), message visibility timeout, DLQ configuration <br>&emsp; + **Amazon DynamoDB**: Table design, partition key strategy, TTL, capacity modes (On-demand vs Provisioned) <br>&emsp; + **Amazon Bedrock**: Model invocation (Nova Lite), prompt structure, token limits, latency considerations <br>&emsp; + **Amazon CloudFront**: Distribution setup, cache behaviors, origin access control (OAC), custom headers | 07/06/2026 | 07/06/2026      | <https://docs.aws.amazon.com/>                                                           |
| 3   | - **Redraw the system workflow diagram of CloudBrief project:** <br>&emsp; + Map out the full data flow: RSS Feed → Collector Worker → SQS → Content Worker → S3 → Summarizer Worker → DynamoDB → Frontend <br>&emsp; + Add CloudFront as the entry point serving both static frontend (S3) and API (EC2) <br>&emsp; + Include IAM roles & policies flow between services <br>&emsp; + Add error handling paths: DLQ for SQS, retry logic for Bedrock throttling <br>&emsp; + Document inter-service communication: which services are public vs private <br>&emsp; + Review and update architecture documentation to match the redrawn diagram | 07/07/2026 | 07/07/2026      | <https://cloudjourney.awsstudygroup.com/>                                                 |
| 4   | - **Code backend for image processing:** <br>&emsp; + Research suitable image processing libraries (Sharp, Jimp...) <br>&emsp; + Code functionality to upload images to S3 <br>&emsp; + Create basic image recognition/processing APIs <br>&emsp; + Integrate image processing flow into CloudBrief's main workflow | 07/08/2026 | 07/08/2026      | <https://docs.aws.amazon.com/>                                                           |
| 5   | - **Fix backend code bugs:** <br>&emsp; + Debug DynamoDB connection issues <br>&emsp; + Fix timeout errors when workers process long articles <br>&emsp; + Refactor concurrency handling code for SQS consumers <br>&emsp; + Optimize API response times and handle exceptions | 07/09/2026 | 07/09/2026      | <https://cloudjourney.awsstudygroup.com/>                                                 |
| 6   | - **Adjust architecture diagram workflow:** <br>&emsp; + Add EventBridge for scheduling automated workers <br>&emsp; + Adjust interaction flow between SQS and Bedrock <br>&emsp; + Add trigger mechanisms for state changes <br>&emsp; + Finalize the system architecture diagram for reporting | 07/10/2026 | 07/10/2026      | <https://cloudjourney.awsstudygroup.com/>                                                 |

### Week 12 Achievements:

* **Deep-dived into each AWS service in the CloudBrief stack** with a focus on understanding *why* each service was chosen:
  * **EC2 `t4g.small` (ARM64)**: Ideal for cost-efficient compute; runs the API server (Express/Bun) and worker processes as background daemons
  * **Amazon SQS (Standard Queue)**: Decouples the Collector, Content, and Summarizer workers — enables retry via visibility timeout and dead-letter queue (DLQ) for failed messages
  * **Amazon DynamoDB**: Stores article records and deduplication hashes; On-demand capacity handles unpredictable RSS collection spikes
  * **Amazon S3**: Hosts clean `.txt` content files (written by Content Worker) and the static frontend build (served by CloudFront)
  * **Amazon Bedrock (Nova Lite)**: Generates AI summaries via InvokeModel API; understanding token limits and throttling behavior is critical for retry design
  * **Amazon CloudFront**: Acts as the sole public entry point — routes `/` to S3 (frontend) and `/api/*` to EC2 (backend) via cache behaviors and Origin Secret Header enforcement

* **Redrawn the CloudBrief system workflow diagram**, covering:
  * Full data pipeline: RSS Feeds → Collector → SQS → Content Worker → S3 + SQS → Summarizer → DynamoDB
  * CloudFront routing: static assets from S3 and API requests forwarded to EC2
  * IAM role assignments: EC2 instance role with permissions scoped to S3, SQS, DynamoDB, and Bedrock
  * Error handling paths: DLQ for poison-pill messages, exponential backoff for Bedrock throttling
  * Security boundary: EC2 not publicly accessible, protected by CloudFront Origin Secret Header

* **Updated architecture documentation** to reflect the redrawn diagram, ensuring all service interactions and security configurations are accurately described.

* **Developed Image Processing Backend:** Researched and integrated an image processing library, creating APIs for image recognition and S3 uploading, seamlessly integrating them into the existing workflow.
* **Resolved Backend Bugs:** Successfully debugged DynamoDB connection issues, fixed worker timeout errors, and refactored SQS consumer concurrency, resulting in a more stable and optimized API response.
* **Finalized System Workflow Diagram:** Adjusted and added EventBridge components, optimized the interaction between SQS and Bedrock, and produced the final, comprehensive architecture diagram for reporting.
* Identified areas for potential improvement in the current architecture:
  * Consider adding CloudWatch Alarms for DLQ message count
  * Evaluate S3 lifecycle policies for cost optimization of old `.txt` files
