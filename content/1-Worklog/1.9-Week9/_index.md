
---
title: "Worklog Week 9"
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Week 9 Objectives:

* **Kinesis Fundamentals:** Clearly understand the architecture and role of the **Amazon Kinesis** streaming data service (Data Streams, Firehose).
* **Data Management:** Master the concepts of **AWS Glue** (Data Catalog, Crawler, ETL Jobs) within the ETL (Extract, Transform, Load) workflow.
* **Metadata Catalog:** Be proficient in creating and managing the **Glue Data Catalog** to store data Metadata.
* **Data Pipeline Integration:** Practice connecting Kinesis Firehose to stream data into S3.

### Planned Tasks for the Week:

| Day | Task/Activity Focus | Start Date | Completion Date | Resource Material |
| :-- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :----------- | :-------------- | :---------------------------------------- |
| **Mon** | * Review and comprehend **Amazon Kinesis Data Streams (KDS)** architecture (Shard, Producer, Consumer). <br> * Learn about **Amazon Kinesis Data Firehose** to simplify data ingestion. <br> * **Hands-on Practice:** Create a Kinesis Data Firehose Delivery Stream. | 03/11/2025 | 03/11/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Tue** | * Study the **AWS Glue Data Catalog** (Metadata Repository) and **Glue Crawler**. <br> * **Hands-on Practice:** <br>&emsp; + Create an IAM Role for the Glue Crawler. <br>&emsp; + Create a Glue Crawler to scan sample data in an S3 Bucket (from Week 4) and update the Data Catalog. | 04/11/2025 | 04/11/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Wed** | * Learn about **AWS Glue ETL Jobs** (Extract, Transform, Load) and execution environments (Spark, Python Shell). <br> * **Hands-on Practice:** <br>&emsp; + Create a basic Glue ETL Job (using Python Shell). <br>&emsp; + Configure the Job to read data from the Data Catalog and write results to S3. | 05/11/2025 | 05/11/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Thu** | * **Kinesis Integration Practice:** <br> * **Hands-on Practice:** <br>&emsp; + Configure the created Kinesis Firehose Delivery Stream with S3 as the destination. <br>&emsp; + Simulate data ingestion into Firehose and verify that the data is stored in S3. | 06/11/2025 | 06/11/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |
| **Fri** | * **Resource Cleanup & Review:** <br> * **Hands-on Practice:** <br>&emsp; + Delete the Glue Job, Glue Crawler, and tables in the Data Catalog. <br>&emsp; + Delete the Kinesis Data Firehose Delivery Stream. <br>&emsp; + Summarize the roles of Kinesis (Speed, Real-time) and Glue (Batch Processing/ETL). | 07/11/2025 | 07/11/2025 | [https://cloudjourney.awsstudygroup.com/](https://cloudjourney.awsstudygroup.com/) |

### Week 9 Achievements:

* **Streaming Processing:** Understood the mechanism of real-time data transmission with Kinesis and how Firehose simplifies data ingestion into destinations (S3, Redshift).
* **Metadata Management:** Proficient in using the **Glue Data Catalog** and **Crawler** to discover and manage Metadata (Schema) for data stored in S3.
* **Basic ETL:** Grasped the Extract, Transform, Load (ETL) workflow and practiced creating **Glue ETL Jobs** for data processing.
* **Integration:** Successfully practiced transmitting data from a source (Firehose) to a destination (S3) and processing the raw data.
* **Big Data Concepts:** Able to differentiate between services suitable for Batch processing (Glue) and Streaming analysis (Kinesis) in a modern data architecture.

---