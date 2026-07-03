---
title: "Blog 2"
date: 2026-07-03
weight: 2
chapter: false
pre: " <b> 3.2. </b> "
---
{{% notice warning %}}
⚠️ **Note:** The information below is for reference purposes only. Please **do not copy verbatim** for your report, including this warning.
{{% /notice %}}

# Amazon Bedrock Baseline Architecture in an AWS Landing Zone: A Platform for Deploying Enterprise Generative AI

Building an AI application isn't overly difficult. However, when an enterprise operates dozens of AI applications simultaneously, the challenge is no longer just connecting to an AI model. The real challenge is managing the entire AI ecosystem to ensure security, stability, and operational efficiency.

Through the Amazon Bedrock Baseline Architecture in an AWS Landing Zone, AWS proposes a reference architecture that helps enterprises build a centralized Generative AI platform, ensuring long-term governance, security, and scalability.

### Why do we need a standard architecture for Generative AI?

In the experimental phase, individual development teams might build AI applications and connect them directly to Amazon Bedrock.
However, as the number of applications grows, enterprises face numerous challenges:
- Difficulties in managing access permissions.
- Difficulties in tracking AI usage costs.
- Difficulties in controlling data and traffic.
- Difficulties in enforcing consistent security policies.
- Difficulties in auditing and compliance.

### Proposed Architecture

- **Service Network Account**: Manages network connectivity, controls AI access, manages security policies, coordinates traffic across accounts, and centralizes all AI traffic into a single hub.
- **Generative AI Account**: Deploys Amazon Bedrock, Bedrock Knowledge Bases, Bedrock Guardrails, Foundation Models, and related AI services. It facilitates centralized governance, cost tracking, and operational standardization.
- **Workload Accounts**: Deploy customer chatbots, internal assistants, document processors, RAG applications, and business applications. These access AI through the central control layer rather than connecting directly to Bedrock.

![Architecture Diagram](../../images/bedrock-baseline.png)

### Key Highlights of the Architecture

- Separates the AI Platform Account from Workload Accounts.
- All AI traffic is centrally controlled via Amazon VPC Lattice.
- Amazon Bedrock is deployed as a shared service across the entire organization.
- Integrates Bedrock Guardrails to enhance content control and security.
- Aligns with the multi-account model and AWS Landing Zone.

### Conclusion

The Amazon Bedrock Baseline Architecture is not just a technical design; it's a governance model for Generative AI at the enterprise level.

By centralizing AI resource management, controlling traffic, enhancing security, and standardizing operational processes, AWS helps enterprises solve three major challenges in AI deployment:
1. **Security**
2. **Governance**
3. **Scalability**

### Recommendations

- **For enterprises experimenting with AI**: Start small, build governance early, and standardize permissions.
- **For enterprises scaling AI**: Separate the AI Account, centrally manage AI resources, and track usage costs.
- **For large-scale enterprises**: Build a shared AI Platform, deploy a Landing Zone, implement centralized governance, and establish AI Governance and AI Security frameworks.

**Original link:** <https://aws.amazon.com/blogs/architecture/amazon-bedrock-baseline-architecture-in-an-aws-landing-zone/>
