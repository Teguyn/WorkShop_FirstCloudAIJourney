---
title: "Các bài blogs đã đăng"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 3. </b> "
---

Các bài blogs đã đăng trên group Facebook [AWS Study Group](https://www.facebook.com/groups/awsstudygroupfcj). 

### [Blog 1 - Vì sao Epic Games phát triển Lore và cách AWS giúp tối ưu lưu trữ binary assets](3.1-Blog1/)
Bài viết tìm hiểu về Lore – hệ thống version control mã nguồn mở của Epic Games dành riêng cho các tệp nhị phân (binary assets) và kiến trúc triển khai trên các dịch vụ AWS như EC2, ECS, S3, DynamoDB giúp tối ưu hóa dung lượng cũng như chi phí lưu trữ cho các studio phát triển game.

### [Blog 2 - Kiến trúc bảo mật Serverless: Cách bảo vệ ứng dụng AI Riddle Generator trên AWS](3.2-Blog2/)
Bài viết chia sẻ phương pháp áp dụng mô hình bảo mật nhiều lớp (Defense in Depth) trên AWS để bảo vệ toàn diện ứng dụng Serverless kết hợp AI. Nội dung bao gồm việc sử dụng AWS WAF, CloudFront chống DDoS vòng ngoài, Amazon Cognito & API Gateway để kiểm soát xác thực người dùng, và cấu hình phân quyền tối thiểu (Least Privilege) qua AWS IAM.

### [Blog 3 - Cách một tổ chức cắt giảm 39% chi phí AWS trong 12 tuần](3.3-Blog3/)
Bài viết phân tích chiến lược tối ưu hóa chi phí điện toán đám mây qua 3 giai đoạn (Phase) của một tổ chức SaaS, từ việc nâng cấp EBS gp2 sang gp3, cấu hình VPC Gateway Endpoint cho S3 để giảm chi phí NAT Gateway, đến việc gom cụm Load Balancer và ứng dụng Karpenter để tối ưu hóa EKS/compute node sử dụng chip ARM Graviton.