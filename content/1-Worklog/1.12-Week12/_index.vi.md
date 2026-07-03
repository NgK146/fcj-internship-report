---
title: "Worklog Tuần 12"
date: 2026-07-03
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

### Mục tiêu tuần 12:

* Thực hiện kiểm thử toàn diện hệ thống, bao gồm kiểm thử chức năng, bảo mật và đồng thời.
* Hoàn thiện tài liệu dự án, tối ưu source code và chuẩn bị tài liệu thuyết trình bảo vệ.

### Các công việc triển khai trong tuần:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2   | - Test tính năng đăng nhập/đăng ký qua Cognito trên Frontend <br> - Xác nhận Lambda `/me` trả về đúng user info <br> - Test các case lỗi (sai password, account không tồn tại) | 06/07/2026 | 06/07/2026 | <https://docs.aws.amazon.com/cognito/latest/developerguide/what-is-amazon-cognito.html> |
| 3   | - Test upload đa dạng loại file (pdf, docx, jpg, xlsx) với nhiều kích thước <br> - Xác nhận file nằm đúng trong S3 Documents Bucket sau khi qua Lambda Processor <br> - Xác nhận dữ liệu metadata trong DynamoDB chính xác | 07/07/2026 | 07/07/2026 | <https://docs.aws.amazon.com/AmazonS3/latest/userguide/using-presigned-url.html> |
| 4   | - Test S3 Versioning: upload trùng file nhiều lần, kiểm tra version ID <br> - Test thời gian hết hạn của Presigned URL download <br> - Test tính năng lịch sử hoạt động (lưu audit log khi upload/download/xóa) | 08/07/2026 | 08/07/2026 | <https://docs.aws.amazon.com/AmazonS3/latest/userguide/Versioning.html> |
| 5   | - Test bảo mật: cố tình truy cập file của user khác (xác nhận hệ thống block) <br> - Test GuardDuty phát hiện mối đe dọa với file nghi ngờ <br> - Xác nhận CloudWatch Logs và SNS gửi email cảnh báo khi có lỗi | 09/07/2026 | 09/07/2026 | <https://docs.aws.amazon.com/guardduty/latest/ug/what-is-guardduty.html> |
| 6   | - Test đồng thời: 5 user cùng upload lúc, xác nhận SQS không làm mất message <br> - Đo lường response time API và độ trễ xử lý SQS → Lambda <br> - Fix các bug phát sinh từ test đồng thời | 10/07/2026 | 10/07/2026 | <https://docs.aws.amazon.com/lambda/latest/dg/with-sqs.html> |
| 7   | - Clean code, dọn dẹp các resource không dùng, tinh chỉnh IAM Policy (least privilege) <br> - Hoàn thiện tài liệu kỹ thuật (mô tả API, schema DB, hướng dẫn deploy) <br> - Chuẩn bị slide thuyết trình và kịch bản demo | 11/07/2026 | 11/07/2026 | <https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html> |
| CN  | - Chạy demo toàn bộ hệ thống: login → upload → list files → download → xem lịch sử <br> - Viết báo cáo tổng kết (kiến trúc, công nghệ, khó khăn, hướng phát triển) <br> - Nộp đồ án cuối kỳ | 12/07/2026 | 12/07/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được tuần 12:

* Vượt qua toàn bộ các bài test tính năng cốt lõi, bảo mật và khả năng chịu tải.
* Xác nhận SQS xử lý tốt lượng upload đồng thời mà không mất mát dữ liệu.
* Đánh giá thành công khả năng phát hiện rủi ro của GuardDuty và cơ chế cảnh báo qua CloudWatch + SNS.
* Hoàn thiện hồ sơ tài liệu, chuẩn bị sẵn sàng demo và chính thức nộp đồ án tốt nghiệp.
