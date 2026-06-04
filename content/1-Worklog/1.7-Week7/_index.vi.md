---
title: "Worklog Tuần 7"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.7. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 7:

* Kết nối, làm quen với các thành viên trong First Cloud Journey.
* Hiểu dịch vụ AWS cơ bản, cách dùng console & CLI.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Ôn tập cách xây dựng ứng dụng web đơn giản theo mô hình serverless bằng bảng điều khiển AWS.<br>- Tìm hiểu AWS Serverless Application Model (SAM) - một open-source framework hỗ trợ xây dựng ứng dụng serverless nhanh hơn.<br>- Học cú pháp YAML của SAM để định nghĩa các hàm, API, cơ sở dữ liệu và event source mappings.<br>- Tìm hiểu cách SAM chuyển đổi và mở rộng cú pháp thành AWS CloudFormation để tự động cung cấp tài nguyên. | 01/06/2026   | 01/06/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 3   | - Tìm hiểu về Amazon Cognito - dịch vụ cung cấp giải pháp xác thực, ủy quyền và quản lý người dùng cho ứng dụng web và di động.<br>- Nghiên cứu hai thành phần chính của Amazon Cognito:<br>&emsp; + Thư mục người dùng cung cấp tính năng đăng ký và đăng nhập (trực tiếp hoặc qua bên thứ ba như Facebook, Google, Apple,...) và kiểm soát quyền truy cập ứng dụng.<br>&emsp; +  Cung cấp thông tin xác thực AWS tạm thời để cấp quyền cho người dùng truy cập trực tiếp vào các tài nguyên AWS khác.<br>- Tìm hiểu ví dụ về cách kết hợp User pools và Identity pools cùng nhau trong kiến trúc ứng dụng. | 02/06/2026   | 02/06/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - Tìm hiểu cách bảo mật ứng dụng web trong quá trình truyền tải dữ liệu bằng chứng chỉ SSL để mã hóa lưu lượng giữa người dùng và trang web tĩnh được lưu trữ trên Amazon S3 (in-flight encryption).<br>- Nghiên cứu các dịch vụ cốt lõi trong kiến trúc lưu trữ web an toàn không máy chủ (serverless):<br>&emsp; + Quản lý việc tạo, lưu trữ và gia hạn chứng chỉ cũng như khóa SSL/TLS X.509 công khai và riêng tư để bảo vệ các trang web và ứng dụng AWS.<br>&emsp; + Dịch vụ Hệ thống Phân giải Tên miền (DNS) đám mây có độ sẵn sàng và khả năng mở rộng cao, giúp định tuyến người dùng đến các tài nguyên và quản lý Hosted zone.<br>&emsp; +Dịch vụ phân phối nội dung (CDN) giúp tăng tốc độ truyền tải nội dung web tĩnh và động qua mạng lưới điểm biên, hỗ trợ cấu hình HTTPS với chứng chỉ SSL.<br>- Tìm hiểu lợi ích của việc kết hợp Amazon S3 với Amazon CloudFront, bao gồm việc sử dụng Origin Access Control (OAC) để giới hạn quyền truy cập trực tiếp vào nội dung S3. | 03/06/2026   | 03/06/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Học cách xử lý đơn đặt hàng của người dùng bằng cách tích hợp Amazon SQS và Amazon SNS vào ứng dụng web serverless.<br>- Tìm hiểu kiến trúc xử lý đơn hàng bao gồm:<br>&emsp; + API POST `/books/order` gửi thông tin đơn hàng vào hàng đợi SQS và phát tin nhắn qua SNS topic.<br>&emsp; +  API GET `/books/order` giúp admin lấy các đơn hàng chưa xử lý trong hàng đợi và các đơn hàng đã xử lý trong DynamoDB.<br>&emsp; +  API POST `/books/order/handle` lưu thông tin vào DynamoDB và xóa đơn hàng khỏi hàng đợi.<br>&emsp; +  API DELETE `/books/order` xóa đơn hàng khỏi hàng đợi.<br>- Tìm hiểu các dịch vụ nhắn tin (messaging) của AWS:<br>&emsp; +  Dịch vụ hàng đợi tin nhắn an toàn, bền vững để tích hợp và tách rời các thành phần phần mềm phân tán, hỗ trợ hàng đợi Standard và FIFO.<br>&emsp; +  Dịch vụ gửi tin nhắn từ nhà xuất bản (publishers) đến người đăng ký (subscribers) theo cơ chế pub/sub không đồng bộ qua các topic giao tiếp. | 04/06/2026   | 04/06/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - **Thực hành:** <br>&emsp; + Tạo EC2 instance <br>&emsp; + Kết nối SSH <br>&emsp; + Gắn EBS volume                                                                                         | 05/06/2026   | 05/06/2026      | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 7:

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


