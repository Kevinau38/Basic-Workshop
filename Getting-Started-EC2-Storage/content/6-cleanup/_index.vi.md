---
title: "Dọn dẹp tài nguyên"

weight: 6
chapter: false
pre: " <b> 6. </b> "
---

Chúng ta sẽ thực hiện các bước sau để xóa các tài nguyên đã tạo trong bài tập này.

#### Xóa EC2 instances

1. Truy cập [EC2 service management console](https://console.aws.amazon.com/ec2/v2/home)
   - Nhấp **Instances**.
   - Chọn cả hai EC2 instances (gốc và được khôi phục từ AMI).
   - Nhấp **Instance state**.
   - Nhấp **Terminate instance**, sau đó nhấp **Terminate** để xác nhận.

![clean](/images/6.clean/001-clean.png)

![clean](/images/6.clean/002-clean.png)

#### Xóa AMI và Snapshots

1. Truy cập [EC2 service management console](https://console.aws.amazon.com/ec2/v2/home)
   - Nhấp **AMIs**.
   - Chọn AMI chúng ta đã tạo.
   - Nhấp **Actions** → **Deregister AMI**.
   - Nhấp **Snapshots**.
   - Chọn các snapshots chúng ta đã tạo.
   - Nhấp **Actions** → **Delete snapshot**.

![clean](/images/6.clean/003-clean.png)

![clean](/images/6.clean/004-clean.png)

#### Xóa Security Group

1. Truy cập [EC2 service management console](https://console.aws.amazon.com/ec2/v2/home)
   - Nhấp **Security Groups**.
   - Chọn security group chúng ta đã tạo.
   - Nhấp **Actions**.
   - Nhấp **Delete security groups**, sau đó nhấp **Delete** để xác nhận.

![clean](/images/6.clean/005-clean.png)

![clean](/images/6.clean/006-clean.png)