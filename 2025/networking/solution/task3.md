# AWS EC2 and Security Groups

# Introduction

Amazon EC2 (Elastic Compute Cloud) is a cloud computing service provided by AWS that allows users to create and manage virtual servers in the cloud.

Security Groups in AWS act as virtual firewalls that control inbound and outbound traffic for EC2 instances.

Understanding Security Groups is very important for:
- Cloud Engineers
- DevOps Engineers
- System Administrators
- Security Engineers

This guide explains how to launch an EC2 instance and configure Security Groups step by step.

---

# What is an EC2 Instance?

An EC2 instance is a virtual machine running in the AWS cloud.

It can be used for:
- Hosting websites
- Running applications
- Database servers
- DevOps tools
- Testing environments

---

# What is a Security Group?

A Security Group is a virtual firewall attached to AWS resources like EC2 instances.

It controls:
- Incoming traffic (Inbound Rules)
- Outgoing traffic (Outbound Rules)

Security Groups help secure cloud infrastructure by allowing only authorized traffic.

---

# Important Features of Security Groups

- Stateful firewall
- Allow rules only
- Attached at instance level
- Controls network traffic
- Supports multiple rules

---

# Common Ports Used in Security Groups

| Service | Port |
|---|---|
| SSH | 22 |
| HTTP | 80 |
| HTTPS | 443 |
| MySQL | 3306 |
| PostgreSQL | 5432 |
| Jenkins | 8080 |

---

# Step-by-Step Guide to Launch an EC2 Instance

# Step 1: Login to AWS Console

Open AWS Console:

```text
https://aws.amazon.com/console/


Login using your AWS account credentials.

Step 2: Open EC2 Dashboard

Search for:

EC2

Then open the EC2 Dashboard.

Step 3: Launch a New EC2 Instance

Click:

Launch Instance
Step 4: Configure Instance Details
Name

Example:

DevOps-Server
Choose AMI (Amazon Machine Image)

Select:

Amazon Linux
Ubuntu
RHEL
Debian

For free tier:

Amazon Linux 2 is recommended.
Choose Instance Type

Select:

t2.micro

or

t3.micro

These are eligible for AWS Free Tier.

Step 5: Create or Select Key Pair

A key pair is used for SSH access.

Create New Key Pair

Example:

Name: devops-key

Download:

.pem

file safely.

Step 6: Configure Security Group

During EC2 setup:

Choose:

Create Security Group
Understanding Inbound and Outbound Rules
Inbound Rules

Control incoming traffic to the EC2 instance.

Example:

Allow SSH access from your laptop.
Outbound Rules

Control outgoing traffic from the EC2 instance.

By default:

All outbound traffic is allowed.
Step 7: Add Security Group Rules
Rule 1: SSH Access
Type	Protocol	Port	Source
SSH	TCP	22	My IP
Purpose

Allows secure remote login to the EC2 instance.

Rule 2: HTTP Access
Type	Protocol	Port	Source
HTTP	TCP	80	Anywhere
Purpose

Allows users to access web applications hosted on the server.

Rule 3: HTTPS Access
Type	Protocol	Port	Source
HTTPS	TCP	443	Anywhere
Purpose

Allows secure encrypted web traffic.

Step 8: Launch Instance

Click:

Launch Instance

AWS will create the EC2 instance.

Step 9: Connect to EC2 Instance

Select the instance and click:

Connect

Use SSH command:

ssh -i devops-key.pem ec2-user@public-ip

Example:

ssh -i devops-key.pem ec2-user@54.x.x.x
Step 10: Verify Security Group Rules

Go to:

EC2 → Instances → Security

You can view:

Inbound rules
Outbound rules
Attached Security Groups
Example Security Group Configuration
Rule Type	Port	Allowed Source
SSH	22	My IP
HTTP	80	0.0.0.0/0
HTTPS	443	0.0.0.0/0
Best Practices for Security Groups
1. Restrict SSH Access

Instead of:

0.0.0.0/0

Use:

My IP

This prevents unauthorized SSH access.

2. Open Only Required Ports

Do not allow unnecessary traffic.

Example:

Open 80 only if hosting a website.
Open 3306 only for database access if needed.
3. Use HTTPS Instead of HTTP

HTTPS encrypts traffic and improves security.

4. Avoid Using All Traffic Rules

Avoid:

All Traffic → Anywhere

unless absolutely necessary.

5. Use Separate Security Groups

Example:

Web Server SG
Database SG
Jenkins SG

This improves security and management.

Real-World DevOps Use Case

Suppose a DevOps engineer deploys a web application on AWS.

The setup may involve:

EC2 instance for application hosting
Security Group allowing:
SSH (22)
HTTP (80)
HTTPS (443)

The engineer may also:

Use Jenkins on port 8080
Connect databases securely
Configure monitoring tools

Security Groups ensure only authorized traffic reaches the servers.

Importance of Security Groups in Cloud Security

Security Groups help:

Prevent unauthorized access
Protect cloud servers
Secure applications
Control network communication
Reduce security risks

They are one of the most important AWS security features.

Difference Between Security Groups and NACLs
Feature	Security Group	NACL
Level	Instance Level	Subnet Level
Stateful	Yes	No
Allow Rules	Yes	Yes
Deny Rules	No	Yes
Troubleshooting Common Issues
SSH Connection Timeout

Possible causes:

Port 22 not allowed
Wrong public IP
Instance stopped
Internet Gateway missing
Website Not Accessible

Possible causes:

Port 80 or 443 blocked
Web server not running
Wrong Security Group attached
Conclusion

AWS EC2 and Security Groups are fundamental concepts in cloud computing and DevOps.

EC2 provides scalable virtual servers, while Security Groups protect those servers by controlling network traffic.

Understanding Security Groups helps DevOps engineers:

Secure cloud infrastructure
Manage application access
Troubleshoot connectivity issues
Deploy secure applications

Mastering EC2 and Security Groups is an essential step toward becoming a cloud and DevOps engineer.

