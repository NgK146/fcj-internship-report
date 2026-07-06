---
title: "Week 4 Worklog"
date: 2026-05-11
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Week 4 Objectives:

* Implement data protection strategies using AWS Backup.
* Deploy hybrid storage solutions and cross-region replication for disaster recovery.

### Tasks carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| Mon | - Create AWS Backup Plan (daily, weekly, monthly) <br> - Assign EC2/RDS/EFS resources <br> - Test backup jobs and lifecycle policies | 11/05/2026 | 11/05/2026 | <https://docs.aws.amazon.com/aws-backup/latest/devguide/whatisbackup.html> |
| Tue | - Deploy SMB Storage Gateway (File Gateway) on-premises <br> - Connect to S3 backend <br> - Mount SMB share on Windows VM | 12/05/2026 | 12/05/2026 | <https://docs.aws.amazon.com/storagegateway/latest/userguide/WhatIsStorageGateway.html> |
| Wed | - Deploy S3 static website (upload HTML/CSS/JS) <br> - Enable static hosting and set bucket policy <br> - Test public website access | 13/05/2026 | 13/05/2026 | <https://docs.aws.amazon.com/AmazonS3/latest/userguide/WebsiteHosting.html> |
| Thu | - Configure Cross-Region Replication (CRR) rule <br> - Upload test file <br> - Verify replication to destination bucket in another region | 14/05/2026 | 14/05/2026 | <https://docs.aws.amazon.com/AmazonS3/latest/userguide/replication.html> |

### Week 4 Achievements:

* Established a centralized AWS Backup policy with lifecycle rules for key resources.
* Deployed an SMB Storage Gateway, providing on-premises servers hybrid access to S3 storage.
* Successfully hosted a live S3 static website.
* Verified disaster recovery readiness through S3 Cross-Region Replication (CRR).
