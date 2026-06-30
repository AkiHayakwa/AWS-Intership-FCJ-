---
title: "Worklog Tuần 10"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 1.10. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 10:

* Kết nối, làm quen với các thành viên trong First Cloud Journey.
* Hiểu dịch vụ AWS cơ bản, cách dùng console & CLI.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Làm quen với các thành viên FCJ <br> - Đọc và lưu ý các nội quy, quy định tại đơn vị thực tập <br>&emsp; + Tìm hiểu tầm quan trọng của vá lỗi hệ điều hành đối với bảo mật và tuân thủ (compliance) <br>&emsp; + Hiểu phương pháp triển khai blue/green để tạo và thay thế AMI <br>&emsp; + Nghiên cứu tự động hóa vá lỗi sử dụng các dịch vụ AWS: <br>&emsp;&emsp; * EC2 Image Builder (tạo AMI tự động) <br>&emsp;&emsp; * Systems Manager Automation Document (điều phối thực thi) <br>&emsp;&emsp; * CloudFormation với chính sách AutoScalingReplacingUpdate (triển khai không gián đoạn) | 22/06/2026   | 22/06/2026      |
| 3   |  <br>&emsp; + Tìm hiểu các khái niệm cơ bản về AWS Elastic Disaster Recovery (AWS DRS): cách giảm thiểu thời gian ngừng hoạt động và mất dữ liệu, chỉ số RTO/RPO, tối ưu chi phí và phục hồi về một thời điểm (point-in-time recovery). <br>&emsp; + Nghiên cứu kiến trúc tổng quan của AWS DRS: sao chép đĩa máy chủ nguồn, cài đặt Replication Agent, máy chủ nhân bản trong vùng Staging Area VPC và các thực thể phục hồi mục tiêu. <br>&emsp; + Tìm hiểu các thành phần môi trường on-premises mô phỏng: public/private subnets, dịch vụ DNS, các ứng dụng cài sẵn. <br>&emsp; + Chuẩn bị kiến thức cơ bản: kết nối SSH đến máy chủ Linux và kết nối RDP đến máy chủ Windows bastion. | 23/06/2026   | 23/06/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 4   |  <br>&emsp; + Kết nối vào máy chủ Windows bastion qua RDP và các máy chủ Linux qua SSH. <br>&emsp; + Cài đặt AWS Replication Agent lên các máy chủ nguồn on-premises mô phỏng để đồng bộ hóa dữ liệu ở cấp độ block-level. <br>&emsp; + Cấu hình các thiết lập nhân bản trên bảng điều khiển AWS DRS và giám sát quá trình đồng bộ hóa dữ liệu ban đầu. <br>&emsp; + Thực hành các thao tác phục hồi thảm họa (Disaster Recovery): chạy thử nghiệm không gián đoạn (drill), Failover (chuyển đổi dự phòng khi có thảm họa) và Failback (phục hồi trở lại môi trường nguồn). | 24/06/2026   | 24/06/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Tìm hiểu Data Engineering Immersion Day. <br> - Lab 1: Phát hiện luồng click chuột bất thường bằng Amazon Managed Service for Apache Flink: <br>&emsp; + Chuẩn bị môi trường: Khởi tạo các tài nguyên (S3, Kinesis Stream, IAM Role). <br>&emsp; + Streaming ETL với Glue: Tạo Data Catalog, thiết lập ETL Job biến đổi dữ liệu real-time. <br>&emsp; + Real-time Streaming với Kinesis: Đẩy dữ liệu mô phỏng clickstream vào Kinesis. <br>&emsp; + Clickstream Analytics sử dụng MSK: Cấu hình Amazon Managed Streaming for Apache Kafka để phân tích sự kiện. | 25/06/2026   | 25/06/2026      | <https://000105.awsstudygroup.com/> |
| 6   | - Lab 2: Nhập data với DMS: <br>&emsp; + Thực hành DMS Migration Lab: Khởi tạo Replication Instance, cấu hình Source/Target Endpoints và chạy Database Migration Task. <br>&emsp; + Tùy chọn: Dùng CloudFormation để chạy AutoComplete DMS Lab (tự động hóa) hoặc Skip DMS Lab nếu không có thời gian. | 26/06/2026   | 26/06/2026      | <https://000105.awsstudygroup.com/> |


### Kết quả đạt được tuần 10:

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


