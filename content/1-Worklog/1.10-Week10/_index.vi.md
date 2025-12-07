---
title: "Worklog Tuần 10"
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu Tuần 10:

* **Hàng đợi Tin nhắn:** Hiểu rõ vai trò và cách thức hoạt động của dịch vụ hàng đợi tin nhắn **Amazon Simple Queue Service (SQS)** (Standard & FIFO).
* **Mô hình Pub/Sub:** Nắm vững kiến trúc **Publish/Subscribe** với dịch vụ thông báo **Amazon Simple Notification Service (SNS)**.
* **Điều phối Luồng công việc:** Thành thạo việc tạo và cấu hình các máy trạng thái **AWS Step Functions** để điều phối các dịch vụ AWS.
* **Thực hành Tích hợp:** Xây dựng một quy trình làm việc phi đồng bộ sử dụng SQS, SNS và Lambda.

### Kế hoạch Triển khai trong Tuần:

| Thứ | Hoạt động Trọng tâm | Ngày Bắt đầu | Ngày Hoàn thành | Tài liệu Tham khảo |
| :-- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :----------- | :-------------- | :---------------------------------------- |
| **Hai** | * Đọc và hiểu kiến trúc **Amazon SQS** (Hàng đợi tin nhắn) và sự khác biệt giữa Standard Queue và FIFO Queue. <br> * **Thực hành:** Tạo một SQS Standard Queue, gửi và nhận tin nhắn thủ công qua Console. | 10/11/2025 | 10/11/2025 | <https://cloudjourney.awsstudygroup.com/> |
| **Ba** | * Tìm hiểu về dịch vụ thông báo **Amazon SNS** (Topic, Subscriber) và mô hình Pub/Sub. <br> * **Thực hành:** <br>&emsp; + Tạo một SNS Topic. <br>&emsp; + Tạo SQS Queue và hàm Lambda (từ tuần 8) làm Subscriber cho Topic. <br>&emsp; + Gửi tin nhắn đến Topic và kiểm tra sự phân phối đến các Subscriber. | 11/11/2025 | 11/11/2025 | <https://cloudjourney.awsstudygroup.com/> |
| **Tư** | * Tìm hiểu về **AWS Step Functions** (State Machine, Task State, Choice State). <br> * **Thực hành:** <br>&emsp; + Tạo một hàm Lambda mới (ví dụ: `ProcessStep1`). <br>&emsp; + Tạo một State Machine đơn giản (chỉ có một bước Task) để điều phối và gọi hàm Lambda này. | 12/11/2025 | 12/11/2025 | <https://cloudjourney.awsstudygroup.com/> |
| **Năm** | * Tìm hiểu về cách **Step Functions** điều phối luồng logic phức tạp (Sequence, Choice, Parallel). <br> * **Thực hành:** Mở rộng State Machine đã tạo: <br>&emsp; + Thêm một bước `Choice` dựa trên kết quả đầu vào. <br>&emsp; + Tích hợp SQS (ví dụ: gửi tin nhắn vào hàng đợi nếu luồng đi theo một nhánh nhất định). | 13/11/2025 | 13/11/2025 | <https://cloudjourney.awsstudygroup.com/> |
| **Sáu** | * **Dọn dẹp Tài nguyên & Tích hợp Tổng quan:** <br> * **Thực hành:** <br>&emsp; + Xóa State Machine, SQS Queue, SNS Topic. <br>&emsp; + Ôn tập về cách các dịch vụ này (SQS, SNS, Step Functions) giải quyết vấn đề giao tiếp phi đồng bộ và decoupling (tách rời) trong kiến trúc ứng dụng. | 14/11/2025 | 14/11/2025 | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả Đạt được Tuần 10:

* **Hàng đợi tin nhắn:** Hiểu rõ vai trò của SQS trong việc **decoupling** và **làm mềm tải** (buffering) ứng dụng. Thành thạo việc gửi/nhận tin nhắn qua SQS.
* **Mô hình Pub/Sub:** Nắm được cơ chế **SNS** để phân phối tin nhắn tới nhiều người đăng ký (Subscriber) một cách hiệu quả và đáng tin cậy.
* **Điều phối Luồng công việc:** Hiểu rõ cách **Step Functions** giúp điều phối các dịch vụ AWS khác thành một quy trình làm việc có tổ chức, có khả năng quản lý lỗi và dễ giám sát.
* **Xây dựng Hệ thống Phi đồng bộ:** Có khả năng thiết kế kiến trúc ứng dụng sử dụng các dịch vụ tích hợp này để tăng tính linh hoạt và khả năng mở rộng.