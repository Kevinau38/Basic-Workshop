---
title: "Test the website"

weight: 6
chapter: false
pre: " <b> 6. </b> "
---

In this step, we will test our static website to verify that it's working correctly. We'll test both the main page (index.html) and the error page (error.html) functionality.

## Test the Main Website

1. Use the static website URL (endpoint copied earlier)
2. Or go to your **S3 Bucket** → **Properties** tab → scroll down to **Static website hosting** section to find the URL
3. Copy the **Bucket website endpoint** URL
4. Open your web browser and paste the URL
5. You should see the content of your `index.html` file displayed

![Test-Main-Page](/images/5.verify/001-test.png)

## Test the Error Page

1. In your browser, access the same URL but add some random characters at the end
2. For example: `your-website-url/random-characters` or `your-website-url/nonexistent-page`
3. You should see the content of your `error.html` file displayed
4. This demonstrates that the error page configuration is working correctly

![Test-Error-Page](/images/5.verify/002-test.png)

## Verify Website Functionality

1. Confirm that both pages load correctly
2. Check that images and styling are displayed properly
3. Verify that the error page appears when accessing non-existent pages

![Test-Main-Page](/images/5.verify/001-test.png)

![Test-Error-Page](/images/5.verify/002-test.png)

We have successfully tested our static website. Both the main page and error page are working correctly. Next, we'll proceed to configure Route53 for custom domain access.