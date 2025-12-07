---
title: "Worklog Tuần 2"
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu Tuần 2:

* **EC2 Chuyên Sâu:** Hiểu rõ vai trò và cơ chế hoạt động của dịch vụ máy chủ ảo **EC2** (Elastic Compute Cloud).
* **Quản lý Vòng đời:** Thành thạo quy trình khởi tạo, quản lý và chấm dứt (Terminate) một EC2 Instance.
* **Kiểm soát Truy cập An toàn:** Nắm vững khái niệm và cách triển khai **IAM Roles** để cấp quyền truy cập dịch vụ AWS một cách bảo mật cho tài nguyên EC2.
* **Vận hành CLI:** Sử dụng thành thạo **AWS CLI** để thực hiện các thao tác quản lý EC2 cơ bản.

### Kế hoạch Triển khai trong Tuần:

| Thứ | Hoạt động Trọng tâm | Ngày Bắt đầu | Ngày Hoàn thành | Tài liệu Tham khảo |
| :-- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :----------- | :-------------- | :---------------------------------------- |
| **Hai** | * Đọc và hiểu các thành phần cốt lõi của **Amazon EC2** (AMI, Instance Type, Key Pair, Security Group). <br> * **Thực hành:** Khởi tạo Instance EC2 đầu tiên (chọn loại Free Tier). | 15/09/2025 | 15/09/2025 | <https://cloudjourney.awsstudygroup.com/> |
| **Ba** | * Tìm hiểu cơ chế cấp quyền an toàn **IAM Roles for EC2** (Instance Profiles). <br> * **Thực hành:** <br>&emsp; + Tạo IAM Policy cho phép `s3:ListBucket`. <br>&emsp; + Tạo IAM Role và gán Policy. <br>&emsp; + Gán Role vừa tạo cho Instance EC2. | 16/09/2025 | 16/09/2025 | <https://cloudjourney.awsstudygroup.com/> |
| **Tư** | * Khám phá các lệnh quản lý dịch vụ **EC2 với AWS CLI**. <br> * **Thực hành:** <br>&emsp; + Dùng CLI để xem thông tin EC2 Instance (`describe-instances`). <br>&emsp; + Dùng CLI để Stop/Start Instance. <br>&emsp; + Quản lý Security Group thông qua CLI. | 17/09/2025 | 17/09/2025 | <https://cloudjourney.awsstudygroup.com/> |
| **Năm** | * **Thực hành Tích Hợp:** Xác thực quyền hạn của IAM Role. <br> * Đăng nhập SSH/Session Manager vào Instance EC2. <br> * **Thực hành:** Dùng lệnh `aws s3 ls` (CLI) từ bên trong EC2 để kiểm tra khả năng đọc (list) các S3 Bucket (chứng minh IAM Role hoạt động). | 18/09/2025 | 18/09/2025 | <https://cloudjourney.awsstudygroup.com/> |
| **Sáu** | * **Quản lý Vòng đời & Chi phí:** <br> * Ôn tập các trạng thái vòng đời của EC2 (Pending, Running, Stopping, Terminated). <br> * **Thực hành:** <br>&emsp; + **Terminate** (Chấm dứt) Instance EC2. <br>&emsp; + Xóa IAM Role, Policy đã tạo để dọn dẹp tài nguyên. | 19/09/2025 | 19/09/2025 | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả Đạt được Tuần 2:

* **EC2 Nâng Cao:** Đã nắm được cách tạo, cấu hình và quản lý vòng đời đầy đủ của máy ảo EC2 thông qua Console và CLI. Hiểu rõ các thành phần cấu tạo nên một EC2 instance.
* **IAM Roles cho Bảo mật:** Hiểu rõ ưu điểm và cách dùng **IAM Role** (Instance Profile) để cấp quyền truy cập dịch vụ AWS một cách bảo mật cho EC2, loại bỏ nhu cầu lưu trữ Access Key tĩnh trên máy chủ.
* **AWS CLI Chuyên Sâu:** Đã biết cách sử dụng các lệnh CLI để quản lý trạng thái của EC2 Instance (Start, Stop, Describe) và thực hiện các thao tác từ xa hiệu quả.
* **Xác thực Tích Hợp:** Đã chứng minh thành công việc EC2 Instance có thể thực thi các hành động trên S3 (ví dụ: `aws s3 ls`) nhờ vào quyền được cấp qua IAM Role, xác nhận mô hình bảo mật hoạt động chính xác.
* **Tối ưu Chi phí:** Nắm vững quy trình chấm dứt EC2 Instance và dọn dẹp các tài nguyên IAM liên quan để đảm bảo không phát sinh chi phí không cần thiết.