---
title: "Test ALB"

weight: 3
chapter: false
pre: " <b> 3. </b> "
---

In this step, we will test our Application Load Balancer to verify that it's properly distributing traffic between our two EC2 instances.

## Check ALB

1. Go to **EC2 Console** → **Load Balancers**

2. Select your load balancer `d-alb-web-alb`

3. Copy the **DNS name** from the Details section

![ALB-DNS](/images/alb-dns.png)

## Access from Browser

1. Open your web browser

2. Paste the DNS name into the address bar

3. You should see a page displaying "Hello World from" followed by the hostname of one of your EC2 instances

![ALB-Browser](/images/alb-browser.png)

## Test Load Balancing

1. Reload the page several times (press F5 or Ctrl+R)

2. You should notice that the hostname changes between your two instances:
   - Sometimes showing `d-ec2-web-server-01`
   - Sometimes showing `d-ec2-web-server-02`

3. This demonstrates that the Application Load Balancer is successfully distributing traffic across both instances

![ALB-LoadBalance](/images/alb-loadbalance.png)

Now that we have successfully tested our Application Load Balancer and verified that it's distributing traffic properly, let's proceed to clean up the resources we created.
