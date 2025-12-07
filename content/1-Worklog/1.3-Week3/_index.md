
---
title: "Worklog Week 3"
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Week 3 Objectives:

* **VPC Architecture:** Clearly understand the role and core components of the **Amazon Virtual Private Cloud (VPC)** networking service.
* **Network Configuration:** Be proficient in creating and configuring a custom VPC, Subnets (Public/Private), Internet Gateway (IGW), and Route Tables.
* **Multi-Layer Security:** Master the two-layer security mechanisms: **Security Group (SG)** and **Network Access Control List (NACL)**.
* **Deployment Practice:** Successfully deploy an EC2 Instance within a custom VPC environment.

### Planned Tasks for the Week:

| Day | Task/Activity Focus | Start Date | Completion Date | Resource Material |
| :-- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :----------- | :-------------- | :---------------------------------------- |
| **Mon** | * Review and comprehend **VPC Architecture**: Concepts of IP, CIDR Block, Subnet, and Availability Zone (AZ). <br> * **Hands-on Practice:** Create a new VPC with a custom CIDR range (e.g., `10.0.0.0/16`). <br> * Create two Subnets: one Public and one Private. | 22/09/2025 | 22/09/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Tue** | * Study **Internet Gateway (IGW)**, **Route Table**, and their roles in providing Internet access. <br> * **Hands-on Practice:** <br>&emsp; + Create and attach the IGW to the VPC. <br>&emsp; + Configure the **Public Route Table** to route traffic to the IGW. <br>&emsp; + Associate the Public Route Table with the Public Subnet. | 23/09/2025 | 23/09/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Wed** | * Learn about the **Security Group (SG)** (Stateful) security mechanism and its operational principles. <br> * **Hands-on Practice:** <br>&emsp; + Launch an EC2 Instance into the Public Subnet. <br>&emsp; + Configure the SG to only allow SSH/RDP (Port 22/3389) from a personal IP address. <br>&emsp; + Test connectivity to validate SG security features. | 24/09/2025 | 24/09/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Thu** | * Learn about the **Network Access Control List (NACL)** (Stateless) security mechanism. <br> * **Hands-on Practice:** <br>&emsp; + Configure NACL for the Public Subnet (experiment with a Deny rule). <br>&emsp; + Detail the differences in inbound/outbound processing between SG and NACL. <br>&emsp; + Research the concept of NAT Gateway (its role in the Private Subnet). | 25/09/2025 | 25/09/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Fri** | * **Cleanup & Comprehensive Review:** <br> * **Hands-on Practice:** <br>&emsp; + **Terminate** the EC2 Instance. <br>&emsp; + **Delete all created VPC components** in the correct sequence (Detach IGW -> Delete Subnets -> Delete Route Tables -> Delete VPC) for cost optimization. <br>&emsp; + Summarize the learned VPC components and their functionalities. | 26/09/2025 | 26/09/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |

### Week 3 Achievements:

* **Complete VPC Configuration:** Successfully understood and manually created a VPC, Subnets (Public/Private), Internet Gateway, and Route Tables to direct network traffic.
* **Network Layer Security:** Fully grasp and distinguish between the two security layers: **Security Group** (Stateful, operates at the Instance level) and **NACL** (Stateless, operates at the Subnet level).
* **Basic Deployment:** Successfully deployed an EC2 Instance within the custom VPC and confirmed Internet access capability.
* **Resource Cleanup Proficiency:** Successfully performed network resource cleanup in the correct order, ensuring efficient cost management.

---