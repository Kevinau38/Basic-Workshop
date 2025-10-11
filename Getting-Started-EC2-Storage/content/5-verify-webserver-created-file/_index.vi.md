---
title: "Kiểm tra webserver và file đã tạo"

weight: 5
chapter: false
pre: " <b> 5. </b> "
---

Trong bước này, chúng ta sẽ kết nối đến **EC2 instance mới được khôi phục từ AMI** và xác minh rằng **web server** và **test file** của chúng ta vẫn còn nguyên vẹn, chứng minh việc lưu trữ dữ liệu thành công thông qua sao lưu và khôi phục AMI.

1. Sau khi EC2 instance đang chạy, kết nối bằng EC2 Instance Connect để kiểm tra xem file được tạo trong **bước 3.3** có còn tồn tại không.

![role1](/images/5.verify/001-verify.png)

![role1](/images/5.verify/002-verify.png)

2. Sau khi kết nối, chạy lệnh sau để xác minh rằng file vẫn tồn tại:

```
ls
```

Bạn sẽ thấy file `test.txt` mà chúng ta đã tạo trước đó.

![role1](/images/5.verify/003-verify.png)

3. Tiếp theo, truy cập web server từ trình duyệt của bạn bằng địa chỉ public IP:

```
http://{public-ip}
```

![role1](/images/5.verify/004-verify.png)

4. Xác minh rằng web server vẫn đang chạy và hiển thị nội dung mong đợi.

![role1](/images/5.verify/005-verify.png)

Chúng ta đã hoàn thành thành công việc xác minh. Tiếp theo là bước thiết yếu **Dọn dẹp tài nguyên**.