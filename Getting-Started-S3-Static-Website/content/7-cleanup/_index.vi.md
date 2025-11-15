---
title: "Dọn dẹp tài nguyên"

weight: 7
chapter: false
pre: " <b> 7. </b> "
---

Chúng ta sẽ thực hiện các bước sau để xóa các tài nguyên đã tạo trong bài tập này để tránh phí không cần thiết.

## Xóa Route53 DNS Record

1. Vào **Route53 Console** → **Hosted zones**
2. Click vào tên domain của bạn

![Delete-Route53](/images/7.clean/001-clean.png)

3. Chọn **A record** cho `s3static`
4. Click **Delete record**

![Delete-Route53](/images/7.clean/002-clean.png)

5. Click **Delete** để xác nhận

![Delete-Route53](/images/7.clean/003-clean.png)

## Làm trống và Xóa S3 Bucket

1. Vào **S3 Console** → **Buckets**
2. Click vào tên bucket của bạn

![Delete-S3-Bucket](/images/7.clean/004-clean.png)

3. Chọn tất cả objects trong bucket
4. Click **Delete**

![Delete-S3-Bucket](/images/7.clean/005-clean.png)

5. Gõ `permanently delete` để xác nhận
6. Click **Delete objects**

![Delete-S3-Bucket](/images/7.clean/006-clean.png)

7. Quay lại danh sách buckets
8. Chọn bucket của bạn
9. Click **Delete**

![Delete-S3-Bucket](/images/7.clean/007-clean.png)

10. Gõ tên bucket để xác nhận
11. Click **Delete bucket**

![Delete-S3-Bucket](/images/7.clean/008-clean.png)

Chúc mừng! Bạn đã hoàn thành thành công workshop S3 Static Website và dọn dẹp tất cả tài nguyên. Bạn đã học cách tạo static website sử dụng S3, cấu hình custom domain với Route53, và quản lý tài nguyên AWS một cách hiệu quả.