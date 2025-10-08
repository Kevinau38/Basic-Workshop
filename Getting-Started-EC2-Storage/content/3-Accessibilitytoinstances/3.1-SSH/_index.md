---
title: "Connect via SSH"

weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

{{% notice info %}}

• Download **AWS CLI** first: https://awscli.amazonaws.com/AWSCLIV2.msi.   
• **Windows**: Use Git Bash in the directory containing your key pair file.  
• **Mac**: Use Terminal in the directory containing your key pair file.   
{{% /notice %}}

1. Go to [EC2 service management console](https://console.aws.amazon.com/ec2/v2/home).

- At the **Instances** page:
  - Click **Lab EC2 - we create on the previous Lab**.
  - Then click  **Connect**.

![Connect](/images/3.connect/001-connect.png)

2. At the **Connect to instance** page:

- Click on **SSH client** tab to get the SSH command.
- **Command 1** to set execute permissions for the .pem file.
- **Command 2** to SSH into EC2 (ensure correct key pair file name).

![Connect](/images/3.connect/002-connect.png)

3. Open **Git Bash** and navigate to the directory containing your key pair file:

• Use **ls** command to verify **the .pem file** is in the current directory:

```
ls
```

• Run **command 1** to set permissions for the key file:

```
chmod 400 "d-key-common.pem"
```

• Run command 2 to SSH into the EC2 instance:

```
  ssh -i "your-key-pair.pem" ec2-user@your-ec2-public-ip
```

• When prompted with the authenticity message, type yes to continue connecting:

```
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
```

• You should see the Amazon Linux welcome message, indicating successful connection.

![Connect](/images/3.connect/003-connect.png)
