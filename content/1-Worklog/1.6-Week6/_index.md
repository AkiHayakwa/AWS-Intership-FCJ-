---
title: "Week 6 Worklog"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.6. </b> "
---


### Week 6 Objectives:

* Build a serverless data lake architecture and data processing pipeline using S3, Kinesis, Athena, and QuickSight.
* Use ETL services (AWS Glue, EMR) to transform and load data into Amazon Redshift.
* Set up a pub/sub messaging model using Amazon SNS and SQS.
* Develop serverless applications using AWS Lambda (image processing via S3 triggers, Lambda Layers) and integrate with Amazon DynamoDB (CRUD, IAM, Monitoring & Troubleshooting).

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2   | - Design serverless data lake architecture. <br> - Build data processing pipeline and Data Lake using Amazon S3 for data storage. <br> - Use Amazon Kinesis for real-time streaming data. <br> - Use Amazon Kinesis Data Analytics for real-time data analysis. <br> - Query data using Amazon Athena and visualize data using Amazon QuickSight. | 05/25/2026 | 05/25/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3   | - Use AWS Glue to automatically index datasets. <br> - Perform data transformation. <br> - Run interactive ETL scripts in a Jupyter notebook on AWS Glue Studio using AWS Glue (interactive sessions). <br> - Use Glue Studio to run and monitor ETL jobs in AWS Glue. <br> - Use Glue DataBrew to prepare data. <br> - Use EMR to run a Spark transformation job. <br> - Load data to Amazon Redshift from Glue. <br> - Introduction to best practices for Amazon Redshift design. | 05/26/2026 | 05/26/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - Learn about Amazon SNS (Simple Notification Service) and Amazon SQS (Simple Queue Service). <br> - Implement the Pub/Sub messaging pattern and configure Subscription Filter Policies to automatically filter and route messages.<br>&emsp; + Create a new SQS queue for EU orders.<br>&emsp; + Set up a subscription filter policy by specifying the location attribute with the value eu-west to receive messages destined for the EU. | 05/27/2026 | 05/27/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Learn about Serverless Architecture: definition, pros/cons, and common use cases. <br>- Study core serverless services: AWS Lambda, Amazon S3, and Amazon DynamoDB.<br>&emsp; + Create and configure a Lambda function (runtime, memory, timeout). <br>&emsp; + Configure Amazon S3 Event Triggers to invoke Lambda automatically upon image upload. <br>&emsp; + Utilize Lambda Layers to package external libraries (e.g., Sharp for Node.js, Pillow for Python) for image resizing. <br>&emsp; + Implement best practices for security (Principle of Least Privilege via IAM Roles) and performance/cost optimization. | 05/28/2026 | 05/28/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6   | <br>&emsp; + Design and create DynamoDB tables with appropriate Partition Keys and Sort Keys. <br>&emsp; + Configure IAM Roles and Permissions allowing Lambda to read/write to the DynamoDB table. <br>&emsp; + Implement CRUD operations using the DynamoDB SDK (AWS SDK v3 or Boto3).<br>&emsp; + Analyze Lambda execution logs using Amazon CloudWatch Logs. <br>&emsp; + Monitor performance metrics (Invocations, Duration, Errors, Throttles) via CloudWatch Metrics. <br>&emsp; + Configure AWS X-Ray for end-to-end tracing of requests from S3 to Lambda and DynamoDB. | 05/29/2026 | 05/29/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Week 6 Achievements:

- **Serverless Data Lake Architecture & Data Querying:**
  + Successfully designed and implemented data processing pipelines using Amazon S3 for storage.
  + Integrated Amazon Kinesis and Kinesis Data Analytics for real-time streaming data ingestion and analytics.
  + Utilized Amazon Athena for interactive SQL queries directly on S3 and visualized metrics using Amazon QuickSight.

- **ETL Pipelines with AWS Glue & Redshift:**
  + Leveraged AWS Glue Crawlers to automatically catalog datasets in S3.
  + Developed and monitored ETL jobs using Glue Studio, Glue DataBrew, and running Spark transformations on Amazon EMR.
  + Loaded processed data into Amazon Redshift and followed best practices for data warehousing design.

- **Messaging & Pub/Sub Systems:**
  + Understood the operation of Amazon SNS and Amazon SQS, distinguishing between queues and topics.
  + Implemented pub/sub patterns and configured Subscription Filter Policies for automated message routing.

- **Serverless Development with Lambda & DynamoDB:**
  + Developed Serverless applications using AWS Lambda and set up Amazon S3 Event Triggers for automated image resizing.
  + Employed Lambda Layers to package external image processing libraries (e.g., Sharp, Pillow), optimizing Lambda deployment size.
  + Designed DynamoDB tables using effective Partition Keys and Sort Keys.
  + Applied security best practices using IAM Roles and policies to enforce the principle of least privilege.
  + Configured monitoring, logging, and tracing using Amazon CloudWatch and AWS X-Ray to troubleshoot Serverless resources.
