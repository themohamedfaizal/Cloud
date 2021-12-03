Hands-On:

Launching an EC2 Instance running Linux

    We’ll be launching our first virtual server using the AWS Console
    We’ll get a first high-level approach to the various parameters
    We’ll see that our web server is launched using EC2 user data
    We’ll learn how to start / stop / terminate our instance. -(IP changes on reboot) use http service as example. secure and not secure.

User script:

```bash
#!/bin/bash
yum update -y
yum install -y httpd
systemctl start httpd
systemctl enable httpd
echo "<h1>Welcome to $(hostname -f)</h1>" > /var/www/html/index.html
```
