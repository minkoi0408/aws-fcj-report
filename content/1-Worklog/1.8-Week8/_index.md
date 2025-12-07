
---
title: "Worklog Week 8"
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Week 8 Objectives:

* **Lambda Fundamentals:** Clearly understand the architecture, advantages, and core components of the **AWS Lambda** serverless compute service.
* **Lambda Deployment:** Be proficient in creating, deploying, and managing Lambda functions.
* **API Gateway Mastery:** Master the role and configuration of **Amazon API Gateway** to create RESTful APIs.
* **Serverless Architecture:** Practice building a simple Serverless application by integrating Lambda and API Gateway.

### Planned Tasks for the Week:

| Day | Task/Activity Focus | Start Date | Completion Date | Resource Material |
| :-- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | :----------- | :-------------- | :---------------------------------------- |
| **Mon** | * Review and comprehend **AWS Lambda Architecture** (Function, Runtime, Handler, Execution Role). <br> * Compare the Serverless model (Lambda) with traditional Compute (EC2). <br> * **Hands-on Practice:** Create and deploy a simple Lambda function (e.g., printing "Hello World"). | 27/10/2025 | 27/10/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Tue** | * Learn about **Event-Driven** mechanisms in Lambda. <br> * **Hands-on Practice:** <br>&emsp; + Configure a Trigger for Lambda to be invoked by an S3 event (e.g., file upload). <br>&emsp; + Configure Lambda to read/write data from DynamoDB (using an IAM Role). | 28/10/2025 | 28/10/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Wed** | * Study the **Amazon API Gateway** service (REST API, Stage, Resource, Method). <br> * **Hands-on Practice:** Create a new REST API on API Gateway. <br> * Define basic Resources and Methods (e.g., GET /items, POST /items). | 29/10/2025 | 29/10/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Thu** | * Learn about the **Integration Type** (Lambda Proxy Integration) between API Gateway and Lambda. <br> * **Hands-on Practice:** <br>&emsp; + Connect the POST /items Method of API Gateway to the Lambda function created earlier. <br>&emsp; + Deploy the API to a Stage (e.g., `prod`) and test via the public URL. | 30/10/2025 | 30/10/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Fri** | * **Security, Monitoring & Cleanup:** <br> * Learn about CORS (Cross-Origin Resource Sharing) and how to enable it on API Gateway. <br> * **Hands-on Practice:** <br>&emsp; + Enable CORS for the API. <br>&emsp; + Review Lambda Logs on CloudWatch. <br>&emsp; + Delete the API Gateway, then delete the Lambda function. | 31/10/2025 | 31/10/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |

### Week 8 Achievements:

* **Lambda Fundamentals:** Clearly understood the Serverless model, proficient in creating, configuring, and managing Lambda functions (Function, Role, Runtime).
* **Event-Driven Architecture:** Understood how Lambda operates based on events and successfully integrated it with other services like S3 and DynamoDB.
* **API Gateway Mastery:** Mastered API Gateway architecture (Resource, Method, Stage) and the ability to create RESTful APIs.
* **Serverless Deployment:** Successfully deployed a basic Serverless architecture (**API Gateway -> Lambda -> DynamoDB**), a common AWS application pattern.
* **Security & Cleanup:** Understood how to manage Lambda Logs via CloudWatch and performed systematic cleanup of Serverless resources.

---