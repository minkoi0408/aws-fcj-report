
---
title: "Worklog Week 11"
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Week 11 Objectives:

* **Perimeter Security:** Clearly understand the role of **AWS WAF** (Web Application Firewall) and **AWS Shield** in protecting applications from Layer 7 (WAF) and DDoS (Shield) attacks.
* **Threat Detection:** Master the operational mechanism and benefits of the intelligent threat detection service **Amazon GuardDuty**.
* **Security Principles:** Review and apply advanced security principles such as **IAM Policy Best Practices** and **Secrets Management**.
* **Configuration Practice:** Practice configuring fundamental security Rules and enabling monitoring services.

### Planned Tasks for the Week:

| Day | Task/Activity Focus | Start Date | Completion Date | Resource Material |
| :-- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :----------- | :-------------- | :---------------------------------------- |
| **Mon** | * Review and comprehend **AWS WAF** and **Web ACL** (Access Control List) architecture. <br> * Learn about Layer 7 attack types (SQL Injection, XSS) that WAF protects against. <br> * **Hands-on Practice:** Create a Web ACL and explore the Managed Rule Groups. | 17/11/2025 | 17/11/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Tue** | * Study **AWS Shield Standard/Advanced** (DDoS Protection) and its integration with WAF/Route 53. <br> * **WAF Practice:** <br>&emsp; + Create a Rate-based Rule (limiting access frequency). <br>&emsp; + Experiment with blocking specific IPs (IP Set) via WAF. | 18/11/2025 | 18/11/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Wed** | * Learn about the **Amazon GuardDuty** threat detection service (utilizing Machine Learning). <br> * **Hands-on Practice:** Enable GuardDuty and review sample Findings (simulated threats) to understand the service's alerting mechanism. | 19/11/2025 | 19/11/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Thu** | * Review and apply **IAM Policy Best Practices** (Principle of Least Privilege). <br> * Learn about **AWS Secrets Manager** (automated credentials rotation) and **AWS Systems Manager Parameter Store** (configuration storage). <br> * **Hands-on Practice:** Re-evaluate IAM Policies created in Week 2. | 20/11/2025 | 20/11/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Fri** | * **Consolidation & Resource Cleanup:** <br> * **Hands-on Practice:** <br>&emsp; + Delete the Web ACL/WAF Rules. <br>&emsp; + **Disable GuardDuty**. <br>&emsp; + Summarize the learned security measures (Perimeter Security, Monitoring, Secrets Management). | 21/11/2025 | 21/11/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |

### Week 11 Achievements:

* **Perimeter Defense:** Clearly understood how WAF and Shield operate at the network edge to protect resources like CloudFront and ALB.
* **Threat Detection:** Proficient in enabling and monitoring alerts from **GuardDuty** to detect suspicious activities within the AWS account.
* **Identity Management:** Reinforced knowledge of **IAM Policies** and understood the importance of managing secrets using dedicated services.
* **Security Architecture:** Grasped how to integrate security services into the application architecture (e.g., using WAF before ALB) and the multi-layered security principle.

---