---
title: "Create Security Groups"

weight: 1
chapter: false
pre: " <b> 2.1 </b> "
---

In this step, we will create two security groups needed for our Application Load Balancer setup. One security group will be for the ALB itself, and another will be for the web servers that will receive traffic from the ALB.

## Create ALB Security Group

1. Go to **EC2 Console** → **Security Groups** → **Create security group**
2. **Security group name**: `ALB-SG`
3. **Description**: `Allow http from internet`
4. **VPC**: Select default VPC
5. **Inbound rules**:
   - Type: HTTP, Port: 80, Source: Anywhere IPv4
6. **Outbound rules**: Default (All traffic)
7. **Tags**:
   - Key: Name, Value: `ALB-SG`
8. Click **Create security group**

![ALB-SG-1](/images/2.prerequisite/001-createsg.png)

![ALB-SG-2](/images/2.prerequisite/002-createsg.png)

![ALB-SG-3](/images/2.prerequisite/003-createsg.png)

## Create Web server Security Group

1. Go to **EC2 Console** → **Security Groups** → **Create security group**
2. **Security group name**: `WebServer-SG`
3. **Description**: `Allow http from ALB`
4. **VPC**: Select default VPC
5. **Inbound rules**:
   - Type: HTTP, Port: 80, Source: Custom → **select ALB-SG**
6. **Outbound rules**: Default (All traffic)
7. **Tags**:
   - Key: Name, Value: `WebServer-SG`
8. Click **Create security group**

![WebServer-SG-1](/images/2.prerequisite/004-createsg.png)

![WebServer-SG-2](/images/2.prerequisite/005-createsg.png)

![WebServer-SG-3](/images/2.prerequisite/006-createsg.png)

![Security-Groups-Created](/images/2.prerequisite/007-createsg.png)

Now that we have created the necessary security groups, let's proceed to create EC2 instances that will serve as our web servers behind the Application Load Balancer.
