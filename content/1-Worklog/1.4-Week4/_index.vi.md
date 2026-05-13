---
title: "Worklog Tuần 4"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.4. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 4:

* Kết nối, làm quen với các thành viên trong First Cloud Journey.
* Hiểu dịch vụ AWS cơ bản, cách dùng console & CLI.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Nghiên cứu cách triển khai ứng dụng web TravelBuddy lên AWS, Sử dụng AWS Tools cho Eclipse để deploy ứng dụng Java lên môi trường Elastic Beanstalk, Cấu hình công cụ AWS Elastic Beanstalk CLI, Sử dụng AWS SDK để truy vấn và chỉnh sửa môi trường AWS                                                                                                | 11/05/2026   | 11/05/2026      |
| 3   | - Áp dụng cấu hình các dịch vụ tự động phát hành ứng dụng kết hợp AWS CodeCommit để lưu trữ mã nguồn an toàn, AWS CodeBuild để xây dựng mã nguồn, AWS CodeDeploy để triển khai ứng dụng lên máy chủ, AWS CodePipeline để liên kết CodeCommit, CodeBuild và CodeDeploy với nhau thành một quy trình làm việc tự động và liền mạch, và AWS CodeStar để cho phép bạn nhanh chóng phát triển, xây dựng và triển khai các ứng dụng trên AWS | 12/05/2026   | 12/05/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - Triển khai một AWS Lambda function.<br>- Chỉnh sửa mã nguồn hàm Java Lambda đã được cung cấp để thay đổi kích thước hình ảnh dưới dạng hình thu nhỏ hoặc xóa tập tin không phải hình ảnh và kết nối trình kích hoạt vào S3 bucket để kiểm tra tính năng.<br>- Sử dụng AWS Serverless Application Model (SAM) và AWS CloudFormation để tạo template nhằm tự động hóa việc triển khai hàm Lambda, một trình kích hoạt S3 và một S3 bucket.<br>- Xác định microservice candidate trong monolithic codebase và tạo dự án AWS CodeStar để quản lý CI/CD pipeline cho microservice đó được lưu trữ trong AWS Lambda. | 13/05/2026   | 13/05/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Tìm hiểu EC2 cơ bản: <br>&emsp; + Instance types <br>&emsp; + AMI <br>&emsp; + EBS <br>&emsp; + ... <br> - Các cách remote SSH vào EC2 <br> - Tìm hiểu Elastic IP   <br>                  | 14/08/2025   | 15/08/2025      | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - **Thực hành:** <br>&emsp; + Tạo EC2 instance <br>&emsp; + Kết nối SSH <br>&emsp; + Gắn EBS volume                                                                                         | 15/08/2025   | 15/08/2025      | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 4:

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


