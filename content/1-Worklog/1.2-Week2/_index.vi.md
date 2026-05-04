---
title: "Worklog Tuần 2"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.2. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 2:

* Kết nối, làm quen với các thành viên trong First Cloud Journey.
* Hiểu dịch vụ AWS cơ bản, cách dùng console & CLI.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                               | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Tìm hiểu và deploy static web hosting bằng S3 bucket <br> - Học được cách set up RDS  <br> học và thực hành với amazon EC2 auto scaling , elastic load balancing và launch template                                                                                          | 27/04/2026   | 27/04/2026    |
| 3   | - Học và thực hành aws cloudwatch workshop , viewing metrics , search và math expression , cloudwatch logs <br> triển khai hybrid dns với route 53 <br> Học và tìm hiểu về AWS CLI                             | 28/04/2026 | 28/04/2026      | <https://cloudjourney.awsstudygroup.com/>
| 4   |- Tìm hiểu cách tạo và triển khai dịch vụ AWS Backup cho hệ thống, thiết lập kế hoạch sao lưu (backup plan), và cấu hình gửi thông báo về email. <br> ghiên cứu và thực hành cách nhập/xuất (import/export) máy ảo (VM) bằng cách sử dụng AWS S3 bucket và EC2 | 29/04/2026 | 29/04/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Tìm hiểu và thực hành cách sử dụng docker container sử dụng các dịch vụ như Amazon ECR ,  RDS , EC2                 | 30/04/2026   | 30/04/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - Tìm hiểu và thực hành cách triển khai ứng dụng trên Amazon ECS, tạo cluster, service, đăng ký namespace với Cloud Map <br> - Học và thực hành triển khai CI/CD với GitLab, GitHub Actions và AWS CodeBuild, cấu hình giám sát ứng dụng bằng Container Insights <br> - Tìm hiểu về AWS Security Hub <br> - Học cách cấu hình VPC Peering để kết nối các VPC với nhau <br> - Học cách thiết lập AWS Transit Gateway để kết nối nhiều VPC thay vì dùng VPC Peering                                                                  | 01/05/2026 | 01/05/2026      | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 2:

- Mở rộng Nền tảng Máy chủ & Cân bằng tải

  + Nắm vững và thực hành thành công Amazon EC2 Auto Scaling, Elastic Load Balancing (ELB), và Launch Templates nhằm đảm bảo tính sẵn sàng cao cho hệ thống.

- Lưu trữ & Cơ sở dữ liệu

  + Triển khai thành công trang web tĩnh (static web hosting) bằng Amazon S3 bucket.
  + Thiết lập và quản lý cơ sở dữ liệu với Amazon RDS.
  + Thực hiện thao tác nhập/xuất (import/export) máy ảo (VM) sử dụng Amazon S3 và EC2.

- Giám sát Hệ thống & Mạng lưới Nâng cao

  + Giám sát hiệu suất hệ thống thông qua AWS CloudWatch (metrics, logs, math expressions) và Container Insights.
  + Thiết lập thành công hệ thống Hybrid DNS sử dụng Amazon Route 53.
  + Cấu hình kết nối mạng đa VPC thông qua VPC Peering và thiết lập AWS Transit Gateway.

- Công cụ Quản lý & Sao lưu

  + Thành thạo cách sử dụng AWS CLI để tương tác và quản lý tài nguyên AWS.
  + Triển khai dịch vụ AWS Backup, thiết lập kế hoạch sao lưu (backup plan) tự động và cấu hình thông báo qua email.

- Containerization & CI/CD

  + Ứng dụng Docker container cùng với các dịch vụ Amazon ECR, RDS, và EC2.
  + Triển khai ứng dụng trên Amazon ECS, bao gồm tạo cluster, service và đăng ký namespace với Cloud Map.
  + Xây dựng luồng tích hợp và triển khai liên tục (CI/CD) bằng GitLab, GitHub Actions và AWS CodeBuild.

- Bảo mật Đám mây

  + Củng cố kiến thức về quản lý bảo mật tập trung trên AWS thông qua AWS Security Hub.


