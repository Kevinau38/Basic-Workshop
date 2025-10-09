---
title: "Create EBS Snapshot"

weight: 2
chapter: false
pre: " <b> 2.2 </b> "
---

### Create EBS Snapshot

In this step, we will create an EBS snapshot of our EC2 instance's root volume. EBS snapshots are point-in-time backups of your EBS volumes that are stored in Amazon S3. These snapshots can be used to create new volumes or restore data.

1. Go to [IAM service administration interface](https://console.aws.amazon.com/iamv2/)
2. In the left navigation bar, click **Roles**.

![role](/images/2.prerequisite/023-iamrole.png)

3. Click **Create role**.

![role1](/images/2.prerequisite/024-iamrole.png)
4. At the **Create role** page:
- In the **Select trusted entity** section:
   - In the **Trusted entity type** field, click **AWS service**.
   - In the **Use case** field, click **EC2**.
- Click **Next**.

![role1](/images/2.prerequisite/025-iamrole.png)

5. In the Search box, enter **AmazonS3FullAccess** and press Enter to search for this policy.

- Click the policy **AmazonS3FullAccess**.
- Click **Next**

![createpolicy](/images/2.prerequisite/026-iamrole.png)

6. In the **Name, review, and create** section:
- In the **Role name** field, enter **EC2S3FullAccessRole**.
- Click **Create Role** \.

![namerole](/images/2.prerequisite/027-iamrole.png)

7. After successfully creating the role, you will see the **EC2S3FullAccessRole** listed in the IAM Roles dashboard,
confirming that the role has been created and is ready to be attached to EC2 instances.

![namerole](/images/2.prerequisite/028-iamrole.png)

Next, we will connect to the **EC2 instance** we created via **SSH**.
