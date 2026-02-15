#Deploy a Real Web Server on the Cloud

Step 1 : Launch an instance from AWS console.

Step 2 : Connect to instance using ssh.

Command : ssh -i "devops-server-key.pem" ubuntu@ec2-3-236-213-183.compute-1.amazonaws.com

Step 3 : Install Nginx

Command : sudo apt update

sudo apt install nginx

Step 3 : Configure security groups for web access. From the AWS console, go to the security group and add an inbound rule for port 80 (default for Nginx).

<img width="821" height="320" alt="nginx" src="https://github.com/user-attachments/assets/c8b7ddcc-2e6f-43cd-b3ca-9a3025d294bb" />

Step 4 : Check logs of nginx service

Command : journalctl -u nginx

Step 5 : Save logs to file

Commad : scp -i "devops-server-key.pem" ubuntu@ec2-3-236-213-183.compute-1.amazonaws.com:/var/log/nginx/access.log .

scp -i "devops-server-key.pem" ubuntu@ec2-3-236-213-183.compute-1.amazonaws.com:~/journalctl.log .

Install Docker
Command sudo apt install docker.io

Challenges Faced
Unable to access Nginx using the public IP.
Solution: I had forgotten to add port 80 to the security group inbound rules. Once added, Nginx became accessible.

My custom HTML page was not loading on the webpage.
Solution: I reloaded the Nginx service. After reloading, my aboutme.html page was accessible.

File permissions issue when accessing logs.
Solution : Needed sudo to read /var/log/nginx/access.log.

What I Learned
Connect to an AWS cloud instance using SSH.

How to manage security group (adding inbound rules)

How to install Nginx and serve a webpage.

The importance of reloading a service after configuration changes or adding new files.

How to transfer files securely from the instance to the local machine using scp.

Confusion between journalctl and access logs. Learned that journalctl -u nginx shows service logs, while HTTP requests are recorded in /var/log/nginx/access.log.
