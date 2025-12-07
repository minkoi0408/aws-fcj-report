---
title: "Worklog Tuần 9"
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu Tuần 9:

* **Kinesis Fundamentals:** Hiểu rõ kiến trúc và vai trò của dịch vụ xử lý dữ liệu truyền tải **Amazon Kinesis** (Data Streams, Firehose).
* **Quản lý Dữ liệu:** Nắm vững các khái niệm về **AWS Glue** (Data Catalog, Crawler, ETL Jobs) trong quy trình ETL (Extract, Transform, Load).
* **Metadata Catalog:** Thành thạo việc tạo và quản lý **Glue Data Catalog** để lưu trữ Metadata về dữ liệu.
* **Tích hợp Data Pipeline:** Thực hành kết nối Kinesis Firehose để truyền tải dữ liệu Stream vào S3.

### Kế hoạch Triển khai trong Tuần:

| Thứ | Hoạt động Trọng tâm | Ngày Bắt đầu | Ngày Hoàn thành | Tài liệu Tham khảo |
| :-- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :----------- | :-------------- | :---------------------------------------- |
| **Hai** | * Đọc và hiểu kiến trúc **Amazon Kinesis Data Streams (KDS)** (Shard, Producer, Consumer). <br> * Tìm hiểu về **Amazon Kinesis Data Firehose** để đơn giản hóa việc nạp dữ liệu. <br> * **Thực hành:** Tạo một Kinesis Data Firehose Delivery Stream. | 03/11/2025 | 03/11/2025 | <https://cloudjourney.awsstudygroup.com/> |
| **Ba** | * Tìm hiểu về **AWS Glue Data Catalog** (Kho lưu trữ Metadata) và **Glue Crawler**. <br> * **Thực hành:** <br>&emsp; + Tạo một IAM Role cho Glue Crawler. <br>&emsp; + Tạo Glue Crawler để quét dữ liệu mẫu trong S3 Bucket (từ tuần 4) và cập nhật Data Catalog. | 04/11/2025 | 04/11/2025 | <https://cloudjourney.awsstudygroup.com/> |
| **Tư** | * Tìm hiểu về **AWS Glue ETL Jobs** (Extract, Transform, Load) và môi trường thực thi (Spark, Python Shell). <br> * **Thực hành:** <br>&emsp; + Tạo một Glue ETL Job cơ bản (sử dụng Python Shell). <br>&emsp; + Cấu hình Job để đọc dữ liệu từ Data Catalog và ghi kết quả ra S3. | 05/11/2025 | 05/11/2025 | <https://cloudjourney.awsstudygroup.com/> |
| **Năm** | * **Thực hành Tích hợp Kinesis:** <br> * **Thực hành:** <br>&emsp; + Định cấu hình Kinesis Firehose Delivery Stream đã tạo để đích đến là S3. <br>&emsp; + Mô phỏng việc nạp dữ liệu (data ingestion) vào Firehose và kiểm tra xem dữ liệu có được lưu trữ trên S3 hay không. | 06/11/2025 | 06/11/2025 | <https://cloudjourney.awsstudygroup.com/> |
| **Sáu** | * **Dọn dẹp Tài nguyên & Ôn tập:** <br> * **Thực hành:** <br>&emsp; + Xóa Glue Job, Glue Crawler, và các bảng trong Data Catalog. <br>&emsp; + Xóa Kinesis Data Firehose Delivery Stream. <br>&emsp; + Tổng kết vai trò của Kinesis (Tốc độ, Real-time) và Glue (Xử lý Batch/ETL). | 07/11/2025 | 07/11/2025 | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả Đạt được Tuần 9:

* **Xử lý Streaming:** Hiểu được cơ chế truyền tải dữ liệu theo thời gian thực (real-time) với Kinesis và cách Firehose đơn giản hóa việc nạp dữ liệu vào các đích đến (S3, Redshift).
* **Quản lý Metadata:** Thành thạo việc sử dụng **Glue Data Catalog** và **Crawler** để khám phá (discover) và quản lý Metadata (Schema) cho dữ liệu trong S3.
* **ETL Cơ bản:** Nắm được quy trình Extract, Transform, Load (ETL) và đã thực hành tạo **Glue ETL Job** để xử lý dữ liệu.
* **Tích hợp:** Thực hành thành công việc truyền dữ liệu từ nguồn (Firehose) đến đích (S3) và xử lý dữ liệu thô.
* **Khái niệm Big Data:** Phân biệt được các dịch vụ phù hợp cho phân tích dữ liệu Batch (Glue) và Streaming (Kinesis) trong một kiến trúc dữ liệu hiện đại.

---