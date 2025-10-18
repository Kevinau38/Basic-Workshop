---
title: "Create Application Load Balancer"

weight: 4
chapter: false
pre: " <b> 2.4 </b> "
---

## Create Application Load Balancer

1. Go to **EC2 Console** → **Load Balancers** → Click **Create load balancer**

2. Select **Create Application Load Balancer**

3. **Load balancer name**: `d-alb-web-alb`

4. **Scheme**: Internet-facing

5. **IP address type**: IPv4

6. **Network mapping**:
   - **VPC**: Select default VPC
   - **Mappings**: Select my-subnet-01 and my-subnet-02

7. **Security groups**: ALB-SG

8. **Listeners and routing**:
   - **Protocol**: HTTP
   - **Port**: 80
   - **Default action**: Select Target group **d-tg-web-server**

9. Click **Create load balancer**

![ALB-Config-1](/images/2.prerequisite/028-createalb.png)

![ALB-Config-2](/images/2.prerequisite/029-createalb.png)

![ALB-Config-3](/images/2.prerequisite/030-createalb.png)

![ALB-Config-4](/images/2.prerequisite/031-createalb.png)

![ALB-Config-5](/images/2.prerequisite/032-createalb.png)

![ALB-Config-6](/images/2.prerequisite/033-createalb.png)

![ALB-Config-7](/images/2.prerequisite/034-createalb.png)

![ALB-Config-8](/images/2.prerequisite/035-createalb.png)

## Verify Health Status

After creating the ALB, wait a moment and you will see the Health status in Target group change to **healthy**.

![ALB-Health](/images/2.prerequisite/036-createalb.png)

Now that we have successfully created our Application Load Balancer and verified that our targets are healthy, let's proceed to test the load balancing functionality.
