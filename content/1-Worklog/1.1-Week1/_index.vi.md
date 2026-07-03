---
title: "Worklog Tuần 1"
date: 2026-04-20
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

### Mục tiêu tuần 1:

* Thiết lập môi trường AWS và quản lý chi phí hiệu quả.
* Tìm hiểu và triển khai IAM để kiểm soát quyền truy cập an toàn theo nguyên tắc least privilege.

### Các công việc triển khai trong tuần:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2   | - Hoàn thành AWS Credit Tasks để nhận $200 credits <br> - Tìm hiểu AWS Budgets để theo dõi chi phí | 20/04/2026 | 20/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 7   | - Tạo AWS Budget (Monthly cost template, cảnh báo 85%, 100%) <br> - Tạo Cost Budget (Customize, cảnh báo 50%, 80%, 100%) <br> - Tạo Usage Budget (EC2 running hours) <br> - Tạo RI Budget & Savings Plans Budget (demo) <br> - Dọn dẹp các budget không cần thiết | 25/04/2026 | 25/04/2026 | <https://docs.aws.amazon.com/cost-management/latest/userguide/budgets-managing-costs.html> |
| 7   | - Tạo IAM Admin Group (AdministratorAccess) <br> - Tạo IAM Admin User & đăng nhập <br> - Tạo Admin Role & Operator User <br> - Cấu hình Role Switching (sts:AssumeRole) <br> - Test IAM Role Switch với OperatorUser <br> - Dọn dẹp tài nguyên IAM | 25/04/2026 | 25/04/2026 | <https://docs.aws.amazon.com/IAM/latest/UserGuide/getting-started.html> |

### Kết quả đạt được tuần 1:

* Nhận thành công $200 AWS credits sau khi hoàn thành các task yêu cầu.

* Thiết lập nhiều loại AWS Budget:
  * Monthly Cost Budget với cảnh báo 85% và 100%
  * Custom Cost Budget với cảnh báo 50%, 80%, 100% — nhận thông báo qua email
  * EC2 Usage Budget theo dõi số giờ chạy
  * RI và Savings Plans Budgets (demo)

* Hiểu best practice quản lý chi phí và cách tránh phát sinh chi phí ngoài ý muốn.

* Triển khai kiểm soát truy cập IAM:
  * Tạo IAM Admin Group với quyền AdministratorAccess
  * Tạo IAM Admin User và IAM Operator User
  * Tạo Admin Role với toàn quyền quản trị
  * Cấu hình inline policy cho OperatorUser để assume AdminRole qua `sts:AssumeRole`
  * Thực hiện thành công IAM Role Switching từ OperatorUser sang AdminRole
