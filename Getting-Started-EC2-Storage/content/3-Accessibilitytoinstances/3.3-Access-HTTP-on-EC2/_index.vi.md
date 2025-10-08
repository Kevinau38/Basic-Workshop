---
title: "Truy cập HTTP trên EC2"

weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---

1. Truy cập [giao diện quản trị dịch vụ EC2](https://console.aws.amazon.com/ec2/v2/home).

- Tại trang **Instances**:
- Click **Lab EC2 - chúng ta tạo ở Lab trước**.
- Sau đó click **Copy our Public IPv4 address**

![KếtNối](/images/3.connect/006-connect.png)

2. Truy cập **http://{public ip}** trong trình duyệt web **(lưu ý: sử dụng http, không phải https)**.

![KếtNối](/images/3.connect/007-connect.png)

![KếtNối](/images/3.connect/008-connect.png)

3. Chúng ta đã tìm hiểu **3 cách** để kết nối đến **EC2**: **SSH**, **Console**, và **http://{EC2 public IP}**. Tiếp theo, chúng ta sẽ gắn role
**EC2S3FullAccessRole** vào **EC2**.