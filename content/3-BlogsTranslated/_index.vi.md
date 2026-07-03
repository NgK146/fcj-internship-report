---
title: "Các bài blogs đã dịch"
date: 2026-07-03
weight: 3
chapter: false
pre: " <b> 3. </b> "
---

Tại đây là danh sách các bài blog kỹ thuật của AWS mà mình đã nghiên cứu, dịch và tổng hợp lại trong quá trình thực tập:

###  [Blog 1 - Cách xây dựng chiến lược AWS KMS tiết kiệm chi phí cho ứng dụng Multi-Tenant](3.1-Blog1/)
Bài blog này chia sẻ giải pháp quản lý khóa mã hóa (KMS) tập trung dành cho các ứng dụng SaaS phục vụ nhiều khách hàng. Giải pháp giúp cân bằng giữa bảo mật mạnh mẽ, chi phí hợp lý và dễ dàng quản lý khi số lượng tenant (khách hàng) tăng lên mà không làm đội chi phí mã hóa.

###  [Blog 2 - Tạo Baseline bảo mật tự động cho Amazon Bedrock với Infrastructure as Code](3.2-Blog2/)
Bài blog tập trung vào cách thiết lập các tiêu chuẩn bảo mật cơ bản (baseline) khi sử dụng các dịch vụ Generative AI của AWS (như Amazon Bedrock) một cách tự động hóa bằng Infrastructure as Code. Nhằm đảm bảo dữ liệu AI luôn an toàn và tuân thủ các chính sách bảo mật của tổ chức.

###  [Blog 3 - Xây dựng báo cáo chi phí AWS hoàn toàn tự động](3.3-Blog3/)
Bài viết hướng dẫn cách xây dựng một hệ thống hoàn toàn tự động (Serverless) để gửi báo cáo biến động chi phí AWS (Delta Cost Usage Report) qua email hàng ngày. Việc này giúp đội ngũ quản lý có thể theo dõi và phát hiện sớm các khoản phí bất thường mà không cần truy cập trực tiếp vào AWS Billing Console.