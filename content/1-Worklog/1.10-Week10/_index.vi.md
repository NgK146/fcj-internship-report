---
title: "Worklog Tuần 10"
date: 2026-06-22
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu tuần 10:

* Phát triển giao diện người dùng (Frontend) cho hệ thống Quản lý tài liệu (DMS).
* Tích hợp Amazon Cognito để xác thực người dùng.
* Xây dựng nền tảng Serverless Backend (API Gateway & Lambda).

### Các công việc triển khai trong tuần:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2   | - Khởi tạo cấu trúc thư mục dự án Frontend <br> - Xây dựng HTML/CSS/JS cơ bản cho trang login, home, quản lý file <br> - Chọn thư viện UI gọn nhẹ | 22/06/2026 | 22/06/2026 | <https://docs.aws.amazon.com/amplify/latest/userguide/getting-started.html> |
| 3   | - Xây dựng trang đăng nhập và đăng ký <br> - Tích hợp Cognito Hosted UI / AWS Amplify cho luồng xác thực <br> - Test login và lưu JWT token vào localStorage | 23/06/2026 | 23/06/2026 | <https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-user-pools-app-integration.html> |
| 4   | - Xây dựng giao diện danh sách file (gom nhóm theo thư mục) <br> - Thêm nút upload kèm thanh tiến trình <br> - Thêm UI tính năng download, xem phiên bản và lịch sử | 24/06/2026 | 24/06/2026 | <https://docs.aws.amazon.com/AmazonS3/latest/userguide/using-presigned-url.html> |
| 5   | - Hoàn thiện UI: responsive, xử lý lỗi, trạng thái loading <br> - Viết hàm Lambda đầu tiên (xử lý login, trả về token) <br> - Tạo API Gateway định tuyến request từ Frontend tới Lambda | 25/06/2026 | 25/06/2026 | <https://docs.aws.amazon.com/lambda/latest/dg/getting-started.html> |
| 6   | - Viết Lambda xử lý upload (tạo S3 Presigned URL) <br> - Viết Lambda xử lý download (Presigned URL giới hạn thời gian) <br> - Viết Lambda lấy danh sách file từ DynamoDB | 26/06/2026 | 26/06/2026 | <https://docs.aws.amazon.com/AmazonS3/latest/userguide/using-presigned-url.html> |
| 7   | - Kết nối Frontend với API Gateway, cấu hình CORS <br> - Test end-to-end: login → list files → upload → download <br> - Ghi nhận lại các bug để fix vào tuần sau | 27/06/2026 | 27/06/2026 | <https://docs.aws.amazon.com/apigateway/latest/developerguide/how-to-cors.html> |
| CN  | - Thiết kế schema bảng DynamoDB (metadata file và audit log) <br> - Cấu hình IAM Role cho phép Lambda truy cập S3 và DynamoDB <br> - Lên kế hoạch tuần tới: kết nối Lambda với DynamoDB, hoàn thiện tính năng | 28/06/2026 | 28/06/2026 | <https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/HowItWorks.html> |

### Kết quả đạt được tuần 10:

* Hoàn thiện giao diện Frontend (đăng nhập, đăng ký, quản lý file).
* Xây dựng các hàm Lambda cốt lõi (auth, tạo Presigned URL cho upload/download, lấy danh sách).
* Kết nối thành công Frontend với Backend thông qua API Gateway.
* Thiết kế xong schema DynamoDB lưu trữ metadata và log hoạt động.
