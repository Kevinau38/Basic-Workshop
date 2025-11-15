---
title: "Kiểm tra website"

weight: 5
chapter: false
pre: " <b> 5. </b> "
---

Trong bước này, chúng ta sẽ kiểm tra static website để xác minh rằng nó hoạt động chính xác. Chúng ta sẽ kiểm tra cả trang chính (index.html) và chức năng trang lỗi (error.html).

## Kiểm tra Website chính

1. Sử dụng static website URL (endpoint đã copy trước đó)
2. Hoặc vào **S3 Bucket** → tab **Properties** → cuộn xuống phần **Static website hosting** để tìm URL
3. Copy **Bucket website endpoint** URL
4. Mở trình duyệt web và paste URL
5. Bạn sẽ thấy nội dung của file `index.html` được hiển thị

![Test-Main-Page](/images/5.verify/001-test.png)

## Kiểm tra trang Error

1. Trong trình duyệt, truy cập cùng URL nhưng thêm một số ký tự ngẫu nhiên ở cuối
2. Ví dụ: `your-website-url/random-characters` hoặc `your-website-url/nonexistent-page`
3. Bạn sẽ thấy nội dung của file `error.html` được hiển thị
4. Điều này chứng minh rằng cấu hình trang lỗi đang hoạt động chính xác

![Test-Error-Page](/images/5.verify/002-test.png)

## Xác minh chức năng Website

1. Xác nhận rằng cả hai trang đều load chính xác
2. Kiểm tra rằng hình ảnh và styling được hiển thị đúng cách
3. Xác minh rằng trang lỗi xuất hiện khi truy cập các trang không tồn tại

![Test-Main-Page](/images/5.verify/001-test.png)

![Test-Error-Page](/images/5.verify/002-test.png)

Chúng ta đã kiểm tra thành công static website. Cả trang chính và trang lỗi đều hoạt động chính xác. Tiếp theo, chúng ta sẽ tiến hành cấu hình Route53 để truy cập custom domain.