---
title: "Worklog Tuần 7"
date: 2026-06-01
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu tuần 7:

* Làm việc với cơ sở dữ liệu quan hệ và NoSQL (Amazon RDS, DynamoDB).
* Xây dựng luồng xử lý dữ liệu streaming với Kinesis, Glue, và Athena.
* Khám phá tích hợp AI bằng DynamoDB Zero-ETL, OpenSearch và Bedrock.

### Các công việc triển khai trong tuần:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2   | - Tạo VPC, EC2 SG, RDS SG, DB Subnet Group <br> - Khởi tạo EC2, cài Git & Node.js <br> - Tạo RDS MySQL instance <br> - Deploy ứng dụng Node.js kết nối với RDS <br> - Thực hiện RDS backup, snapshot và restore | 01/06/2026 | 01/06/2026 | <https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Welcome.html> |
| 4   | - Tạo IAM Role/Policy cho Glue <br> - Tạo Kinesis Firehose → S3 <br> - Gửi data mẫu bằng Kinesis Data Generator <br> - Tạo Glue Crawler → Data Catalog <br> - Truy vấn Athena, transform data với Glue Interactive Sessions <br> - Trực quan hóa bằng QuickSight | 03/06/2026 | 03/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Khởi tạo DynamoDB lab qua CloudFormation <br> - Tạo bảng (ProductCatalog, Forum, Thread, Reply) <br> - Thực thi CRUD: Scan, Query, PutItem, UpdateItem <br> - Dùng TransactWriteItems cho giao dịch atomic <br> - Tạo Global Secondary Index (GSI) | 04/06/2026 | 04/06/2026 | <https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Introduction.html> |
| 6   | - Cấu hình OpenSearch & Bedrock models (Claude, Titan) <br> - Tạo DynamoDB Zero-ETL pipeline sang OpenSearch <br> - Truy vấn gợi ý sản phẩm bằng AI qua DynamoDB, OpenSearch và Bedrock | 05/06/2026 | 05/06/2026 | <https://docs.aws.amazon.com/opensearch-service/latest/developerguide/what-is.html> |
| 7   | - Khởi tạo Cloud9 lab, kiểm tra Python/boto3 <br> - Tạo bảng DynamoDB `logfile_scan` <br> - Load 1 triệu bản ghi server log | 06/06/2026 | 06/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| CN  | - Tạo bảng DynamoDB (Orders, OrdersHistory) <br> - Tạo Lambda xử lý DynamoDB Streams → OrdersHistory <br> - Mô phỏng cập nhật đơn hàng và kiểm tra lịch sử <br> - Chuyển đổi sang dùng Kinesis Data Streams + SQS DLQ + Lambda | 07/06/2026 | 07/06/2026 | <https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Streams.html> |

### Kết quả đạt được tuần 7:

* Triển khai ứng dụng Node.js kết nối thành công với cơ sở dữ liệu Amazon RDS.
* Xây dựng pipeline phân tích dữ liệu streaming: Kinesis → S3 → Glue → Athena → QuickSight.
* Nắm vững các thao tác cốt lõi trên DynamoDB: CRUD, GSI, và ACID Transactions.
* Ứng dụng AI tạo gợi ý sản phẩm thông qua DynamoDB Zero-ETL, OpenSearch và Amazon Bedrock.
* Triển khai hệ thống theo dõi đơn hàng event-driven sử dụng DynamoDB Streams và Kinesis Data Streams kết hợp Lambda.
