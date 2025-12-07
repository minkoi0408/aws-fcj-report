
---
title: "Worklog Week 4"
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Week 4 Objectives:

* **S3 Fundamentals:** Clearly understand the role, architecture, and durability of the **Amazon S3** (Simple Storage Service).
* **Bucket Management & Security:** Be proficient in creating and managing **Buckets**, and implementing security policies like **Bucket Policy**.
* **Storage Optimization:** Master S3's storage classes (**Standard, IA, Glacier**) and know how to use **Lifecycle Rules** for automated cost optimization.
* **Practical Application:** Practice deploying a static website (**Static Website Hosting**) on S3.

### Planned Tasks for the Week:

| Day | Task/Activity Focus | Start Date | Completion Date | Resource Material |
| :-- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :----------- | :-------------- | :---------------------------------------- |
| **Mon** | * Review and comprehend the fundamental architecture of **Amazon S3** (Object, Key, Bucket, Region). <br> * Learn about security features: Block Public Access, Access Control List (ACL). <br> * **Hands-on Practice:** Create a new S3 Bucket and customize Block Public Access settings. | 29/09/2025 | 29/09/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Tue** | * Explore S3's **Storage Classes** (Standard, Standard-IA, One Zone-IA, Glacier, Deep Archive). <br> * Understand **Lifecycle Rules** for automated transition between storage tiers. <br> * **Hands-on Practice:** Configure a Lifecycle Rule for the Bucket, transitioning old objects to Standard-IA. | 30/09/2025 | 30/09/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Wed** | * Study the **Versioning** feature and the procedure for object recovery. <br> * Learn about **Bucket Policy** for centralized access management. <br> * **Hands-on Practice:** Enable Versioning for the Bucket and attempt to delete/restore an object. | 01/10/2025 | 01/10/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Thu** | * Research the **Static Website Hosting** feature on S3. <br> * **Hands-on Practice:** <br>&emsp; + Upload HTML/CSS/JS files (Index.html & Error.html). <br>&emsp; + Enable Static Website Hosting and set up a Bucket Policy to allow public access. <br>&emsp; + Access the website via the S3 Endpoint. | 02/10/2025 | 02/10/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Fri** | * **Cleanup and S3 CLI Review:** <br> * **Hands-on Practice:** <br>&emsp; + Use **AWS CLI** to upload/download/sync data with S3 (`aws s3 cp`, `aws s3 sync`). <br>&emsp; + **Resource Cleanup:** Disable Versioning, delete all objects (including old versions), and then delete the Bucket. | 03/10/2025 | 03/10/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |

### Week 4 Achievements:

* **Comprehensive S3 Management:** Clearly understood, created, configured, and managed S3 Buckets. Grasped the roles of **Block Public Access** and **ACL**.
* **Storage Cost Optimization:** Mastered S3's **Storage Classes** and know how to use **Lifecycle Rules** to automatically transition data to less expensive tiers over time.
* **Security and Data Governance:** Successfully practiced enabling/disabling **Versioning** and applying **Bucket Policy** to control public and IAM User access.
* **Practical Application:** Successfully deployed a static website on S3 and accessed it via the public Endpoint.
* **CLI Proficiency:** Proficiently used the AWS CLI for efficient data management on S3 (upload, download, sync).

---