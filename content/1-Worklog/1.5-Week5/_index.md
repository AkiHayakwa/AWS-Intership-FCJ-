---
title: "Week 5 Worklog"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.5. </b> "
---


### Week 5 Objectives:

* Understand and utilize AWS Systems Manager Session Manager for secure server management.
* Research Amazon ElastiCache (Redis) to improve caching and in-memory data store performance.
* Learn about and manage service limits using AWS Service Quotas.
* Install tools, initialize and deploy applications, and build CI/CD pipelines on an OpenShift cluster (ROSA).

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Learn the Session Manager feature in AWS Systems Manager to securely manage servers without opening SSH ports, Bastion Hosts, or managing SSH keys.<br> - Understand how Session Manager helps comply with security policies, centrally control access using AWS IAM, and log access sessions and executed commands.<br> - Grasp the advantages: configuring connections without internet access, and quick server access with a single click.<br> - Utilize its multi-platform support (Linux, Windows, MacOS) to provide end-user access. | 05/18/2026 | 05/18/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - Learn about Amazon ElastiCache to easily set up, manage, and scale distributed in-memory data stores or cache environments.<br> - Explore ElastiCache for Redis features such as automatic failure detection and node recovery, data partitioning (up to 500 shards), flexible Availability Zone placement, and integration with AWS services (EC2, CloudWatch, SNS, CloudTrail).<br> - Understand the core components of ElastiCache:<br> &emsp; + Clusters: A collection of cache nodes running a Redis instance, with customizable compute, memory, and data tiering options, deployable within a VPC.<br> &emsp; + Nodes: The smallest building block, a fixed-size chunk of network-attached RAM running a Redis engine instance with its own DNS and port.<br> &emsp; + Shards: A group of 1 to 6 related nodes; Redis clusters (cluster mode enabled) can support up to 500 shards. | 05/19/2026 | 05/19/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - Learn about AWS Service Quotas to view and manage your limits for AWS services from a central interface.<br> - Understand that quotas, also referred to as limits in AWS services, are the maximum values for the resources, actions, and items in your AWS account.<br> - Grasp that each AWS service defines its quotas and establishes default values for those quotas | 05/20/2026 | 05/20/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | - Install required tools for ROSA (AWS CLI, ROSA CLI, OpenShift CLI `oc`, and configure necessary IAM permissions).<br>- Initialize and set up the OpenShift cluster on AWS (ROSA - Red Hat OpenShift on AWS).<br>- Deploy a containerized application onto the ROSA cluster.<br>- Set up and automate a CI/CD pipeline on ROSA using AWS CodePipeline, AWS CodeCommit, and AWS CodeBuild. | 05/21/2026 | 05/21/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | - Practice verifying and monitoring the containerized application and OpenShift cluster via the OpenShift Web Console.<br>- Perform clean-up of all created resources including the ROSA cluster, IAM Roles, and related AWS resources to prevent unexpected charges. | 05/22/2026 | 05/22/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Week 5 Achievements:

- **Server Management & Security (Systems Manager Session Manager):**
  + Understood how AWS Systems Manager Session Manager works to securely manage and connect to servers without opening SSH ports or using Bastion Hosts.
  + Learned how to control access permissions via IAM policies and audit session logs.

- **Caching & Performance Optimization (Amazon ElastiCache):**
  + Mastered the architecture and operations of Amazon ElastiCache for Redis (Clusters, Nodes, Shards).
  + Learned how to set up, automatically detect failures, and scale in-memory data structures to improve application response times.

- **Resource & Limit Management (AWS Service Quotas):**
  + Acquired the knowledge to check, manage, and request service limit increases (Service Quotas) on AWS from a centralized console.

- **Container Deployment & CI/CD on AWS ROSA (Red Hat OpenShift on AWS):**
  + Successfully installed necessary command-line tools: AWS CLI, ROSA CLI, and OpenShift CLI (`oc`).
  + Initialized, configured, and deployed a Red Hat OpenShift cluster on AWS (ROSA).
  + Successfully deployed a containerized application to the ROSA cluster.
  + Constructed and automated a CI/CD pipeline integrated with AWS CodeCommit (source repository), AWS CodeBuild (container build & deployment), and AWS CodePipeline (workflow orchestration).
  + Successfully cleaned up cluster resources and IAM roles to prevent unexpected charges.
