---
title: "Tạo S3 bucket"

weight: 3
chapter: false
pre: " <b> 3. </b> "
---

{{% notice info %}}

• **Region**: US East (N. Virginia) - us-east-1 (Bắt buộc cho S3 static website hosting).  
• **Bucket name**: Phải khớp chính xác với tên miền của bạn.  
{{% /notice %}}

Trong bước này, chúng ta sẽ tạo một S3 bucket để host static website của chúng ta. Tên bucket phải khớp chính xác với tên miền của bạn để cấu hình custom domain hoạt động đúng cách.

## Tạo S3 Bucket

1. Vào **S3 Console** → **Buckets**
2. Click **Create bucket**

![Create-S3-Bucket](/images/3.connect/001-s3.png)

3. **Bucket name**: Nhập tên miền của bạn (ví dụ: `s3static.basic-workshop.click`)

![Create-S3-Bucket](/images/3.connect/002-s3.png)

4. **Block Public Access settings**: Bỏ check **Block all public access**
5. Check **I acknowledge that the current settings might result in this bucket and the objects within becoming public**

![Create-S3-Bucket](/images/3.connect/003-s3.png)

6. Click **Create bucket**

![Create-S3-Bucket](/images/3.connect/004-s3.png)

Bây giờ chúng ta đã tạo S3 bucket, hãy tiến hành kích hoạt cài đặt static website hosting.