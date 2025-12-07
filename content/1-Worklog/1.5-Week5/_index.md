
---
title: "Worklog Week 5"
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Week 5 Objectives:

* **RDS Role:** Clearly understand the role and benefits of the **Amazon RDS** service compared to self-managing databases on EC2.
* **Core Operations:** Be proficient in creating and connecting to a DB Instance (e.g., MySQL or PostgreSQL).
* **Key Features Mastery:** Master critical features: **Multi-AZ** (High Availability), **Read Replicas** (Read Scaling), and **Snapshot/Backup** procedures.
* **Network Security:** Practice managing network security for the DB Instance through Security Groups.

### Planned Tasks for the Week:

| Day | Task/Activity Focus | Start Date | Completion Date | Resource Material |
| :-- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | :----------- | :-------------- | :---------------------------------------- |
| **Mon** | * Review and comprehend **Amazon RDS Architecture** (DB Instance, Engine, Master Username/Password, DB Security Group). <br> * Compare RDS with self-managed databases on EC2. <br> * **Hands-on Practice:** Launch a DB Instance (Free Tier) within the VPC created in Week 3 (selecting a Private Subnet). | 06/10/2025 | 06/10/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Tue** | * Investigate connection methods and network security for RDS. <br> * **Hands-on Practice:** <br>&emsp; + Configure the RDS **Security Group** to allow access *only* from the **EC2 Instance's Security Group**. <br>&emsp; + Use a Client tool or EC2 to connect and create a basic table. | 07/10/2025 | 07/10/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Wed** | * Study **Multi-AZ Deployment** for ensuring High Availability (HA). <br> * Learn about **Automated Backups** and **DB Snapshots** (manual backups). <br> * **Hands-on Practice:** Enable Multi-AZ for the Instance and create a manual DB Snapshot. | 08/10/2025 | 08/10/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Thu** | * Explore **Read Replicas** to offload read traffic from the DB Master. <br> * **Hands-on Practice:** <br>&emsp; + Create a Read Replica for the primary DB Instance. <br>&emsp; + Simulate connecting an application to the Read Replica for read scaling. <br>&emsp; + Research the process of Promoting a Read Replica to a Standalone DB. | 09/10/2025 | 09/10/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Fri** | * **Cleanup and Optimization:** <br> * **Hands-on Practice:** <br>&emsp; + Delete the Read Replica. <br>&emsp; + Delete the primary DB Instance (Note: Uncheck 'Create Final Snapshot' if not needed). <br>&emsp; + Clean up all related Snapshots and Security Groups. | 10/10/2025 | 10/10/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |

### Week 5 Achievements:

* **RDS Management:** Clearly understood the benefits of RDS and are proficient in creating, configuring, and connecting to a DB Instance.
* **Connection Security:** Mastered using Security Groups to restrict database access *only* to specified resources (like EC2), ensuring strong network layer security.
* **High Availability (HA):** Understood and successfully implemented **Multi-AZ** deployment to protect the database against Availability Zone failures.
* **Scalability:** Understood and practiced creating **Read Replicas** to optimize read performance and reduce load on the DB Master.
* **Backup & Recovery:** Grasped the procedure for creating **DB Snapshots** and how RDS automatically performs **Automated Backups** for data recovery.

---