---
title: "Worklog Tuần 5"
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu Tuần 5:

* **Vai trò của RDS:** Hiểu rõ vai trò và lợi ích vượt trội của dịch vụ **Amazon RDS** so với việc tự quản lý cơ sở dữ liệu trên EC2.
* **Vận hành Cơ bản:** Thành thạo việc tạo và kết nối đến một DB Instance (ví dụ: MySQL hoặc PostgreSQL).
* **Tính năng Cốt lõi:** Nắm vững các tính năng quan trọng: **Multi-AZ** (Tính sẵn sàng cao), **Read Replicas** (Mở rộng khả năng đọc), và **Snapshot/Backup**.
* **Bảo mật Mạng:** Thực hành quản lý bảo mật mạng cho DB Instance thông qua Security Group.

### Kế hoạch Triển khai trong Tuần:

| Thứ | Hoạt động Trọng tâm | Ngày Bắt đầu | Ngày Hoàn thành | Tài liệu Tham khảo |
| :-- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | :----------- | :-------------- | :---------------------------------------- |
| **Hai** | * Đọc và hiểu kiến trúc của **Amazon RDS** (DB Instance, Engine, Master Username/Password, DB Security Group). <br> * So sánh RDS với cơ sở dữ liệu trên EC2 (tự quản lý). <br> * **Thực hành:** Khởi tạo DB Instance (chọn Free Tier) trong VPC đã tạo (chọn Private Subnet). | 06/10/2025 | 06/10/2025 | <https://cloudjourney.awsstudygroup.com/> |
| **Ba** | * Tìm hiểu về cách kết nối và bảo mật mạng cho RDS. <br> * **Thực hành:** <br>&emsp; + Cấu hình **Security Group** cho RDS chỉ cho phép truy cập từ **Security Group của EC2 Instance**. <br>&emsp; + Dùng công cụ Client hoặc EC2 để kết nối và tạo một bảng cơ bản. | 07/10/2025 | 07/10/2025 | <https://cloudjourney.awsstudygroup.com/> |
| **Tư** | * Tìm hiểu về tính năng **Multi-AZ Deployment** (Đa vùng sẵn sàng) để đảm bảo High Availability (HA). <br> * Tìm hiểu về **Automated Backups** và **DB Snapshots** (Sao lưu thủ công). <br> * **Thực hành:** Bật Multi-AZ cho Instance và tạo một DB Snapshot thủ công. | 08/10/2025 | 08/10/2025 | <https://cloudjourney.awsstudygroup.com/> |
| **Năm** | * Tìm hiểu về **Read Replicas** để mở rộng khả năng đọc và giảm tải cho DB Master. <br> * **Thực hành:** <br>&emsp; + Tạo một Read Replica cho DB Instance chính. <br>&emsp; + Mô phỏng việc kết nối ứng dụng đến Read Replica để mở rộng khả năng đọc. <br>&emsp; + Nghiên cứu về việc Promote Read Replica thành Standalone DB. | 09/10/2025 | 09/10/2025 | <https://cloudjourney.awsstudygroup.com/> |
| **Sáu** | * **Dọn dẹp & Tối ưu Chi phí:** <br> * **Thực hành:** <br>&emsp; + Xóa Read Replica. <br>&emsp; + Xóa DB Instance chính (Lưu ý: Bỏ chọn tạo Final Snapshot nếu không cần thiết). <br>&emsp; + Dọn dẹp tất cả các Snapshot và Security Group liên quan. | 10/10/2025 | 10/10/2025 | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả Đạt được Tuần 5:

* **Quản lý RDS:** Đã hiểu rõ lợi ích của RDS và thành thạo việc tạo, cấu hình, và kết nối đến DB Instance.
* **Bảo mật Kết nối:** Nắm vững cách sử dụng Security Group để chỉ cho phép các tài nguyên cụ thể (như EC2) truy cập vào cơ sở dữ liệu, đảm bảo bảo mật lớp mạng chặt chẽ.
* **Tính sẵn sàng cao (HA):** Hiểu và thực hành thành công việc triển khai **Multi-AZ** để bảo vệ cơ sở dữ liệu khỏi sự cố vùng sẵn sàng (AZ Failure).
* **Khả năng mở rộng:** Hiểu và thực hành việc tạo **Read Replicas** để tối ưu hiệu suất đọc và giảm tải cho DB Master.
* **Sao lưu & Phục hồi:** Nắm được quy trình tạo **DB Snapshot** và cách RDS tự động thực hiện **Automated Backups** để khôi phục dữ liệu.