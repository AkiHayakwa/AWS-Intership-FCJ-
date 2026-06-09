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

* Learn and practice building serverless applications using AWS SAM.
* Understand user authentication and authorization with Amazon Cognito.
* Configure secure web hosting using SSL certificates, Route 53, and CloudFront.
* Integrate messaging services (Amazon SQS and Amazon SNS) for application decoupling.
* Learn application monitoring and tracing using Amazon CloudWatch and AWS X-Ray.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 2   | - Review how to build a simple serverless web application using the AWS Console.<br>- Learn about AWS Serverless Application Model (SAM) - an open-source framework for building serverless applications.<br>- Study SAM's YAML syntax to express functions, APIs, databases, and event source mappings.<br>- Understand how SAM transforms and expands the SAM syntax into AWS CloudFormation syntax to automatically provision resources. | 06/01/2026 | 06/01/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 3   | - Learn about Amazon Cognito - a service providing authentication, authorization, and user management for web and mobile applications.<br>- Study the two main components of Amazon Cognito:<br>&emsp; +  User directories providing sign-up and sign-in options (direct or via third-parties like Facebook, Google, Apple, etc.) and application access control.<br>&emsp; + Provide temporary AWS credentials to grant users access to other AWS services.<br>- Explore examples of combining User pools and Identity pools together in application architectures. | 06/02/2026 | 06/02/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - Learn how to secure a web application in transit by using an SSL certificate to encrypt traffic between users and static websites hosted on Amazon S3 (in-flight encryption).<br>- Study the role of key services in secure web hosting:<br>&emsp; + Handles creating, storing, and renewing public/private SSL/TLS X.509 certificates and keys to protect websites and applications.<br>&emsp; + A highly available and scalable cloud DNS web service to route user requests and manage Hosted Zones.<br>&emsp; + A global content delivery network (CDN) that speeds up the distribution of static/dynamic web content through edge locations and supports HTTPS using SSL certificates.<br>- Explore the advantages of using Amazon S3 together with Amazon CloudFront, including setting up Origin Access Control (OAC) to restrict direct access to S3 content. | 06/03/2026 | 06/03/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Learn how to process user orders by integrating Amazon SQS and Amazon SNS into a serverless web application.<br>- Study the order processing architecture, including:<br>&emsp; + POST `/books/order` API pushes order details to an SQS queue and publishes a message to an SNS topic.<br>&emsp; + GET `/books/order` API retrieves unprocessed orders from the queue and processed orders from DynamoDB.<br>&emsp; +POST `/books/order/handle` API saves order data to DynamoDB and deletes it from the queue.<br>&emsp; +  DELETE `/books/order` API deletes the order from the queue.<br>- Understand AWS messaging services:<br>&emsp; +  A secure, durable, and hosted queue service to integrate and decouple distributed software systems and components.<br>&emsp; +  A managed pub/sub service that delivers messages asynchronously from publishers to subscribers via logical communication channels called topics. | 06/04/2026 | 06/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - Learn the importance of application monitoring and observability in ensuring service reliability and fault tolerance.<br>- Understand AWS observability tools: AWS CloudWatch, AWS X-Ray, and AWS CloudTrail.<br>- Study Amazon CloudWatch for real-time resource and application monitoring:<br>&emsp; + **Metrics:** Collect and track variables to measure resources and applications.<br>&emsp; + **Logs:** Collect, store, and analyze log files (e.g., debugging AWS Lambda).<br>&emsp; + **Events:** Send notifications in response to system events.<br>&emsp; + **Alarms:** Set trigger thresholds (alerts) to execute automated actions.<br>- Study AWS X-Ray for analyzing and debugging distributed/microservices applications:<br>&emsp; + Differentiate and resolve the root cause of performance issues and failures.<br>&emsp; + Retrieve an end-to-end view of requests moving through the application.<br>&emsp; + View a map of the application's components. | 06/05/2026 | 06/05/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Week 7 Achievements:

* **AWS Serverless Application Model (SAM):**
  * Mastered the YAML syntax of SAM to define functions, APIs, databases, and event source mappings.
  * Successfully initialized and deployed serverless applications, understanding how SAM transforms into AWS CloudFormation templates.

* **Amazon Cognito User & Identity Pools:**
  * Understood the role of Amazon Cognito in managing user directories (User Pools) and obtaining temporary credentials (Identity Pools).
  * Implemented secure user authentication and authorization flows for web applications.

* **Secure Web Application Hosting:**
  * Created and configured SSL/TLS certificates via AWS Certificate Manager (ACM) to encrypt traffic in transit.
  * Routed domain traffic using Route 53 and optimized content delivery globally via CloudFront.
  * Secured direct S3 bucket access by implementing Origin Access Control (OAC).

* **Decoupling and Messaging (SQS & SNS):**
  * Built asynchronous message processing systems using SQS queues and SNS topics.
  * Successfully integrated order processing logic where APIs publish to SNS topics and SQS queues, with messages processed into DynamoDB.

* **Application Monitoring and Tracing:**
  * Understood the role of AWS CloudWatch (Metrics, Logs, Events, Alarms) in debugging and observing serverless resources.
  * Utilized AWS X-Ray to establish end-to-end tracing and analyze request lifecycles across microservices.

