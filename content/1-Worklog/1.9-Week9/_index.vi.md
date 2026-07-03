---
title: "Worklog Tuần 9"
date: 2026-06-15
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu tuần 9:

* Bắt đầu đồ án cuối kỳ: Hệ thống Quản lý tài liệu nội bộ (Document Management System).
* Tìm hiểu và phân tích yêu cầu nghiệp vụ của hệ thống.
* Nghiên cứu các dịch vụ AWS phù hợp cho từng tính năng.
* Thiết kế và hoàn thiện sơ đồ kiến trúc hệ thống.

### Các công việc triển khai trong tuần:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2   | - Đọc đề bài dự án DMS cuối kỳ <br> - Xác định phạm vi và các tính năng cần có (xác thực, upload/download, versioning, phân quyền, lịch sử hoạt động) <br> - Nghiên cứu hệ thống DMS thực tế (SharePoint, Google Drive) | 15/06/2026 | 15/06/2026 | <https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html> |
| 3   | - Nghiên cứu xác thực người dùng với Amazon Cognito User Pools và Identity Pools <br> - Tìm hiểu JWT token và luồng xác thực OAuth 2.0 | 16/06/2026 | 16/06/2026 | <https://docs.aws.amazon.com/cognito/latest/developerguide/what-is-amazon-cognito.html> |
| 4   | - Nghiên cứu S3 để lưu trữ file <br> - Tìm hiểu S3 Presigned URL cho upload/download bảo mật <br> - Tìm hiểu S3 Versioning quản lý phiên bản file và khôi phục | 17/06/2026 | 17/06/2026 | <https://docs.aws.amazon.com/AmazonS3/latest/userguide/versioning-workflows.html> |
| 5   | - Nghiên cứu kiểm soát truy cập theo vai trò (RBAC) bằng IAM Policies và Cognito Groups <br> - So sánh theo dõi hoạt động: DynamoDB audit logs vs. CloudTrail | 18/06/2026 | 18/06/2026 | <https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies.html> |
| 6   | - Bắt đầu thiết kế kiến trúc hệ thống tổng thể <br> - Lựa chọn dịch vụ AWS: CloudFront, Cognito, API Gateway + Lambda, S3, DynamoDB, GuardDuty, CloudWatch + SNS | 19/06/2026 | 19/06/2026 | <https://docs.aws.amazon.com/architecture/> |
| 7   | - Vẽ sơ đồ kiến trúc chi tiết trên draw.io <br> - Xác định API endpoint chính (đăng nhập, upload, download, danh sách file, xem lịch sử) <br> - Định nghĩa cấu trúc bảng DynamoDB cho metadata file và audit log | 20/06/2026 | 20/06/2026 | <https://docs.aws.amazon.com/apigateway/latest/developerguide/welcome.html> |
| CN  | - Xem lại và điều chỉnh sơ đồ kiến trúc hoàn chỉnh <br> - Viết tài liệu thiết kế giải thích lý do chọn dịch vụ <br> - Lên kế hoạch tuần tới: xây dựng Frontend trước rồi đến Backend | 21/06/2026 | 21/06/2026 | <https://docs.aws.amazon.com/architecture/> |

### Kết quả đạt được tuần 9:

* Xác định rõ 5 nhóm tính năng DMS: xác thực, quản lý file, versioning, kiểm soát truy cập và lịch sử hoạt động.
* Lựa chọn bộ dịch vụ AWS đầy đủ: Cognito, S3, API Gateway + Lambda, DynamoDB, CloudFront, GuardDuty, CloudWatch + SNS.
* Hoàn thành sơ đồ kiến trúc hệ thống và tài liệu thiết kế.
