---
title: "Worklog Tuần 1"
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

### Mục tiêu Tuần 1:

* **Hội nhập:** Kết nối và làm quen với các thành viên trong chương trình First Cloud Journey (FCJ).
* **Nền tảng AWS:** Nắm vững các dịch vụ AWS cốt lõi, quy trình khởi tạo tài khoản và phương pháp quản lý chi phí hiệu quả.
* **Kỹ năng Vận hành:** Thành thạo việc sử dụng cả AWS Management Console và AWS CLI để tương tác và quản lý dịch vụ.

### Kế hoạch Triển khai trong Tuần:

| Thứ | Hoạt động Trọng tâm | Ngày Bắt đầu | Ngày Hoàn thành | Tài liệu Tham khảo |
| :--- | :--- | :--- | :--- | :--- |
| **Hai** | * Giao lưu, làm quen với các thành viên FCJ. <br> * Đọc kỹ và tuân thủ các nội quy, quy định tại đơn vị thực tập. | 08/09/2025 | 08/09/2025 | |
| **Ba** | * Nghiên cứu tổng quan về AWS và các nhóm dịch vụ cơ bản: <br> &emsp; + **Compute** (EC2) <br> &emsp; + **Storage** (S3) <br> &emsp; + **Networking** (VPC) <br> &emsp; + **Database** (RDS) | 09/09/2025 | 09/09/2025 | <https://cloudjourney.awsstudygroup.com/> |
| **Tư** | * Khởi tạo tài khoản AWS Free Tier. <br> * Tìm hiểu AWS Console & AWS CLI. <br> * **Thực hành:** <br> &emsp; + Tạo tài khoản AWS. <br> &emsp; + Quản lý Danh tính và Truy cập (IAM). <br> &emsp; + Cài đặt & cấu hình AWS CLI. <br> &emsp; + Thực hiện các thao tác quản trị cơ bản với AWS CLI. | 10/09/2025 | 10/09/2025 | <https://cloudjourney.awsstudygroup.com/> |
| **Năm** | * Tìm hiểu phương pháp quản lý chi phí hiệu quả với AWS Budget: <br> &emsp; + Cost Budget, Usage Budget, <br> &emsp; + Reservation (RI) Budget, Saving Plans Budget. <br> * **Thực hành:** <br> &emsp; + Thiết lập các loại Budget (Cost, Usage, RI, Savings Plans). <br> &emsp; + **Quy trình dọn dẹp Tài nguyên** để tối ưu chi phí. | 11/09/2025 | 11/09/2025 | <https://cloudjourney.awsstudygroup.com/> |
| **Sáu** | * Nghiên cứu dịch vụ AWS Support và các gói hỗ trợ: <br> &emsp; + Basic, Developer, Business và Enterprise. <br> * Tìm hiểu các loại yêu cầu hỗ trợ: <br> &emsp; + Hỗ trợ Tài khoản và Thanh toán. <br> &emsp; + Hỗ trợ nâng Hạn mức dịch vụ. <br> &emsp; + Hỗ trợ Kỹ thuật. <br> * **Thực hành:** <br> &emsp; + Chọn gói hỗ trợ Basic. <br> &emsp; + Tạo yêu cầu hỗ trợ mẫu. | 12/09/2025 | 12/09/2025 | <https://cloudjourney.awsstudygroup.com/> |

---

### Kết quả Đạt được Tuần 1:

* **Kiến thức AWS Nền tảng:**
  * Hiểu rõ về AWS và nắm vững chức năng của 4 nhóm dịch vụ cốt lõi:
    * **Compute:** Cung cấp tài nguyên xử lý cho ứng dụng (máy ảo, container, v.v.).
    * **Storage:** Dùng để lưu trữ dữ liệu, thực hiện sao lưu và phục hồi.
    * **Networking:** Quản lý hạ tầng mạng, bảo mật và kết nối giữa các tài nguyên.
    * **Database:** Cung cấp dịch vụ quản lý cơ sở dữ liệu quan hệ và phi quan hệ.
* **Quản lý Danh tính và Truy cập (IAM):**
  * Đã khởi tạo, cấu hình và xác thực thành công tài khoản AWS Free Tier.
  * Thành thạo việc tạo và quản lý **Group User** và **User**.
  * Hiểu cơ chế đăng nhập bằng IAM; các User trong cùng Group sẽ được dùng chung quyền được cấp.
* **Kỹ năng Vận hành (Console & CLI):**
  * Làm quen với **AWS Management Console** và biết cách tìm, truy cập, sử dụng dịch vụ qua giao diện web.
  * Hoàn tất cài đặt và cấu hình **AWS CLI** trên máy tính, bao gồm: `Access Key`, `Secret Key`, và `Region` mặc định.
  * Sử dụng AWS CLI để thực hiện các thao tác quản trị cơ bản:
    * Kiểm tra thông tin tài khoản & cấu hình.
    * Lấy danh sách Region.
    * Tạo/xóa S3 Bucket, sử dụng dịch vụ Amazon SNS.
    * Quản lý IAM (tạo group, user, thêm user).
    * Tạo/xóa Access Key.
    * Cấu hình cơ bản và quản lý vòng đời của EC2 (chạy và chấm dứt instance).
* **Quản lý Chi phí (Cost Management):**
  * Nắm được cách quản lý và giám sát chi phí trên AWS thông qua công cụ Budgets.
  * Đã tạo và cấu hình thành công các loại Budget (`Cost`, `Usage`, `RI`, `Savings Plan`).
  * Hiểu và thực hiện quy trình **dọn dẹp tài nguyên** để quản lý chi phí hiệu quả.
* **Dịch vụ Hỗ trợ (AWS Support):**
  * Hiểu rõ về các cấp độ hỗ trợ của AWS:
    * **Basic:** Miễn phí, hỗ trợ các vấn đề về tài khoản và thanh toán qua trung tâm trợ giúp.
    * **Developer:** $29/tháng, tư vấn kiến trúc cơ bản và hỗ trợ kỹ thuật không giới hạn (tạo từ Root User).
    * **Business:** $100/tháng, cung cấp chỉ dẫn theo Use-case, hỗ trợ sử dụng API, và không giới hạn yêu cầu hỗ trợ từ tất cả IAM User.
    * **Enterprise:** $15.000/tháng, đảm bảo tiêu chuẩn bảo mật nghiêm ngặt, hỗ trợ toàn diện về kiến trúc, chiến lược, tối ưu chi phí, và được ưu tiên xử lý đặc biệt.
  * Làm quen với giao diện AWS Console và sử dụng tốt các thao tác cơ bản qua cả Console và CLI.

---