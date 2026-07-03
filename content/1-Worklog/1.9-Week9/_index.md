---
title: "Week 9 Worklog"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.9. </b> "
---

### Week 9 Objectives:

* Connect and get acquainted with members of First Cloud Journey.
* Understand basic AWS services, how to use the console & CLI.
* Research and deploy AWS Managed Microsoft AD to migrate corporate Active Directory to AWS.
* Practice managing AWS Directory Service and integrating domain join with Windows Server EC2 instances.
* Research and deploy AWS Secrets Manager to manage sensitive credentials.
* Integrate Secrets Manager with Amazon RDS and configure automatic Secret Rotation.
* Deploy applications on AWS Fargate Container to securely access Amazon RDS database via Secrets Manager VPC Endpoint.
* Study and apply secure remote access practices on AWS Cloud using Security Groups and AWS Network Firewall based on CISO Stephan Schmidt's recommendations.
* Master centralized security management using AWS Firewall Manager, AWS Config, AWS Organizations, and AWS Resource Access Manager (RAM).
* Learn threat detection and automated remediation using Amazon GuardDuty, EventBridge Event Rules, and AWS Lambda.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2   | - Research and study about the built-in AWS Directory Service <br>- Learn about its architecture, core features (such as Multi-region replication, trust relationships), and the differences between Standard and Enterprise editions.<br>&emsp; + Set up the network environment (VPC, Subnets) that meets the Directory Service requirements.<br>&emsp; + Successfully deploy AWS Managed Microsoft AD.<br>&emsp; + Launch a Windows Server EC2 instance and perform a domain join.<br>&emsp; + Install Active Directory Administration Tools on the Windows Server to manage the directory (create Organizational Units, Users, Groups).    | 06/15/2026 | 06/15/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 3   | - Research database credentials security solutions using AWS Secrets Manager integrated with Amazon RDS.<br>- Understand secure network architecture (VPC, private subnets, security groups) between Bastion Host and Amazon RDS MySQL (Private).<br>&emsp; + Set up a VPC with necessary Subnets and Route Tables.<br>&emsp; + Provision a private Amazon RDS MySQL database instance.<br>&emsp; + Configure AWS Secrets Manager to store and manage RDS database credentials.<br>&emsp; + Launch an Amazon EC2 Bastion Host and perform database access tests using credentials retrieved from Secrets Manager. | 06/16/2026 | 06/16/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - Study the automated  process to change passwords periodically according to CSF  and CAF  best practices.<br>- Learn to integrate serverless container service AWS Fargate  to securely connect to private RDS database using credentials from Secrets Manager via Interface VPC Endpoint.<br>&emsp; + Enable and test automated Secret Rotation using AWS Secrets Manager and Shell Scripts.<br>&emsp; + Package a sample application into a Docker container and push it to Amazon ECR.<br>&emsp; + Deploy AWS Fargate Container in the VPC.<br>&emsp; + Configure Fargate Task Role and Secrets Manager Interface VPC Endpoint to allow the container to securely retrieve passwords and connect to RDS MySQL. | 06/17/2026 | 06/17/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Research AWS Cloud security based on AWS CISO Stephan Schmidt's 10 safety tips, emphasizing secure remote access.<br>- Learn to implement network access control using Security Groups and AWS Network Firewall.<br>- Explore remote access security scenarios via SSH and RDP protocols. | 06/18/2026 | 06/18/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - Research and study threat detection and remediation using Amazon GuardDuty.<br>- Reproduce attack scenarios and automated fixes by combining EventBridge Event Rules and Lambda Functions.<br>&emsp; + Deploy CloudFormation template to set up the lab environment in us-west-2 (Oregon).<br>&emsp; + Detect and recover compromised EC2 instances using GuardDuty findings, EventBridge, and Lambda.<br>&emsp; + Identify API calls made with compromised IAM credentials and perform manual remediation.<br>&emsp; + Detect and remediate exfiltrated IAM role credentials used from external servers using AWS Lambda. | 06/19/2026 | 06/19/2026      | <https://cloudjourney.awsstudygroup.com/> |


### Week 9 Achievements:

* **Deploy AWS Managed Microsoft AD & Active Directory Administration:**
  * Mastered the concepts and architectural design of AWS Directory Service, focusing on AWS Managed Microsoft AD.
  * Deployed AWS Managed Microsoft AD across multiple Availability Zones (AZs) for high availability.
  * Successfully joined a Windows Server EC2 instance to the Active Directory domain.
  * Installed and utilized Active Directory Administration Tools on the Windows Server to manage organizational resources, including creating Organizational Units (OUs), Users, and Groups.

* **AWS Secrets Manager, RDS & AWS Fargate Integration:**
  * Understood the security prevention role of Secrets Manager under CSF (Prevention) and CAF (Preventative) frameworks.
  * Successfully set up a VPC Endpoint for private connection to Secrets Manager.
  * Integrated and configured automated Secret Rotation for the Amazon RDS MySQL database.
  * Packaged a sample application with Docker, uploaded it to Amazon ECR, and ran it on AWS Fargate Container.
  * Established secure database connections from both Fargate container and EC2 Bastion Host by programmatically retrieving credentials from Secrets Manager.

* **Secure Remote Access & AWS Network Firewall Integration:**
  * Studied the 10 most notable security tips by AWS CISO Stephan Schmidt, focusing on securing remote access to servers and services.
  * Familiarized with and configured Amazon EC2 Security Groups and AWS Network Firewall to restrict remote access using IP address, port, and protocol constraints.
  * Explored configuration steps and remote access scenarios via SSH (Port 22) and RDP (Port 3389) protocols.
  * Understood how to manage security policies centrally across multiple accounts using AWS Firewall Manager, AWS Organizations, AWS Config, and AWS Resource Access Manager (RAM).

* **Threat Detection & Remediation with Amazon GuardDuty:**
  * Configured Amazon GuardDuty to detect system threats and generate security findings.
  * Reproduced attacks and automated fixes using CloudFormation, EventBridge Event Rules, and AWS Lambda.
  * Successfully handled compromised EC2 instances, identified compromised IAM credentials, and prevented IAM role exfiltration.
  * Applied NIST CSF (Protect, Detect, Respond) and AWS CAF (Preventative, Detective, Responsive) security perspectives.

