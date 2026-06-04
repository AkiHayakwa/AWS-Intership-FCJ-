---
title: "Week 7 Worklog"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.7. </b> "
---
{{% notice warning %}} 
⚠️ **Note:** The following information is for reference purposes only. Please **do not copy verbatim** for your own report, including this warning.
{{% /notice %}}


### Week 7 Objectives:

* Connect and get acquainted with members of First Cloud Journey.
* Understand basic AWS services, how to use the console & CLI.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 2   | - Review how to build a simple serverless web application using the AWS Console.<br>- Learn about AWS Serverless Application Model (SAM) - an open-source framework for building serverless applications.<br>- Study SAM's YAML syntax to express functions, APIs, databases, and event source mappings.<br>- Understand how SAM transforms and expands the SAM syntax into AWS CloudFormation syntax to automatically provision resources. | 06/01/2026 | 06/01/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 3   | - Learn about Amazon Cognito - a service providing authentication, authorization, and user management for web and mobile applications.<br>- Study the two main components of Amazon Cognito:<br>&emsp; +  User directories providing sign-up and sign-in options (direct or via third-parties like Facebook, Google, Apple, etc.) and application access control.<br>&emsp; + Provide temporary AWS credentials to grant users access to other AWS services.<br>- Explore examples of combining User pools and Identity pools together in application architectures. | 06/02/2026 | 06/02/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - Learn how to secure a web application in transit by using an SSL certificate to encrypt traffic between users and static websites hosted on Amazon S3 (in-flight encryption).<br>- Study the role of key services in secure web hosting:<br>&emsp; + Handles creating, storing, and renewing public/private SSL/TLS X.509 certificates and keys to protect websites and applications.<br>&emsp; + A highly available and scalable cloud DNS web service to route user requests and manage Hosted Zones.<br>&emsp; + A global content delivery network (CDN) that speeds up the distribution of static/dynamic web content through edge locations and supports HTTPS using SSL certificates.<br>- Explore the advantages of using Amazon S3 together with Amazon CloudFront, including setting up Origin Access Control (OAC) to restrict direct access to S3 content. | 06/03/2026 | 06/03/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Learn how to process user orders by integrating Amazon SQS and Amazon SNS into a serverless web application.<br>- Study the order processing architecture, including:<br>&emsp; + POST `/books/order` API pushes order details to an SQS queue and publishes a message to an SNS topic.<br>&emsp; + GET `/books/order` API retrieves unprocessed orders from the queue and processed orders from DynamoDB.<br>&emsp; +POST `/books/order/handle` API saves order data to DynamoDB and deletes it from the queue.<br>&emsp; +  DELETE `/books/order` API deletes the order from the queue.<br>- Understand AWS messaging services:<br>&emsp; +  A secure, durable, and hosted queue service to integrate and decouple distributed software systems and components.<br>&emsp; +  A managed pub/sub service that delivers messages asynchronously from publishers to subscribers via logical communication channels called topics. | 06/04/2026 | 06/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - **Practice:** <br>&emsp; + Launch an EC2 instance <br>&emsp; + Connect via SSH <br>&emsp; + Attach an EBS volume                                                                                     | 06/05/2026 | 06/05/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Week 7 Achievements:

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
