---
title: "Week 6 Worklog"
date: 2026-05-25
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Week 6 Objectives:

* Implement centralized security monitoring and automated operations (ChatOps).
* Enforce granular access controls using ABAC and KMS encryption.
* Audit resource events using CloudTrail and Athena.

### Tasks carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| Mon | - Enable Security Hub (AWS Foundational, CIS, PCI DSS) & AWS Config <br> - Analyze Security Score, disable unneeded EC2 SSM controls | 25/05/2026 | 25/05/2026 | <https://docs.aws.amazon.com/securityhub/latest/userguide/what-is-securityhub.html> |
| Mon | - Create VPC, EC2 'lambda-lab-instance' with environment_auto=true tag <br> - Configure Slack Incoming Webhook <br> - Deploy Lambda auto-stop & auto-start (Python, EC2 tag filter, EventBridge) <br> - Test EC2 state transitions and Slack alerts | 25/05/2026 | 25/05/2026 | <https://docs.aws.amazon.com/lambda/latest/dg/welcome.html> |
| Tue | - Launch 2 EC2s with tags (Environment: Test & UAT) <br> - Bulk/individual tag management via Console and CLI <br> - Create Tag-Based Resource Group 'MarketingBu' | 26/05/2026 | 26/05/2026 | <https://docs.aws.amazon.com/tag-editor/latest/userguide/tagging.html> |
| Wed | - Create custom ABAC IAM policies with tag conditions (Team: Alpha) and region restrictions <br> - Create cross-account IAM Role, execute Role Switch <br> - Validate ABAC: wrong tag → Launch Failed; correct tag → Success | 27/05/2026 | 27/05/2026 | <https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction_attribute-based-access-control.html> |
| Thu | - Create KMS Symmetric key & S3 Bucket with SSE-KMS <br> - Create CloudTrail (Management + Data events) <br> - Create Athena external table, query top 100 events <br> - Test Presigned URL expiry window | 28/05/2026 | 28/05/2026 | <https://docs.aws.amazon.com/kms/latest/developerguide/overview.html> |
| Fri | - Create IAM Group and 4 users with different permissions <br> - Test Switch Role with No-permission-user <br> - Add IP restriction (aws:SourceIp) and temporal boundary (aws:CurrentTime) to block access | 29/05/2026 | 29/05/2026 | <https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies.html> |
| Sat | - Launch EC2, create S3 bucket and upload script with hardcoded static keys (security risk) <br> - Create EC2 IAM Instance Profile with S3FullAccess <br> - Rewrite script without static credentials, verify token-based IMDS S3 upload | 30/05/2026 | 30/05/2026 | <https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/iam-roles-for-amazon-ec2.html> |

### Week 6 Achievements:

* Configured AWS Security Hub for centralized compliance monitoring across 3 standards.
* Implemented Lambda ChatOps for automated EC2 start/stop scheduling with Slack notifications.
* Enforced ABAC (Attribute-Based Access Control) using resource tags.
* Built a governance pipeline with KMS encryption, CloudTrail logging, and Athena querying.
* Applied advanced IAM controls including IP/time restrictions and EC2 Instance Profiles for credential-less access.
