---
title: "Bản đề xuất"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

# AI-Powered Data Extraction & Summarization Platform
## Dự án nhóm: Giải pháp tự động hoá thu thập và tổng hợp dữ liệu sử dụng AWS & Amazon Bedrock

### 1. Tóm tắt điều hành  
Dự án "AI-Powered Data Extraction & Summarization Platform" được thiết kế và phát triển bởi nhóm chúng em nhằm giải quyết bài toán tự động thu thập, trích xuất và tóm tắt khối lượng lớn dữ liệu từ các nguồn API bên ngoài. Thay vì xử lý thủ công tốn thời gian, nền tảng tận dụng sức mạnh của Amazon Bedrock (Generative AI) kết hợp với kiến trúc AWS có khả năng mở rộng cao (EC2 Auto Scaling, SQS, EventBridge) để xử lý dữ liệu định kỳ một cách hoàn toàn tự động, an toàn và tối ưu chi phí.

### 2. Tuyên bố vấn đề  
*Vấn đề hiện tại*  
Hiện tại, việc thu thập thông tin từ các nguồn dữ liệu bên ngoài (External APIs) và tóm tắt nội dung đang được thực hiện thủ công hoặc thông qua các kịch bản (script) rời rạc. Điều này dẫn đến sự thiếu ổn định, khó mở rộng khi lượng dữ liệu tăng lên, và tiêu tốn nhiều thời gian của nhân sự để đọc và phân tích dữ liệu.

*Giải pháp của nhóm*  
Nhóm chúng tôi đề xuất một hệ thống tự động hóa hoàn toàn trên AWS. Giao diện người dùng được phân phối qua CloudFront. Backend xử lý dữ liệu chạy trên các máy chủ EC2 (nằm trong Private Subnet để bảo mật) được quản lý bởi Auto Scaling Group. Quá trình lấy dữ liệu và xử lý được lập lịch tự động mỗi 8 giờ bởi EventBridge và SQS. Sức mạnh cốt lõi của giải pháp là việc tích hợp Amazon Bedrock để AI tự động đọc hiểu, làm sạch và tóm tắt dữ liệu. Kết quả được lưu trữ bền vững trên S3 và DynamoDB.

*Lợi ích và hoàn vốn đầu tư (ROI)*  
Giải pháp giúp tự động hóa 100% quy trình thu thập và báo cáo dữ liệu định kỳ, tiết kiệm hàng chục giờ làm việc mỗi tuần cho đội ngũ phân tích. Bằng việc sử dụng Auto Scaling và giới hạn tài nguyên, hệ thống tối ưu được chi phí vận hành do chỉ cấp phát tài nguyên khi thực sự có tác vụ xử lý dữ liệu.

### 3. Kiến trúc giải pháp và Luồng chạy (Execution Flow)
Kiến trúc của dự án được nhóm thiết kế tuân thủ các tiêu chuẩn bảo mật (Security) và độ sẵn sàng cao (High Availability) trên AWS. Đảm bảo luồng dữ liệu được xử lý khép kín và an toàn.

![Architecture Diagram](/images/2-Proposal/cloudbrief-current-architecture.drawio.png)


*Luồng chạy chi tiết của dự án (Execution Flow):*
1. **Giao tiếp người dùng (Frontend)**: Người dùng truy cập ứng dụng thông qua **CloudFront** (được bảo vệ bởi **AWS WAF**). CloudFront phân phối nội dung tĩnh từ **S3 bucket (frontend, private, versioned)** một cách an toàn thông qua tính năng OAC (Origin Access Control) cùng các behavior đã thiết lập.
2. **Kích hoạt tự động hóa**: **EventBridge Trigger** được cấu hình để kích hoạt mỗi 8 giờ, gửi thông điệp vào hàng đợi **SQS** để bắt đầu quy trình trích xuất dữ liệu.
3. **Mạng lưới tính toán**: Hệ thống sử dụng **Auto Scaling Group** quản lý các **EC2 Worker**. Các máy chủ này được phân bổ vào các **Private Subnet (A và B)** (không có Public IP) nhằm đảm bảo an ninh. Các Worker này liên tục kéo (pull) công việc (job) từ hàng đợi thông qua **SQS VPC Endpoint**.
4. **Thu thập dữ liệu (Outbound Traffic)**: Để lấy dữ liệu từ **External API**, các EC2 Worker kết nối ra internet thông qua **NAT Gateway** (đặt ở Public Subnet) và đi qua **Internet Gateway**.
5. **Tích hợp Generative AI**: Sau khi lấy được dữ liệu, EC2 Worker đẩy nội dung sang **Amazon Bedrock** thông qua **Bedrock VPC Endpoint** để mô hình AI xử lý ngôn ngữ thực hiện việc trích xuất thông tin và tóm tắt.
6. **Lưu trữ kết quả an toàn**: 
   - Dữ liệu văn bản sau khi làm sạch (Cleaned content) được Worker đẩy trực tiếp vào **S3 bucket** thông qua **S3 Gateway Endpoint**.
   - Các siêu dữ liệu (metadata), thông tin có cấu trúc được lưu vào **DynamoDB** thông qua **DynamoDB VPC Endpoint**. Cơ sở dữ liệu này được cấu hình sao lưu (Backup) tự động.
   - Các thông điệp trạng thái hoặc job tóm tắt nâng cao có thể được đẩy vào hàng đợi **SQS Summarize** cũng qua SQS Endpoint.
