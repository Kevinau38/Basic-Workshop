---
title: "Create EBS Snapshot"

weight: 2
chapter: false
pre: " <b> 2.2 </b> "
---

### Create EBS Snapshot

In this step, we will create an EBS snapshot of our EC2 instance's root volume. EBS snapshots are point-in-time backups of your EBS volumes that are stored in Amazon S3. These snapshots can be used to create new volumes or restore data.

1. Go to [EC2 service management console](https://console.aws.amazon.com/ec2/v2/home)

2. In the left navigation bar, click **Volumes**.

![role](/images/2.prerequisite/023-createebsvolumes.png)

3. Select the volume of the created instance, right-click and select **Create snapshot**.

![role1](/images/2.prerequisite/024-createebsvolumes.png)

4. At the **Create snapshot** page:
- In the **Snapshot details** section:
   - In the **Description** field, enter **Snapshot for bastion host volume**.
- In the **Tags** section:
   - In the **Key** field, enter **Name**.
   - In the **Value - optional** field, enter **Lab EBS Snapshot**.
- Click **Create snapshot**.

![role1](/images/2.prerequisite/025-createebsvolumes.png)

5. From the left menu in EC2 console, click **Snapshots** to verify that the snapshot has been created.

![createpolicy](/images/2.prerequisite/026-createebsvolumes.png)

6. Wait for a moment and you will see the Snapshot status change to **Completed**, indicating success.

![namerole](/images/2.prerequisite/027-createebsvolumes.png)

Next, we will proceed to **create AMI**.