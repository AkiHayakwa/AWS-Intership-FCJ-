---
title: "Worklog Tuần 3"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.3. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 3:

* Kết nối, làm quen với các thành viên trong First Cloud Journey.
* Hiểu dịch vụ AWS cơ bản, cách dùng console & CLI.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Học và cấu hình hàm Lambda để nâng cao hiệu quả chi phí, tìm hiểu về EventBridge trong dịch vụ CloudWatch <br> - Nghiên cứu cách triển khai ứng dụng lên EC2 bằng AWS CodePipeline, bao gồm cấu hình Git credential, Git connection, CodeDeploy agent và CodePipeline                                                                                            | 04/05/2026   | 04/05/2026      |
| 3   | - Học cách thiết lập AWS Storage Gateway, tạo file share và kết nối ổ đĩa với máy cá nhân để đồng bộ dữ liệu <br> - Thực hành thiết lập AWS Web Application Firewall, triển khai bảo mật ứng dụng sử dụng các quy tắc AWS WAF <br> - Tạo thẻ (tag) để tổ chức tài nguyên và sử dụng AWS Resource Groups để quản lý và tự động hóa các tác vụ | 05/05/2026  | 05/05/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - Nghiên cứu và cài đặt Grafana để giám sát tài nguyên trên AWS, kết nối với CloudWatch <br> - Tạo IAM Permission Boundary và Organization Policy để quản lý tối ưu chi phí và bảo mật <br> - Quản lý bản vá bằng lệnh Run Command trên nhiều máy chủ | 06/05/2026 | 06/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Học và thực hành cách mã hóa dữ liệu với AWS KMS, AWS CloudTrail và truy xuất dữ liệu bằng Athena, chia sẻ dữ liệu đã mã hóa trên S3 <br> - Tìm hiểu cách tính toán, xem chi tiết và sử dụng tính năng quản lý chi phí theo từng dịch vụ | 07/05/2026   | 07/05/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - Làm quen với cách lưu trữ, phân tích và chuyển đổi dữ liệu với Data Lake. <br> - Học cách thiết lập và triển khai kiến trúc cơ bản sử dụng AWS CDK <br> - Tìm hiểu cách sử dụng AWS Glue kết hợp với Athena để truy xuất dữ liệu, phân tích chi phí và hiệu suất. | 08/05/2026 | 08/05/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 3:

- Điện toán Máy chủ ảo (Serverless) & Tự động hóa Triển khai

  + Cấu hình các hàm Lambda và EventBridge.
  + Triển khai ứng dụng lên EC2 bằng AWS CodePipeline và CodeDeploy.

- Bảo mật, Lưu trữ & Quản lý Tài nguyên

  + Cấu hình AWS Storage Gateway để đồng bộ dữ liệu lai (hybrid).
  + Triển khai các quy tắc AWS WAF để bảo vệ ứng dụng web.
  + Tổ chức tài nguyên hiệu quả bằng tag (thẻ) và AWS Resource Groups.
  + Thiết lập IAM Permission Boundaries và Organization Policies.
  + Thực hành mã hóa dữ liệu (encrypt at rest) với AWS KMS và giám sát hoạt động bằng CloudTrail.

- Giám sát & Vận hành Hệ thống

  + Tích hợp Grafana với CloudWatch để giám sát tài nguyên mạnh mẽ hơn.
  + Quản lý bản vá lỗi trên nhiều máy chủ bằng AWS Systems Manager (Run Command).
  + Tính toán và phân tích chi tiết chi phí sử dụng dịch vụ AWS.

- Data Engineering & Infrastructure as Code (IaC)

  + Xây dựng kiến trúc Data Lake cơ bản bằng AWS CDK.
  + Sử dụng AWS Glue và Athena để truy xuất, chuyển đổi dữ liệu và phân tích hiệu suất.
  + Chia sẻ dữ liệu đã mã hóa an toàn qua Amazon S3.
