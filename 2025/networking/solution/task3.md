# AWS EC2 and Security Groups

# Introduction

Amazon Web Services (AWS) is one of the most widely used cloud computing platforms in the world. AWS provides many cloud services such as virtual machines, databases, storage, networking, and security services.

One of the most important AWS services is:

```text
Amazon EC2 (Elastic Compute Cloud)
```

EC2 allows users to launch and manage virtual servers in the cloud.

To secure these servers, AWS provides a feature called:

```text
Security Groups
```

Security Groups act as virtual firewalls that control incoming and outgoing traffic for EC2 instances.

Understanding EC2 and Security Groups is essential for:
- DevOps Engineers
- Cloud Engineers
- System Administrators
- Security Engineers

This guide explains:
- What EC2 is
- What Security Groups are
- How to launch an EC2 instance
- How to configure Security Groups
- Best security practices
- Real-world DevOps use cases

---

# What is Amazon EC2?

Amazon EC2 (Elastic Compute Cloud) is a cloud service that provides virtual servers on demand.

EC2 instances can be used for:
- Hosting websites
- Running applications
- Databases
- CI/CD tools
- Kubernetes clusters
- Development and testing environments

---

# Benefits of EC2

- Scalable infrastructure
- Pay-as-you-go pricing
- Easy deployment
- Cloud accessibility
- Flexible configurations

---

# What is a Security Group?

A Security Group is a virtual firewall attached to AWS resources such as EC2 instances.

It controls:
- Inbound traffic (incoming traffic)
- Outbound traffic (outgoing traffic)

Security Groups help protect cloud infrastructure from unauthorized access.

---

# Important Features of Security Groups

| Feature | Description |
|---|---|
| Stateful Firewall | Return traffic is automatically allowed |
| Instance Level Security | Applied directly to EC2 instances |
| Allow Rules Only | Supports allow rules, not deny rules |
| Multiple Rules | Multiple ports and protocols supported |
| Highly Secure | Restricts unauthorized access |

---

# Common Ports Used in AWS Security Groups

| Service | Port Number |
|---|---|
| SSH | 22 |
| HTTP | 80 |
| HTTPS | 443 |
| MySQL | 3306 |
| PostgreSQL | 5432 |
| Jenkins | 8080 |
| Kubernetes API | 6443 |

---

# Understanding Inbound and Outbound Rules

# Inbound Rules

Inbound rules control traffic coming INTO the EC2 instance.

Example:
- Allow SSH access from your laptop.

---

# Outbound Rules

Outbound rules control traffic leaving the EC2 instance.

By default:
- AWS allows all outbound traffic.

---

# Step-by-Step Guide to Launch an EC2 Instance

# Step 1: Login to AWS Console

Open AWS Console:

```text
https://aws.amazon.com/console/
```

Login using your AWS account credentials.

---

# Step 2: Open EC2 Dashboard

Search for:

```text
EC2
```

Then open the EC2 Dashboard.

---

# Step 3: Launch a New EC2 Instance

Click:

```text
Launch Instance
```

---

# Step 4: Configure Instance Details

# Instance Name

Example:

```text
DevOps-Server
```

---

# Choose AMI (Amazon Machine Image)

Select an operating system such as:
- Amazon Linux
- Ubuntu
- RHEL
- Debian

For beginners and free tier usage:

```text
Amazon Linux 2
```

is recommended.

---

# Choose Instance Type

Select:

```text
t2.micro
```

or

```text
t3.micro
```

These instance types are eligible for AWS Free Tier.

---

# Step 5: Create or Select a Key Pair

A key pair is required for secure SSH login.

# Create New Key Pair

Example:

```text
devops-key
```

Download the:

```text
.pem
```

file safely.

---

# Step 6: Configure Security Group

During instance setup:

Choose:

```text
Create Security Group
```

---

# Step 7: Add Security Group Rules

# Rule 1: SSH Access

| Type | Protocol | Port | Source |
|---|---|---|---|
| SSH | TCP | 22 | My IP |

---

## Purpose

Allows secure remote login to the EC2 instance.

---

# Rule 2: HTTP Access

| Type | Protocol | Port | Source |
|---|---|---|---|
| HTTP | TCP | 80 | Anywhere |

---

## Purpose

Allows users to access web applications hosted on the EC2 server.

---

# Rule 3: HTTPS Access

