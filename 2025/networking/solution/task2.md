# Common Protocols and Ports Used in DevOps

# Introduction

Protocols are a set of rules that allow devices and applications to communicate over a network. In DevOps and cloud environments, protocols are extremely important because they help systems exchange data securely and efficiently.

Every protocol usually works on a specific port number. Ports help identify which service or application should receive the incoming network traffic.

Understanding protocols and ports is essential for:
- DevOps Engineers
- Cloud Engineers
- System Administrators
- Network Engineers
- Security Engineers

---

# What is a Port?

A port is a logical communication endpoint used by network services.

Example:
- HTTP uses Port 80
- HTTPS uses Port 443

When a client sends a request to a server, the port number tells the operating system which application should handle the request.

---

# Common Protocols and Ports

| Protocol | Port Number | Purpose |
|---|---|---|
| HTTP | 80 | Web communication |
| HTTPS | 443 | Secure web communication |
| FTP | 21 | File transfer |
| SFTP | 22 | Secure file transfer |
| SSH | 22 | Secure remote login |
| DNS | 53 | Domain name resolution |
| SMTP | 25 | Sending emails |
| POP3 | 110 | Receiving emails |
| IMAP | 143 | Email synchronization |
| Telnet | 23 | Remote access (insecure) |
| LDAP | 389 | Directory services |
| NTP | 123 | Time synchronization |
| SNMP | 161 | Network monitoring |
| MySQL | 3306 | MySQL database |
| PostgreSQL | 5432 | PostgreSQL database |
| Redis | 6379 | In-memory database |
| MongoDB | 27017 | MongoDB database |
| Kubernetes API | 6443 | Kubernetes control plane |
| Jenkins | 8080 | Jenkins automation server |
| Docker | 2375/2376 | Docker daemon communication |

---

1. HTTP (HyperText Transfer Protocol)

port 

80



Purpose

HTTP is used for communication between web browsers and web servers.

Real-World Example

When users access websites without encryption.

Example:

http://example.com
DevOps Relevance
Used for web applications
API communication
Health checks in monitoring systems
Internal application traffic

---

# 1. HTTP (HyperText Transfer Protocol)

## Port
443
Purpose

HTTPS is the secure version of HTTP. It encrypts data using SSL/TLS.

Real-World Example

Secure banking websites and login pages.

Example:

https://github.com
DevOps Relevance
Secure application deployment
SSL certificate management
Secure APIs
Kubernetes ingress controllers
Cloud load balancers
3. FTP (File Transfer Protocol)
Port
21
Purpose

Used for transferring files between systems.

Real-World Example

Uploading website files to a server.

DevOps Relevance
Legacy deployment systems
File backups
Artifact transfer
Security Note

FTP is not encrypted and is considered insecure.

4. SFTP (SSH File Transfer Protocol)
Port
22
Purpose

Securely transfers files using SSH encryption.

Real-World Example

Securely uploading application files to Linux servers.

DevOps Relevance
Secure CI/CD artifact transfer
Server automation
Backup management
5. SSH (Secure Shell)
Port
22
Purpose

Provides secure remote access to servers.

Real-World Example

Connecting to Linux servers using terminal.

Example:

ssh user@server-ip
DevOps Relevance
Server administration
Remote deployments
GitHub authentication using SSH keys
Infrastructure automation using Ansible
6. DNS (Domain Name System)
Port
53
Purpose

Converts domain names into IP addresses.

Real-World Example

Converting:

google.com → 142.250.x.x
DevOps Relevance
Route traffic to applications
Kubernetes service discovery
Cloud networking
Load balancing
7. SMTP (Simple Mail Transfer Protocol)
Port
25
Purpose

Used for sending emails.

Real-World Example

Sending password reset emails from applications.

DevOps Relevance
Alert notifications
Monitoring systems
CI/CD email reports
8. POP3 (Post Office Protocol Version 3)
Port
110
Purpose

Used for downloading emails from mail servers.

DevOps Relevance

Used in email systems and enterprise communication infrastructure.

9. IMAP (Internet Message Access Protocol)
Port
143
Purpose

Allows synchronization of emails across multiple devices.

DevOps Relevance

Used in enterprise email services and cloud mail platforms.

10. Telnet
Port
23
Purpose

Remote server access protocol.

Security Note

Telnet is insecure because it sends data in plain text.

DevOps Relevance

Mostly replaced by SSH.

11. LDAP (Lightweight Directory Access Protocol)
Port
389
Purpose

Used for directory and authentication services.

DevOps Relevance
Centralized authentication
Enterprise user management
Active Directory integration
12. NTP (Network Time Protocol)
Port
123
Purpose

Synchronizes system time across servers.

DevOps Relevance
Kubernetes clusters
Log synchronization
Monitoring systems
Distributed systems
13. SNMP (Simple Network Management Protocol)
Port
161
Purpose

Used for network monitoring and management.

DevOps Relevance
Infrastructure monitoring
Router/switch monitoring
Observability systems
Database Ports
MySQL
Port
3306
DevOps Relevance

Used by applications hosted on servers and cloud platforms.

PostgreSQL
Port
5432
DevOps Relevance

Widely used in cloud-native applications and Kubernetes environments.

Redis
Port
6379
DevOps Relevance

Caching, message queues, and fast data storage.

MongoDB
Port
27017
DevOps Relevance

NoSQL database used in scalable web applications.

DevOps Tools and Their Ports
Jenkins
Port
8080
Purpose

Automation server for CI/CD pipelines.

DevOps Relevance
Build automation
Deployment automation
Continuous Integration
Kubernetes API Server
Port
6443
Purpose

Communication with Kubernetes control plane.

DevOps Relevance
Cluster management
kubectl communication
Automation scripts
Docker Daemon
Ports
2375 / 2376
Purpose

Docker daemon communication.

DevOps Relevance
Container management
Remote Docker API
Importance of Protocols and Ports in DevOps

Understanding protocols and ports is important because DevOps engineers frequently work with:

Cloud infrastructure
CI/CD pipelines
Kubernetes
Docker containers
Linux servers
Monitoring tools
Security groups and firewalls

Common tasks include:

Opening firewall ports
Troubleshooting connectivity issues
Configuring load balancers
Managing secure communication
Deploying applications
Real-World DevOps Scenario

Suppose a DevOps engineer deploys a web application on AWS.

The workflow may involve:

HTTPS (443) for secure user traffic
SSH (22) for server access
DNS (53) for domain resolution
MySQL (3306) for database connectivity
Jenkins (8080) for CI/CD pipelines
Kubernetes API (6443) for cluster management

This shows how protocols and ports are essential in real-world DevOps operations.

Conclusion

Protocols and ports form the foundation of networking and DevOps infrastructure. Every application, cloud service, and deployment pipeline depends on network communication.

A strong understanding of protocols and ports helps DevOps engineers:

Deploy applications efficiently
Secure infrastructure
Troubleshoot network issues
Configure cloud services
Manage automation tools

Mastering these concepts is an important step toward becoming a successful DevOps engineer.