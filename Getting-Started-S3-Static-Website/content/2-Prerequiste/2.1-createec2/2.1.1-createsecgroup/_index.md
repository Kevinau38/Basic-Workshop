---
title: "Create security group"

weight: 1
chapter: false
pre: " <b> 2.1.1 </b> "
---

#### Create security group **Lab security group**

1. Go to [EC2 service management console](https://console.aws.amazon.com/ec2/v2/home)
   - Click **Security Groups**.
   - Click **Create security group**.

![SG](/images/2.prerequisite/001-createsg.png)

2. At the **Create security group** page.
- In the **Basic details** section:
   - In the **Security group name** field, enter **Lab SG**.
   - In the **Description** field, enter **Allow ssh and http from internet**.
   - In the **VPC** field, click **Default VPC**.
- In the **Inbound rules** section:
   - In the **Type** field, click **SSH**.
   - In the **Source** field, click **Anywhere-IPv4**.
   - In the **Type** field, click **HTTP**.
   - In the **Source** field, click **Anywhere-IPv4**.   
- In the **Tags - optional** section:
   - In the **Key** field, enter **Name**.
   - In the **Value - optional** field, enter **Lab SG**.
- Click **Create security group**.

![SG](/images/2.prerequisite/002-createsg.png)

![SG](/images/2.prerequisite/003-createsg.png)

3. So we are done creating **Security Groups**. The next step is to create **EC2**

![SG](/images/2.prerequisite/004-createsg.png)