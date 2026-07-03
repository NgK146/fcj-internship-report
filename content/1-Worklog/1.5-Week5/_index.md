---
title: "Week 5 Worklog"
date: 2026-05-18
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Week 5 Objectives:

* Execute Virtual Machine migration between on-premises and AWS.
* Deploy and manage high-performance file storage using Amazon FSx.
* Optimize content delivery with Amazon CloudFront and S3.

### Tasks carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| Mon | - Export VMware VM to OVF (.vmdk), upload to S3 <br> - Import to AMI via vmimport, launch EC2 'Import-Server', verify SSH <br> - Export EC2 back to VMDK via create-instance-export-task | 18/05/2026 | 18/05/2026 | <https://docs.aws.amazon.com/vm-import/latest/userguide/vmimport-image-import.html> |
| Tue | - Create S3 Bucket for Storage Gateway (Singapore) | 19/05/2026 | 19/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| Wed | - Deploy FSx lab via CloudFormation (2 AZ, ~40 min) <br> - Create FSx SSD Multi-AZ (300 GiB) and HDD Multi-AZ (2000 GiB) <br> - RDP to Windows Instance 0, map drive Z: to FSx UNC, sync NASA data <br> - Create File Shares (application, data) via fsmgmt.msc | 20/05/2026 | 20/05/2026 | <https://docs.aws.amazon.com/fsx/latest/WindowsGuide/what-is.html> |
| Wed | - Run DiskSpd & fio benchmarks on FSx <br> - Create CloudWatch Alarm (Total Throughput >200 MB/s, SNS email) <br> - Enable Data Deduplication (MinimumFileAgeDays=0) <br> - Enable Shadow Copies (manual snapshot, file restore) <br> - Scale throughput to 64 MB/s and storage +10% | 20/05/2026 | 20/05/2026 | <https://docs.aws.amazon.com/fsx/latest/WindowsGuide/performance.html> |
| Fri | - Create S3 bucket (ACLs disabled, Block all public access) <br> - Upload website source and enable static hosting <br> - Disable Block Public Access, enable ACLs, make objects public-read <br> - Verify website loads, then re-enable Block Public Access (verified 403 Forbidden) | 22/05/2026 | 22/05/2026 | <https://docs.aws.amazon.com/AmazonS3/latest/userguide/WebsiteHosting.html> |
| Fri | - Create CloudFront Distribution with S3 Origin (OAI) <br> - Verify latency reduced from ~0.614s to ~13ms via x-amz-cf-pop header <br> - Enable S3 Versioning, test rollback by deleting latest version <br> - Move objects to new bucket and configure CRR rule Singapore → N. Virginia | 22/05/2026 | 22/05/2026 | <https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html> |

### Week 5 Achievements:

* Performed bidirectional VM migration (VMware to EC2 and vice versa).
* Deployed Amazon FSx Multi-AZ with data deduplication, shadow copies, and dynamic scaling.
* Optimized static website delivery using CloudFront CDN (latency reduced to ~13ms).
* Validated S3 versioning rollbacks and cross-region replication (CRR).
