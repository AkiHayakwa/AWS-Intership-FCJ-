---
title: "Worklog Tuần 6"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.6. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 6:

* Kết nối, làm quen với các thành viên trong First Cloud Journey.
* Hiểu dịch vụ AWS cơ bản, cách dùng console & CLI.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Thiết kế kiến trúc data lake serverless. <br> - Xây dựng đường ống xử lý dữ liệu và Data Lake bằng cách sử dụng Amazon S3 để lưu trữ dữ liệu. <br> - Sử dụng Amazon Kinesis cho dữ liệu truyền phát thời gian thực. <br> - Sử dụng Amazon Kinesis Data Analytics cho phân tích dữ liệu thời gian thực. <br> - Truy vấn dữ liệu bằng Amazon Athena và trực quan hóa dữ liệu bằng Amazon QuickSight. | 25/05/2026 | 25/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3   | - Sử dụng AWS Glue để tự động lập chỉ mục các bộ dữ liệu. <br> - Biến đổi dữ liệu. <br> - Chạy các script ETL tương tác trong một cuốn sổ Jupyter trên AWS Glue Studio sử dụng AWS Glue (interactive sessions). <br> - Sử dụng Glue Studio để chạy và giám sát các ETL jobs trong AWS Glue. <br> - Sử dụng Glue DataBrew để chuẩn bị dữ liệu. <br> - Sử dụng EMR để chạy một job biến đổi Spark. <br> - Tải dữ liệu lên Amazon Redshift từ Glue. <br> - Giới thiệu về các quy thực hành thiết kế tốt cho Amazon Redshift. | 26/05/2026 | 26/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - Tìm hiểu cơ chế hoạt động của Amazon SNS (Simple Notification Service) và Amazon SQS (Simple Queue Service). <br> - Triển khai mô hình Pub/Sub và cấu hình chính sách bộ lọc (Subscription Filter Policy) để lọc và định tuyến tin nhắn tự động. <br> - **Thực hành:** <br>&emsp; + Tạo hàng đợi SQS mới cho Đơn đặt hàng ở EU (EU orders). <br>&emsp; + Đăng ký subscribe hàng đợi SQS vào SNS Topic Đơn hàng. <br>&emsp; + Thiết lập chính sách lọc tin nhắn cho subscribe bằng cách chỉ định thuộc tính location với giá trị eu-west để chỉ nhận các thông điệp từ EU. | 27/05/2026 | 27/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Tìm hiểu EC2 cơ bản: <br>&emsp; + Instance types <br>&emsp; + AMI <br>&emsp; + EBS <br>&emsp; + ... <br> - Các cách remote SSH vào EC2 <br> - Tìm hiểu Elastic IP   <br>                  | 14/08/2025   | 15/08/2025      | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - **Thực hành:** <br>&emsp; + Tạo EC2 instance <br>&emsp; + Kết nối SSH <br>&emsp; + Gắn EBS volume                                                                                         | 15/08/2025   | 15/08/2025      | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 6:
* Hiểu AWS là gì và nắm được các nhóm dịch vụ cơ bản: 
  * Compute
  * Storage
  * Networking 
  * Database
  * ...

* Đã tạo và cấu hình AWS Free Tier account thành công.

* Làm quen với AWS Management Console và biết cách tìm, truy cập, sử dụng dịch vụ từ giao diện web.

* Cài đặt và cấu hình AWS CLI trên máy tính bao gồm:
  * Access Key
  * Secret Key
  * Region mặc định
  * ...

* Sử dụng AWS CLI để thực hiện các thao tác cơ bản như:

  * Kiểm tra thông tin tài khoản & cấu hình
  * Lấy danh sách region
  * Xem dịch vụ EC2
  * Tạo và quản lý key pair
  * Kiểm tra thông tin dịch vụ đang chạy
  * ...

* Có khả năng kết nối giữa giao diện web và CLI để quản lý tài nguyên AWS song song.
* ...


