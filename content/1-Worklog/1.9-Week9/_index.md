---
title: "Week 9 Worklog"
date: 2026-06-15
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Week 9 Objectives:

* Kick off the final project: Internal Document Management System (DMS).
* Analyze and document business requirements for the system.
* Research suitable AWS services for each feature.
* Design and finalize the system architecture diagram.

### Tasks carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| Mon | - Read project brief for DMS final project <br> - Define scope and required features (auth, file upload/download, versioning, access control, activity history) <br> - Research real-world DMS systems (SharePoint, Google Drive) | 15/06/2026 | 15/06/2026 | <https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html> |
| Tue | - Research user authentication with Amazon Cognito User Pools and Identity Pools <br> - Study JWT tokens and OAuth 2.0 auth flow | 16/06/2026 | 16/06/2026 | <https://docs.aws.amazon.com/cognito/latest/developerguide/what-is-amazon-cognito.html> |
| Wed | - Research S3 for file storage <br> - Study S3 Presigned URLs for secure upload/download <br> - Study S3 Versioning for file version management and rollback | 17/06/2026 | 17/06/2026 | <https://docs.aws.amazon.com/AmazonS3/latest/userguide/versioning-workflows.html> |
| Thu | - Research role-based access control (RBAC) with IAM Policies + Cognito Groups <br> - Research activity tracking options: DynamoDB audit logs vs. CloudTrail | 18/06/2026 | 18/06/2026 | <https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies.html> |
| Fri | - Start designing overall system architecture <br> - Select AWS services per layer: CloudFront, Cognito, API Gateway + Lambda, S3, DynamoDB, GuardDuty, CloudWatch + SNS | 19/06/2026 | 19/06/2026 | <https://docs.aws.amazon.com/architecture/> |
| Sat | - Draw detailed architecture diagram on draw.io <br> - Define main API endpoints (login, upload, download, list files, view history) <br> - Define DynamoDB table structure for file metadata and audit logs | 20/06/2026 | 20/06/2026 | <https://docs.aws.amazon.com/apigateway/latest/developerguide/welcome.html> |
| Sun | - Review full architecture diagram and adjust <br> - Write design document explaining service selection <br> - Plan next week: build Frontend first then Backend | 21/06/2026 | 21/06/2026 | <https://docs.aws.amazon.com/architecture/> |

### Week 9 Achievements:

* Clearly defined 5 DMS feature groups: authentication, file management, versioning, access control, and activity history.
* Selected complete AWS stack: Cognito, S3, API Gateway + Lambda, DynamoDB, CloudFront, GuardDuty, CloudWatch + SNS.
* Completed system architecture diagram and design document.
