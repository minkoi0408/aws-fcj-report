---
title: "Các Blog Đã Dịch"
weight: 3
chapter: false
pre: " <b> 3. </b> "
---

{{% notice warning %}}
⚠️ **Lưu ý:** Thông tin dưới đây chỉ nhằm mục đích tham khảo. Vui lòng **không sao chép nguyên văn** cho báo cáo của bạn, bao gồm cả cảnh báo này.
{{% /notice %}}

Phần này sẽ liệt kê và giới thiệu các blog bạn đã dịch. Ví dụ:

### [Blog 1 - Nền tảng Thời tiết IoT cho Nghiên cứu Phòng thí nghiệm](3.1-Blog1/)
Đề xuất này phác thảo về **Nền tảng Thời tiết IoT** được thiết kế cho nhóm ITea Lab để thu thập và phân tích dữ liệu thời tiết thời gian thực. Giải pháp sử dụng các thiết bị biên **Raspberry Pi/ESP32** để truyền dữ liệu qua **MQTT** đến **AWS IoT Core**. Nền tảng tận dụng các dịch vụ **AWS Serverless**, bao gồm S3 (Data Lake), **AWS Glue (ETL)**, và giao diện web **Amplify/Next.js**, được bảo mật bởi **Amazon Cognito**. Mục tiêu là cung cấp khả năng giám sát tập trung, phân tích dự đoán và hiệu quả chi phí cao (ước tính $0.7/tháng).

### [Blog 2 - Tăng cường bảo mật cấp tổ chức của Pinterest với tường lửa DNS: Phần 1](3.2-Blog2/)
Blog này giới thiệu cách tiếp cận của **Pinterest** nhằm tăng cường bảo mật cấp tổ chức bằng Tường lửa DNS, **Phần 1**. Bài viết trình bày chi tiết lý do **khả năng hiển thị lưu lượng truy cập DNS** rất quan trọng để ngăn chặn rò rỉ dữ liệu, và cách **Route 53 Resolver Query Logs** được thu thập và **phân tích bằng Python** để xây dựng danh sách các miền có thẩm quyền (**Allowlists**). Bài viết hướng dẫn các bước để **thiết lập nền tảng cho chiến lược "Vườn Tường" (Walled Garden)** và kiểm soát hiệu quả lưu lượng truy cập đi ra (egress).

### [Blog 3 - Sử dụng báo thức CloudWatch và Lambda để phát hiện lưu lượng truy cập bất thường](3.3-Blog3/)
Blog này hướng dẫn cách **giám sát ứng dụng** và tự động phát hiện **lưu lượng truy cập/sự bất thường ngoại lệ (anomalies)**. Bạn sẽ tìm hiểu lý do **CloudWatch Alarms** quan trọng đối với việc theo dõi số liệu theo thời gian thực, và cách tính năng **Phát hiện Bất thường (Anomaly Detection)**, được hỗ trợ bởi ML, giúp đặt ngưỡng cảnh báo linh hoạt. Một hàm **AWS Lambda** được sử dụng làm mục tiêu hành động để thực hiện **các phản hồi tự động** khi báo thức kích hoạt, chẳng hạn như gửi thông báo nâng cao hoặc thu thập dữ liệu chẩn đoán để giảm MTTR.

