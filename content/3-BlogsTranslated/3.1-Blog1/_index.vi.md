---
title: "Blog 1: Phát triển Data Lake Y tế với Microservices"
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

# Bắt Đầu với Data Lakes Y Tế: Sử Dụng Microservices

Một **data lake** (hồ dữ liệu) là một kho lưu trữ tập trung, bảo mật, lưu trữ tất cả dữ liệu (thô và đã xử lý) để phân tích, giúp các nhà cung cấp dịch vụ y tế phá vỡ các silo dữ liệu, thu thập thông tin chuyên sâu về kinh doanh và bảo vệ quyền riêng tư của bệnh nhân. Bài đăng này trình bày chi tiết sự phát triển kiến trúc của một giải pháp data lake y tế theo hướng tiếp cận dựa trên **microservices**.

---

## Hướng Dẫn Kiến Trúc: Từ Monolith sang Microservices

Sự thay đổi thiết kế chính liên quan đến việc phân tách một dịch vụ đơn lẻ thành các **microservices** nhỏ hơn, chuyên biệt. Việc này nhằm mục đích nâng cao khả năng bảo trì và tính linh hoạt, đặc biệt khi tích hợp các định dạng dữ liệu y tế đa dạng (như HL7v2). Các trình kết nối (connector) hiện được đóng gói riêng biệt, cho phép sửa đổi độc lập. Các microservices này được **liên kết lỏng lẻo** (loosely coupled) thông qua mô hình publish/subscribe xoay quanh một "trung tâm pub/sub." [Image of Microservices Architecture communicating through a Message Broker]

Phạm vi hiện tại tập trung vào việc tiếp nhận và phân tích cú pháp cơ bản các **tin nhắn HL7v2** được định dạng theo **Encoding Rules 7 (ER7)** thông qua giao diện REST.

> Tiếp cận microservices đảm bảo khả năng tái sử dụng và tính tự chủ, chuyên môn hóa mỗi dịch vụ để làm tốt một việc, thường được triển khai bằng **kiến trúc hướng sự kiện** (event-driven architecture).

---

## Quyết Định về Ranh Giới Microservice

Ranh giới cho các microservices được xác định dựa trên các yếu tố nội tại, ngoại tại và con người:

| Thể loại | Ví dụ về những điều cần cân nhắc |
| :--- | :--- |
| **Nội tại** | Ngăn xếp công nghệ, yêu cầu hiệu suất, nhu cầu mở rộng quy mô |
| **Ngoại tại** | Chức năng phụ thuộc, tốc độ thay đổi, tiềm năng tái sử dụng |
| **Con người** | Quyền sở hữu của nhóm, quản lý *tải nhận thức* (cognitive load) giữa các nhóm phát triển |

---

## Lựa Chọn Công Nghệ và Phạm Vi Giao Tiếp

Các công nghệ chính được cân nhắc cho giao tiếp giữa các dịch vụ:

| Phạm vi Giao tiếp | Công nghệ / Pattern được sử dụng |
| :--- | :--- |
| **Trong một microservice** | Amazon Simple Queue Service (Amazon SQS), AWS Step Functions |
| **Giữa các microservice** (Một dịch vụ) | AWS CloudFormation cross-stack references, Amazon Simple Notification Service (Amazon SNS) |
| **Giữa các dịch vụ** (Cấp tổ chức) | Amazon EventBridge, AWS Cloud Map, Amazon API Gateway |

---

## Trung Tâm Pub/Sub và Giao Tiếp Bất Đồng Bộ

Kiến trúc **hub-and-spoke** sử dụng message broker (Trung tâm Pub/Sub) là lý tưởng cho một số lượng nhỏ microservices có liên quan chặt chẽ. Thiết kế này:
* Giảm sự phụ thuộc, vì mỗi microservice chỉ phụ thuộc vào trung tâm.
* Hạn chế các kết nối giữa các microservice chỉ bằng nội dung tin nhắn đã xuất bản.
* Giảm các lệnh gọi đồng bộ vì mô hình pub/sub là cơ chế *đẩy* bất đồng bộ một chiều.

> **Hạn chế:** Cần **phối hợp và giám sát** mạnh mẽ để ngăn các dịch vụ xử lý nhầm tin nhắn không dành cho chúng.

---

## Triển Khai Microservices Cốt Lõi

### 1. Core Microservice
Dịch vụ này cung cấp lớp dữ liệu và giao tiếp nền tảng:
* **Lưu trữ Dữ liệu:** Sử dụng **Amazon S3** cho data lake và **Amazon DynamoDB** cho danh mục dữ liệu.
* **Logic tiếp nhận:** Các hàm **AWS Lambda** chịu trách nhiệm ghi tin nhắn vào data lake và danh mục.
* **Trung tâm Giao tiếp:** Một topic **Amazon SNS** đóng vai trò là *trung tâm*.

### 2. Front Door Microservice
Lớp này xử lý tương tác bên ngoài và bảo mật:
* Cung cấp **API Gateway** cho tương tác REST bên ngoài.
* **Xác thực/Ủ