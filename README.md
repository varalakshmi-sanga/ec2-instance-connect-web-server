# EC2 Instance Connect – Web Server Setup

## Project Overview
This project demonstrates how to deploy a basic web server on an AWS EC2 instance using **EC2 Instance Connect**.

## Services Used
- Amazon EC2
- EC2 Instance Connect
- Security Groups
- Apache HTTP Server
- Amazon Linux

## Step-by-Step Implementation

### Step 1: Launch EC2 Instance
- Launched an Amazon Linux EC2 instance
- Enabled EC2 Instance Connect
- Assigned a public IPv4 address

### Step 2: Configure Security Group
- Allowed SSH (Port 22) from Anywhere (for EC2 Instance Connect)
- Allowed HTTP (Port 80) from Anywhere to access the website

### Step 3: Connect to EC2
- Connected using EC2 Instance Connect from AWS Console
- Logged in as `ec2-user`

### Step 4: Install Web Server
```bash
sudo yum update -y
sudo yum install httpd -y
### Step 5: Start and Enable Apache
sudo systemctl start httpd
sudo systemctl enable httpd

 ###Step 6: Create Web Page
sudo nano /var/www/html/index.html

<h1>Welcome to My EC2 Web Server</h1>
<p>Hosted using EC2 Instance Connect</p>

 ###Step 7: Access Website

Opened the website using the EC2 Public IPv4 address

Result

The Apache web server was successfully deployed and the website was accessible via the public IP.

Key Learnings

EC2 Instance Connect allows browser-based SSH access

Security Groups control inbound traffic

Apache service management using Linux commands

Author

Varalakshmi Sanga

