---
title: "Create EC2"

weight: 2
chapter: false
pre: " <b> 2.1.2 </b> "
---

{{% notice info %}}

• **Key pair (login) section**: In the previous lab – Getting Started with EC2, we created a key pair – we will reuse that key to continue with the next steps.  
• **Subnet in the Network settings section**: We can also reuse the previously created subnet.    
{{% /notice %}}


#### Create EC2 **Lab EC2**

1. Go to [EC2 service management console](https://console.aws.amazon.com/ec2/v2/home)
   - Click **Instances**.
   - Click **Launch instances**.

![EC2](/images/2.prerequisite/005-createec2.png)

2. At the **Launch instances** page.
- In the **Name and tags** section:
   - In the **Name** field, enter **Lab EC2**.
   - On the right of **Name** field, click **Add additional tags**.

![EC2](/images/2.prerequisite/006-createec2.png)

![EC2](/images/2.prerequisite/007-createec2.png)

- In the **Application and OS Images (Amazon Machine Image)** section:
   - In the **Quick Start** field, click **Amazon Linux**.

![EC2](/images/2.prerequisite/008-createec2.png)

- In the **Instance type** section:
   - In the **Instance type** field, click **t2.micro**.

![EC2](/images/2.prerequisite/009-createec2.png)

- In the **Key pair (login)** section:
   - On the right of **Key pair name - required** field, click **Create new key pair**.

![EC2](/images/2.prerequisite/010-createec2.png)

3. At the **Create key pair** page.
   - In the **Key pair name** field, enter **d-key-common**.
   - Click **Create key pair**.

![EC2](/images/2.prerequisite/011-createec2.png)

   - In the **Key pair name - required** field, click **d-key-common** (the Key we just created above).

![EC2](/images/2.prerequisite/012-createec2.png)

- In the **Network settings** section:
   - On the right of **Network settings** section, click **Edit**.

![EC2](/images/2.prerequisite/013-createec2.png)

- In the **VPC - required** field, click **Default VPC**.
- On the right of **Subnet** field, click **Create new subnet**.
- In the **Auto-assign public IP** field, click **Enable**.
- In the **Firewall (security groups)** field, click **Select existing security group**.
- In the **Common security groups** field, click **Security groups - we create on the previous Lab**.

![EC2](/images/2.prerequisite/014-createec2.png)

4. At the **Create subnet** page.
- In the **VPC** section:
   - In the **VPC ID** field, click **Default VPC**.

![EC2](/images/2.prerequisite/015-createec2.png)

- In the **Subnet settings** section:
   - In the **Subnet name** field, enter **my-subnet-01**.
   - In the **Availability zone** field, click **Asia Pacific (Singapore) / apse1-az2 (ap-southeast-1a)**.
   - In the **IPv4 subnet CIDR block** field, enter **172.31.0.0/20**.
   - Click **Create key pair**.

![EC2](/images/2.prerequisite/016-createec2.png)

- So here is there results after creating Subnet.

![EC2](/images/2.prerequisite/017-createec2.png)

5. After creating **Subnet** - We come back to **Launch instances** page.
- In the **Network settings** section:
   - In the **Subnet** field, click **my-subnet-01** (the Subnet we just created above).

![EC2](/images/2.prerequisite/018-createec2.png)

- In the **Configure storage** section:
   - All parameters in this section will be left as default.

![EC2](/images/2.prerequisite/019-createec2.png)

- In the **Advanced details** section:
   - In the **User data - optional** field, enter:
 ```
 #!/bin/bash
yum update -y
yum install -y httpd.x86_64
systemctl start httpd.service
systemctl enable httpd.service
echo “Hello World from $(hostname -f)” > /var/www/html/index.html
 ```
 
 - Click **Create key pair**.

![EC2](/images/2.prerequisite/020-createec2.png)

- Instances are starting - They take 3 to 4 minutes to initialize.
![EC2](/images/2.prerequisite/021-createec2.png)

6. So we are done creating **EC2**. The next step is to create **IAM Role**

![EC2](/images/2.prerequisite/022-createec2.png)
