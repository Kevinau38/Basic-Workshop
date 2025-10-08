---
title: "Configure EC2 IAM role"

weight: 4
chapter: false
pre: " <b> 4. </b> "
---

1. Go to [EC2 service management console](https://console.aws.amazon.com/ec2/v2/home).

- At the **Instances** page:
  - Click **Lab EC2 - we create on the previous Lab**.
  - Click **Actions** button.
  - Click **Security**.
  - Click **Modify IAM role**.

![S3](/images/4.configure-IAM-role/001-s3.png)

2. Select **Role - we create on the previous Lab** from the dropdown.
- Click Update IAM role.

![S3](/images/4.configure-IAM-role/002-s3.png)

3. Test IAM role connection

- Connect to EC2 instance using EC2 Instance Connect ([Section 3.2: Connect via Console]({{< ref "3-Accessibilitytoinstances/3.2-Console" >}})).
- Run the following command to test S3 access:

```
  aws s3 ls
```

- **Expected result:**
  - If you have S3 buckets: List of buckets will display
  - If no buckets exist: No output (blank), but no error messages
  - **Success indicator:** No permission denied or authentication errors

![S3](/images/4.configure-IAM-role/003-s3.png)