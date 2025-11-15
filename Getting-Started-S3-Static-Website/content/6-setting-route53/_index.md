---
title: "Setting Route53 to access http://s3static.{domain}"

weight: 6
chapter: false
pre: " <b> 6. </b> "
---

In this step, we will configure Route53 to create a custom subdomain that points to our S3 static website. When you purchased a domain in Route53, AWS automatically created a public hosted zone with your domain name and included default NS and SOA records.

## Access Route53 Hosted Zone

1. Go to **Route53 Console** → **Hosted zones**
2. Click on your domain name (the hosted zone was automatically created when you registered the domain)
3. You should see the default **NS** and **SOA** records

![Hosted-Zone](/images/6-setting-route53/001-setting-route53.png)

![Hosted-Zone](/images/6-setting-route53/002-setting-route53.png)

## Create A Record for Subdomain

1. Click **Create record**
2. **Record name**: `s3static`
3. **Record type**: A
4. **Alias**: Enable (toggle on)
5. **Route traffic to**: Alias to S3 website endpoint
6. **Region**: US East (N. Virginia) [us-east-1]
7. **S3 Endpoint**: Select your bucket endpoint (should show your bucket name)
8. Click **Create records**

![Create-Record](/images/6-setting-route53/003-setting-route53.png)

## Verify DNS Record

1. After creating the record, you should see the new **A** record in your hosted zone
2. The record should show **s3static.your-domain.com** pointing to your S3 endpoint

![Verify-Record](/images/6-setting-route53/004-setting-route53.png)

## Test Custom Domain Access

1. Open your web browser
2. Navigate to: `http://s3static.your-domain.com` (replace with your actual domain)
3. You should see your static website loading through the custom domain
4. Test the error page by adding random characters: `http://s3static.your-domain.com/random`

![Test-Custom-Domain](/images/6-setting-route53/005-setting-route53.png)

![Test-Custom-Domain](/images/6-setting-route53/006-setting-route53.png)

We have successfully configured Route53 to provide custom domain access to our S3 static website, allowing users to access the website using a friendly domain name instead of the S3 endpoint URL. Now that we have completed the entire workshop and our static website is fully functional with custom domain access, let's proceed to clean up the resources we created to avoid unnecessary charges.