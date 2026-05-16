---
title: "Week 4 Worklog"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.4. </b> "
---

### Week 4 Objectives:

* Connect and get acquainted with members of First Cloud Journey.
* Understand basic AWS services, how to use the console & CLI.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 2   | - Research the way how to deploy web application TravelBuddy to run on AWS , Use AWS Tools for Eclipse to deploy a Java Application to an Elastic Beanstalk environment ,  configure the AWS Elastic Beanstalk CLI tool , Use the AWS SDK to query and modify the AWS environment                                                                                                 | 05/11/2026 | 05/11/2026      |
| 3   | - Applying configure app auto release services combine AWS CodeCommit to store source code securely , AWS CodeBuild to build source code , AWS CodeDeploy to deploy application to instance , AWS Codepipeline to link CodeCommit, CodeBuild, and CodeDeploy together into a seamless, automated workflow and AWS CodeStar to enables you to quickly develop, build, and deploy applications on AWS           | 05/12/2026 | 05/12/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - Implement an AWS Lambda function.<br>- Edit the provided Java Lambda function source code to resize an image as a thumbnail or delete non-image files, and connect the trigger to an S3 bucket to test the feature.<br>- Use AWS Serverless Application Model (SAM) and AWS CloudFormation to create a template to automate the deployment of the Lambda function, an S3 trigger, and an S3 bucket.<br>- Identify a microservice candidate in a monolithic codebase and create an AWS CodeStar project to manage the CI/CD pipeline for that microservice hosted in AWS Lambda. | 05/13/2026 | 05/13/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Use the AWS SDK for Java to scan an Amazon DynamoDB table to return results.<br>- Use the AWS SDK for Java to query an Amazon DynamoDB table to return matching results.<br>- Use Indexes in DynamoDB tables to perform lookups on attributes other than the partition key.<br>- Create a DynamoDB table manually using the console and populate data manually.<br>- Create a workflow using AWS Step Functions.<br>- Create AWS Lambda functions that provide Task actions for Step Functions. | 05/14/2026 | 05/14/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - Understand the operations of different messaging methods on the AWS platform.<br>- Explain the difference between queues and data streams.<br>- Use messaging methods on AWS from a web browser and programming with Java SDK.<br>- Understand how to read data from an Amazon Kinesis stream using an AWS Lambda function.<br>- Create a pub/sub communication channel between two EC2 instances, via an Amazon Kinesis stream, using the AWS SDK for Java.<br>- Learn how to create a git repository in AWS CodeCommit and access the repository in a development environment and an EC2 instance. | 05/15/2026 | 05/15/2026      | <https://cloudjourney.awsstudygroup.com/> |


### Week 4 Achievements:

- Application Deployment & CI/CD Automation

  + Acquired hands-on experience deploying a Java web application (TravelBuddy) to an AWS Elastic Beanstalk environment.
  + Gained comprehensive knowledge of AWS CI/CD services (CodeCommit, CodeBuild, CodeDeploy, CodePipeline, CodeStar).
  + Mastered version control on AWS by creating Git repositories in CodeCommit and accessing them across environments.

- Database & Data Management

  + Utilized the AWS SDK for Java to query and modify DynamoDB, including scanning, querying, and utilizing indexes.

- Serverless Computing & Workflows

  + Mastered serverless computing with AWS Lambda, SAM, and CloudFormation, including S3 triggers.
  + Designed and executed serverless workflows using AWS Step Functions, integrating them seamlessly with Lambda.

- Messaging & Application Integration

  + Explored and implemented various AWS messaging methods, distinguishing between message queues and data streams.
  + Successfully built a pub/sub communication channel between EC2 instances using Amazon Kinesis and the AWS SDK for Java.
