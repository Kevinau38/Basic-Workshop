---
title: "Tạo IAM Role"

weight: 2
chapter: false
pre: " <b> 2.2 </b> "
---

### Tạo IAM Role

Trong bước này, chúng ta sẽ tiến hành tạo IAM Role **EC2S3FullAccessRole**. Trong IAM Role này, policy **AmazonS3FullAccess**
sẽ được gán, cho phép EC2 server có quyền truy cập đầy đủ vào các dịch vụ S3.

1. Truy cập [giao diện quản trị dịch vụ IAM](https://console.aws.amazon.com/iamv2/)
2. Trong thanh điều hướng bên trái, click **Roles**.

![role](/images/2.prerequisite/023-iamrole.png)

3. Click **Create role**.

![role1](/images/2.prerequisite/024-iamrole.png)
4. Tại trang **Create role**:
- Trong phần **Select trusted entity**:
   - Trong trường **Trusted entity type**, click **AWS service**.
   - Trong trường **Use case**, click **EC2**.
- Click **Next**.

![role1](/images/2.prerequisite/025-iamrole.png)

5. Trong ô Search, nhập **AmazonS3FullAccess** và nhấn Enter để tìm kiếm policy này.

- Click policy **AmazonS3FullAccess**.
- Click **Next**

![createpolicy](/images/2.prerequisite/026-iamrole.png)

6. Trong phần **Name, review, and create**:
- Trong trường **Role name**, nhập **EC2S3FullAccessRole**.
- Click **Create Role**.

![namerole](/images/2.prerequisite/027-iamrole.png)

7. Sau khi tạo role thành công, bạn sẽ thấy **EC2S3FullAccessRole** được liệt kê trong dashboard IAM Roles,
xác nhận rằng role đã được tạo và sẵn sàng để gắn vào EC2 instances.

![namerole](/images/2.prerequisite/028-iamrole.png)

Tiếp theo, chúng ta sẽ kết nối đến **EC2 instance** chúng ta đã tạo qua **SSH**.