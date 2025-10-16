---
title: "Chuẩn bị "

weight: 2
chapter: false
pre: " <b> 2. </b> "
---

{{% notice info %}}

• **Region**: Singapore - ap-southeast-1 (Khuyến nghị).  
• **VPC**: Default VPC.  
• **Instance**: Tạo 1 Linux instance trên public subnet.  
{{% /notice %}}




Trong giai đoạn chuẩn bị này, chúng ta sẽ thiết lập các thành phần nền tảng cần thiết cho workshop EC2 Storage. Chúng ta sẽ tạo một Security Group để truy cập mạng, khởi chạy một EC2 instance với web server, và sau đó tạo các tài nguyên liên quan đến storage bao gồm EBS snapshots và Amazon Machine Image (AMI) cho các tình huống sao lưu và khôi phục.

### Nội dung

- [Chuẩn bị EC2](2.1-createec2/)
- [Tạo EBS Snapshot](2.2-create-ebs-snapshot/)
- [Tạo AMI](2.3-create-ami/)