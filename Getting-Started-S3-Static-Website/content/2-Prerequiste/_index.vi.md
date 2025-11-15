---
title: "Đăng ký domain với Route53"

weight: 2
chapter: false
pre: " <b> 2. </b> "
---

{{% notice info %}}

• **Region**: US East (N. Virginia) - us-east-1 (Bắt buộc cho Route53).  
• **Domain**: Chọn tên miền cho static website của bạn.  
{{% /notice %}}




Trong bước này, chúng ta sẽ đăng ký một tên miền tùy chỉnh sử dụng Amazon Route53. Tên miền này là bắt buộc cho trải nghiệm workshop hoàn chỉnh vì chúng ta sẽ cấu hình nó để truy cập static website của bạn với URL tùy chỉnh thay vì endpoint S3 website mặc định.

## Kiểm tra tính khả dụng của Domain

1. Vào **Route53 Console** → **Registered domains**
2. Click **Register domain**

![Check-Domain](/images/2.prerequisite/001-domain.png)

3. Nhập tên miền mong muốn (ví dụ: `basic-workshop.click`)
4. Click **Search** để xác minh tính khả dụng

![Check-Domain](/images/2.prerequisite/002-domain.png)

5. Nếu có sẵn, chọn domain và click **Proceed to checkout**

![Check-Domain](/images/2.prerequisite/003-domain.png)

![Check-Domain](/images/2.prerequisite/004-domain.png)

## Đăng ký Domain với Route53

1. Xem lại lựa chọn domain trong giỏ hàng
2. Chọn thời gian đăng ký (tối thiểu 1 năm)
3. **Auto-renew**: click để **Disable** và click Next

![Register-Domain](/images/2.prerequisite/005-domain.png)

4. Điền thông tin liên hệ:
   - **Contact Type**: Person
   - **First Name**: Tên của bạn
   - **Last Name**: Họ của bạn
   - **Email**: Địa chỉ email của bạn
   - **Phone**: Số điện thoại của bạn
   - **Address**: Địa chỉ của bạn
   - **Country**: Quốc gia của bạn
   - **City**: Thành phố của bạn
   - **Zip code**: Mã bưu điện của thành phố
5. **Privacy Protection**: Enable
6. **Admin contact**: Same as the registrant contact
7. **Tech contact**: Same as the registrant contact
8. **Billing contact**: Same as the registrant contact
9. Click **Next**

![Register-Domain](/images/2.prerequisite/006-domain.png)

![Register-Domain](/images/2.prerequisite/007-domain.png)

10. Xem lại tất cả thông tin bạn đã nhập
11. Click vào checkbox **Terms and Conditions**
12. Click **Submit**

![Register-Domain](/images/2.prerequisite/008-domain.png)

![Register-Domain](/images/2.prerequisite/009-domain.png)

## Xác minh đăng ký Domain

1. Vào **Route53 Console** → **Requests**
2. Đợi trạng thái domain thay đổi thành **Successful**
3. Lưu ý: Đăng ký domain có thể mất đến 15 phút
4. Sau khi đăng ký, domain sẽ xuất hiện trong danh sách registered domains của bạn

![Verify-Domain](/images/2.prerequisite/010-domain.png)

![Verify-Domain](/images/2.prerequisite/011-domain.png)

{{% notice warning %}}
**Quan trọng**: Đăng ký domain không thể hoàn tiền. Hãy chắc chắn bạn muốn giữ domain trước khi hoàn tất việc mua. Chi phí thông thường cho domain `.click` khoảng $3-5 mỗi năm.
{{% /notice %}}

Bây giờ chúng ta đã đăng ký thành công domain, hãy tiến hành tạo S3 bucket để host static website của chúng ta.