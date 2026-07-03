---
title: "Worklog Tuần 6"
date: 2026-05-25
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu tuần 6:

* Triển khai giám sát bảo mật tập trung và tự động hóa vận hành (ChatOps).
* Thực thi kiểm soát truy cập chi tiết bằng ABAC và mã hóa KMS.
* Giám sát các sự kiện hệ thống bằng CloudTrail và Athena.

### Các công việc triển khai trong tuần:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2   | - Bật Security Hub (AWS Foundational, CIS, PCI DSS) & AWS Config <br> - Phân tích Security Score, tắt các control EC2 SSM không cần thiết | 25/05/2026 | 25/05/2026 | <https://docs.aws.amazon.com/securityhub/latest/userguide/what-is-securityhub.html> |
| 2   | - Tạo VPC, EC2 'lambda-lab-instance' với tag environment_auto=true <br> - Cấu hình Slack Incoming Webhook <br> - Deploy Lambda auto-stop & auto-start (Python, EventBridge) <br> - Test quá trình bật/tắt EC2 và cảnh báo Slack | 25/05/2026 | 25/05/2026 | <https://docs.aws.amazon.com/lambda/latest/dg/welcome.html> |
| 3   | - Khởi tạo 2 EC2 với các tag (Environment: Test & UAT) <br> - Quản lý tag hàng loạt qua Console và CLI <br> - Tạo Tag-Based Resource Group 'MarketingBu' | 26/05/2026 | 26/05/2026 | <https://docs.aws.amazon.com/tag-editor/latest/userguide/tagging.html> |
| 4   | - Tạo IAM policies ABAC tùy chỉnh với điều kiện tag (Team: Alpha) và giới hạn region <br> - Tạo cross-account IAM Role, thực thi Role Switch <br> - Test ABAC: sai tag → lỗi khởi tạo; đúng tag → thành công | 27/05/2026 | 27/05/2026 | <https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction_attribute-based-access-control.html> |
| 5   | - Tạo KMS Symmetric key & S3 Bucket với SSE-KMS <br> - Tạo CloudTrail (Management + Data events) <br> - Tạo Athena external table, query top 100 events <br> - Test giới hạn thời gian của Presigned URL | 28/05/2026 | 28/05/2026 | <https://docs.aws.amazon.com/kms/latest/developerguide/overview.html> |
| 6   | - Tạo IAM Group và 4 user với các quyền khác nhau <br> - Test Switch Role với user không có quyền <br> - Thêm giới hạn IP (aws:SourceIp) và giới hạn thời gian (aws:CurrentTime) | 29/05/2026 | 29/05/2026 | <https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies.html> |
| 7   | - Khởi tạo EC2, tạo S3 bucket và upload script chứa static keys (cố tình tạo lỗ hổng) <br> - Tạo EC2 IAM Instance Profile với quyền S3FullAccess <br> - Sửa lại script không dùng static credentials, test upload S3 bằng token IMDS | 30/05/2026 | 30/05/2026 | <https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/iam-roles-for-amazon-ec2.html> |

### Kết quả đạt được tuần 6:

* Cấu hình AWS Security Hub giám sát tuân thủ bảo mật theo 3 tiêu chuẩn quốc tế.
* Triển khai Lambda ChatOps tự động lập lịch bật/tắt EC2 kèm thông báo Slack.
* Thực thi ABAC (Attribute-Based Access Control) sử dụng resource tags.
* Xây dựng luồng quản trị và giám sát với mã hóa KMS, CloudTrail log và truy vấn Athena.
* Áp dụng các tính năng IAM nâng cao: giới hạn IP/thời gian và EC2 Instance Profiles giúp loại bỏ hoàn toàn việc lưu trữ credentials cứng.
