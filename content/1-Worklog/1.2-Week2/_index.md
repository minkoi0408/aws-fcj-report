---
title: "Worklog Week 2"
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Week 2 Objectives:

* **In-depth EC2 Understanding:** Clearly understand the role and operational mechanics of the **EC2** (Elastic Compute Cloud) virtual server service.
* **EC2 Lifecycle Management:** Be proficient in the process of launching, managing, and terminating an EC2 Instance.
* **Secure Access Control:** Master the concept and practical application of **IAM Roles** for securely granting access to AWS services for EC2 resources. [Image of AWS IAM Role structure for EC2]
* **Advanced CLI Usage:** Utilize the **AWS CLI** to execute fundamental EC2 management operations efficiently.

### Planned Tasks for the Week:

| Day | Task/Activity Focus | Start Date | Completion Date | Resource Material |
| :-- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :----------- | :-------------- | :---------------------------------------- |
| **Mon** | * Review and comprehend the core components of **Amazon EC2** (AMI, Instance Type, Key Pair, Security Group). <br> * **Hands-on Practice:** Launch the first EC2 Instance (selecting a Free Tier eligible type). | 15/09/2025 | 15/09/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Tue** | * Investigate the secure authorization mechanism: **IAM Roles for EC2** (Instance Profiles). <br> * **Hands-on Practice:** <br>&emsp; + Create an IAM Policy permitting `s3:ListBucket`. <br>&emsp; + Create an IAM Role and attach the newly created Policy. <br>&emsp; + Attach the IAM Role to the EC2 Instance. | 16/09/2025 | 16/09/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Wed** | * Explore the essential commands for managing **EC2 via AWS CLI**. <br> * **Hands-on Practice:** <br>&emsp; + Use the CLI to retrieve EC2 Instance information (`describe-instances`). <br>&emsp; + Use the CLI to Stop/Start the Instance. <br>&emsp; + Manage Security Groups using the CLI. | 17/09/2025 | 17/09/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Thu** | * **Integration Validation:** Verify IAM Role permissions. <br> * Access the EC2 Instance via SSH/Session Manager. <br> * **Hands-on Practice:** Execute the `aws s3 ls` (CLI command) from within the EC2 instance to confirm its ability to list S3 Buckets (proving the IAM Role functionality). | 18/09/2025 | 18/09/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Fri** | * **Lifecycle & Cost Management:** <br> * Review EC2 Instance lifecycle states (Pending, Running, Stopping, Terminated). [Image of AWS EC2 Instance lifecycle states diagram] <br> * **Hands-on Practice:** <br>&emsp; + **Terminate** the EC2 Instance. <br>&emsp; + Delete the associated IAM Role and Policy to ensure resource cleanup. | 19/09/2025 | 19