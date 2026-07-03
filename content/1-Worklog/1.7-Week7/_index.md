---
title: "Week 7 Worklog"
date: 2026-06-01
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Week 7 Objectives:

* Work with relational and NoSQL databases (Amazon RDS, DynamoDB).
* Build data streaming pipelines using Kinesis, Glue, and Athena.
* Explore AI integrations with DynamoDB Zero-ETL, OpenSearch, and Bedrock.

### Tasks carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| Mon | - Create VPC, EC2 SG, RDS SG, DB Subnet Group <br> - Launch EC2, install Git & Node.js <br> - Create RDS MySQL instance <br> - Deploy Node.js app connected to RDS <br> - Perform RDS backup, snapshot, and restore | 01/06/2026 | 01/06/2026 | <https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Welcome.html> |
| Wed | - Create IAM Role/Policy for Glue <br> - Create Kinesis Firehose → S3 <br> - Send sample data via Kinesis Data Generator <br> - Create Glue Crawler → Data Catalog <br> - Query with Athena, transform with Glue Interactive Sessions <br> - Visualize with QuickSight | 03/06/2026 | 03/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| Thu | - Init DynamoDB lab via CloudFormation <br> - Create tables (ProductCatalog, Forum, Thread, Reply) <br> - Perform CRUD: Scan, Query, PutItem, UpdateItem <br> - Use TransactWriteItems for atomic operations <br> - Create Global Secondary Index (GSI) | 04/06/2026 | 04/06/2026 | <https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Introduction.html> |
| Fri | - Configure OpenSearch & Bedrock models (Claude, Titan) <br> - Create DynamoDB Zero-ETL pipeline to OpenSearch <br> - Query AI-based product recommendations via DynamoDB, OpenSearch, and Bedrock | 05/06/2026 | 05/06/2026 | <https://docs.aws.amazon.com/opensearch-service/latest/developerguide/what-is.html> |
| Sat | - Init Cloud9 lab, verify Python/boto3 <br> - Create `logfile_scan` DynamoDB table <br> - Load 1 million server log records | 06/06/2026 | 06/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| Sun | - Create DynamoDB tables (Orders, OrdersHistory) <br> - Create Lambda for DynamoDB Streams → OrdersHistory <br> - Simulate order updates and verify history <br> - Switch to Kinesis Data Streams + SQS DLQ + Lambda for event-driven tracking | 07/06/2026 | 07/06/2026 | <https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Streams.html> |

### Week 7 Achievements:

* Deployed a full-stack Node.js application connected to Amazon RDS.
* Built an end-to-end streaming analytics pipeline: Kinesis → S3 → Glue → Athena → QuickSight.
* Mastered DynamoDB core operations including CRUD, GSI, and ACID Transactions.
* Generated AI product recommendations utilizing DynamoDB Zero-ETL, OpenSearch, and Amazon Bedrock.
* Implemented event-driven order tracking systems using both DynamoDB Streams and Kinesis Data Streams with Lambda.
