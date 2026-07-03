---
title: "Blog 3"
date: 2026-07-03
weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---
{{% notice warning %}}
⚠️ **Note:** The information below is for reference purposes only. Please **do not copy verbatim** for your report, including this warning.
{{% /notice %}}

# Sending Daily Delta Cost Reports in a Multi-Account Environment Using AWS Lambda and Cost Explorer

In a multi-account AWS environment, tracking costs is always a tough challenge, especially when finance or management teams lack direct access to the AWS Billing Console.

While researching cost management and automation on AWS, I read a blog post explaining how to automatically send daily delta cost reports in a multi-account environment. I found this solution highly practical because it increases "cost visibility" while significantly reducing manual effort in cloud cost management.

### Common Problems

AWS Organizations allows managing and consolidating billing for multiple accounts within an organization. However, cost reports are typically only available to users with billing access in the management account.
This leads to several issues:
- Finance or management teams lack AWS access.
- Sharing cost reports usually requires manual effort.
- It's difficult to track cost changes across different accounts.
- A lack of organizational "cost visibility."
- The cost management process becomes overly complex with multiple accounts like Production, Non-Production, or Sandbox.

### The Core Solution

The solution uses AWS Lambda to automatically generate and send a daily "delta cost" report via email.
"Delta cost" refers to the cost difference between the current day and the previous day, helping teams quickly detect abnormal fluctuations in cloud costs.

The system leverages native AWS services such as:
- **AWS Lambda**
- **AWS Cost Explorer API**
- **Amazon EventBridge**
- **Amazon Simple Email Service (SES)**

What I like most is that the entire architecture is serverless and relies on managed services, meaning there is virtually no infrastructure to manage.

### Overall Architecture

**Workflow:**
1. **Amazon EventBridge** triggers Lambda on a daily cron schedule.
2. **Lambda** calls the AWS Cost Explorer API to retrieve cost data from accounts in the organization.
3. **Lambda** calculates the percentage change in cost (delta) compared to the previous day.
4. The data is formatted into an HTML report.
5. **Amazon SES** sends the email to the recipient list.

![Architecture Diagram](../../images/delta-cost.png)

### Key Benefits

- Fully automates the cost reporting process.
- Makes information easily accessible to leadership and finance teams.
- Operates effectively in a multi-account environment.
- Enhances organizational cost visibility.
- Easy to deploy using a CloudFormation template.
- Can be extended to store report history in S3 for long-term analysis.

Additionally, this solution helps technical and finance teams collaborate more effectively to optimize cloud costs through FinOps practices.

### Main Deployment Steps

1. Download the CloudFormation template from the original blog.
2. Configure account IDs and email recipients.
3. Verify emails in Amazon SES.
4. Deploy the stack.
5. Grant Billing permissions to the IAM Role.
6. Configure the EventBridge rule with a cron expression.

Once completed, the system will automatically send cost reports via email every day.

### Personal Reflection

I find this solution very practical because it addresses a common problem for AWS teams: cloud costs increasing without timely tracking.
The architecture is compact, primarily relying on native AWS services like Lambda, EventBridge, and SES, so deployment isn't overly complex. For me, this is a clear example of how AWS uses automation to reduce manual operational tasks.

Beyond sending cost reports, I believe this model could be extended—such as saving history to S3, creating tracking dashboards, or integrating alerts for unusual cost spikes.

**Original link:** <https://aws.amazon.com/blogs/mt/email-delta-cost-usage-report/>
