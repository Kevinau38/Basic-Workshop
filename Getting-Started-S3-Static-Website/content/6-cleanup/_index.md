---
title: "Clean up resources"

weight: 6
chapter: false
pre: " <b> 6. </b> "
---

We will take the following steps to delete the resources we created in this exercise.

#### Delete EC2 instances

1. Go to [EC2 service management console](https://console.aws.amazon.com/ec2/v2/home)
   - Click **Instances**.
   - Select both EC2 instances (original and restored from AMI).
   - Click **Instance state**.
   - Click **Terminate instance**, then click **Terminate** to confirm.

![clean](/images/6.clean/001-clean.png)

![clean](/images/6.clean/002-clean.png)

#### Delete AMI and Snapshots

1. Go to [EC2 service management console](https://console.aws.amazon.com/ec2/v2/home)
   - Click **AMIs**.
   - Select the AMI we created.
   - Click **Actions** → **Deregister AMI**.
   - Click **Snapshots**.
   - Select the snapshots we created.
   - Click **Actions** → **Delete snapshot**.

![clean](/images/6.clean/003-clean.png)

![clean](/images/6.clean/004-clean.png)

#### Delete Security Group

1. Go to [EC2 service management console](https://console.aws.amazon.com/ec2/v2/home)
   - Click **Security Groups**.
   - Select the security group we created.
   - Click **Actions**.
   - Click **Delete security groups**, then click **Delete** to confirm.

![clean](/images/6.clean/005-clean.png)

![clean](/images/6.clean/006-clean.png)