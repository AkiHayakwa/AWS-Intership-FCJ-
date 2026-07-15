---
title: "Proposal"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 2. </b> "
---
{{% notice warning %}}
⚠️ **Note:** The information below is for reference purposes only. Please **do not copy verbatim** for your report, including this warning.
{{% /notice %}}

In this section, you need to summarize the contents of the workshop that you **plan** to conduct.

# AI-Powered Data Extraction & Summarization Platform
## Group Project: Automated Data Collection and Summarization Solution using AWS & Amazon Bedrock

### 1. Executive Summary  
The "AI-Powered Data Extraction & Summarization Platform" project is designed and developed by our team to solve the problem of automatically collecting, extracting, and summarizing large volumes of data from external APIs. Instead of time-consuming manual processing, the platform leverages the power of Amazon Bedrock (Generative AI) combined with a highly scalable AWS architecture (EC2 Auto Scaling, SQS, EventBridge) to process data periodically in a fully automated, secure, and cost-optimized manner.

### 2. Problem Statement  
*Current Problem*  
Currently, collecting information from external data sources (External APIs) and summarizing content is done manually or through disjointed scripts. This leads to instability, difficulty in scaling when data volume increases, and consumes a lot of personnel time to read and analyze data.

*Our Team's Solution*  
Our team proposes a fully automated system on AWS. The user interface is distributed via CloudFront. The data processing backend runs on EC2 instances (located in a Private Subnet for security) managed by an Auto Scaling Group. The data retrieval and processing workflow is automatically scheduled every 8 hours by EventBridge and SQS. The core strength of the solution is the integration of Amazon Bedrock so that AI can automatically read, clean, and summarize data. The results are durably stored in S3 and DynamoDB.

*Benefits and Return on Investment (ROI)*  
The solution helps 100% automate the periodic data collection and reporting process, saving dozens of working hours per week for the analysis team. By using Auto Scaling and resource limits, the system optimizes operating costs as it only allocates resources when there are actual data processing tasks.

### 3. Solution Architecture and Execution Flow
The project's architecture is designed by the team to comply with security standards and high availability on AWS, ensuring the data flow is processed in a closed and secure manner.

![Architecture Diagram](/images/2-Proposal/cloudbrief-current-architecture.drawio.png)

*Detailed Execution Flow:*
1. **User Communication (Frontend)**: Users access the application via **CloudFront** (protected by **AWS WAF**). CloudFront securely distributes static content from the **S3 bucket (frontend, private, versioned)** via OAC (Origin Access Control) and configured behaviors.
2. **Automation Trigger**: An **EventBridge Trigger** is configured to trigger every 8 hours, sending a message to an **SQS** queue to initiate the data extraction process.
3. **Compute Network**: The system uses an **Auto Scaling Group** managing **EC2 Workers**. These servers are allocated in **Private Subnets (A and B)** (without Public IPs) to ensure security. These Workers continuously pull jobs from the queue via the **SQS VPC Endpoint**.
4. **Data Collection (Outbound Traffic)**: To retrieve data from **External APIs**, the EC2 Workers connect to the internet via a **NAT Gateway** (located in a Public Subnet) and route through an **Internet Gateway**.
5. **Generative AI Integration**: After retrieving the data, the EC2 Worker pushes the content to **Amazon Bedrock** via the **Bedrock VPC Endpoint** for the language model to extract information and summarize.
6. **Secure Result Storage**: 
   - Cleaned text data (Cleaned content) is pushed directly by the Worker into an **S3 bucket** via the **S3 Gateway Endpoint**.
   - Metadata and structured information are saved to **DynamoDB** via the **DynamoDB VPC Endpoint**. This database is configured for automatic Backup.
   - Advanced summary jobs or status messages can also be pushed to the **SQS Summarize** queue via the SQS Endpoint.
7. **Monitoring & Alerting**:
   - The EC2 Workers are managed via **Systems Manager (Session Manager - SSM)**, eliminating the need to open SSH ports.
   - All logs and metrics are collected by **CloudWatch**.
   - If the system detects abnormalities exceeding thresholds (CloudWatch Alarm), notifications are sent via an **SNS Topic** to the **Admin's Email**.
8. **Security and Cost Management**:
   - Use **Security Groups** and **IAM Roles** for the ASG following the principle of least privilege (least scoped).
   - Set up **AWS Budgets** to automatically send email alerts when system costs exceed control levels.

### 4. Technical Implementation  
*Team Assignment and Implementation Phases:*
- **Phase 1 (Design & Initialization)**: The team builds the foundational VPC network with full Public/Private Subnets, NAT Gateway. Establishes the secure S3 Frontend via CloudFront and WAF.
- **Phase 2 (AI Integration & Scheduling)**: Installs and configures the Auto Scaling Group for EC2 Workers. Builds the EventBridge schedule and SQS. Develops source code for the EC2 Worker to call External APIs and Amazon Bedrock.
- **Phase 3 (Internal Storage)**: Sets up VPC Endpoints (S3, DynamoDB, SQS, Bedrock) to ensure traffic does not go over the public internet. Creates DynamoDB tables and corresponding S3 buckets.
- **Phase 4 (Monitoring & Finalization)**: Integrates CloudWatch, SNS, Systems Manager. Reviews and tests IAM Roles and Security Groups to accept the project.

### 5. Timeline & Milestones  
- **Week 10**: Agree on the architecture diagram, set up the VPC network and basic security infrastructure.
- **Week 10**: Write source code for the Worker to collect data and successfully integrate with Amazon Bedrock.
- **Week 11**: Configure EC2 Auto Scaling, EventBridge, SQS, and test connections through VPC Endpoints.
- **Week 12**: Set up CloudWatch monitoring, SNS alerts, conduct security testing, and present the group project results.

### 6. Risk Assessment and Contingency Plan 
- **Connection Error to External API**: Build a *Retry* mechanism combined with storing incomplete jobs in SQS.
- **Unexpected Costs from Amazon Bedrock**: Set strict ceilings in *AWS Budgets* to alert the team immediately if costs spike.
- **Server Security Risks**: Strictly do not grant Public IPs to EC2, use *Session Manager* for access, and close all unnecessary inbound ports on Security Groups.

### 7. Expected Outcomes  
Our team's AWS architecture project will create a robust data processing flow, combining flexible computing power (EC2 Auto Scaling) and artificial intelligence (Amazon Bedrock). The isolated VPC network structure combined with Endpoints helps fully meet enterprise-grade security standards, making this a reliable solution for any data analysis and summarization system.