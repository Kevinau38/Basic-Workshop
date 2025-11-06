---
title: "Khôi phục EC2 từ AMI"

weight: 4
chapter: false
pre: " <b> 4. </b> "
---

1. Truy cập [EC2 service management console](https://console.aws.amazon.com/ec2/v2/home)

2. Trong thanh điều hướng bên trái, nhấp **AMIs**.

![role](/images/4.restore-ec2-ami/001-s3.png)

3. Chọn AMI chúng ta đã tạo trước đó, nhấp chuột phải và chọn **Launch instances from AMI**.

![role1](/images/4.restore-ec2-ami/002-s3.png)

4. Tại trang **Launch an instance**:
- Trong trường **Name**, nhập **Lab EC2 host from AMI**.
- Cấu hình các thiết lập instance theo nhu cầu (sử dụng thiết lập mặc định cho Lab này).
- Trong phần **Key pair**, chọn cùng key pair đã sử dụng cho instance gốc.
- Trong **Network settings**:
   - Sử dụng cùng VPC, subnet và security group như instance gốc.
   - **Auto-assign public IP**: Enable.
- Nhấp **Launch instance**.

![role1](/images/4.restore-ec2-ami/003-s3.png)

![role1](/images/4.restore-ec2-ami/004-s3.png)

5. Chờ instance mới ở trạng thái **Running**.

![role1](/images/4.restore-ec2-ami/005-s3.png)

Tiếp theo, chúng ta sẽ tiến hành **xác minh webserver và file đã tạo** để xác nhận tính bền vững của dữ liệu.