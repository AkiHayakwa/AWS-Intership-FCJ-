---
title: "Week 5 Worklog"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.5. </b> "
---


### Week 5 Objectives:

* Connect and get acquainted with members of First Cloud Journey.
* Understand basic AWS services, how to use the console & CLI.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 2   | - Learn the Session Manager feature in AWS Systems Manager to securely manage servers without opening SSH ports, Bastion Hosts, or managing SSH keys.<br> - Understand how Session Manager helps comply with security policies, centrally control access using AWS IAM, and log access sessions and executed commands.<br> - Grasp the advantages: configuring connections without internet access, and quick server access with a single click.<br> - Utilize its multi-platform support (Linux, Windows, MacOS) to provide end-user access. | 05/18/2026 | 05/18/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 3   | - Learn about Amazon ElastiCache to easily set up, manage, and scale distributed in-memory data stores or cache environments.<br> - Explore ElastiCache for Redis features such as automatic failure detection and node recovery, data partitioning (up to 500 shards), flexible Availability Zone placement, and integration with AWS services (EC2, CloudWatch, SNS, CloudTrail).<br> - Understand the core components of ElastiCache:<br> &emsp; + Clusters: A collection of cache nodes running a Redis instance, with customizable compute, memory, and data tiering options, deployable within a VPC.<br> &emsp; + Nodes: The smallest building block, a fixed-size chunk of network-attached RAM running a Redis engine instance with its own DNS and port.<br> &emsp; + Shards: A group of 1 to 6 related nodes; Redis clusters (cluster mode enabled) can support up to 500 shards. | 05/19/2026 | 05/19/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - Learn about AWS Service Quotas to view and manage your limits for AWS services from a central interface.<br> - Understand that quotas, also referred to as limits in AWS services, are the maximum values for the resources, actions, and items in your AWS account.<br> - Grasp that each AWS service defines its quotas and establishes default values for those quotas | 05/20/2026 | 05/20/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Learn basic EC2: <br>&emsp; + Instance types <br>&emsp; + AMI <br>&emsp; + EBS <br>&emsp; + ... <br> - SSH connection methods to EC2 <br> - Learn about Elastic IP   <br>                            | 08/14/2025 | 08/15/2025      | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - **Practice:** <br>&emsp; + Launch an EC2 instance <br>&emsp; + Connect via SSH <br>&emsp; + Attach an EBS volume                                                                                     | 08/15/2025 | 08/15/2025      | <https://cloudjourney.awsstudygroup.com/> |


### Week 5 Achievements:

* Understood what AWS is and mastered the basic service groups: 
  * Compute
  * Storage
  * Networking 
  * Database
  * ...

* Successfully created and configured an AWS Free Tier account.

* Became familiar with the AWS Management Console and learned how to find, access, and use services via the web interface.

* Installed and configured AWS CLI on the computer, including:
  * Access Key
  * Secret Key
  * Default Region
  * ...

* Used AWS CLI to perform basic operations such as:

  * Check account & configuration information
  * Retrieve the list of regions
  * View EC2 service
  * Create and manage key pairs
  * Check information about running services
  * ...

* Acquired the ability to connect between the web interface and CLI to manage AWS resources in parallel.
* ...
