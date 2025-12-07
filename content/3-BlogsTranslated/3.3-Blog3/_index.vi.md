---
title: "Blog 3: Phát hiện Lưu lượng Truy cập Bất thường bằng CloudWatch Alarms và Lambda"
weight: 1
chapter: false
pre: " <b> 3.3. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Thông tin dưới đây chỉ nhằm mục đích tham khảo. Vui lòng **không sao chép nguyên văn** cho báo cáo của bạn, bao gồm cả cảnh báo này.
{{% /notice %}}

# Bắt Đầu với Data Lakes Y Tế: Sử Dụng Microservices

Data lakes có thể giúp các bệnh viện và cơ sở chăm sóc sức khỏe biến dữ liệu thành thông tin chuyên sâu về kinh doanh, duy trì tính liên tục trong kinh doanh và bảo vệ quyền riêng tư của bệnh nhân. Một **data lake** (hồ dữ liệu) là kho lưu trữ tập trung, được quản lý và bảo mật để lưu trữ tất cả dữ liệu của bạn, cả ở dạng thô và đã xử lý để phân tích. Data lakes cho phép bạn phá vỡ các silo dữ liệu và kết hợp các loại hình phân tích khác nhau để thu thập thông tin chi tiết và đưa ra các quyết định kinh doanh tốt hơn.

Bài đăng trên blog này là một phần của loạt bài lớn hơn về việc bắt đầu thiết lập data lake y tế. Trong bài đăng cuối cùng của loạt bài, *“Bắt Đầu với Data Lakes Y Tế: Đi sâu vào Amazon Cognito”*, tôi đã tập trung vào các chi tiết cụ thể về việc sử dụng Amazon Cognito và Kiểm soát truy cập dựa trên thuộc tính (ABAC) để xác thực và ủy quyền người dùng trong giải pháp data lake y tế. Trong blog này, tôi trình bày chi tiết cách giải pháp phát triển ở cấp độ nền tảng, bao gồm các quyết định thiết kế tôi đã đưa ra và các tính năng bổ sung đã sử dụng. Bạn có thể truy cập các mẫu code cho giải pháp trong Git repo này để tham khảo.

---

## Hướng Dẫn Kiến Trúc: Từ Monolith sang Microservices

Thay đổi chính kể từ lần trình bày cuối cùng về kiến trúc tổng thể là việc phân tách một dịch vụ đơn lẻ thành một tập hợp các dịch vụ nhỏ hơn để cải thiện khả năng bảo trì và tính linh hoạt. Việc tích hợp một lượng lớn dữ liệu chăm sóc sức khỏe đa dạng thường yêu cầu các trình kết nối chuyên biệt cho từng định dạng; bằng cách giữ chúng được đóng gói riêng biệt dưới dạng microservices, chúng ta có thể thêm, xóa và sửa đổi từng trình kết nối mà không ảnh hưởng đến các trình kết nối khác. Các microservices được liên kết lỏng lẻo thông qua cơ chế nhắn tin publish/subscribe tập trung vào cái mà tôi gọi là “trung tâm pub/sub” (pub/sub hub).

[Image of Microservices Architecture communicating through a Message Broker]


Giải pháp này đại diện cho một lần lặp lại sprint hợp lý khác kể từ bài đăng trước của tôi. Phạm vi vẫn giới hạn ở việc tiếp nhận và phân tích cú pháp cơ bản các **tin nhắn HL7v2** được định dạng theo **Encoding Rules 7 (ER7)** thông qua giao diện REST.

> Cách tiếp cận microservices đảm bảo khả năng tái sử dụng và tính tự chủ, chuyên môn hóa từng dịch vụ để làm tốt một việc, thường được triển khai trong một **kiến trúc hướng sự kiện** (event-driven architecture).

---

## Quyết Định về Ranh Giới Microservice

Khi xác định nơi để vạch ra ranh giới giữa các microservices, hãy cân nhắc:

| Thể loại | Ví dụ về những điều cần cân nhắc |
| :--- | :--- |
| **Nội tại** | Công nghệ được sử dụng, hiệu suất, độ tin cậy, khả năng mở rộng |
| **Ngoại tại** | Chức năng phụ thuộc, tốc độ thay đổi, khả năng tái sử dụng |
| **Con người** | Quyền sở hữu của nhóm, quản lý *tải nhận thức* (cognitive load) |

---

## Lựa Chọn Công Nghệ và Phạm Vi Giao Tiếp

| Phạm vi Giao tiếp | Công nghệ / Pattern được cân nhắc |
| :--- | :--- |
| Trong một microservice | Amazon Simple Queue Service (Amazon SQS), AWS Step Functions |
| Giữa các microservices trong một dịch vụ | Tham chiếu lồng ghép AWS CloudFormation (cross-stack references), Amazon Simple Notification Service (Amazon SNS) |
| Giữa các dịch vụ | Amazon EventBridge, AWS Cloud Map, Amazon API Gateway |

---

## Trung Tâm Pub/Sub

