---
title: "Worklog Tuần 1"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

### Mục tiêu tuần 1:

* Kết nối, làm quen với các thành viên trong First Cloud Journey.
* Hiểu dịch vụ AWS cơ bản, cách dùng console & CLI.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Làm quen với các thành viên FCJ <br> - Đọc và lưu ý các nội quy, quy định tại đơn vị thực tập                                                                                             | 20/04/2026   | 20/04/2026      |
| 3   | - Tìm hiểu AWS và các loại dịch vụ <br>&emsp; + Compute <br>&emsp; + Storage <br>&emsp; + Networking <br>&emsp; + Database <br>&emsp; + ... <br>                                            | 21/04/2026  | 21/04/2026    | <https://cloudjourney.awsstudygroup.com/> |
| 4   | -  Tìm hiểu về Firewall trong VPC <br> - Tạo VPC , Subnet , Internet Gateway , Route Table , Security Group và VPC Flow Logs <br> - Làm việc deploying Amazon EC2 Instance | 22/04/2026  | 22/04/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Cấu hình Elastic IP , tạo NAT Gateway , Sử dụng EC2 instance endpoint để kết nối server <br> Học cách xây dựng site-to-site VPN connection                  | 23/04/2026   | 23/04/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - Tìm hiểu và làm việc cách tạo EC2 instance windows , linux và kết nối máy tính đến microsoft window server , linux server <br> Học được cách chuyển loại instance của EC2 , tạo và quản lý được cách làm việc với snapshot EBS , AMI và recovering access của window instance <br> Học được cách set up LAMP server và config database để deployee ứng dụng <br> Làm việc với cách chia role và gán role để quản lý chi phí IAM                                                                                   | 24/04/2026  | 24/04/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 7  | Tìm hiểu và nghiên cứu về cách sử dụng Instance Profile của IAM Role dành cho máy chủ EC2| 25/04/2026 | 25/04/2026      | <https://cloudjourney.awsstudygroup.com/> |
| Chủ nhật | - học và tạo cloud9 trong môi trường phát triển  | 26/04/2026 | 26/04/2026   | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được tuần 1:

- Hội nhập & Nền tảng AWS

  + Làm quen với các thành viên nhóm FCJ, nắm vững nội quy thực tập và hiểu được các khái niệm cốt lõi về dịch vụ đám mây của AWS (Điện toán, Lưu trữ, Mạng, Cơ sở dữ liệu).

- Quản lý Danh tính & Truy cập (IAM)

  + Thành thạo việc khởi tạo và quản lý IAM User, Group, Role và Policy.
  + Hiểu sâu về các cơ chế bảo mật nâng cao như chuyển đổi quyền (Assume Role), phân biệt các loại Policy, và cách áp dụng IAM Instance Profile cho máy chủ ảo EC2.

- Mạng đám mây (VPC)

  + Tự thiết kế và triển khai thành công một mạng riêng ảo (VPC) hoàn chỉnh.
  + Cấu hình chi tiết các thành phần mạng cốt lõi bao gồm Subnet, Route Table, Internet Gateway, NAT Gateway, Security Group, VPC Flow Logs, Elastic IP và tìm hiểu về kết nối Site-to-Site VPN.

- Dịch vụ Máy chủ ảo (Amazon EC2)

  + Tích lũy kinh nghiệm thực tế trong việc khởi tạo, kết nối (qua SSH/RDP) và quản trị máy chủ EC2 trên cả hai hệ điều hành Linux và Windows.
  + Thực hiện thành công các tác vụ quản trị máy chủ nâng cao như: thay đổi cấu hình máy (instance types), quản lý bản sao lưu (EBS snapshot, AMI), khôi phục quyền truy cập máy chủ Windows và cài đặt môi trường web LAMP.

 - Môi trường Phát triển

  + Khởi tạo và thiết lập thành công môi trường lập trình trực tuyến AWS Cloud9 (Cloud IDE) để phục vụ cho các công việc phát triển dự án tiếp theo.
