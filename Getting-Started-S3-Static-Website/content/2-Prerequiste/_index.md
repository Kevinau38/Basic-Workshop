---
title: "Register domain with Route53"

weight: 2
chapter: false
pre: " <b> 2. </b> "
---

{{% notice info %}}

• **Region**: US East (N. Virginia) - us-east-1 (Required for Route53).  
• **Domain**: Choose a domain name for your static website.  
{{% /notice %}}




In this step, we will register a custom domain name using Amazon Route53. This domain is required for the complete workshop experience as we will configure it to access your static website with a custom URL instead of the default S3 website endpoint.

## Check Domain Availability

1. Go to **Route53 Console** → **Registered domains**
2. Click **Register domain**

![Check-Domain](/images/2.prerequisite/001-domain.png)

3. Enter your desired domain name (e.g., `basic-workshop.click`)
4. Click **Search** to verify availability

![Check-Domain](/images/2.prerequisite/002-domain.png)

5. If available, select the domain and click **Proceed to checkout**

![Check-Domain](/images/2.prerequisite/003-domain.png)

![Check-Domain](/images/2.prerequisite/004-domain.png)

## Register Domain with Route53

1. Review your domain selection in the cart
2. Choose registration period (1 year minimum)
3. **Auto-renew**: click to **Disable** and click Next

![Register-Domain](/images/2.prerequisite/005-domain.png)

4. Fill in contact information:
   - **Contact Type**: Person
   - **First Name**: Your first name
   - **Last Name**: Your last name
   - **Email**: Your email address
   - **Phone**: Your phone number
   - **Address**: Your address
   - **Country**: Your country
   - **City**: Your city
   - **Zip code**: Your city zip code
5. **Privacy Protection**: Enable
6. **Admin contact**: Same as the registrant contact
7. **Tech contact**: Same as the registrant contact
8. **Billing contact**: Same as the registrant contact
9. Click **Next**

![Register-Domain](/images/2.prerequisite/006-domain.png)

![Register-Domain](/images/2.prerequisite/007-domain.png)

10. Review all the information you have entered
11. Click the **Terms and Conditions** checkbox
12. Click **Submit**

![Register-Domain](/images/2.prerequisite/008-domain.png)

![Register-Domain](/images/2.prerequisite/009-domain.png)

## Verify Domain Registration

1. Go to **Route53 Console** → **Requests**
2. Wait for domain status to change to **Successful**
3. Note: Domain registration can take up to 15 minutes
4. Once registered, the domain will appear in your registered domains list

![Verify-Domain](/images/2.prerequisite/010-domain.png)

![Verify-Domain](/images/2.prerequisite/011-domain.png)

{{% notice warning %}}
**Important**: Domain registration is non-refundable. Make sure you want to keep the domain before completing the purchase. Typical cost for `.click` domains is around $3-5 per year.
{{% /notice %}}

Now that we have successfully registered our domain, let's proceed to create an S3 bucket for hosting our static website.
