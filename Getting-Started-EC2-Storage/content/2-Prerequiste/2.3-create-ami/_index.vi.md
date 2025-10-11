---
title: "Tạo AMI"

weight: 3
chapter: false
pre: " <b> 2.3 </b> "
---

### Tạo AMI

Trong bước này, chúng ta sẽ tạo một Amazon Machine Image (AMI) từ EC2 instance của chúng ta. AMI là một template chứa cấu hình phần mềm (hệ điều hành, application server và các ứng dụng) cần thiết để khởi chạy một instance. AMI này sẽ ghi lại trạng thái hiện tại của instance bao gồm bất kỳ phần mềm và cấu hình nào đã cài đặt.

1. Truy cập [EC2 service management console](https://console.aws.amazon.com/ec2/v2/home)

2. Trong thanh điều hướng bên trái, nhấp **Instances**.

![role](/images/2.prerequisite/028-createami.png)

3. Chọn instance đã tạo, nhấp chuột phải và chọn **Image and templates**. Sau đó nhấp **Create image**.

![role1](/images/2.prerequisite/029-createami.png)

4. Tại trang **Create image**:
- Trong phần **Image details**:
   - Trong trường **Image name**, nhập **Lab AMI**.
   - Trong trường **Tags - optional**, nhấp **Tag image and snapshots separately**:
      - Trong trường **Key** của **Tag image**, nhập **Name**.
      - Trong trường **Value - optional** của **Tag image**, nhập **Lab AMI**.
      - Trong trường **Key** của **Tag snapshots**, nhập **Name**.
      - Trong trường **Value - optional** của **Tag snapshots**, nhập **Lab AMI Snapshot**.


- Nhấp **Create image**.

![role1](/images/2.prerequisite/030-createami.png)

![role1](/images/2.prerequisite/031-createami.png)

5. Từ menu bên trái trong EC2 console, nhấp **AMIs** để xác minh rằng AMI đã được tạo.

![createpolicy](/images/2.prerequisite/032-createami.png)

6. Chờ một lúc và bạn sẽ thấy trạng thái AMI chuyển thành **Available**, cho biết thành công.

![namerole](/images/2.prerequisite/033-createami.png)

Tiếp theo, chúng ta sẽ tiếp tục với [**Khôi phục EC2 từ AMI**]({{< ref "4-restore-ec2-ami" >}}).