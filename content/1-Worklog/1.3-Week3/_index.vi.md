---
title: "Worklog Tuần 3"
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu Tuần 3:

* **Kiến trúc VPC:** Hiểu rõ vai trò và các thành phần cốt lõi của dịch vụ mạng ảo **Amazon Virtual Private Cloud (VPC)**.
* **Cấu hình Mạng:** Thành thạo việc tạo, cấu hình VPC, Subnet (Public/Private), Internet Gateway (IGW) và Route Table.
* **Bảo mật Đa lớp:** Nắm vững cơ chế bảo mật hai lớp: **Security Group (SG)** và **Network Access Control List (NACL)**.
* **Thực hành Triển khai:** Triển khai thành công một EC2 Instance vào một VPC tùy chỉnh.

### Kế hoạch Triển khai trong Tuần:

| Thứ | Hoạt động Trọng tâm | Ngày Bắt đầu | Ngày Hoàn thành | Tài liệu Tham khảo |
| :-- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :----------- | :-------------- | :---------------------------------------- |
| **Hai** | * Đọc và hiểu kiến trúc của **VPC**: Khái niệm về IP, CIDR Block, Subnet, Availability Zone (AZ). <br> * **Thực hành:** Tạo một VPC mới với dải CIDR tùy chỉnh (ví dụ: `10.0.0.0/16`). <br> * Tạo hai Subnet: một Public và một Private. | 22/09/2025 | 22/09/2025 | <https://cloudjourney.awsstudygroup.com/> |
| **Ba** | * Tìm hiểu về **Internet Gateway (IGW)**, **Route Table** và vai trò trong việc cung cấp truy cập Internet. <br> * **Thực hành:** <br>&emsp; + Tạo và đính kèm IGW vào VPC. <br>&emsp; + Cấu hình **Route Table Public** để định tuyến traffic ra IGW. <br>&emsp; + Liên kết Route Table Public với Public Subnet. | 23/09/2025 | 23/09/2025 | <https://cloudjourney.awsstudygroup.com/> |
| **Tư** | * Tìm hiểu về cơ chế bảo mật **Security Group (SG)** (Stateful) và nguyên tắc hoạt động. <br> * **Thực hành:** <br>&emsp; + Khởi tạo một EC2 Instance trong Public Subnet. <br>&emsp; + Cấu hình SG chỉ cho phép SSH/RDP (Port 22/3389) từ IP cá nhân. <br>&emsp; + Kiểm tra khả năng truy cập để xác nhận tính năng bảo mật của SG. | 24/09/2025 | 24/09/2025 | <https://cloudjourney.awsstudygroup.com/> |
| **Năm** | * Tìm hiểu về cơ chế bảo mật **Network Access Control List (NACL)** (Stateless). <br> * **Thực hành:** <br>&emsp; + Cấu hình NACL cho Public Subnet (thử nghiệm tạo rule Deny). <br>&emsp; + Phân biệt chi tiết sự khác biệt khi xử lý inbound/outbound giữa SG và NACL. <br>&emsp; + Nghiên cứu khái niệm về NAT Gateway (vai trò trong Private Subnet). | 25/09/2025 | 25/09/2025 | <https://cloudjourney.awsstudygroup.com/> |
| **Sáu** | * **Dọn dẹp & Tổng kết:** <br> * **Thực hành:** <br>&emsp; + Chấm dứt (Terminate) EC2 Instance. <br>&emsp; + **Xóa toàn bộ các thành phần VPC** theo đúng thứ tự (Detach IGW -> Xóa Subnets -> Xóa Route Tables -> Xóa VPC) để tối ưu chi phí. <br>&emsp; + Tổng kết các thành phần VPC đã học và chức năng của chúng. | 26/09/2025 | 26/09/2025 | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả Đạt được Tuần 3:

* **VPC Cấu hình Hoàn chỉnh:** Đã hiểu và tự tay tạo được VPC, Subnet (Public/Private), Internet Gateway, và Route Table để định tuyến lưu lượng truy cập mạng.
* **Bảo mật Lớp Mạng:** Nắm vững và phân biệt được cơ chế bảo mật hai lớp: **Security Group** (Stateful, hoạt động ở cấp Instance) và **NACL** (Stateless, hoạt động ở cấp Subnet).
* **Triển khai Cơ bản:** Đã triển khai thành công EC2 Instance trong VPC tùy chỉnh và xác nhận khả năng truy cập Internet.
* **Kỹ năng Dọn dẹp Tài nguyên:** Thực hiện thành công việc dọn dẹp các tài nguyên mạng theo đúng thứ tự, đảm bảo quản lý chi phí hiệu quả.