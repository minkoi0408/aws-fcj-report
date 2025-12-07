---
title: "Worklog Tuần 4"
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu Tuần 4:

* **S3 Cơ bản:** Hiểu rõ vai trò, kiến trúc và tính bền vững (Durability) của dịch vụ **Amazon S3** (Simple Storage Service).
* **Quản lý Bucket & Bảo mật:** Thành thạo việc tạo, quản lý **Bucket**, và áp dụng các chính sách bảo mật như **Bucket Policy**.
* **Tối ưu Lưu trữ:** Nắm vững các lớp lưu trữ của S3 (**Standard, IA, Glacier**) và cách sử dụng **Lifecycle Rules** để tự động tối ưu chi phí.
* **Ứng dụng:** Thực hành triển khai một trang web tĩnh (**Static Website Hosting**) trên S3.

### Kế hoạch Triển khai trong Tuần:

| Thứ | Hoạt động Trọng tâm | Ngày Bắt đầu | Ngày Hoàn thành | Tài liệu Tham khảo |
| :-- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :----------- | :-------------- | :---------------------------------------- |
| **Hai** | * Đọc và hiểu kiến trúc cơ bản của **Amazon S3** (Object, Key, Bucket, Region). <br> * Tìm hiểu các tính năng bảo mật: Block Public Access, Access Control List (ACL). <br> * **Thực hành:** Tạo S3 Bucket mới và tùy chỉnh cài đặt Block Public Access. | 29/09/2025 | 29/09/2025 | <https://cloudjourney.awsstudygroup.com/> |
| **Ba** | * Tìm hiểu về các **Lớp Lưu Trữ (Storage Classes)** của S3 (Standard, Standard-IA, One Zone-IA, Glacier, Deep Archive). <br> * Tìm hiểu về **Lifecycle Rules** để chuyển đổi tự động giữa các lớp lưu trữ. <br> * **Thực hành:** Cấu hình Lifecycle Rule cho Bucket, chuyển đổi đối tượng cũ sang Standard-IA. | 30/09/2025 | 30/09/2025 | <https://cloudjourney.awsstudygroup.com/> |
| **Tư** | * Tìm hiểu về tính năng **Versioning** (Quản lý phiên bản) và quy trình khôi phục đối tượng. <br> * Tìm hiểu về **Bucket Policy** để quản lý quyền truy cập tập trung. <br> * **Thực hành:** Bật Versioning cho Bucket và thử xóa/khôi phục một đối tượng. | 01/10/2025 | 01/10/2025 | <https://cloudjourney.awsstudygroup.com/> |
| **Năm** | * Tìm hiểu về tính năng **Static Website Hosting** trên S3. <br> * **Thực hành:** <br>&emsp; + Tải lên file HTML/CSS/JS (Index.html & Error.html). <br>&emsp; + Bật Static Website Hosting và thiết lập Bucket Policy cho phép truy cập công cộng. <br>&emsp; + Truy cập trang web thông qua Endpoint công cộng của S3. | 02/10/2025 | 02/10/2025 | <https://cloudjourney.awsstudygroup.com/> |
| **Sáu** | * **Dọn dẹp và Ôn tập S3 CLI:** <br> * **Thực hành:** <br>&emsp; + Dùng **AWS CLI** để upload/download/sync dữ liệu với S3 (`aws s3 cp`, `aws s3 sync`). <br>&emsp; + **Dọn dẹp tài nguyên:** Tắt Versioning, xóa tất cả các đối tượng (bao gồm các phiên bản cũ), sau đó xóa Bucket. | 03/10/2025 | 03/10/2025 | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả Đạt được Tuần 4:

* **Quản lý S3 Toàn diện:** Đã hiểu rõ và tự tay tạo, cấu hình, và quản lý các S3 Bucket. Nắm được vai trò của **Block Public Access** và **ACL**.
* **Tối ưu Chi phí Lưu trữ:** Nắm vững các **Storage Classes** của S3 và biết cách sử dụng **Lifecycle Rules** để tự động chuyển dữ liệu sang các lớp lưu trữ ít tốn kém hơn theo thời gian.
* **Bảo mật & Quản lý Dữ liệu:** Thực hành thành công việc bật/tắt **Versioning** và áp dụng **Bucket Policy** để kiểm soát quyền truy cập công cộng và của IAM User.
* **Ứng dụng Thực tế:** Triển khai thành công một trang web tĩnh trên S3 và truy cập được qua Endpoint công cộng.
* **Thao tác CLI:** Thành thạo sử dụng AWS CLI để quản lý dữ liệu trên S3 (upload, download, sync) một cách hiệu quả.