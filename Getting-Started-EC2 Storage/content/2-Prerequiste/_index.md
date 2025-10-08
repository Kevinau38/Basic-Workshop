---
title: "Preparation "

weight: 2
chapter: false
pre: " <b> 2. </b> "
---

{{% notice info %}}

• **Region**: Singapore - ap-southeast-1 (Recommended).  
• **VPC**: Default VPC.  
• **Instance**: Create 1 Linux instance on the public subnet.  
{{% /notice %}}




In order to securely manage our EC2 instances on AWS, especially within a VPC architecture, we need to configure appropriate permissions and networking settings. As part of the preparation, we will create an IAM Role to grant the necessary permissions for EC2 instances to interact with other AWS services such as Amazon S3 and Amazon VPC.

### Content

- [Prepare EC2](2.1-createec2/)
- [Create IAM Role](2.2-createiamrole/)
