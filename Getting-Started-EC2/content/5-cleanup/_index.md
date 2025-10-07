+++
title = "Clean up resources"
date = 2022
weight = 5
chapter = false
pre = "<b>5. </b>"
+++

We will take the following steps to delete the resources we created in this exercise.

#### Delete EC2 instance

1. Go to [EC2 service management console](https://console.aws.amazon.com/ec2/v2/home)
   - Click **Instances**.
   - Select **Our instances**.
   - Click **Instance state**.
   - Click **Terminate instance**, then click **Terminate** to confirm.

![Clean](/images/5.clean/001-clean.png)

![Clean](/images/5.clean/002-clean.png)

#### Delete IAM Role

1. Go to [IAM service management console](https://console.aws.amazon.com/iamv2/home#/home)
   - Click **Roles**.
   - In the search box, enter **EC2S3FullAccessRole**.
   - Click to select **EC2S3FullAccessRole**.
   - Click **Delete**, then enter the role name **EC2S3FullAccessRole** and click **Delete** to delete the role.

![Clean](/images/5.clean/003-clean.png)

![Clean](/images/5.clean/004-clean.png)

#### Delete Security Group

1. Go to [EC2 service management console](https://console.aws.amazon.com/ec2/v2/home)
   - Click **Security Groups**.
   - Select **Our security groups**.
   - Click **Actions**.
   - Click **Delete security groups**, then click **Delete** to confirm.

![Clean](/images/5.clean/005-clean.png)

![Clean](/images/5.clean/006-clean.png)