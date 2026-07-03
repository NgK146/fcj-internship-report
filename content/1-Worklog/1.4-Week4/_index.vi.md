---
title: "Worklog Tuần 4"
date: 2026-05-11
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu tuần 4:

* Triển khai chiến lược bảo vệ dữ liệu bằng AWS Backup.
* Xây dựng giải pháp lưu trữ hybrid và sao chép dữ liệu liên vùng (CRR) để dự phòng thảm họa.

### Các công việc triển khai trong tuần:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2   | - Tạo AWS Backup Plan (daily, weekly, monthly) <br> - Assign các resource EC2/RDS/EFS <br> - Test các job backup và lifecycle policies | 11/05/2026 | 11/05/2026 | <https://docs.aws.amazon.com/aws-backup/latest/devguide/whatisbackup.html> |
| 3   | - Deploy SMB Storage Gateway (File Gateway) phía on-premises <br> - Kết nối tới S3 backend <br> - Mount SMB share trên máy ảo Windows | 12/05/2026 | 12/05/2026 | <https://docs.aws.amazon.com/storagegateway/latest/userguide/WhatIsStorageGateway.html> |
| 4   | - Deploy S3 static website (upload HTML/CSS/JS) <br> - Bật static hosting và set bucket policy <br> - Test truy cập website public | 13/05/2026 | 13/05/2026 | <https://docs.aws.amazon.com/AmazonS3/latest/userguide/WebsiteHosting.html> |
| 4   | - Cấu hình Cross-Region Replication (CRR) rule <br> - Upload file test <br> - Xác nhận file được replicate sang bucket ở region đích | 13/05/2026 | 13/05/2026 | <https://docs.aws.amazon.com/AmazonS3/latest/userguide/replication.html> |

### Kết quả đạt được tuần 4:

* Thiết lập chính sách AWS Backup tập trung kèm lifecycle rule cho các tài nguyên quan trọng.
* Triển khai SMB Storage Gateway, cung cấp giải pháp lưu trữ hybrid kết nối on-premises với S3.
* Đưa website tĩnh (static website) hoạt động thành công trên S3.
* Xác nhận khả năng dự phòng thảm họa bằng cách thiết lập S3 Cross-Region Replication (CRR).
