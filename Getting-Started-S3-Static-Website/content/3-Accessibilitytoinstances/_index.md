---
title: "Creating a S3 bucket"

weight: 3
chapter: false
pre: " <b> 3. </b> "
---

{{% notice info %}}

• **Region**: US East (N. Virginia) - us-east-1 (Required for S3 static website hosting).  
• **Bucket name**: Must match your domain name exactly.  
{{% /notice %}}

In this step, we will create an S3 bucket that will host our static website. The bucket name must match your domain name exactly for the custom domain configuration to work properly.

## Create S3 Bucket

1. Go to **S3 Console** → **Buckets**
2. Click **Create bucket**

![Create-S3-Bucket](/images/3.connect/001-s3.png)

3. **Bucket name**: Enter your domain name (e.g., `s3static.basic-workshop.click`)

![Create-S3-Bucket](/images/3.connect/002-s3.png)

4. **Block Public Access settings**: Uncheck **Block all public access**
5. Check **I acknowledge that the current settings might result in this bucket and the objects within becoming public**

![Create-S3-Bucket](/images/3.connect/003-s3.png)

6. Click **Create bucket**

![Create-S3-Bucket](/images/3.connect/004-s3.png)

Now that we have created our S3 bucket, let's proceed to enable static website hosting settings.