---
title: "Worklog Tuần 2"
date: 2026-04-27
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu tuần 2:

* Xây dựng mạng VPC hoàn chỉnh với public/private subnet, NAT Gateway và kết nối VPN.
* Thực hành AWS Systems Manager Session Manager như giải pháp thay thế SSH an toàn.

### Các công việc triển khai trong tuần:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2   | - Tạo VPC với CIDR 10.10.0.0/16 <br> - Tạo 2 public subnet và 2 private subnet trên 2 AZ <br> - Tạo và gắn Internet Gateway <br> - Cấu hình Route Table public và private <br> - Bật auto-assign public IP cho public subnet | 27/04/2026 | 27/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 2   | - Tạo NAT Gateway trong public subnet <br> - Cập nhật route table private: 0.0.0.0/0 → NAT Gateway <br> - Khởi tạo EC2 trong private subnet, test internet qua NAT <br> - Cấu hình Systems Manager (SSM) Session Manager <br> - Kết nối EC2 private không cần SSH key qua Session Manager | 27/04/2026 | 27/04/2026 | <https://docs.aws.amazon.com/vpc/latest/userguide/what-is-amazon-vpc.html> |
| 2   | - Tạo Customer Gateway và Virtual Private Gateway <br> - Thiết lập Site-to-Site VPN (BGP routing) <br> - Tải và cấu hình VPN config phía on-premises <br> - Xác nhận trạng thái VPN tunnel (UP) và test kết nối | 27/04/2026 | 27/04/2026 | <https://docs.aws.amazon.com/vpn/latest/s2svpn/VPC_VPN.html> |

### Kết quả đạt được tuần 2:

* Xây dựng kiến trúc VPC multi-AZ hoàn chỉnh:
  * CIDR: 10.10.0.0/16 với 4 subnet trên 2 AZ
  * Internet Gateway cho public subnet truy cập internet
  * NAT Gateway cho private subnet kết nối ra ngoài

* Cấu hình Session Manager kết nối EC2 không cần key pair, bảo mật hơn SSH truyền thống.

* Thiết lập Site-to-Site VPN giữa AWS VPC và mạng on-premises:
  * Cấu hình BGP dynamic routing
  * Xác nhận VPN tunnel ở trạng thái UP
  * Kiểm tra kết nối thành công giữa hai mạng
