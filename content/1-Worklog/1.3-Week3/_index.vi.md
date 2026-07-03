---
title: "Worklog Tuần 3"
date: 2026-05-05
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu tuần 3:

* Thiết lập Libreswan VPN và Hybrid DNS giữa môi trường on-premises và AWS.
* Kết nối nhiều VPC với nhau bằng VPC Peering và AWS Transit Gateway.

### Các công việc triển khai trong tuần:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 3   | - Cài đặt & cấu hình Libreswan VPN trên EC2 <br> - Thiết lập IPsec tunnel tới AWS VGW <br> - Xác nhận tunnel UP | 05/05/2026 | 05/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - Cấu hình Hybrid DNS với Route 53 Resolver <br> - Tạo Inbound/Outbound endpoints <br> - Cấu hình rules forwarding giữa DNS on-premises ↔ AWS DNS | 06/05/2026 | 06/05/2026 | <https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/resolver.html> |
| 7   | - Tạo VPC Peering giữa 2 VPC <br> - Cập nhật route tables <br> - Test kết nối EC2 chéo giữa các VPC | 09/05/2026 | 09/05/2026 | <https://docs.aws.amazon.com/vpc/latest/peering/what-is-vpc-peering.html> |
| CN  | - Tạo Transit Gateway <br> - Attach 3 VPCs vào TGW <br> - Cấu hình route tables cho TGW <br> - Xác nhận kết nối multi-VPC thành công | 10/05/2026 | 10/05/2026 | <https://docs.aws.amazon.com/vpc/latest/tgw/what-is-transit-gateway.html> |

### Kết quả đạt được tuần 3:

* Thiết lập thành công IPsec tunnel bằng Libreswan kết nối on-premises với AWS.
* Cấu hình Hybrid DNS hoạt động ổn định hai chiều.
* Kết nối các VPC bằng VPC Peering (hiểu rõ tính chất non-transitive).
* Triển khai AWS Transit Gateway giúp đơn giản hóa kết nối mạng quy mô lớn (transitive routing).
