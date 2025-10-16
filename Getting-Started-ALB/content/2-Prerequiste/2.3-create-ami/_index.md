---
title: "Create AMI"

weight: 3
chapter: false
pre: " <b> 2.3 </b> "
---

### Create AMI

In this step, we will create an Amazon Machine Image (AMI) from our EC2 instance. An AMI is a template that contains the software configuration (operating system, application server, and applications) required to launch an instance. This AMI will capture the current state of our instance including any installed software and configurations.

1. Go to [EC2 service management console](https://console.aws.amazon.com/ec2/v2/home)

2. In the left navigation bar, click **Instances**.

![role](/images/2.prerequisite/028-createami.png)

3. Select the created instance, right-click and select **Image and templates**. Then click **Create image**.

![role1](/images/2.prerequisite/029-createami.png)

4. At the **Create image** page:
- In the **Image details** section:
   - In the **Image name** field, enter **Lab AMI**.
   - In the **Tags - optional** field, click **Tag image and snapshots separately**:
      - In the **Key** field of **Tag image**, enter **Name**.
      - In the **Value - optional** field of **Tag image**, enter **Lab AMI**.
      - In the **Key** field of **Tag snapshots**, enter **Name**.
      - In the **Value - optional** field of **Tag snapshots**, enter **Lab AMI Snapshot**.


- Click **Create image**.

![role1](/images/2.prerequisite/030-createami.png)

![role1](/images/2.prerequisite/031-createami.png)

5. From the left menu in EC2 console, click **AMIs** to verify that the AMIs has been created.

![createpolicy](/images/2.prerequisite/032-createami.png)

6. Wait for a moment and you will see the AMIs status change to **Available**, indicating success.

![namerole](/images/2.prerequisite/033-createami.png)

Next, we will continue with.
