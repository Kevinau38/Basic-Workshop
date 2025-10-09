---
title: "Access HTTP on EC2"

weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---

1. Go to [EC2 service management console](https://console.aws.amazon.com/ec2/v2/home).

- At the **Instances** page:
- Click **Lab EC2 - we create on the previous Lab**.
- Then click  **Copy our Public IPv4 address**

![Connect](/images/3.connect/006-connect.png)

2. Access **http://{public ip}** in your web browser **(note: use http, not https)**.

![Connect](/images/3.connect/007-connect.png)

![Connect](/images/3.connect/008-connect.png)

3. We've covered **3 ways** to connect to **EC2**: **SSH**, **Console**, and **http://{EC2 public IP}**. Next, we'll attach role
**EC2S3FullAccessRole** to **EC2**.