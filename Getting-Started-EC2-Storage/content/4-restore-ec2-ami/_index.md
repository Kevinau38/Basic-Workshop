---
title: "Restore EC2 from AMI"

weight: 4
chapter: false
pre: " <b> 4. </b> "
---

1. Go to [EC2 service management console](https://console.aws.amazon.com/ec2/v2/home)

2. In the left navigation bar, click **AMIs**.

![role](/images/4.restore-ec2-ami/001-s3.png)

3. Select the AMI we created earlier, right-click and select **Launch instances from AMI**.

![role1](/images/4.restore-ec2-ami/002-s3.png)

4. At the **Launch an instance** page:
- In the **Name** field, enter **Lab EC2 host from AMI**.
- Configure the instance settings as needed (use default settings for this Lab).
- In the **Key pair** section, select the same key pair used for the original instance.
- In the **Network settings**:
   - Use the same VPC, subnet, and security group as the original instance.
   - **Auto-assign public IP**: Enable.
- Click **Launch instance**.

![role1](/images/4.restore-ec2-ami/003-s3.png)

![role1](/images/4.restore-ec2-ami/004-s3.png)

5. Wait for the new instance to be in **Running** state.

![role1](/images/4.restore-ec2-ami/005-s3.png)

Next, we will proceed to **verify webserver and created file** to confirm data persistence.