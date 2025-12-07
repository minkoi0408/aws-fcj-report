weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu Tuần 6:

* **NoSQL Cơ bản:** Hiểu rõ kiến trúc và ưu điểm của cơ sở dữ liệu NoSQL **Amazon DynamoDB** (Key-Value/Document).
* **Quản lý DynamoDB:** Thành thạo việc tạo, quản lý bảng DynamoDB và sử dụng các loại Index (**GSI/LSI**).
* **Vai trò Caching:** Nắm vững vai trò của **Amazon ElastiCache** trong việc tăng tốc độ phản hồi ứng dụng.
* **Thực hành Caching:** Thực hành tạo và cấu hình Cluster ElastiCache (Redis/Memcached).

### Kế hoạch Triển khai trong Tuần:

| Thứ | Hoạt động Trọng tâm | Ngày Bắt đầu | Ngày Hoàn thành | Tài liệu Tham khảo |
| :-- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :----------- | :-------------- | :---------------------------------------- |
| **Hai** | * Đọc và hiểu kiến trúc **Amazon DynamoDB** (Primary Key, Partition Key, Sort Key). <br> * Tìm hiểu các khái niệm về Read/Write Capacity Units (RCU/WCU) và chế độ On-Demand. <br> * **Thực hành:** Tạo bảng DynamoDB đầu tiên, chèn và truy vấn dữ liệu cơ bản. | 13/10/2025 | 13/10/2025 | <https://cloudjourney.awsstudygroup.com/> |
| **Ba** | * Tìm hiểu chuyên sâu về các loại Index: **Local Secondary Index (LSI)** và **Global Secondary Index (GSI)**. <br> * **Thực hành:** Tạo GSI cho bảng DynamoDB để hỗ trợ các truy vấn không dựa trên khóa chính (non-key attributes). | 14/10/2025 | 14/10/2025 | <https://cloudjourney.awsstudygroup.com/> |
| **Tư** | * Tìm hiểu về dịch vụ bộ nhớ đệm **Amazon ElastiCache** (Redis và Memcached). <br> * Phân tích lợi ích của việc sử dụng caching layer để giảm tải cho RDS/DynamoDB. <br> * **Thực hành:** Khởi tạo một Cluster ElastiCache (ví dụ: Redis) trong Private Subnet. | 15/10/2025 | 15/10/2025 | <https://cloudjourney.awsstudygroup.com/> |
| **Năm** | * Tìm hiểu về cách **cấu hình Security Group** cho ElastiCache để đảm bảo kết nối an toàn từ EC2. <br> * Tìm hiểu cách ứng dụng kết nối và thao tác dữ liệu cơ bản trên ElastiCache. <br> * **Thực hành:** Cấu hình Security Group cho ElastiCache Cluster. | 16/10/2025 | 16/10/2025 | <https://cloudjourney.awsstudygroup.com/> |
| **Sáu** | * **Dọn dẹp Tài nguyên & Tổng kết Kiến thức:** <br> * **Thực hành:** <br>&emsp; + Xóa bảng DynamoDB đã tạo. <br>&emsp; + Xóa ElastiCache Cluster. <br>&emsp; + Tổng kết ưu nhược điểm và Use-case của RDS, DynamoDB, và ElastiCache. | 17/10/2025 | 17/10/2025 | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả Đạt được Tuần 6:

* **DynamoDB Nền tảng:** Hiểu rõ mô hình NoSQL của DynamoDB, thành thạo việc tạo, quản lý bảng (table) và các loại khóa chính.
* **Tối ưu Truy vấn & Chi phí:** Nắm được vai trò của **GSI/LSI** và các chế độ cấp dung lượng (On-Demand/Provisioned) trong DynamoDB.
* **ElastiCache Kiến trúc:** Hiểu được sự khác biệt và lợi ích của Redis/Memcached. Nắm được vai trò của bộ nhớ đệm (caching layer) trong kiến trúc ứng dụng.
* **Triển khai Caching:** Khởi tạo thành công ElastiCache Cluster và thiết lập bảo mật mạng thông qua Security Group.
* **Phân biệt Dịch vụ:** Có khả năng so sánh và lựa chọn giữa RDS, DynamoDB và ElastiCache cho các yêu cầu dữ liệu và hiệu suất khác nhau.