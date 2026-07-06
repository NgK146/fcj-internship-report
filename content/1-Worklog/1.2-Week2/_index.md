---
title: "Week 2 Worklog"
date: 2026-04-27
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Week 2 Objectives:

* Build a complete VPC network with public/private subnets, NAT Gateway, and VPN connectivity.
* Practice AWS Systems Manager Session Manager as a secure alternative to SSH.

### Tasks carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| Mon | - Create VPC with CIDR 10.10.0.0/16 <br> - Create 2 public subnets and 2 private subnets across 2 AZs <br> - Create and attach Internet Gateway <br> - Configure public and private Route Tables <br> - Enable auto-assign public IP on public subnets | 27/04/2026 | 27/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| Tue | - Create NAT Gateway in public subnet <br> - Update private route table to route 0.0.0.0/0 → NAT Gateway <br> - Launch EC2 in private subnet, test internet access via NAT <br> - Configure Systems Manager (SSM) Session Manager <br> - Connect to private EC2 without SSH key via Session Manager | 28/04/2026 | 28/04/2026 | <https://docs.aws.amazon.com/vpc/latest/userguide/what-is-amazon-vpc.html> |
| Wed | - Create Customer Gateway and Virtual Private Gateway <br> - Set up Site-to-Site VPN connection (BGP routing) <br> - Download and configure VPN config on on-premises side <br> - Verify VPN tunnel status (UP) and test connectivity | 29/04/2026 | 29/04/2026 | <https://docs.aws.amazon.com/vpn/latest/s2svpn/VPC_VPN.html> |

### Week 2 Achievements:

* Built a complete multi-AZ VPC architecture:
  * CIDR: 10.10.0.0/16 with 4 subnets across 2 AZs
  * Internet Gateway for public subnet internet access
  * NAT Gateway for private subnet outbound access

* Configured Systems Manager Session Manager as a keyless, secure EC2 connection method.

* Established Site-to-Site VPN between AWS VPC and on-premises network:
  * BGP dynamic routing configured
  * VPN tunnel status verified as UP
  * Cross-network connectivity confirmed
