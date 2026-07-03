---
title: "Week 1 Worklog"
date: 2026-04-20
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

### Week 1 Objectives:

* Set up the AWS environment and manage costs effectively.
* Understand and implement IAM for secure access control following the principle of least privilege.

### Tasks carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| Mon | - Complete AWS Credit Tasks to receive $200 credits <br> - Learn AWS Budgets for cost monitoring | 20/04/2026 | 20/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| Sat | - Create AWS Budget (Monthly cost template, alerts at 85%, 100%) <br> - Create Cost Budget (Customize, alerts at 50%, 80%, 100%) <br> - Create Usage Budget (EC2 running hours) <br> - Create RI Budget & Savings Plans Budget (demo) <br> - Clean up unnecessary budgets | 25/04/2026 | 25/04/2026 | <https://docs.aws.amazon.com/cost-management/latest/userguide/budgets-managing-costs.html> |
| Sat | - Create IAM Admin Group (AdministratorAccess) <br> - Create IAM Admin User & login <br> - Create Admin Role & Operator User <br> - Configure Role Switching (sts:AssumeRole) <br> - Test IAM Role Switch as OperatorUser <br> - Review IAM resource cleanup | 25/04/2026 | 25/04/2026 | <https://docs.aws.amazon.com/IAM/latest/UserGuide/getting-started.html> |

### Week 1 Achievements:

* Successfully received $200 AWS credits by completing required tasks.

* Set up multiple AWS Budget types:
  * Monthly Cost Budget with alerts at 85% and 100%
  * Custom Cost Budget with alerts at 50%, 80%, and 100% — notifications delivered via email
  * EC2 Usage Budget for running hours tracking
  * RI and Savings Plans Budgets (for demonstration purposes)

* Understood cost management best practices and how to avoid unexpected AWS charges.

* Implemented IAM access control:
  * Created IAM Admin Group with AdministratorAccess policy
  * Created IAM Admin User and IAM Operator User
  * Created Admin Role with full administrative permissions
  * Configured inline policy for OperatorUser to assume AdminRole via `sts:AssumeRole`
  * Successfully performed IAM Role Switching from OperatorUser to AdminRole
  * Retained essential IAM resources for future labs
