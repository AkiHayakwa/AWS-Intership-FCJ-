---
title: "Worklog Tuần 8"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.8. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 8:

* Kết nối, làm quen với các thành viên trong First Cloud Journey.
* Hiểu dịch vụ AWS cơ bản, cách dùng console & CLI.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Học cách xây dựng hệ thống nhắn tin (messaging) cho ứng dụng web sử dụng AWS AppSync tương tác với GraphQL.<br>- Tìm hiểu cách hoạt động của AWS AppSync:<br>&emsp; + Dịch vụ được quản lý toàn phần (managed service) giúp đơn giản hóa việc xây dựng các API GraphQL linh hoạt để truy cập, thao tác và kết hợp dữ liệu từ nhiều nguồn một cách an toàn.<br>&emsp; + Hỗ trợ xây dựng các API GraphQL có khả năng mở rộng, tích hợp với DynamoDB, Lambda, Elasticsearch, cũng như các nguồn dữ liệu HTTP/SQL/REST.<br>&emsp; + Các tính năng nổi bật: đồng bộ hóa dữ liệu ngoại tuyến (offline), cập nhật thời gian thực (real-time updates) và kiểm soát quyền truy cập chi tiết.<br>- Thực hành các thao tác CRUD (tạo, cập nhật, đọc, xóa dữ liệu) trên bảng DynamoDB thông qua API GraphQL của AWS AppSync. | 09/06/2026   | 09/06/2026     | <https://cloudjourney.awsstudygroup.com/> |
| 3   | - Nghiên cứu AWS Toolkit cho Visual Studio Code <br>- Nghiên cứu Amazon Q <br>&emsp; <br>&emsp; + Viết unit test, sinh mã nguồn, gỡ lỗi, khắc phục sự cố và tối ưu hóa mã nguồn.<br>&emsp; + Gợi ý mã nguồn thời gian thực trên 15+ ngôn ngữ (bao gồm cả CloudFormation, CDK, Terraform).<br>&emsp; + Tối ưu hóa các gợi ý mã nguồn cho các dịch vụ AWS APIs (EC2, Lambda, S3).<br>&emsp; + Quét bảo mật tích hợp để phát hiện các lỗ hổng khó tìm và đề xuất cách khắc phục ngay lập tức. | 10/06/2026   | 10/06/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - Tạo AWS Free Tier account <br> - Tìm hiểu AWS Console & AWS CLI <br> - **Thực hành:** <br>&emsp; + Tạo AWS account <br>&emsp; + Cài AWS CLI & cấu hình <br> &emsp; + Cách sử dụng AWS CLI | 13/08/2025   | 13/08/2025      | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Tìm hiểu EC2 cơ bản: <br>&emsp; + Instance types <br>&emsp; + AMI <br>&emsp; + EBS <br>&emsp; + ... <br> - Các cách remote SSH vào EC2 <br> - Tìm hiểu Elastic IP   <br>                  | 14/08/2025   | 15/08/2025      | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - **Thực hành:** <br>&emsp; + Tạo EC2 instance <br>&emsp; + Kết nối SSH <br>&emsp; + Gắn EBS volume                                                                                         | 15/08/2025   | 15/08/2025      | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 8:

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


