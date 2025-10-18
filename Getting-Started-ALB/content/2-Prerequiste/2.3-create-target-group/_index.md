---
title: "Create Target Group"

weight: 3
chapter: false
pre: " <b> 2.3 </b> "
---

## Create Target Group

1. Go to **EC2 Console** → **Target Groups** → Click **Create target group**

2. **Choose a target type**: Instances

3. **Target group name**: `d-tg-web-server`

4. **Protocol**: HTTP

5. **Port**: 80

6. **VPC**: Select default VPC

7. **Tags**:
   - Key: Name, Value: `d-tg-web-server`

8. Keep other settings as default

9. Click **Next**

![Target-Group-Config](/images/target-group-config.png)

## Register EC2 instances to Target Group

1. At this step, we will add the 2 instances created earlier to Targets

2. Check and select both instances:
   - d-ec2-web-server-01
   - d-ec2-web-server-02

3. Click **Include as pending below**

4. Click **Create target group**

![Target-Group-Register](/images/target-group-register.png)

Now that we have created our Target Group and registered our EC2 instances, let's proceed to create the Application Load Balancer to distribute traffic across these instances.
