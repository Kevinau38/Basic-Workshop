---
title: "Chuẩn bị"

weight: 2
chapter: false
pre: " <b> 2. </b> "
---

{{% notice info %}}

• **Region**: Singapore - ap-southeast-1 (Khuyến nghị).  
• **VPC**: Default VPC.  
• **Instance**: Tạo 1 Linux instance trên public subnet.  
{{% /notice %}}




Để quản lý an toàn các EC2 instances trên AWS, đặc biệt trong kiến trúc VPC, chúng ta cần cấu hình các quyền và cài đặt mạng phù hợp. Như một phần của việc chuẩn bị, chúng ta sẽ tạo một IAM Role để cấp các quyền cần thiết cho EC2 instances tương tác với các dịch vụ AWS khác như Amazon S3 và Amazon VPC.

### Nội dung

- [Chuẩn bị EC2](2.1-createec2/)
- [Tạo IAM Role](2.2-createiamrole/)