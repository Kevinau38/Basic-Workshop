---
title: "Tạo EC2"

weight: 2
chapter: false
pre: " <b> 2.1.2 </b> "
---

#### Tạo EC2 **Lab EC2**

1. Truy cập [giao diện quản trị dịch vụ EC2](https://console.aws.amazon.com/ec2/v2/home)
   - Click **Instances**.
   - Click **Launch instances**.

![EC2](/images/2.prerequisite/005-createec2.png)

2. Tại trang **Launch instances**.
- Trong phần **Name and tags**:
   - Trong trường **Name**, nhập **Lab EC2**.
   - Bên phải trường **Name**, click **Add additional tags**.

![EC2](/images/2.prerequisite/006-createec2.png)

![EC2](/images/2.prerequisite/007-createec2.png)

- Trong phần **Application and OS Images (Amazon Machine Image)**:
   - Trong trường **Quick Start**, click **Amazon Linux**.

![EC2](/images/2.prerequisite/008-createec2.png)

- Trong phần **Instance type**:
   - Trong trường **Instance type**, click **t2.micro**.

![EC2](/images/2.prerequisite/009-createec2.png)

- Trong phần **Key pair (login)**:
   - Bên phải trường **Key pair name - required**, click **Create new key pair**.

![EC2](/images/2.prerequisite/010-createec2.png)

3. Tại trang **Create key pair**.
   - Trong trường **Key pair name**, nhập **d-key-common**.
   - Click **Create key pair**.

![EC2](/images/2.prerequisite/011-createec2.png)

   - Trong trường **Key pair name - required**, click **d-key-common** (Key chúng ta vừa tạo ở trên).

![EC2](/images/2.prerequisite/012-createec2.png)

- Trong phần **Network settings**:
   - Bên phải phần **Network settings**, click **Edit**.

![EC2](/images/2.prerequisite/013-createec2.png)

- Trong trường **VPC - required**, click **Default VPC**.
- Bên phải trường **Subnet**, click **Create new subnet**.
- Trong trường **Auto-assign public IP**, click **Enable**.
- Trong trường **Firewall (security groups)**, click **Select existing security group**.
- Trong trường **Common security groups**, click **Security groups - chúng ta tạo ở Lab trước**.

![EC2](/images/2.prerequisite/014-createec2.png)

4. Tại trang **Create subnet**.
- Trong phần **VPC**:
   - Trong trường **VPC ID**, click **Default VPC**.

![EC2](/images/2.prerequisite/015-createec2.png)

- Trong phần **Subnet settings**:
   - Trong trường **Subnet name**, nhập **my-subnet-01**.
   - Trong trường **Availability zone**, click **Asia Pacific (Singapore) / apse1-az2 (ap-southeast-1a)**.
   - Trong trường **IPv4 subnet CIDR block**, nhập **172.31.0.0/20**.
   - Click **Create subnet**.

![EC2](/images/2.prerequisite/016-createec2.png)

- Đây là kết quả sau khi tạo Subnet.

![EC2](/images/2.prerequisite/017-createec2.png)

5. Sau khi tạo **Subnet** - Chúng ta quay lại trang **Launch instances**.
- Trong phần **Network settings**:
   - Trong trường **Subnet**, click **my-subnet-01** (Subnet chúng ta vừa tạo ở trên).

![EC2](/images/2.prerequisite/018-createec2.png)

- Trong phần **Configure storage**:
   - Tất cả các tham số trong phần này sẽ được để mặc định.

![EC2](/images/2.prerequisite/019-createec2.png)

- Trong phần **Advanced details**:
   - Trong trường **User data - optional**, nhập:
 ```
 #!/bin/bash
yum update -y
yum install -y httpd.x86_64
systemctl start httpd.service
systemctl enable httpd.service
echo "Hello World from $(hostname -f)" > /var/www/html/index.html
 ```
 
 - Click **Launch instance**.

![EC2](/images/2.prerequisite/020-createec2.png)

- Instances đang khởi động - Chúng mất 3 đến 4 phút để khởi tạo.
![EC2](/images/2.prerequisite/021-createec2.png)

6. Vậy là chúng ta đã hoàn thành việc tạo **EC2**. Bước tiếp theo là tạo **IAM Role**

![EC2](/images/2.prerequisite/022-createec2.png)