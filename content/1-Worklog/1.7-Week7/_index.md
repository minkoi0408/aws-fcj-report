
---
title: "Worklog Week 7"
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Week 7 Objectives:

* **Automated Scaling:** Clearly understand the role and configuration of **EC2 Auto Scaling Group (ASG)** for automatic resource scaling (scaling out and in).
* **Load Balancing:** Master the architecture and operation of **Elastic Load Balancer (ELB)** (specifically ALB) for distributing traffic.
* **Monitoring:** Be proficient in using **Amazon CloudWatch** to collect metrics and logs, create Dashboards, and set up Alarms.
* **Operational Automation:** Practice establishing **Scaling Policies** based on monitored performance indicators.

### Planned Tasks for the Week:

| Day | Task/Activity Focus | Start Date | Completion Date | Resource Material |
| :-- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | :----------- | :-------------- | :---------------------------------------- |
| **Mon** | * Review and comprehend **Auto Scaling Group (ASG)** and Launch Template architecture. <br> * Learn about different Load Balancer types (Classic, Application, Network). <br> * **Hands-on Practice:** Create a Launch Template and configure a basic ASG. | 20/10/2025 | 20/10/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Tue** | * In-depth study of **Application Load Balancer (ALB)** and its components (Listener, Target Group, Health Check). <br> * **Hands-on Practice:** <br>&emsp; + Create an ALB and Target Group. <br>&emsp; + Register the ASG's EC2 Instances with the Target Group. | 21/10/2025 | 21/10/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Wed** | * Learn about the **Amazon CloudWatch** monitoring service (Metrics, Logs, Events). <br> * **Hands-on Practice:** <br>&emsp; + View EC2, ALB, and ASG Metrics in CloudWatch. <br>&emsp; + Create a CloudWatch Dashboard to track key indicators (CPU Utilization, Request Count). | 22/10/2025 | 22/10/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Thu** | * Study **CloudWatch Alarms** and different **Scaling Policy** types (Target Tracking, Step Scaling). <br> * **Hands-on Practice:** <br>&emsp; + Create a CloudWatch Alarm based on CPU Utilization (e.g., > 80%). <br>&emsp; + Configure a Scaling Policy for the ASG using the new Alarm (scale out on high CPU). | 23/10/2025 | 23/10/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Fri** | * **Testing & Resource Cleanup:** <br> * **Hands-on Practice:** <br>&emsp; + Verify the Scale Out/In process functions correctly. <br>&emsp; + **Cleanup:** Delete CloudWatch Alarms, delete the ASG (which automatically terminates EC2 instances), delete the ALB, and delete the Launch Template. | 24/10/2025 | 24/10/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |

### Week 7 Achievements:

* **Scalability:** Successfully deployed an application architecture capable of automatic scaling (Scale Out/In) via **ASG** and **Launch Template**.
* **Load Balancing:** Understood and configured the **Application Load Balancer (ALB)** to distribute traffic and perform effective Health Checks.
* **Observability:** Mastered the use of **CloudWatch** for collecting, visualizing (Dashboard), and monitoring resource health indicators.
* **Automation:** Successfully implemented an automated scaling mechanism based on performance (Scaling Policy and CloudWatch Alarms).
* **Cost Management:** Proficient in the cleanup procedure for costly resources such as ALB and ASG.

---