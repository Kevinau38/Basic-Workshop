---
title: "Create EC2 Instances"

weight: 2
chapter: false
pre: " <b> 2.2 </b> "
---

To test Load balancing, we will create 2 EC2 instances in 2 different Availability Zones as below:

## Create d-ec2-web-server-01

1. Go to **EC2 Console** → **Instances** → **Launch instances**
2. **Name**: `d-ec2-web-server-01`
3. **OS**: Default (Amazon Linux 2023)
4. **Instance type**: Default (t2.micro)
5. **Key pair**: Create new keypair with name: `d-key-common`
6. **Network Setting**:
   - **VPC**: Default
   - **Subnet**: **my-subnet-01**
   - **Auto-assign public IP**: Enable
   - **Select existing security group**: **WebServer-SG**
7. **Advanced details (User data)**:
```bash
#!/bin/bash
yum update -y
yum install -y httpd.x86_64
systemctl start httpd.service
systemctl enable httpd.service
echo "Hello World from $(hostname -f)" > /var/www/html/index.html
```
8. Click **Launch instance**

![EC2-01-1](/images/2.prerequisite/008-createec2.png)

![EC2-01-2](/images/2.prerequisite/009-createec2.png)

![EC2-01-3](/images/2.prerequisite/010-createec2.png)

![EC2-01-4](/images/2.prerequisite/011-createec2.png)

![EC2-01-5](/images/2.prerequisite/012-createec2.png)

![EC2-01-6](/images/2.prerequisite/013-createec2.png)

## Create d-ec2-web-server-02

1. Go to **EC2 Console** → **Instances** → **Launch instances**
2. **Name**: `d-ec2-web-server-02`
3. **OS**: Default (Amazon Linux 2023)
4. **Instance type**: Default (t2.micro)
5. **Key pair**: Use existing keypair: `d-key-common`
6. **Network Setting**:
   - **VPC**: Default
   - **Subnet**: **my-subnet-02**
   - **Auto-assign public IP**: Enable
   - **Select existing security group**: **WebServer-SG**
7. **Advanced details (User data)**:
```bash
#!/bin/bash
yum update -y
yum install -y httpd.x86_64
systemctl start httpd.service
systemctl enable httpd.service
echo "Hello World from $(hostname -f)" > /var/www/html/index.html
```
8. Click **Launch instance**

![EC2-02-1](/images/2.prerequisite/014-createec2.png)

![EC2-02-2](/images/2.prerequisite/015-createec2.png)

![EC2-02-3](/images/2.prerequisite/016-createec2.png)

![EC2-02-4](/images/2.prerequisite/017-createec2.png)

![EC2-02-5](/images/2.prerequisite/018-createec2.png)

![EC2-02-6](/images/2.prerequisite/019-createec2.png)

![EC2-Instances-Created](/images/2.prerequisite/020-createec2.png)

Now that we have created our web server instances, let's proceed to create a Target Group to organize these instances for our Application Load Balancer.