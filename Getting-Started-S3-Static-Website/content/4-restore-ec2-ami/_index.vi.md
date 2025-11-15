---
title: "Kích hoạt cài đặt Static Website hosting"

weight: 4
chapter: false
pre: " <b> 4. </b> "
---

{{% notice info %}}

• **Index document**: index.html  
• **Error document**: error.html  
{{% /notice %}}

Trong bước này, chúng ta sẽ kích hoạt static website hosting trên S3 bucket và cấu hình các tài liệu index và error.

## Kích hoạt Static Website Hosting

1. Vào **S3 Console** và click vào bucket của bạn
2. Click vào tab **Properties**

![Enable-Static-Hosting](/images/4.restore-ec2-ami/001-staticwebsite.png)

3. Cuộn xuống phần **Static website hosting**
4. Click **Edit**

![Enable-Static-Hosting](/images/4.restore-ec2-ami/002-staticwebsite.png)

5. Chọn **Enable** cho Static website hosting
6. **Hosting type**: Host a static website
7. **Index document**: `index.html`
8. **Error document**: `error.html`

![Enable-Static-Hosting](/images/4.restore-ec2-ami/003-staticwebsite.png)

9. Click **Save changes**

![Enable-Static-Hosting](/images/4.restore-ec2-ami/004-staticwebsite.png)

10. Ghi chú **Bucket website endpoint** URL xuất hiện - copy URL này vì nó sẽ được sử dụng để truy cập website của bạn

![Enable-Static-Hosting](/images/4.restore-ec2-ami/005-staticwebsite.png)

## Upload Website Files

1. Download các file cần thiết:
   - index.html - Trang website chính
   - error.html - Trang lỗi
2. Vào **S3 Console** và click vào bucket của bạn
3. Click **Upload**

![Upload-Files](/images/4.restore-ec2-ami/006-staticwebsite.png)

4. Click **Add files**
5. Chọn cả hai file `index.html` và `error.html` từ downloads của bạn
6. Click **Upload**

![Upload-Files](/images/4.restore-ec2-ami/007-staticwebsite.png)

7. Đợi quá trình upload hoàn tất

![Upload-Files](/images/4.restore-ec2-ami/008-staticwebsite.png)

## Cấu hình Bucket Policy cho Public Access

1. Click vào tab **Permissions**
2. Cuộn xuống phần **Bucket policy**
3. Click **Edit**

![Bucket-Policy](/images/4.restore-ec2-ami/009-staticwebsite.png)

4. Thêm bucket policy sau (thay thế `your-bucket-arn` bằng Bucket ARN của bạn):

```json
{
  "Id": "Policy1",
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "s3-static-website",
      "Action": [
        "s3:GetObject"
      ],
      "Effect": "Allow",
      "Resource": "replace-this-string-with-your-bucket-arn/*",
      "Principal": "*"
    }
  ]
}
```

5. Click **Save changes**

![Bucket-Policy](/images/4.restore-ec2-ami/010-staticwebsite.png)

Bây giờ chúng ta đã thành công kích hoạt static website hosting, upload các file HTML, và cấu hình public access với bucket policy phù hợp, hãy tiến hành kiểm tra chức năng website và xác minh rằng mọi thứ đang hoạt động chính xác.