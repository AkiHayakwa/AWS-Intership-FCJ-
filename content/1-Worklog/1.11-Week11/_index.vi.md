---
title: "Worklog Tuần 11"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 1.11. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 11:

* Kết nối, làm quen với các thành viên trong First Cloud Journey.
* Hiểu dịch vụ AWS cơ bản, cách dùng console & CLI.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Lab 3: Transforming data with Glue: <br>&emsp; + Data Validation và ETL: Sử dụng AWS Glue để làm sạch, kiểm tra và chuyển đổi dữ liệu. <br>&emsp; + Incremental Data Processing với Hudi: Áp dụng Apache Hudi xử lý dữ liệu thay đổi (upsert/delete) trên S3. <br> - Lab 4: Query và Visualize: <br>&emsp; + Phân tích dữ liệu: Truy vấn dữ liệu S3 bằng Amazon Athena và tạo Dashboard trực quan bằng QuickSight. <br>&emsp; + Athena nâng cao: Sử dụng Federated query để truy cập đa nguồn và kết nối với SageMaker để dự đoán. | 29/06/2026   | 29/06/2026      | https://cloudjourney.awsstudygroup.com/>  |
| 3   | - Lab 5: Data Lake Automation: <br>&emsp; + Lake Formation cơ bản: Đăng ký data lake location, thiết lập Data Catalog và cấp quyền truy cập. <br>&emsp; + Áp dụng Lake Formation: Quản lý quyền cho các định dạng dữ liệu mở như Apache Hudi, Iceberg, Delta Tables. <br> - Bonus Lab: Glue DataBrew: <br>&emsp; + Sử dụng Glue DataBrew để làm sạch và chuẩn bị dữ liệu (Data Preparation) thông qua giao diện trực quan. | 30/06/2026   | 30/06/2026      | https://cloudjourney.awsstudygroup.com/> |
| 4   | - Tạo AWS Free Tier account <br> - Tìm hiểu AWS Console & AWS CLI <br> - **Thực hành:** <br>&emsp; + Tạo AWS account <br>&emsp; + Cài AWS CLI & cấu hình <br> &emsp; + Cách sử dụng AWS CLI | 13/08/2025   | 13/08/2025      | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Tìm hiểu EC2 cơ bản: <br>&emsp; + Instance types <br>&emsp; + AMI <br>&emsp; + EBS <br>&emsp; + ... <br> - Các cách remote SSH vào EC2 <br> - Tìm hiểu Elastic IP   <br>                  | 14/08/2025   | 15/08/2025      | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - **Thực hành:** <br>&emsp; + Tạo EC2 instance <br>&emsp; + Kết nối SSH <br>&emsp; + Gắn EBS volume                                                                                         | 15/08/2025   | 15/08/2025      | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 11:

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


