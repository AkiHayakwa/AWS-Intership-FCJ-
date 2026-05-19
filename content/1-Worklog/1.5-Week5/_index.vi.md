---
title: "Worklog Tuần 5"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.5. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 5:

* Kết nối, làm quen với các thành viên trong First Cloud Journey.
* Hiểu dịch vụ AWS cơ bản, cách dùng console & CLI.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Tìm hiểu chức năng Session Manager thuộc dịch vụ AWS Systems Manager để quản lý máy chủ an toàn mà không cần mở port SSH, không cần Bastion Host hay quản lý SSH key.<br> - Hiểu cách Session Manager giúp dễ dàng tuân thủ các chính sách bảo mật, kiểm soát quyền truy cập tập trung bằng AWS IAM và ghi log lại các phiên kết nối, câu lệnh đã thực thi.<br> - Nắm bắt các ưu điểm: cấu hình kết nối không cần đi ra ngoài internet, truy cập tới server nhanh chóng, đơn giản bằng một cú click chuột.<br> - Tận dụng khả năng hỗ trợ đa nền tảng (Linux, Windows, MacOS) của Session Manager để cấp quyền truy cập cho người dùng . | 18/05/2026   | 18/05/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 3   | - Tìm hiểu về dịch vụ Amazon ElastiCache để dễ dàng thiết lập, quản lý và mở rộng kho dữ liệu in-memory phân tán hoặc môi trường cache.<br> - Khám phá các tính năng của ElastiCache for Redis như tự động phát hiện và phục hồi lỗi node, phân vùng dữ liệu , linh hoạt vị trí Availability Zone và tích hợp với các dịch vụ AWS khác (EC2, CloudWatch, SNS, CloudTrail).<br> - Nắm vững kiến trúc và thành phần của ElastiCache:<br> - Clusters: Thành phần cơ bản tập hợp các cache node chạy Redis, cung cấp khả năng tính toán, phân cấp dữ liệu, có thể chọn loại node standard hoặc memory-optimized và hoạt động trong VPC| 19/05/2026   | 19/05/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - Tạo AWS Free Tier account <br> - Tìm hiểu AWS Console & AWS CLI <br> - **Thực hành:** <br>&emsp; + Tạo AWS account <br>&emsp; + Cài AWS CLI & cấu hình <br> &emsp; + Cách sử dụng AWS CLI | 13/08/2025   | 13/08/2025      | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Tìm hiểu EC2 cơ bản: <br>&emsp; + Instance types <br>&emsp; + AMI <br>&emsp; + EBS <br>&emsp; + ... <br> - Các cách remote SSH vào EC2 <br> - Tìm hiểu Elastic IP   <br>                  | 14/08/2025   | 15/08/2025      | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - **Thực hành:** <br>&emsp; + Tạo EC2 instance <br>&emsp; + Kết nối SSH <br>&emsp; + Gắn EBS volume                                                                                         | 15/08/2025   | 15/08/2025      | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 5:

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


