---
title: "Worklog Tuần 11"
date: 2026-06-29
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Mục tiêu tuần 11:

* Triển khai hoàn chỉnh toàn bộ Backend cho hệ thống DMS.
* Thực thi xử lý bất đồng bộ (event-driven) thông qua SQS và S3 Event Notifications.
* Bảo mật và giám sát hệ thống bằng CloudFront, GuardDuty và CloudWatch.

### Các công việc triển khai trong tuần:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2   | - Hoàn thiện Lambda Upload Intent (tạo Presigned URL, lưu metadata vào DynamoDB) <br> - Cấu hình SQS Queue nhận S3 Event Notifications | 29/06/2026 | 29/06/2026 | <https://docs.aws.amazon.com/AmazonS3/latest/userguide/NotificationHowTo.html> |
| 3   | - Viết Lambda Upload Processor (đọc message SQS, chuyển file vào S3 Documents Bucket) <br> - Kết nối S3 Event Notification → SQS → Lambda trigger <br> - Test toàn bộ luồng upload | 30/06/2026 | 30/06/2026 | <https://docs.aws.amazon.com/lambda/latest/dg/with-sqs.html> |
| 4   | - Deploy Frontend lên S3 Frontend Bucket <br> - Tạo CloudFront Distribution (cấu hình Origin Access Control) <br> - Xác nhận UI load qua URL HTTPS của CloudFront | 01/07/2026 | 01/07/2026 | <https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/GettingStartedCreateDistrib.html> |
| 5   | - Bật Amazon GuardDuty bảo vệ bucket S3 <br> - Bật CloudWatch Logs cho tất cả Lambda functions <br> - Tạo CloudWatch Alarm theo dõi tỷ lệ lỗi Lambda | 02/07/2026 | 02/07/2026 | <https://docs.aws.amazon.com/guardduty/latest/ug/what-is-guardduty.html> |
| 6   | - Tạo SNS Topic, subscribe email nhận cảnh báo <br> - Kết nối CloudWatch Alarm → SNS → Email <br> - Test luồng chính: Cognito login → API Gateway → Lambda → S3 → SQS → Lambda Processor → Documents Bucket | 03/07/2026 | 03/07/2026 | <https://docs.aws.amazon.com/sns/latest/dg/welcome.html> |
| 7   | - Fix lỗi CORS trên API Gateway, thiếu quyền IAM, timeout SQS <br> - Test tính năng S3 Versioning khi upload trùng tên file <br> - Xác nhận Lambda `/me` trả về đúng thông tin user từ Cognito | 04/07/2026 | 04/07/2026 | <https://docs.aws.amazon.com/apigateway/latest/developerguide/how-to-cors.html> |
| CN  | - Rà soát lại toàn bộ hệ thống so với sơ đồ kiến trúc <br> - Xác nhận 16 luồng kết nối hoạt động bình thường <br> - Lên danh sách test case cho đợt kiểm thử chính thức vào tuần sau | 05/07/2026 | 05/07/2026 | <https://docs.aws.amazon.com/architecture/> |

### Kết quả đạt được tuần 11:

* Deploy hoàn chỉnh kiến trúc Serverless Backend.
* Tích hợp luồng xử lý event-driven qua S3 Event Notifications, SQS và Lambda.
* Triển khai Frontend phân phối toàn cầu qua S3 và CloudFront.
* Cấu hình giám sát tự động và phát hiện rủi ro với CloudWatch, SNS và GuardDuty.
