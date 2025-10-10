---
title: "Verify webserver and created file"

weight: 5
chapter: false
pre: " <b> 5. </b> "
---

In this step, we will connect to the **new EC2 instance restored from AMI** and verify that **our web server** and **test file** are still intact, demonstrating successful data persistence through AMI backup and restore.

1. After the EC2 instance is running, connect using EC2 Instance Connect to check if the file created in **step 3.3** still exists.

![role1](/images/5.verify/001-verify.png)

![role1](/images/5.verify/002-verify.png)

2. After connecting, run the following command to verify that the file still exists:

```
ls
```

You should see the `test.txt` file that we created earlier.

![role1](/images/5.verify/003-verify.png)

3. Next, access the web server from your browser using the public IP address:

```
http://{public-ip}
```

![role1](/images/5.verify/004-verify.png)

4. Verify that the web server is still running and displaying the expected content.

![role1](/images/5.verify/005-verify.png)

We have successfully completed the verification. Next is the essential step of **Clean up resources**.