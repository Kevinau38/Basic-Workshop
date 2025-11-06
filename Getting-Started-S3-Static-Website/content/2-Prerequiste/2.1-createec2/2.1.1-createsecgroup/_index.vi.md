---
title: "Tạo security group"

weight: 1
chapter: false
pre: " <b> 2.1.1 </b> "
---

#### Tạo security group **Lab security group**

1. Truy cập [giao diện quản trị dịch vụ EC2](https://console.aws.amazon.com/ec2/v2/home)
   - Click **Security Groups**.
   - Click **Create security group**.

![SG](/images/2.prerequisite/001-createsg.png)

2. Tại trang **Create security group**.
- Trong phần **Basic details**:
   - Trong trường **Security group name**, nhập **Lab SG**.
   - Trong trường **Description**, nhập **Allow ssh and http from internet**.
   - Trong trường **VPC**, click **Default VPC**.
- Trong phần **Inbound rules**:
   - Trong trường **Type**, click **SSH**.
   - Trong trường **Source**, click **Anywhere-IPv4**.
   - Trong trường **Type**, click **HTTP**.
   - Trong trường **Source**, click **Anywhere-IPv4**.   
- Trong phần **Tags - optional**:
   - Trong trường **Key**, nhập **Name**.
   - Trong trường **Value - optional**, nhập **Lab SG**.
- Click **Create security group**.

![SG](/images/2.prerequisite/002-createsg.png)

![SG](/images/2.prerequisite/003-createsg.png)

3. Vậy là chúng ta đã hoàn thành việc tạo **Security Groups**. Bước tiếp theo là tạo **EC2**

![SG](/images/2.prerequisite/004-createsg.png)