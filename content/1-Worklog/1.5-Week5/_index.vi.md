---
title: "Worklog Tuần 5"
date: 2026-05-18
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu tuần 5:

* Thực hiện di chuyển máy ảo (VM Migration) giữa on-premises và AWS.
* Triển khai và quản lý hệ thống lưu trữ tệp hiệu năng cao với Amazon FSx.
* Tối ưu hóa phân phối nội dung với Amazon CloudFront và S3.

### Các công việc triển khai trong tuần:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2   | - Export VMware VM sang OVF (.vmdk), upload lên S3 <br> - Import thành AMI qua vmimport, khởi chạy EC2, test SSH <br> - Export EC2 ngược lại thành VMDK qua create-instance-export-task <br> - Tạo S3 Bucket cho Storage Gateway (Singapore) | 18/05/2026 | 18/05/2026 | <https://docs.aws.amazon.com/vm-import/latest/userguide/vmimport-image-import.html> |
| 3   | - Triển khai FSx lab qua CloudFormation (2 AZ, ~40 phút) <br> - Tạo FSx SSD Multi-AZ (300 GiB) và HDD Multi-AZ (2000 GiB) <br> - RDP vào Windows Instance 0, map ổ đĩa Z: tới FSx UNC, đồng bộ dữ liệu NASA <br> - Tạo File Shares (application, data) qua fsmgmt.msc | 19/05/2026 | 19/05/2026 | <https://docs.aws.amazon.com/fsx/latest/WindowsGuide/what-is.html> |
| 4   | - Chạy benchmark DiskSpd & fio trên FSx <br> - Tạo CloudWatch Alarm (Total Throughput >200 MB/s, cảnh báo SNS) <br> - Bật Data Deduplication (MinimumFileAgeDays=0) <br> - Bật Shadow Copies (tạo snapshot thủ công, khôi phục file) <br> - Scale throughput lên 64 MB/s và dung lượng +10% | 20/05/2026 | 20/05/2026 | <https://docs.aws.amazon.com/fsx/latest/WindowsGuide/performance.html> |
| 5   | - Tạo S3 bucket (tắt ACLs, Block all public access) <br> - Upload source website và bật static hosting <br> - Tắt Block Public Access, bật ACLs, cấp quyền public-read cho object <br> - Test website load, sau đó bật lại Block Public Access (xác nhận lỗi 403) | 21/05/2026 | 21/05/2026 | <https://docs.aws.amazon.com/AmazonS3/latest/userguide/WebsiteHosting.html> |
| 6   | - Tạo CloudFront Distribution với S3 Origin (OAI) <br> - Xác nhận độ trễ giảm từ ~0.614s xuống ~13ms qua header x-amz-cf-pop <br> - Bật S3 Versioning, test rollback bằng cách xóa phiên bản mới nhất <br> - Di chuyển object sang bucket mới và cấu hình CRR Singapore → N. Virginia | 22/05/2026 | 22/05/2026 | <https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html> |

### Kết quả đạt được tuần 5:

* Thực hiện di chuyển VM hai chiều (VMware lên EC2 và ngược lại).
* Triển khai Amazon FSx Multi-AZ tích hợp data deduplication, shadow copies và dynamic scaling.
* Tối ưu hóa phân phối website tĩnh bằng CloudFront CDN (giảm độ trễ xuống ~13ms).
* Xác minh tính năng khôi phục phiên bản S3 và sao chép liên vùng (CRR).
