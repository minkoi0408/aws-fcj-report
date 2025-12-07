---
title: "Worklog Week 10"
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Week 10 Objectives:

* **Message Queuing:** Clearly understand the role and operation of the **Amazon Simple Queue Service (SQS)** message queuing service (Standard & FIFO).
* **Pub/Sub Architecture:** Master the **Publish/Subscribe** architecture using the **Amazon Simple Notification Service (SNS)** notification service.
* **Workflow Orchestration:** Be proficient in creating and configuring **AWS Step Functions** state machines to coordinate AWS services.
* **Integration Practice:** Practice building an asynchronous workflow using SQS, SNS, and Lambda.

### Planned Tasks for the Week:

| Day | Task/Activity Focus | Start Date | Completion Date | Resource Material |
| :-- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :----------- | :-------------- | :---------------------------------------- |
| **Mon** | * Review and comprehend **Amazon SQS** architecture (Message Queue) and the difference between Standard and FIFO Queues. <br> * **Hands-on Practice:** Create an SQS Standard Queue, manually send, and receive messages via the Console. | 10/11/2025 | 10/11/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Tue** | * Study the **Amazon SNS** notification service (Topic, Subscriber) and the Pub/Sub model. <br> * **Hands-on Practice:** <br>&emsp; + Create an SNS Topic. <br>&emsp; + Create an SQS Queue and a Lambda function (from Week 8) as Subscribers to the Topic. <br>&emsp; + Publish a message to the Topic and verify delivery to SQS/Lambda. | 11/11/2025 | 11/11/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Wed** | * Learn about **AWS Step Functions** (State Machine, Task State, Choice State). <br> * **Hands-on Practice:** <br>&emsp; + Create a new Lambda function (e.g., `ProcessStep1`). <br>&emsp; + Create a simple State Machine (with a single Task step) to orchestrate and invoke this Lambda function. | 12/11/2025 | 12/11/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Thu** | * Study how **Step Functions** orchestrate complex logical flows (Sequence, Choice, Parallel). <br> * **Hands-on Practice:** Extend the created State Machine: <br>&emsp; + Add a `Choice` step based on the input result. <br>&emsp; + Integrate SQS (e.g., send a message to a queue if the flow follows a specific path). | 13/11/2025 | 13/11/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Fri** | * **Resource Cleanup & Overall Integration Review:** <br> * **Hands-on Practice:** <br>&emsp; + Delete the State Machine, SQS Queue, and SNS Topic. <br>&emsp; + Review how these services (SQS, SNS, Step Functions) solve asynchronous communication and application decoupling challenges. | 14/11/2025 | 14/11/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |

### Week 10 Achievements:

* **Message Queuing:** Clearly understood the role of SQS in application **decoupling** and **load leveling** (buffering). Proficient in sending/receiving messages via SQS.
* **Pub/Sub Model:** Mastered the **SNS** mechanism for efficiently and reliably distributing messages to multiple subscribers.
* **Workflow Orchestration:** Clearly understood how **Step Functions** coordinates other AWS services into an organized, failure-manageable, and easily monitored workflow.
* **Asynchronous System Building:** Capable of designing application architectures using these integration services to enhance flexibility and scalability.

---