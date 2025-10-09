---
title: "Cấu hình EC2 IAM role"

weight: 5
chapter: false
pre: " <b> 5. </b> "
---

Chúng ta sẽ thực hiện các bước sau để xóa các tài nguyên đã tạo trong bài tập này.

#### Xóa EC2 instance

1. Truy cập [giao diện quản trị dịch vụ EC2](https://console.aws.amazon.com/ec2/v2/home)
   - Click **Instances**.
   - Chọn **Instances của chúng ta**.
   - Click **Instance state**.
   - Click **Terminate instance**, sau đó click **Terminate** để xác nhận.

![DọnDẹp](/images/5.clean/001-clean.png)

![DọnDẹp](/images/5.clean/002-clean.png)

#### Xóa IAM Role

1. Truy cập [giao diện quản trị dịch vụ IAM](https://console.aws.amazon.com/iamv2/home#/home)
   - Click **Roles**.
   - Trong ô tìm kiếm, nhập **EC2S3FullAccessRole**.
   - Click để chọn **EC2S3FullAccessRole**.
   - Click **Delete**, sau đó nhập tên role **EC2S3FullAccessRole** và click **Delete** để xóa role.

![DọnDẹp](/images/5.clean/003-clean.png)

![DọnDẹp](/images/5.clean/004-clean.png)

#### Xóa Security Group

1. Truy cập [giao diện quản trị dịch vụ EC2](https://console.aws.amazon.com/ec2/v2/home)
   - Click **Security Groups**.
   - Chọn **Security groups của chúng ta**.
   - Click **Actions**.
   - Click **Delete security groups**, sau đó click **Delete** để xác nhận.

![DọnDẹp](/images/5.clean/005-clean.png)

![DọnDẹp](/images/5.clean/006-clean.png)