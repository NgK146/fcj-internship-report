---
title: "Week 3 Worklog"
date: 2026-05-05
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Week 3 Objectives:

* Set up Libreswan VPN and Hybrid DNS between AWS and on-premises environments.
* Connect multiple VPCs using VPC Peering and AWS Transit Gateway.

### Tasks carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| Tue | - Install & configure Libreswan VPN on EC2 <br> - Establish IPsec tunnel to AWS VGW <br> - Verify tunnel UP | 05/05/2026 | 05/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| Wed | - Configure Hybrid DNS with Route 53 Resolver <br> - Set up Inbound/Outbound endpoints <br> - Configure forwarding rules for on-premises DNS ↔ AWS DNS | 06/05/2026 | 06/05/2026 | <https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/resolver.html> |
| Sat | - Create VPC Peering between 2 VPCs <br> - Update route tables <br> - Test cross-VPC EC2 connectivity | 09/05/2026 | 09/05/2026 | <https://docs.aws.amazon.com/vpc/latest/peering/what-is-vpc-peering.html> |
| Sun | - Create Transit Gateway <br> - Attach 3 VPCs <br> - Configure TGW route tables <br> - Verify multi-VPC connectivity | 10/05/2026 | 10/05/2026 | <https://docs.aws.amazon.com/vpc/latest/tgw/what-is-transit-gateway.html> |

### Week 3 Achievements:

* Established a secure Libreswan IPsec tunnel connecting the on-premises lab to AWS.
* Configured Hybrid DNS, allowing seamless hostname resolution in both directions.
* Successfully connected VPCs using VPC Peering (understanding its non-transitive nature).
* Implemented AWS Transit Gateway to simplify multi-VPC connectivity (transitive routing).
