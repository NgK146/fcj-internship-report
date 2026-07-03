---
title: "Week 11 Worklog"
date: 2026-06-29
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Week 11 Objectives:

* Complete full backend deployment for the DMS.
* Implement asynchronous event-driven processing via SQS and S3 Event Notifications.
* Secure and monitor the system using CloudFront, GuardDuty, and CloudWatch.

### Tasks carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| Mon | - Complete Lambda Upload Intent (generate S3 Presigned URL, save metadata to DynamoDB) <br> - Configure SQS Queue to receive S3 Event Notifications | 29/06/2026 | 29/06/2026 | <https://docs.aws.amazon.com/AmazonS3/latest/userguide/NotificationHowTo.html> |
| Tue | - Build Lambda Upload Processor (read SQS messages, move files to S3 Documents Bucket) <br> - Connect S3 Event Notification → SQS → Lambda trigger <br> - Test full upload flow | 30/06/2026 | 30/06/2026 | <https://docs.aws.amazon.com/lambda/latest/dg/with-sqs.html> |
| Wed | - Deploy Frontend to S3 Frontend Bucket <br> - Create CloudFront Distribution (Origin Access Control) <br> - Verify UI loads via CloudFront HTTPS URL | 01/07/2026 | 01/07/2026 | <https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/GettingStartedCreateDistrib.html> |
| Thu | - Enable Amazon GuardDuty for S3 bucket protection <br> - Enable CloudWatch Logs for all Lambda functions <br> - Create CloudWatch Alarm for Lambda error rates | 02/07/2026 | 02/07/2026 | <https://docs.aws.amazon.com/guardduty/latest/ug/what-is-guardduty.html> |
| Fri | - Create SNS Topic, subscribe email for alerts <br> - Connect CloudWatch Alarm → SNS → Email <br> - Test full main flow: Cognito login → API Gateway → Lambda → S3 → SQS → Lambda Processor → Documents Bucket | 03/07/2026 | 03/07/2026 | <https://docs.aws.amazon.com/sns/latest/dg/welcome.html> |
| Sat | - Fix CORS on API Gateway, missing IAM permissions, SQS timeout <br> - Verify S3 Versioning works on same-name uploads <br> - Confirm Lambda-Get `/me` returns correct Cognito user info | 04/07/2026 | 04/07/2026 | <https://docs.aws.amazon.com/apigateway/latest/developerguide/how-to-cors.html> |
| Sun | - Review full system against architecture diagram <br> - Confirm all 16 connection flows working <br> - List test cases for official testing next week | 05/07/2026 | 05/07/2026 | <https://docs.aws.amazon.com/architecture/> |

### Week 11 Achievements:

* Fully deployed the Serverless Backend architecture.
* Integrated event-driven processing using S3 Event Notifications, SQS, and Lambda.
* Deployed the Frontend globally via S3 and CloudFront.
* Configured automated monitoring and threat detection with CloudWatch, SNS, and GuardDuty.
