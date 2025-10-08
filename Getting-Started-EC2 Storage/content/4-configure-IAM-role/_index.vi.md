---
title: "Cấu hình EC2 IAM role"

weight: 4
chapter: false
pre: " <b> 4. </b> "
---

1. Truy cập [giao diện quản trị dịch vụ EC2](https://console.aws.amazon.com/ec2/v2/home).

- Tại trang **Instances**:
  - Click **Lab EC2 - chúng ta tạo ở Lab trước**.
  - Click nút **Actions**.
  - Click **Security**.
  - Click **Modify IAM role**.

![S3](/images/4.configure-IAM-role/001-s3.png)

2. Chọn **Role - chúng ta tạo ở Lab trước** từ dropdown.
- Click Update IAM role.

![S3](/images/4.configure-IAM-role/002-s3.png)

3. Kiểm tra kết nối IAM role

- Kết nối đến EC2 instance sử dụng EC2 Instance Connect ([Phần 3.2: Kết nối qua Console]({{< ref "3-Accessibilitytoinstances/3.2-Console" >}})).
- Chạy lệnh sau để kiểm tra quyền truy cập S3:

```
  aws s3 ls
```

- **Kết quả mong đợi:**
  - Nếu bạn có S3 buckets: Danh sách buckets sẽ hiển thị
  - Nếu không có buckets: Không có output (trống), nhưng không có thông báo lỗi
  - **Chỉ báo thành công:** Không có lỗi permission denied hoặc authentication errors

![S3](/images/4.configure-IAM-role/003-s3.png)