---
title: "Translated Blogs"
weight: 3
chapter: false
pre: " <b> 3. </b> "
---

{{% notice warning %}}
⚠️ **Note:** The information below is for reference purposes only. Please **do not copy verbatim** for your report, including this warning.
{{% /notice %}}

This section will list and introduce the blogs you have translated. For example:

### [Blog 1 - IoT Weather Platform for Lab Research](3.1-Blog1/)
This proposal outlines the **IoT Weather Platform** designed for the ITea Lab team to collect and analyze real-time weather data. The solution uses **Raspberry Pi/ESP32** edge devices to transmit data via **MQTT** to **AWS IoT Core**. The platform leverages **AWS Serverless** services, including S3 (Data Lake), **AWS Glue (ETL)**, and an **Amplify/Next.js** web interface, secured by **Amazon Cognito**. The goal is to provide centralized monitoring, predictive analytics, and high cost efficiency (estimated at $0.7/month).

### [Blog 2 - Enhancing Pinterest's organizational security with a DNS firewall: Part 1](3.2-Blog2/)
This blog introduces **Pinterest's** approach to enhancing organizational security using a DNS Firewall, **Part 1**. It details why **DNS traffic visibility** is crucial for preventing data exfiltration, and how **Route 53 Resolver Query Logs** are collected and **analyzed using Python** to construct authoritative domain **Allowlists**. The article guides the steps to **establish the foundation for the "Walled Garden" strategy** and effectively control outbound (egress) network traffic.

### [Blog 3 - Detecting Exceptional Traffic using CloudWatch Alarms and Lambda](3.3-Blog3/)
This blog instructs on how to automatically **monitor applications** and detect **exceptional traffic/anomalies**. You will learn why **CloudWatch Alarms** are important for real-time metric tracking, and how the **Anomaly Detection** feature, powered by ML, helps set flexible alerting thresholds. An **AWS Lambda** function is used as the action target to perform **automated responses** when an alarm triggers, such as sending enhanced notifications or gathering diagnostic data to reduce MTTR.

