
---
title: "Worklog Week 6"
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Week 6 Objectives:

* **NoSQL Fundamentals:** Clearly understand the architecture and advantages of the **Amazon DynamoDB** NoSQL service (Key-Value/Document model).
* **DynamoDB Management:** Be proficient in creating and managing DynamoDB tables and utilizing Index types (**GSI/LSI**).
* **Caching Role:** Master the role of **Amazon ElastiCache** in accelerating application response times.
* **Caching Practice:** Practice creating and configuring an ElastiCache Cluster (Redis/Memcached).

### Planned Tasks for the Week:

| Day | Task/Activity Focus | Start Date | Completion Date | Resource Material |
| :-- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :----------- | :-------------- | :---------------------------------------- |
| **Mon** | * Review and comprehend **Amazon DynamoDB Architecture** (Primary Key, Partition Key, Sort Key). <br> * Learn concepts of Read/Write Capacity Units (RCU/WCU) and On-Demand mode. <br> * **Hands-on Practice:** Create the first DynamoDB table, insert, and query basic data. | 13/10/2025 | 13/10/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Tue** | * In-depth study of Index types: **Local Secondary Index (LSI)** and **Global Secondary Index (GSI)**. <br> * **Hands-on Practice:** Create a GSI for the DynamoDB table to support non-primary key queries. | 14/10/2025 | 14/10/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Wed** | * Learn about the **Amazon ElastiCache** caching service (Redis and Memcached). <br> * Analyze the benefits of using a caching layer to offload traffic from RDS/DynamoDB. <br> * **Hands-on Practice:** Launch an ElastiCache Cluster (e.g., Redis) in a Private Subnet. | 15/10/2025 | 15/10/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Thu** | * Study how to **configure Security Group** for ElastiCache to ensure secure connectivity from EC2. <br> * Learn how applications connect to and perform basic data operations on ElastiCache. <br> * **Hands-on Practice:** Configure the Security Group for the ElastiCache Cluster. | 16/10/2025 | 16/10/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Fri** | * **Resource Cleanup & Knowledge Review:** <br> * **Hands-on Practice:** <br>&emsp; + Delete the created DynamoDB table. <br>&emsp; + Delete the ElastiCache Cluster. <br>&emsp; + Summarize the pros/cons and Use-cases for RDS, DynamoDB, and ElastiCache. | 17/10/2025 | 17/10/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |

### Week 6 Achievements:

* **DynamoDB Fundamentals:** Clearly understood the DynamoDB NoSQL model, proficient in creating, managing tables, and primary key types.
* **Query & Cost Optimization:** Grasped the role of **GSI/LSI** and capacity modes (On-Demand/Provisioned) in DynamoDB.
* **ElastiCache Architecture:** Understood the differences and benefits of Redis/Memcached. Grasped the role of the caching layer in application architecture.
* **Caching Deployment:** Successfully launched an ElastiCache Cluster and set up network security via Security Group.
* **Service Differentiation:** Able to compare and choose between RDS, DynamoDB, and ElastiCache based on different data and performance requirements.

---