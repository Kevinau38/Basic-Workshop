---
title: "Tạo EBS Snapshot"

weight: 2
chapter: false
pre: " <b> 2.2 </b> "
---

{{% notice info %}}

Hoàn thành phần rước, sau đó quay lại hoàn thành các phần còn lại **2.2** và **2.3** của giai đoạn chuẩn bị.
{{% /notice %}}

### Tạo EBS Snapshot

Trong bước này, chúng ta sẽ tạo một EBS snapshot của root volume của EC2 instance. EBS snapshots là các bản sao lưu tại thời điểm cụ thể của EBS volumes được lưu trữ trong Amazon S3. Các snapshots này có thể được sử dụng để tạo volumes mới hoặc khôi phục dữ liệu.

1. Truy cập [EC2 service management console](https://console.aws.amazon.com/ec2/v2/home)

2. Trong thanh điều hướng bên trái, nhấp vào **Volumes**.

![role](/images/2.prerequisite/023-createebsvolumes.png)

3. Chọn volume của instance đã tạo, nhấp chuột phải và chọn **Create snapshot**.

![role1](/images/2.prerequisite/024-createebsvolumes.png)

4. Tại trang **Create snapshot**:
- Trong phần **Snapshot details**:
   - Trong trường **Description**, nhập **Snapshot for bastion host volume**.
- Trong phần **Tags**:
   - Trong trường **Key**, nhập **Name**.
   - Trong trường **Value - optional**, nhập **Lab EBS Snapshot**.
- Nhấp **Create snapshot**.

![role1](/images/2.prerequisite/025-createebsvolumes.png)

5. Từ menu bên trái trong EC2 console, nhấp vào **Snapshots** để xác minh rằng snapshot đã được tạo.

![createpolicy](/images/2.prerequisite/026-createebsvolumes.png)

6. Chờ một lúc và bạn sẽ thấy trạng thái Snapshot chuyển sang **Completed**, cho biết đã thành công.

![namerole](/images/2.prerequisite/027-createebsvolumes.png)

Tiếp theo, chúng ta sẽ tiến hành **tạo AMI**.