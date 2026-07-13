---
title: "Worklog Tuần 10"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 1.10. </b> "
---


### Mục tiêu tuần 10:

* Kết nối, làm quen với các thành viên trong First Cloud Journey.
* Hiểu dịch vụ AWS cơ bản, cách dùng console & CLI.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Làm quen với các thành viên FCJ <br> - Đọc và lưu ý các nội quy, quy định tại đơn vị thực tập <br>&emsp; + Tìm hiểu tầm quan trọng của vá lỗi hệ điều hành đối với bảo mật và tuân thủ (compliance) <br>&emsp; + Hiểu phương pháp triển khai blue/green để tạo và thay thế AMI <br>&emsp; + Nghiên cứu tự động hóa vá lỗi sử dụng các dịch vụ AWS: <br>&emsp;&emsp; * EC2 Image Builder (tạo AMI tự động) <br>&emsp;&emsp; * Systems Manager Automation Document (điều phối thực thi) <br>&emsp;&emsp; * CloudFormation với chính sách AutoScalingReplacingUpdate (triển khai không gián đoạn) | 22/06/2026   | 22/06/2026      |
| 3   |  <br>&emsp; + Tìm hiểu các khái niệm cơ bản về AWS Elastic Disaster Recovery (AWS DRS): cách giảm thiểu thời gian ngừng hoạt động và mất dữ liệu, chỉ số RTO/RPO, tối ưu chi phí và phục hồi về một thời điểm (point-in-time recovery). <br>&emsp; + Nghiên cứu kiến trúc tổng quan của AWS DRS: sao chép đĩa máy chủ nguồn, cài đặt Replication Agent, máy chủ nhân bản trong vùng Staging Area VPC và các thực thể phục hồi mục tiêu. <br>&emsp; + Tìm hiểu các thành phần môi trường on-premises mô phỏng: public/private subnets, dịch vụ DNS, các ứng dụng cài sẵn. <br>&emsp; + Chuẩn bị kiến thức cơ bản: kết nối SSH đến máy chủ Linux và kết nối RDP đến máy chủ Windows bastion. | 23/06/2026   | 23/06/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 4   |  <br>&emsp; + Kết nối vào máy chủ Windows bastion qua RDP và các máy chủ Linux qua SSH. <br>&emsp; + Cài đặt AWS Replication Agent lên các máy chủ nguồn on-premises mô phỏng để đồng bộ hóa dữ liệu ở cấp độ block-level. <br>&emsp; + Cấu hình các thiết lập nhân bản trên bảng điều khiển AWS DRS và giám sát quá trình đồng bộ hóa dữ liệu ban đầu. <br>&emsp; + Thực hành các thao tác phục hồi thảm họa (Disaster Recovery): chạy thử nghiệm không gián đoạn (drill), Failover (chuyển đổi dự phòng khi có thảm họa) và Failback (phục hồi trở lại môi trường nguồn). | 24/06/2026   | 24/06/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Tìm hiểu Data Engineering Immersion Day. <br> - Lab 1: Phát hiện luồng click chuột bất thường bằng Amazon Managed Service for Apache Flink: <br>&emsp; + Chuẩn bị môi trường: Khởi tạo các tài nguyên (S3, Kinesis Stream, IAM Role). <br>&emsp; + Streaming ETL với Glue: Tạo Data Catalog, thiết lập ETL Job biến đổi dữ liệu real-time. <br>&emsp; + Real-time Streaming với Kinesis: Đẩy dữ liệu mô phỏng clickstream vào Kinesis. <br>&emsp; + Clickstream Analytics sử dụng MSK: Cấu hình Amazon Managed Streaming for Apache Kafka để phân tích sự kiện. | 25/06/2026   | 25/06/2026      | https://cloudjourney.awsstudygroup.com/>  |
| 6   | - Lab 2: Nhập data với DMS: <br>&emsp; + Thực hành DMS Migration Lab: Khởi tạo Replication Instance, cấu hình Source/Target Endpoints và chạy Database Migration Task. <br>&emsp; + Tùy chọn: Dùng CloudFormation để chạy AutoComplete DMS Lab (tự động hóa) hoặc Skip DMS Lab nếu không có thời gian. | 26/06/2026   | 26/06/2026      | https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 10:

* **Tự động hóa vá lỗi và triển khai Blue/Green cho AMI:**
  * Hiểu rõ tầm quan trọng của vá lỗi hệ điều hành (OS patching) đối với tính bảo mật và tuân thủ (compliance) của hệ thống.
  * Nắm vững phương pháp triển khai Blue/Green để tạo và thay thế AMI mà không gây gián đoạn dịch vụ.
  * Nghiên cứu và áp dụng tự động hóa quy trình vá lỗi thông qua sự kết hợp của các dịch vụ AWS: EC2 Image Builder (tự động hóa tạo AMI), Systems Manager (SSM) Automation Document (điều phối quy trình) và CloudFormation với chính sách AutoScalingReplacingUpdate.

* **Triển khai và vận hành phục hồi thảm họa với AWS Elastic Disaster Recovery (AWS DRS):**
  * Nắm vững các khái niệm cốt lõi về phục hồi thảm họa (Disaster Recovery), chỉ số RTO (Recovery Time Objective), RPO (Recovery Point Objective), tối ưu hóa chi phí và phục hồi về một thời điểm (point-in-time recovery).
  * Hiểu rõ kiến trúc hoạt động của AWS DRS bao gồm: cách cài đặt Replication Agent trên máy chủ nguồn (on-premises mô phỏng), cơ chế sao chép đĩa cấp độ block-level, vùng đệm Staging Area VPC và các thực thể phục hồi mục tiêu.
  * Thực hành kết nối thành công qua SSH/RDP vào các máy chủ nguồn Linux và Windows bastion.
  * Cài đặt AWS Replication Agent và cấu hình nhân bản trên AWS DRS console.
  * Thực hiện thành công các thao tác DR quan trọng: chạy thử nghiệm không ảnh hưởng hoạt động (drill), Failover (chuyển đổi dự phòng khi gặp sự cố) và Failback (phục hồi trở lại môi trường nguồn).

* **Phân tích dữ liệu thời gian thực (Data Engineering Immersion Day - Lab 1):**
  * Chuẩn bị môi trường hạ tầng dữ liệu bao gồm Amazon S3, Kinesis Stream và phân quyền IAM Roles phù hợp.
  * Xây dựng luồng Streaming ETL với AWS Glue bằng cách tạo Data Catalog và thiết lập Glue ETL Job để xử lý, chuyển đổi dữ liệu real-time.
  * Thực hành truyền dữ liệu thời gian thực (Real-time Streaming) bằng cách đẩy luồng dữ liệu clickstream mô phỏng vào Amazon Kinesis.
  * Nghiên cứu giải pháp Clickstream Analytics sử dụng Amazon Managed Streaming for Apache Kafka (Amazon MSK) và Amazon Managed Service for Apache Flink để phát hiện các luồng click chuột bất thường.

* **Nhập dữ liệu và chuyển dịch cơ sở dữ liệu với AWS DMS (Lab 2):**
  * Hiểu và thực hành quy trình dịch chuyển cơ sở dữ liệu sử dụng AWS Database Migration Service (AWS DMS).
  * Khởi tạo thành công Replication Instance, cấu hình các điểm đầu/cuối nguồn và đích (Source/Target Endpoints).
  * Thiết lập và chạy Database Migration Task để dịch chuyển dữ liệu một cách an toàn và tin cậy (hoặc tự động hóa bằng CloudFormation).



