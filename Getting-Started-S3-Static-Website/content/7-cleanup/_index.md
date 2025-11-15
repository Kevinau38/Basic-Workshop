---
title: "Clean up resources"

weight: 7
chapter: false
pre: " <b> 7. </b> "
---

We will take the following steps to delete the resources we created in this exercise to avoid unnecessary charges.

## Delete Route53 DNS Record

1. Go to **Route53 Console** → **Hosted zones**
2. Click on your domain name

![Delete-Route53](/images/7.clean/001-clean.png)

3. Select the **A record** for `s3static`
4. Click **Delete record**

![Delete-Route53](/images/7.clean/002-clean.png)

5. Click **Delete** to confirm

![Delete-Route53](/images/7.clean/003-clean.png)

## Empty and Delete S3 Bucket

1. Go to **S3 Console** → **Buckets**
2. Click on your bucket name

![Delete-S3-Bucket](/images/7.clean/004-clean.png)

3. Select all objects in the bucket
4. Click **Delete**

![Delete-S3-Bucket](/images/7.clean/005-clean.png)

5. Type `permanently delete` to confirm
6. Click **Delete objects**

![Delete-S3-Bucket](/images/7.clean/006-clean.png)

7. Go back to buckets list
8. Select your bucket
9. Click **Delete**

![Delete-S3-Bucket](/images/7.clean/007-clean.png)

10. Type your bucket name to confirm
11. Click **Delete bucket**

![Delete-S3-Bucket](/images/7.clean/008-clean.png)

Congratulations! You have successfully completed the S3 Static Website workshop and cleaned up all the resources. You learned how to create a static website using S3, configure custom domain with Route53, and manage AWS resources effectively.