---
title: "Tự đánh giá"
date: 2026-07-03
weight: 6
chapter: false
pre: " <b> 6. </b> "
---

Trong suốt 12 tuần thực tập tại **Amazon Web Services Vietnam (AWS Vietnam)** ở vị trí **FCJ Cloud Intern**, mình đã có cơ hội cọ xát và chuyển hóa những lý thuyết trên giảng đường HUTECH thành kinh nghiệm thực tiễn. 

Dự án lớn nhất mình tham gia là xây dựng **Hệ thống Quản lý tài liệu nội bộ (Document Management System - DMS)**. Qua đó, mình đã trực tiếp làm việc với kiến trúc Serverless (Lambda, API Gateway), quản lý lưu trữ với S3, xử lý bất đồng bộ qua SQS và thiết lập bảo mật với Cognito. Trải nghiệm này không chỉ giúp mình nâng cao khả năng code backend mà còn thay đổi tư duy về cách thiết kế một hệ thống scalable và bảo mật trên Cloud.

Dưới đây là phần tự đánh giá khách quan của mình sau kỳ thực tập:

| STT | Tiêu chí                            | Mô tả                                                                                            | Tốt | Khá | Trung bình |
| --- | ----------------------------------- | ------------------------------------------------------------------------------------------------ | --- | --- | ---------- |
| 1   | **Kiến thức và kỹ năng chuyên môn** | Nắm bắt nhanh kiến trúc AWS, ứng dụng tốt các dịch vụ Serverless vào đồ án thực tế.              | ✅   | ☐   | ☐          |
| 2   | **Khả năng học hỏi**                | Chủ động tìm đọc document của AWS, tự test và debug lỗi khi deploy hệ thống.                     | ✅   | ☐   | ☐          |
| 3   | **Sự chủ động**                     | Thường xuyên tự đề xuất giải pháp xử lý luồng dữ liệu (dùng SQS thay vì gọi đồng bộ).            | ☐   | ✅   | ☐          |
| 4   | **Tinh thần trách nhiệm**           | Hoàn thành các milestone của dự án DMS đúng deadline hàng tuần, đảm bảo chất lượng code.         | ✅   | ☐   | ☐          |
| 5   | **Tính kỷ luật**                    | Tuân thủ tốt lịch daily meeting, viết báo cáo worklog đầy đủ, rõ ràng đúng hạn.                  | ✅   | ☐   | ☐          |
| 6   | **Tính cầu tiến**                   | Lắng nghe feedback từ mentor để tối ưu chi phí và bảo mật cho ứng dụng.                          | ✅   | ☐   | ☐          |
| 7   | **Giao tiếp**                       | Truyền đạt vấn đề kỹ thuật khá rành mạch nhưng đôi lúc còn bối rối khi present bằng tiếng Anh.   | ☐   | ✅   | ☐          |
| 8   | **Hợp tác nhóm**                    | Tương tác tốt với các thành viên khác trong chương trình FCJ, hỗ trợ nhau fix bug.               | ☐   | ✅   | ☐          |
| 9   | **Ứng xử chuyên nghiệp**            | Tôn trọng văn hóa công ty, giữ thái độ hòa nhã và khiêm tốn khi làm việc với anh chị Mentor.     | ✅   | ☐   | ☐          |
| 10  | **Tư duy giải quyết vấn đề**        | Biết cách chia nhỏ bài toán lớn, dùng CloudWatch để trace log và tìm nguyên nhân gốc rễ.         | ☐   | ✅   | ☐          |
| 11  | **Đóng góp vào dự án/tổ chức**      | Hoàn thiện hệ thống DMS có khả năng sử dụng thực tế, đóng góp các bài viết blog kỹ thuật.        | ✅   | ☐   | ☐          |
| 12  | **Tổng thể**                        | Đánh giá chung về toàn bộ quá trình thực tập: Vượt qua kỳ vọng ban đầu của bản thân.             | ✅   | ☐   | ☐          |

### Những điểm cần cải thiện

* **Tối ưu hóa Code:** Mặc dù hệ thống đã chạy đúng requirement, nhưng mình nhận thấy cách viết code trong Lambda đôi khi chưa tối ưu tốt về mặt cold start và thời gian thực thi.
* **Kỹ năng mềm:** Cần mạnh dạn hơn trong các buổi chia sẻ kỹ thuật (Tech talk) của team, cải thiện thêm tiếng Anh chuyên ngành để đọc hiểu tài liệu sâu hơn.
* **Quản trị chi phí (FinOps):** Quá trình làm dự án đôi lúc mình cấu hình dịch vụ hơi dư thừa resource, cần phải tập thói quen tính toán chi phí trước khi deploy.