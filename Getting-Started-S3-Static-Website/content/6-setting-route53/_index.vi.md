---
title: "Cấu hình Route53 để truy cập http://s3static.{domain}"

weight: 6
chapter: false
pre: " <b> 6. </b> "
---

Trong bước này, chúng ta sẽ cấu hình Route53 để tạo một subdomain tùy chỉnh trỏ đến S3 static website của chúng ta. Khi bạn mua domain trong Route53, AWS tự động tạo một public hosted zone với tên domain của bạn và bao gồm các record NS và SOA mặc định.

## Truy cập Route53 Hosted Zone

1. Vào **Route53 Console** → **Hosted zones**
2. Click vào tên domain của bạn (hosted zone đã được tự động tạo khi bạn đăng ký domain)
3. Bạn sẽ thấy các record **NS** và **SOA** mặc định

![Hosted-Zone](/images/6-setting-route53/001-setting-route53.png)

![Hosted-Zone](/images/6-setting-route53/002-setting-route53.png)

## Tạo A Record cho Subdomain

1. Click **Create record**
2. **Record name**: `s3static`
3. **Record type**: A
4. **Alias**: Enable (bật toggle)
5. **Route traffic to**: Alias to S3 website endpoint
6. **Region**: US East (N. Virginia) [us-east-1]
7. **S3 Endpoint**: Chọn bucket endpoint của bạn (sẽ hiển thị tên bucket)
8. Click **Create records**

![Create-Record](/images/6-setting-route53/003-setting-route53.png)

## Xác minh DNS Record

1. Sau khi tạo record, bạn sẽ thấy **A** record mới trong hosted zone
2. Record sẽ hiển thị **s3static.your-domain.com** trỏ đến S3 endpoint của bạn

![Verify-Record](/images/6-setting-route53/004-setting-route53.png)

## Kiểm tra truy cập Custom Domain

1. Mở trình duyệt web
2. Điều hướng đến: `http://s3static.your-domain.com` (thay thế bằng domain thực của bạn)
3. Bạn sẽ thấy static website load thông qua custom domain
4. Kiểm tra trang lỗi bằng cách thêm ký tự ngẫu nhiên: `http://s3static.your-domain.com/random`

![Test-Custom-Domain](/images/6-setting-route53/005-setting-route53.png)

![Test-Custom-Domain](/images/6-setting-route53/006-setting-route53.png)

Chúng ta đã cấu hình thành công Route53 để cung cấp truy cập custom domain cho S3 static website, cho phép người dùng truy cập website bằng tên miền thân thiện thay vì S3 endpoint URL. Bây giờ chúng ta đã hoàn thành toàn bộ workshop và static website hoạt động đầy đủ với truy cập custom domain, hãy tiến hành dọn dẹp các tài nguyên đã tạo để tránh phí không cần thiết.