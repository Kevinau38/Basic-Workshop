---
title: "Enable Static Website hosting settings"

weight: 4
chapter: false
pre: " <b> 4. </b> "
---

{{% notice info %}}

• **Index document**: index.html  
• **Error document**: error.html  
{{% /notice %}}

In this step, we will enable static website hosting on our S3 bucket and configure the index and error documents.

## Enable Static Website Hosting

1. Go to **S3 Console** and click on your bucket
2. Click on the **Properties** tab

![Enable-Static-Hosting](/images/4.restore-ec2-ami/001-staticwebsite.png)

3. Scroll down to **Static website hosting** section
4. Click **Edit**

![Enable-Static-Hosting](/images/4.restore-ec2-ami/002-staticwebsite.png)

5. Select **Enable** for Static website hosting
6. **Hosting type**: Host a static website
7. **Index document**: `index.html`
8. **Error document**: `error.html`

![Enable-Static-Hosting](/images/4.restore-ec2-ami/003-staticwebsite.png)

9. Click **Save changes**

![Enable-Static-Hosting](/images/4.restore-ec2-ami/004-staticwebsite.png)

10. Note the **Bucket website endpoint** URL that appears - copy this URL as it will be used to access your website

![Enable-Static-Hosting](/images/4.restore-ec2-ami/005-staticwebsite.png)

## Upload Website Files

1. Download the required files:
   - index.html - Main website page
   - error.html - Error page
2. Go to **S3 Console** and click on your bucket
3. Click **Upload**

![Upload-Files](/images/4.restore-ec2-ami/006-staticwebsite.png)

4. Click **Add files**
5. Select both `index.html` and `error.html` files from your downloads
6. Click **Upload**

![Upload-Files](/images/4.restore-ec2-ami/007-staticwebsite.png)

7. Wait for the upload to complete

![Upload-Files](/images/4.restore-ec2-ami/008-staticwebsite.png)

## Configure Bucket Policy for Public Access

1. Click on the **Permissions** tab
2. Scroll down to **Bucket policy** section
3. Click **Edit**

![Bucket-Policy](/images/4.restore-ec2-ami/009-staticwebsite.png)

4. Add the following bucket policy (replace `your-bucket-arn` with your Bucket ARN):

```json
{
  "Id": "Policy1",
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "s3-static-website",
      "Action": [
        "s3:GetObject"
      ],
      "Effect": "Allow",
      "Resource": "replace-this-string-with-your-bucket-arn/*",
      "Principal": "*"
    }
  ]
}
```

5. Click **Save changes**

![Bucket-Policy](/images/4.restore-ec2-ami/010-staticwebsite.png)

Now that we have successfully enabled static website hosting, uploaded our HTML files, and configured public access with the appropriate bucket policy, let's proceed to test the website functionality and verify that everything is working correctly.