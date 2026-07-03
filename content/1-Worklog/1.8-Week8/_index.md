---
title: "Week 8 Worklog"
date: 2026-06-08
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Week 8 Objectives:

* Perform advanced cost analysis using Cost and Usage Reports (CUR) and Athena.
* Programmatically interact with DynamoDB using the Python SDK (boto3).
* Build a comprehensive Data Lake and analytics pipeline (Glue, EMR, Redshift, QuickSight).

### Tasks carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| Mon | - Configure CUR data in S3 <br> - Run Glue Crawler + Athena for CUR DB <br> - Query usage, service costs, and tags <br> - Analyze RI, Savings Plans, and On-Demand usage | 08/06/2026 | 08/06/2026 | <https://docs.aws.amazon.com/cur/latest/userguide/what-is-cur.html> |
| Tue | - Use Python SDK (boto3) for DynamoDB CRUD <br> - Load 250+ movies from moviedata.json <br> - Perform complex Scan and Query with FilterExpressions | 09/06/2026 | 09/06/2026 | <https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/GettingStartedDynamoDB.html> |
| Wed | - Download Airbnb dataset via Cloud9, upload to S3 <br> - Run Glue DataBrew Profile Job to clean data <br> - Convert CSV to Parquet using Glue ETL PySpark jobs <br> - Run Glue Crawler to update Data Catalog | 10/06/2026 | 10/06/2026 | <https://docs.aws.amazon.com/glue/latest/dg/what-is-glue.html> |
| Thu | - Build visual ETL with Glue Studio (join/transform) <br> - Deploy EMR Cluster and run PySpark aggregation <br> - Deploy Kinesis Data Analytics Studio (Flink SQL) <br> - Deploy Redshift Cluster, ETL from S3 via Glue | 11/06/2026 | 11/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| Fri | - Upload dataset to Amazon QuickSight <br> - Create Line Chart (Forecast), KPI, Insights <br> - Create Donut Chart (Drill-down) and Pivot Table <br> - Publish interactive dashboard | 12/06/2026 | 12/06/2026 | <https://docs.aws.amazon.com/quicksight/latest/user/what-is-quicksight.html> |
| Sat | - Format QuickSight dashboard with custom theme/colors <br> - Add Sankey chart, Sales Map, and Conditional Formatting <br> - Configure Cascading Filters and Navigation Actions | 13/06/2026 | 13/06/2026 | <https://docs.aws.amazon.com/quicksight/latest/user/what-is-quicksight.html> |
| Sun | - Review all data pipeline configurations <br> - Summarize Data Lake analytics architecture <br> - Document lessons learned before final project | 14/06/2026 | 14/06/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Week 8 Achievements:

* Conducted deep AWS cost analysis using CUR and Athena SQL (by account, service, and tag).
* Mastered DynamoDB programmatic access via Python/boto3 (CRUD, batch processing, GSI querying).
* Constructed a complete Airbnb Data Lake: S3 → DataBrew → Glue → Parquet format.
* Deployed an end-to-end enterprise analytics pipeline: Kinesis → EMR → Athena → Redshift.
* Built a professional QuickSight dashboard with AI forecasting, cascading filters, and navigation actions.
