---
title: "Introduction"

weight: 1
chapter: false
pre: " <b> 1. </b> "
---

Application Load Balancer (ALB) is a Layer 7 load balancer that automatically distributes incoming application traffic across multiple targets, such as EC2 instances, containers, and IP addresses, in multiple Availability Zones. ALB increases the availability and fault tolerance of your applications.

With Application Load Balancer, users can:

- Distribute traffic across multiple EC2 instances in different Availability Zones.
- Perform health checks on targets to ensure traffic is only routed to healthy instances.
- Support advanced routing based on content, host headers, and path patterns.
- Integrate with AWS services like Auto Scaling and CloudWatch.
- Provide SSL/TLS termination and certificate management.
- Handle millions of requests per second with low latency.

This workshop focuses on practical load balancing scenarios including creating target groups, configuring health checks, and setting up an Application Load Balancer to demonstrate how ALB provides high availability and scalability for web applications.
