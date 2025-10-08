---
title: "Kết nối qua SSH"

weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

{{% notice info %}}

• Tải **AWS CLI** trước: https://awscli.amazonaws.com/AWSCLIV2.msi.   
• **Windows**: Sử dụng Git Bash trong thư mục chứa key pair file.  
• **Mac**: Sử dụng Terminal trong thư mục chứa key pair file.   
{{% /notice %}}

1. Truy cập [giao diện quản trị dịch vụ EC2](https://console.aws.amazon.com/ec2/v2/home).

- Tại trang **Instances**:
  - Click **Lab EC2 - chúng ta tạo ở Lab trước**.
  - Sau đó click **Connect**.

![KếtNối](/images/3.connect/001-connect.png)

2. Tại trang **Connect to instance**:

- Click tab **SSH client** để lấy lệnh SSH.
- **Lệnh 1** để thiết lập quyền thực thi cho file .pem.
- **Lệnh 2** để SSH vào EC2 (đảm bảo tên key pair file đúng).

![KếtNối](/images/3.connect/002-connect.png)

3. Mở **Git Bash** và điều hướng đến thư mục chứa key pair file:

• Sử dụng lệnh **ls** để xác minh **file .pem** có trong thư mục hiện tại:

```
ls
```

• Chạy **lệnh 1** để thiết lập quyền cho key file:

```
chmod 400 "d-key-common.pem"
```

• Chạy lệnh 2 để SSH vào EC2 instance:

```
  ssh -i "your-key-pair.pem" ec2-user@your-ec2-public-ip
```

• Khi được nhắc với thông báo xác thực, gõ yes để tiếp tục kết nối:

```
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
```

• Bạn sẽ thấy thông báo chào mừng Amazon Linux, cho biết kết nối thành công.

![KếtNối](/images/3.connect/003-connect.png)