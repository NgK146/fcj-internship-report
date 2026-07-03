---
title: "Blog 1"
date: 2026-07-03
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---
{{% notice warning %}}
⚠️ **Note:** The information below is for reference purposes only. Please **do not copy verbatim** for your report, including this warning.
{{% /notice %}}

# HOW TO BUILD A COST-EFFECTIVE AWS KMS STRATEGY FOR MULTI-TENANT APPLICATIONS

During my studies and internship, I realized that when building SaaS applications for multiple customers (multi-tenant), managing data encryption is just one part of the equation. The real challenge arises when you need to balance strong security, reasonable costs, and easy management as the number of tenants grows. Amazon KMS provides powerful encryption tools, but creating separate keys for each tenant and service can quickly drive up costs and make management complex.

To solve this, AWS recommends a centralized key management approach. This solution builds a central key management layer on top of AWS KMS, combining it with IAM roles, aliases, AWS STS, and other services. This architecture helps reduce costs, simplifies management, maintains isolation between tenants, and fully leverages KMS encryption capabilities.

### HIGHLIGHTS OF THE SOLUTION:

**Centralized key management in a dedicated account**
All customer-managed KMS keys for tenants are placed in Account A (Centralized key management service). Services serving customers in Account B are only granted temporary permissions when needed. This prevents key sprawl and helps control the entire key lifecycle (creation, rotation, deletion) in one place.

**Using aliases and IAM roles for secure key sharing**
Each tenant has an alias like `alias/customer-<tenant-id>`. Service B (typically Lambda) receives a JWT containing the tenant ID, then assumes ServiceBRole → assumes ServiceARole in Account A to access the key via the alias. Thanks to AWS STS, permissions are temporary and tightly controlled.

**Client-side data encryption and secure storage**
Sensitive data (passwords, API keys, license info...) is encrypted using Boto3 or the AWS Encryption SDK before being stored in DynamoDB or S3. Because each tenant uses their own key, data is fully isolated, even when stored in the same database.

**Easy scaling for large systems**
When the number of tenants grows from tens to thousands, the architecture continues to perform well. You simply create new keys and aliases in Account A. No code changes are required in customer-facing services. Costs remain manageable, as each key only costs around $1-3/month.

**Adherence to security and operational best practices**
The solution uses IAM policies with conditions to restrict permissions strictly to `alias/customer-<tenant-id>`, integrated with CloudTrail for auditing. This reduces risks and simplifies compliance with security standards.

### HOW IT WORKS IN PRACTICE

Suppose a customer sends sensitive information (passwords, API keys, licenses...) via Service B.
- Service B receives a JWT containing the tenant ID.
- Lambda (or another service) validates the JWT.
- Assumes Service B Role → Assumes Service A Role in Account A.
- Uses the alias (e.g., `alias/customer-<tenant-id>`) to access the correct tenant key.
- Encrypts data using Boto3 or AWS Encryption SDK.
- Stores the encrypted data in DynamoDB.

Everything happens seamlessly, and data is always protected using each tenant's dedicated key.

![Architecture Diagram](../../images/kms-multitenant.png)

### THE ROLE OF AWS SERVICES

The architecture is built on the clear coordination of multiple services:
- **AWS KMS**: Provides customer-managed keys for each tenant.
- **IAM & AWS STS**: Manages assume role permissions across accounts.
- **AWS Lambda**: Processes requests, validates JWTs, and performs encryption.
- **Amazon DynamoDB / S3**: Stores encrypted data.
- **Alias**: Keeps the code clean and maintainable without hardcoding key IDs.

Each component has a distinct responsibility. As a result, the system is easy to manage, easy to debug, and reduces dependency on any single service.

### BUSINESS VALUE

Adopting a centralized KMS strategy provides several practical benefits:
- Significantly reduces key management costs.
- Simplifies operations and auditing by centralizing keys.
- Ensures high isolation and security between tenants.
- Facilitates rapid scaling as the business grows.
- Reduces the burden on DevOps teams, eliminating "key explosion" concerns.
- Flexibly applies to multiple services (DynamoDB, S3, EBS...).

This solution is ideal for SaaS applications, enterprise platforms, sensitive data processing systems, or any multi-tenant project on AWS.

### CONCLUSION

AWS KMS is a robust encryption service, but using it for multi-tenant systems at scale requires a smarter approach to control costs and operations. By building a centralized key management service combined with IAM roles, aliases, and JWT assume-role workflows, we can effectively solve this problem.

This solution reflects a common approach in modern AWS architecture: each service focuses on doing one thing well, and they connect to form a flexible, secure, and cost-effective system.

As an intern, I haven't worked on a real KMS multi-tenant task yet, but after reading the original article and diagram, I find this pattern highly educational. It helped me better understand how to design cloud systems that balance security, cost, and scalability.

**Original link (Vietnamese):** <https://aws.amazon.com/blogs/aws/simplify-multi-tenant-kms/>