Sử dụng kiến trúc **hub-and-spoke** (hoặc message broker) hoạt động tốt với một số lượng nhỏ microservices có liên quan chặt chẽ.
- Mỗi microservice chỉ phụ thuộc vào *trung tâm* - Các kết nối giữa các microservice bị giới hạn bởi nội dung của tin nhắn đã xuất bản
- Giảm số lượng lệnh gọi đồng bộ vì pub/sub là cơ chế *đẩy* bất đồng bộ một chiều

Hạn chế: Cần **phối hợp và giám sát** để tránh microservices xử lý nhầm tin nhắn.

---

## Core Microservice

Cung cấp lớp dữ liệu và giao tiếp nền tảng, bao gồm:
- **Amazon S3** bucket cho dữ liệu
- **Amazon DynamoDB** cho danh mục dữ liệu
- **AWS Lambda** để ghi tin nhắn vào data lake và danh mục
- **Amazon SNS** topic đóng vai trò là *trung tâm* - **Amazon S3** bucket cho các tạo phẩm (artifacts) như mã Lambda

> Chỉ cho phép ghi gián tiếp vào data lake thông qua hàm Lambda → đảm bảo tính nhất quán.

---

## Front Door Microservice

- Cung cấp API Gateway cho tương tác REST bên ngoài
- Xác thực & ủy quyền dựa trên **OIDC** qua **Amazon Cognito** - Cơ chế *khử trùng lặp* tự quản lý bằng DynamoDB thay vì SNS FIFO vì:
    1. TTL khử trùng lặp của SNS chỉ là 5 phút
    2. SNS FIFO yêu cầu SQS FIFO
    3. Khả năng chủ động thông báo cho người gửi rằng tin nhắn là trùng lặp

---

## Staging ER7 Microservice

- Lambda “trigger” đăng ký vào trung tâm pub/sub, lọc tin nhắn theo thuộc tính
- Step Functions Express Workflow để chuyển đổi ER7 → JSON
- Hai Lambdas:
    1. Sửa lỗi định dạng ER7 (ký tự xuống dòng, carriage return)
    2. Logic phân tích cú pháp
- Kết quả hoặc lỗi được đẩy trở lại trung tâm pub/sub

---

## New Features in the Solution

### 1. Tự động phát hiện và phản hồi lưu lượng bất thường (CloudWatch & Lambda)

Tính năng này cho phép quan sát nâng cao và tự động hóa quy trình phản hồi sự cố bằng cách kết hợp **Amazon CloudWatch** và **AWS Lambda**.

#### Phát hiện Bất thường (Anomaly Detection)
* **CloudWatch Alarms:** Được sử dụng để giám sát các số liệu chính (ví dụ: số lượng lỗi API, lưu lượng mạng) theo thời gian thực. Thay vì ngưỡng tĩnh, tính năng **CloudWatch Anomaly Detection** tạo ra một mô hình ML về hành vi bình thường của số liệu, tự động điều chỉnh các ranh giới cảnh báo.
* **Mục tiêu:** Gắn cờ các "sự kiện ngoại lệ" thực sự nằm ngoài hành vi lịch sử dự kiến, chẳng hạn như đột biến lỗi đột ngột hoặc giảm lưu lượng truy cập không mong muốn.

#### Tự động hóa Phản hồi (Automated Response)
* Khi **CloudWatch Alarm** chuyển sang trạng thái `ALARM`, nó sẽ kích hoạt một hàm **AWS Lambda** làm mục tiêu hành động.
* **Chức năng Lambda:** Lambda thực hiện các tác vụ phản hồi tự động để giảm Thời gian Trung bình để Khắc phục (MTTR), bao gồm:
    1. **Thông báo nâng cao:** Gửi tin nhắn chi tiết qua **Amazon SNS** đến các kênh như Slack hoặc PagerDuty.
    2. **Thu thập Chẩn đoán:** Gọi các API AWS khác để thu thập log ngữ cảnh hoặc thông tin trạng thái hệ thống xung quanh thời điểm xảy ra sự bất thường.
    3. **Khắc phục Cơ bản:** Thực hiện các bước khắc phục đơn giản, chẳng hạn như giới hạn yêu cầu (throttle) đối với một tài nguyên cụ thể hoặc khởi động lại một thành phần không phản hồi.

### 2. Tham Chiếu Lồng Ghép AWS CloudFormation (Cross-Stack References)
Tính năng này cho phép tách biệt logic và khả năng tái sử dụng bằng cách cho phép các CloudFormation stack khác nhau tham chiếu và sử dụng an toàn các tài nguyên được tạo và **Exported** (Xuất) bởi stack Core Microservice.

Ví dụ về *outputs* trong core microservice:
```yaml
Outputs:
  Bucket:
    Value: !Ref Bucket
    Export:
      Name: !Sub ${AWS::StackName}-Bucket
  ArtifactBucket:
    Value: !Ref ArtifactBucket
    Export:
      Name: !Sub ${AWS::StackName}-ArtifactBucket
  Topic:
    Value: !Ref Topic
    Export:
      Name: !Sub ${AWS::StackName}-Topic
  Catalog:
    Value: !Ref Catalog
    Export:
      Name: !Sub ${AWS::StackName}-Catalog
  CatalogArn:
    Value: !GetAtt Catalog.Arn
    Export:
      Name: !Sub ${AWS::StackName}-CatalogArn