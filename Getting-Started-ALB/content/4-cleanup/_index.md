---
title: "Clean up resources"

weight: 4
chapter: false
pre: " <b> 4. </b> "
---

We will take the following steps to delete the resources we created in this exercise.

## Terminate EC2 Instances

1. Go to **EC2 Console** → **Instances**
2. Select both EC2 instances:
   - d-ec2-web-server-01
   - d-ec2-web-server-02
3. Click **Instance state** → **Terminate instance**
4. Click **Terminate** to confirm

![Terminate-EC2](/images/cleanup-ec2.png)

## Delete Application Load Balancer

1. Go to **EC2 Console** → **Load Balancers**
2. Select the load balancer `d-alb-web-alb`
3. Click **Actions** → **Delete load balancer**
4. Type **confirm** and click **Delete**

![Delete-ALB](/images/cleanup-alb.png)

## Delete Target Group

1. Go to **EC2 Console** → **Target Groups**
2. Select the target group `d-tg-web-server`
3. Click **Actions** → **Delete**
4. Click **Yes, delete** to confirm

![Delete-TG](/images/cleanup-tg.png)

## Delete Security Groups

1. Go to **EC2 Console** → **Security Groups**
2. Select the security groups:
   - WebServer-SG
   - ALB-SG
3. Click **Actions** → **Delete security groups**
4. Click **Delete** to confirm

![Delete-SG](/images/cleanup-sg.png)

Congratulations! You have successfully completed the Application Load Balancer workshop and cleaned up all the resources.