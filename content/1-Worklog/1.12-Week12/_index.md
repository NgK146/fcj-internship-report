---
title: "Week 12 Worklog"
date: 2026-07-03
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

### Week 12 Objectives:

* Conduct comprehensive system testing, including functionality, security, and concurrency tests.
* Complete project documentation, refine codebase, and finalize presentation materials.

### Tasks carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| Mon | - Test login/registration via Cognito from Frontend <br> - Verify Lambda-Get `/me` returns correct user info <br> - Test error cases (wrong password, non-existent account) | 06/07/2026 | 06/07/2026 | <https://docs.aws.amazon.com/cognito/latest/developerguide/what-is-amazon-cognito.html> |
| Tue | - Test uploading files (pdf, docx, jpg, xlsx, various sizes) <br> - Confirm files stored in S3 Documents Bucket after Lambda Processor <br> - Verify DynamoDB metadata accuracy | 07/07/2026 | 07/07/2026 | <https://docs.aws.amazon.com/AmazonS3/latest/userguide/using-presigned-url.html> |
| Wed | - Test S3 Versioning: upload same file multiple times, confirm separate version IDs <br> - Test Presigned URL download expiry <br> - Test activity history: upload/download/delete events in audit log | 08/07/2026 | 08/07/2026 | <https://docs.aws.amazon.com/AmazonS3/latest/userguide/Versioning.html> |
| Thu | - Security test: try accessing another user's file (access control blocks correctly) <br> - Test GuardDuty detection with suspicious file upload <br> - Verify CloudWatch Logs and SNS email alerts on anomalies | 09/07/2026 | 09/07/2026 | <https://docs.aws.amazon.com/guardduty/latest/ug/what-is-guardduty.html> |
| Fri | - Concurrent test: 5 users upload simultaneously, verify SQS no message loss <br> - Measure API response times and SQS → Lambda processing latency <br> - Fix bugs from concurrent testing | 10/07/2026 | 10/07/2026 | <https://docs.aws.amazon.com/lambda/latest/dg/with-sqs.html> |
| Sat | - Clean up code, remove unused resources, refine IAM Policies (least privilege) <br> - Complete technical documentation (API descriptions, DB schema, deployment guide) <br> - Prepare presentation slides and demo script | 11/07/2026 | 11/07/2026 | <https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html> |
| Sun | - Run full system demo: login → upload → list files → download → view history <br> - Write final project report (architecture, technologies, challenges, future improvements) <br> - Submit final project | 12/07/2026 | 12/07/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Week 12 Achievements:

* Successfully tested all DMS core features (Functionality, Security, Concurrency).
* Verified that SQS handles concurrent upload bursts with zero data loss.
* Validated GuardDuty threat detection and CloudWatch + SNS alerting mechanisms.
* Finalized system documentation, prepared the demo script, and successfully submitted the final project.