| Type | Protocol | Port | Source |
|---|---|---|---|
| HTTPS | TCP | 443 | Anywhere |

---

## Purpose

Allows secure encrypted web traffic.

---

# Step 8: Launch Instance

Click:

```text
Launch Instance
```

AWS will create the EC2 instance.

---

# Step 9: Connect to EC2 Instance

Select the instance and click:

```text
Connect
```

Use SSH command:

```bash
ssh -i devops-key.pem ec2-user@public-ip
```

---

# Example

```bash
ssh -i devops-key.pem ec2-user@54.x.x.x
```

---

# Step 10: Verify Security Group Rules

Navigate to:

```text
EC2 → Instances → Security
```

You can view:
- Inbound rules
- Outbound rules
- Attached Security Groups

---

# Example Security Group Configuration

| Rule Type | Port | Allowed Source |
|---|---|---|
| SSH | 22 | My IP |
| HTTP | 80 | 0.0.0.0/0 |
| HTTPS | 443 | 0.0.0.0/0 |

---

# Real-World DevOps Example

Suppose a DevOps engineer deploys a web application on AWS EC2.

The setup may include:
- EC2 instance for application hosting
- Security Group allowing:
  - SSH (22)
  - HTTP (80)
  - HTTPS (443)

Additional services may include:
- Jenkins on port 8080
- MySQL on port 3306
- Kubernetes API on port 6443

Security Groups ensure that only authorized traffic reaches the server.

---

# Why Security Groups Are Important

Security Groups help:
- Protect cloud servers
- Prevent unauthorized access
- Restrict malicious traffic
- Secure applications
- Control network communication

Without proper Security Group configuration, cloud servers may become vulnerable to attacks.

---

# Best Practices for Security Groups

# 1. Restrict SSH Access

Instead of:

```text
0.0.0.0/0
```

Use:

```text
My IP
```

This prevents unauthorized SSH access.

---

# 2. Open Only Required Ports

Do not expose unnecessary ports.

Example:
- Open port 80 only if hosting a website.
- Open database ports only when required.

---

# 3. Use HTTPS Instead of HTTP

HTTPS encrypts communication and improves security.

---

# 4. Avoid Allowing All Traffic

Avoid rules such as:

```text
All Traffic → Anywhere
```

unless absolutely necessary.

---

# 5. Use Separate Security Groups

Examples:
- Web Server Security Group
- Database Security Group
- Jenkins Security Group

This improves security and management.

---

# Difference Between Security Groups and NACLs

| Feature | Security Group | NACL |
|---|---|---|
| Applied At | Instance Level | Subnet Level |
| Stateful | Yes | No |
| Allow Rules | Yes | Yes |
| Deny Rules | No | Yes |

---

# Common Troubleshooting Issues

# SSH Connection Timeout

Possible reasons:
- Port 22 blocked
- Wrong Security Group
- Incorrect public IP
- Internet Gateway missing

---

# Website Not Accessible

Possible reasons:
- Port 80 or 443 not allowed
- Web server not running
- Incorrect Security Group attached

---

# EC2 Instance Unreachable

Possible reasons:
- Instance stopped
- Security Group misconfigured
- Route table issues

---

# Importance of EC2 and Security Groups in DevOps

EC2 and Security Groups are fundamental concepts in:
- AWS Cloud
- DevOps Engineering
- Infrastructure Automation
- Kubernetes
- Cloud Security

DevOps engineers frequently use them for:
- Application deployment
- CI/CD pipelines
- Infrastructure management
- Monitoring systems
- Secure cloud networking

---

# Real-World DevOps Scenario

Suppose a DevOps engineer deploys a Node.js application on AWS.

The infrastructure may involve:
- EC2 instance hosting the application
- Security Group allowing:
  - SSH (22)
  - HTTP (80)
  - HTTPS (443)
- Jenkins pipeline for deployment
- Nginx reverse proxy
- Monitoring tools

Security Groups ensure only required traffic is allowed.

---

# Conclusion

Amazon EC2 and Security Groups are core components of AWS cloud infrastructure.

EC2 provides scalable virtual servers, while Security Groups secure those servers by controlling network traffic.

Understanding these concepts helps DevOps engineers:
- Deploy cloud infrastructure securely
- Troubleshoot networking issues
- Protect applications
- Manage cloud environments efficiently

Mastering EC2 and Security Groups is an essential step toward becoming a successful Cloud and DevOps Engineer.