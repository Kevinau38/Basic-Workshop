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

2. Run the following command to verify the web server is running:

```
curl localhost
```

If the result returns "Hello world from ip xxxxxx", it means the web server is working correctly.

3. Run the following command to check if our test file still exists:

```
ls
```

You should see the `test.txt` file that we created earlier, confirming that data persistence works with AMI restoration.

Next, we will proceed to **clean up resources**.