7. **Giám sát và Vận hành (Monitoring & Alerting)**:
   - Các EC2 Worker được quản trị thông qua **Systems Manager (Session Manager - SSM)**, không cần mở cổng SSH.
   - Toàn bộ logs và metrics (chỉ số) được thu thập bởi **CloudWatch**.
   - Nếu hệ thống phát hiện bất thường vượt ngưỡng (CloudWatch Alarm), thông báo sẽ được gửi qua **SNS Topic** đến **Email của Admin**.
8. **Bảo mật và Chi phí**:
   - Sử dụng **Security Group** và **IAM Role** cho ASG với nguyên tắc đặc quyền tối thiểu (least scoped).
   - Thiết lập **AWS Budgets** để tự động gửi email cảnh báo khi chi phí hệ thống vượt mức kiểm soát.

### 4. Triển khai kỹ thuật  
*Phân công và các giai đoạn thực hiện của nhóm:*
- **Giai đoạn 1 (Thiết kế & Khởi tạo)**: Nhóm xây dựng mạng VPC nền tảng với đầy đủ Public/Private Subnets, NAT Gateway. Thiết lập S3 Frontend bảo mật qua CloudFront và WAF.
- **Giai đoạn 2 (Tích hợp AI & Lập lịch)**: Cài đặt cấu hình Auto Scaling Group cho EC2 Worker. Xây dựng lịch trình EventBridge và SQS. Phát triển mã nguồn cho EC2 Worker gọi External API và Amazon Bedrock.
- **Giai đoạn 3 (Lưu trữ nội bộ)**: Thiết lập các VPC Endpoints (S3, DynamoDB, SQS, Bedrock) để đảm bảo traffic không đi qua mạng internet công cộng. Tạo các bảng DynamoDB và S3 bucket tương ứng.
- **Giai đoạn 4 (Giám sát & Hoàn thiện)**: Tích hợp CloudWatch, SNS, Systems Manager. Rà soát, kiểm thử các IAM Roles, Security Groups để nghiệm thu dự án.

### 5. Lộ trình & Mốc triển khai  
- **Tuần 10**: Thống nhất sơ đồ kiến trúc, thiết lập mạng VPC và hạ tầng bảo mật cơ bản.
- **Tuần 10**: Viết mã nguồn cho Worker thu thập dữ liệu và tích hợp thành công với Amazon Bedrock.
- **Tuần 11**: Cấu hình EC2 Auto Scaling, EventBridge, SQS và kiểm thử kết nối qua các VPC Endpoints.
- **Tuần 12**: Thiết lập CloudWatch monitoring, SNS alerts, tiến hành kiểm thử bảo mật và trình bày kết quả dự án nhóm.

### 6. Đánh giá rủi ro và Kế hoạch dự phòng 
- **Lỗi kết nối tới External API**: Xây dựng cơ chế *Retry* kết hợp lưu trữ lại công việc chưa hoàn thành trong SQS.
- **Chi phí phát sinh từ Amazon Bedrock**: Đặt các mức trần trong *AWS Budgets* để cảnh báo nhóm ngay lập tức nếu chi phí tăng bất thường.
- **Rủi ro bảo mật máy chủ**: Tuyệt đối không cấp Public IP cho EC2, sử dụng *Session Manager* để truy cập và đóng tất cả các in-bound port không cần thiết trên Security Group.

### 7. Kết quả kỳ vọng  
Dự án kiến trúc AWS của nhóm sẽ tạo ra một luồng xử lý dữ liệu mạnh mẽ, kết hợp khả năng tính toán linh hoạt (EC2 Auto Scaling) và sức mạnh trí tuệ nhân tạo (Amazon Bedrock). Cấu trúc mạng VPC cô lập kết hợp các Endpoint giúp đáp ứng hoàn toàn tiêu chuẩn bảo mật doanh nghiệp (Enterprise-grade security), biến đây thành một giải pháp đáng tin cậy cho bất kỳ hệ thống phân tích, tổng hợp dữ liệu nào.