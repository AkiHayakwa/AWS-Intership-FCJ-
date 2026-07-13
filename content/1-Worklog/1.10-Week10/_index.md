---
title: "Week 10 Worklog"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 1.10. </b> "
---

### Week 10 Objectives:

* Connect and get acquainted with members of First Cloud Journey.
* Understand basic AWS services, how to use the console & CLI.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 2   | - Get acquainted with FCJ members <br> - Read and take note of internship unit rules and regulations  <br>&emsp; + Learn the importance of OS patching for security strategy and compliance <br>&emsp; + Understand the blue/green deployment methodology for AMI creation and replacement <br>&emsp; + Study patching automation using AWS services: <br>&emsp;&emsp; * EC2 Image Builder (AMI creation) <br>&emsp;&emsp; * Systems Manager Automation Document (orchestration) <br>&emsp;&emsp; * CloudFormation with AutoScalingReplacingUpdate policy (graceful deployment) | 06/22/2026 | 06/22/2026      |
| 3   |  <br>&emsp; + Learn basic concepts of AWS Elastic Disaster Recovery (AWS DRS): minimizing downtime and data loss, RTO/RPO, cost-efficiency, and point-in-time recovery. <br>&emsp; + Understand AWS DRS general architecture: source server disk replication, replication agents, replication servers in the staging area VPC, and target recovery instances. <br>&emsp; + Study simulated on-premises source environment components: public/private subnets, active directory/DNS service, and pre-installed applications. <br>&emsp; + Familiarize with prerequisites: SSH connections to Linux servers and RDP connections to Windows bastion server. | 06/23/2026 | 06/23/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 4   |  <br>&emsp; + Connect to the Windows bastion server via RDP and Linux servers via SSH. <br>&emsp; + Deploy AWS Replication Agent on simulated on-premises source servers to replicate block-level data. <br>&emsp; + Configure replication settings in AWS DRS console and monitor initial data replication. <br>&emsp; + Perform disaster recovery operations: non-disruptive tests (launching drill instances), Failover (recovering applications to target VPC), and Failback (reversing replication direction). | 06/24/2026 | 06/24/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Introduction to Data Engineering Immersion Day. <br> - Lab 1: Anomaly clickstream detection using Amazon Managed Service for Apache Flink: <br>&emsp; + Preparation: Provision resources (S3, Kinesis Stream, IAM Roles). <br>&emsp; + Streaming ETL with Glue: Create Data Catalog, configure an ETL Job for real-time transformation. <br>&emsp; + Real-time Streaming with Kinesis: Produce simulated clickstream data to Kinesis. <br>&emsp; + Clickstream Analytics using MSK: Configure Amazon Managed Streaming for Apache Kafka to analyze events. | 06/25/2026 | 06/25/2026      | https://cloudjourney.awsstudygroup.com/> |
| 6   | - Lab 2: Data Ingestion with DMS: <br>&emsp; + DMS Migration Lab: Provision a Replication Instance, configure Source/Target Endpoints, and run a Migration Task. <br>&emsp; + Alternatives: Use CloudFormation for AutoComplete DMS Lab or Skip DMS Lab if short on time. | 06/26/2026 | 06/26/2026      | https://cloudjourney.awsstudygroup.com/>  |


### Week 10 Achievements:

* **Patching Automation and Blue/Green Deployment for AMIs:**
  * Understood the importance of OS patching for system security strategy and compliance.
  * Mastered the blue/green deployment methodology for creating and replacing AMIs without service disruption.
  * Studied and implemented patching automation using AWS services: EC2 Image Builder (for automated AMI creation), Systems Manager (SSM) Automation Document (for orchestration), and CloudFormation with AutoScalingReplacingUpdate policy (for graceful deployment).

* **Disaster Recovery Implementation with AWS Elastic Disaster Recovery (AWS DRS):**
  * Grasped the fundamental concepts of Disaster Recovery (DR), including RTO (Recovery Time Objective), RPO (Recovery Point Objective), cost-efficiency, and point-in-time recovery.
  * Understood AWS DRS architecture: replication of source server disks, deploying replication agents, replication servers in the staging area VPC, and launching target recovery instances.
  * Successfully connected to Linux source servers via SSH and Windows bastion server via RDP.
  * Installed the AWS Replication Agent on simulated on-premises source servers and configured replication settings in the AWS DRS console.
  * Successfully performed critical disaster recovery operations: non-disruptive tests (running drills), Failover (recovering applications to the target VPC), and Failback (reversing the replication direction back to the source).

* **Real-time Data Streaming and Analytics (Data Engineering Immersion Day - Lab 1):**
  * Provisioned the required data infrastructure resources including Amazon S3, Kinesis Streams, and IAM Roles.
  * Built a Streaming ETL pipeline with AWS Glue by creating a Data Catalog and setting up a Glue ETL Job for real-time data transformation.
  * Implemented real-time streaming by producing and feeding simulated clickstream data into Amazon Kinesis.
  * Analyzed clickstream events and detected anomalies using Amazon Managed Streaming for Apache Kafka (Amazon MSK) and Amazon Managed Service for Apache Flink.

* **Data Ingestion and Migration with AWS DMS (Lab 2):**
  * Understood and practiced database migration workflows using AWS Database Migration Service (AWS DMS).
  * Provisioned a Replication Instance, configured Source and Target Endpoints, and executed Database Migration Tasks (or automated the process using CloudFormation).

