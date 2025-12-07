---
title: "Blog 1: Evolving the Healthcare Data Lake with Microservices"
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

# Getting Started with Healthcare Data Lakes: Using Microservices

A **data lake** is a centralized, secure repository that stores all data (raw and processed) for analysis, helping healthcare providers break down silos, gain business insights, and protect patient privacy. This post details the architectural evolution of a healthcare data lake solution toward a **microservices-based approach**.

---

## Architecture Guidance: From Monolith to Microservices

The primary design shift involved decomposing a single service into smaller, specialized **microservices**. This was done to enhance maintainability and flexibility, especially when integrating diverse healthcare data formats (like HL7v2). Connectors are now encapsulated separately, allowing independent modification. The microservices are **loosely coupled** via a publish/subscribe model centered around a "pub/sub hub."

[Image of Microservices Architecture communicating through a Message Broker]


The current scope focuses on the ingestion and basic parsing of **HL7v2 messages** formatted in **Encoding Rules 7 (ER7)** through a REST interface.

> The microservices approach ensures reusability and autonomy, specializing each service to do one thing well, often implemented using an **event-driven architecture**.

---

## Microservice Boundary Decisions

Boundaries for microservices were drawn based on intrinsic, extrinsic, and human factors:

| Category | Consideration Examples |
| :--- | :--- |
| **Intrinsic** | Technology stack, performance requirements, scalability needs |
| **Extrinsic** | Dependent functionality, rate of change, potential for reuse |
| **Human** | Team ownership, managing *cognitive load* across development teams |

---

## Technology Choices and Communication Scope

Key technologies considered for inter-service communication:

| Communication scope | Technologies / patterns used |
| :--- | :--- |
| **Within a microservice** | Amazon Simple Queue Service (Amazon SQS), AWS Step Functions |
| **Between microservices** (Single service) | AWS CloudFormation cross-stack references, Amazon Simple Notification Service (Amazon SNS) |
| **Between services** (Organizational) | Amazon EventBridge, AWS Cloud Map, Amazon API Gateway |

---

## The Pub/Sub Hub and Asynchronous Communication

A **hub-and-spoke** architecture using a message broker (the Pub/Sub Hub) is ideal for a small number of tightly related microservices. This design:
* Reduces coupling, as each microservice depends only on the hub.
* Limits inter-microservice connections to the message content.
* Reduces synchronous calls since the pub/sub model is an asynchronous *push*.

> **Drawback:** Requires robust **coordination and monitoring** to prevent services from incorrectly processing messages not intended for them.

---

## Core Microservices Implementation

### 1. Core Microservice
This service provides the foundational data and communication layer:
* **Data Storage:** Uses **Amazon S3** for the data lake and **Amazon DynamoDB** for the data catalog.
* **Ingestion Logic:** **AWS Lambda** functions are responsible for writing messages into the data lake and catalog.
* **Communication Hub:** An **Amazon SNS** topic acts as the central *hub*.

### 2. Front Door Microservice
This layer handles external interaction and security:
* Provides an **API Gateway** for external REST interaction.
* **Authentication/Authorization:** Managed via **OIDC** using **Amazon Cognito**.
* **Deduplication:** A self-managed deduplication mechanism using **DynamoDB** is implemented instead of relying on SNS FIFO limitations (5-minute TTL, mandatory SQS FIFO).

### 3. Staging ER7 Microservice
Responsible for data format conversion:
* A Lambda "trigger" subscribes to the pub/sub hub, using **attribute filtering**.
* Uses a **Step Functions Express Workflow** to execute the conversion logic (**ER7 → JSON**).
* The workflow uses two Lambdas: one for fixing ER7 formatting (newlines) and one for parsing logic.
* Results (or errors) are pushed back into the pub/sub hub for downstream processing.

---

## New Features and Security Enhancements

### 1. AWS CloudFormation Cross-Stack References
This feature enables logical separation and reusability by allowing different CloudFormation stacks (e.g., Front Door) to securely reference and consume resources (like the SNS Topic or S3 Bucket) created and **Exported** by the Core Microservice stack.

Example *outputs* in the core microservice:
```yaml
Outputs:
  Bucket:
    Value: !Ref Bucket
    Export:
      Name: !Sub ${AWS::StackName}-Bucket
...