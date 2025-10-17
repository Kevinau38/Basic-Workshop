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
   - **Default action**: Select Target group `d-tg-web-server`

9. Click **Create load balancer**

![ALB-Config](/images/alb-config.png)

## Verify Health Status

After creating the ALB, wait a moment and you will see the Health status in Target group change to **healthy**.

![ALB-Health](/images/alb-health.png)

Now that we have successfully created our Application Load Balancer and verified that our targets are healthy, let's proceed to test the load balancing functionality.
