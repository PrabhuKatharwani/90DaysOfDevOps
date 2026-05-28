# Common Protocols and Ports Used in DevOps

# Introduction

Protocols are a set of rules that allow devices, servers, and applications to communicate over a network. Every protocol generally uses a specific port number that helps identify which service should receive the incoming traffic.

In DevOps and cloud environments, protocols and ports are extremely important because applications, servers, APIs, containers, and cloud services constantly communicate with each other over networks.

Understanding protocols and ports is essential for:
- DevOps Engineers
- Cloud Engineers
- System Administrators
- Network Engineers
- Security Engineers

Protocols and ports are widely used in:
- AWS
- Azure
- Docker
- Kubernetes
- CI/CD Pipelines
- Linux Servers
- Monitoring Tools

---

# What is a Protocol?

A protocol is a set of communication rules used between devices and applications over a network.

Examples:
- HTTP
- HTTPS
- SSH
- FTP
- DNS

Protocols define:
- How data is sent
- How data is received
- How communication is established

---

# What is a Port?

A port is a logical communication endpoint used by applications and services.

Each protocol usually uses a specific port number.

Examples:
- HTTP → Port 80
- HTTPS → Port 443
- SSH → Port 22

Ports help the operating system identify which service should receive incoming network traffic.

---

# Common Protocols and Their Ports

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
| Telnet | 23 | Remote access |
| LDAP | 389 | Directory services |
| NTP | 123 | Time synchronization |
| SNMP | 161 | Network monitoring |
| MySQL | 3306 | MySQL database |
| PostgreSQL | 5432 | PostgreSQL database |
| Redis | 6379 | In-memory database |
| MongoDB | 27017 | MongoDB database |
| Jenkins | 8080 | CI/CD automation |
| Kubernetes API | 6443 | Kubernetes control plane |
| Docker | 2375/2376 | Docker daemon communication |

---

# 1. HTTP (HyperText Transfer Protocol)

## Port Number

```text
80
```

---

## Purpose

HTTP is used for communication between web browsers and web servers.

---

## Real-World Example

When users access websites without encryption.

Example:

```text
http://example.com
```

---

## DevOps Relevance

HTTP is used in:
- Web applications
- API communication
- Internal services
- Health checks
- Monitoring systems

---

# 2. HTTPS (HyperText Transfer Protocol Secure)

## Port Number

```text
443
```

---

## Purpose

HTTPS is the secure version of HTTP.

It encrypts communication using SSL/TLS.

---

## Real-World Example

Secure websites such as:
- Banking applications
- GitHub
- Cloud dashboards

Example:

```text
https://github.com
```

---

## DevOps Relevance

HTTPS is essential for:
- Secure application deployment
- API security
- SSL certificate management
- Kubernetes ingress
- Load balancers

---

# 3. FTP (File Transfer Protocol)

## Port Number

```text
21
```

---

## Purpose

FTP is used for transferring files between systems.

---

## Real-World Example

Uploading website files to remote servers.

---

## DevOps Relevance

FTP may be used in:
- Legacy systems
- File transfers
- Backup systems
- Artifact storage

---

## Security Note

FTP is insecure because data is transferred without encryption.

---

# 4. SFTP (SSH File Transfer Protocol)

## Port Number

```text
22
```

---

## Purpose

SFTP securely transfers files using SSH encryption.

---

## Real-World Example

Uploading deployment files securely to Linux servers.

---

## DevOps Relevance

Used for:
- Secure file transfer
- CI/CD artifact upload
- Automated backups
- Remote server management

---

# 5. SSH (Secure Shell)

## Port Number

```text
22
```

---

## Purpose

SSH provides secure remote access to servers.

---

## Example

```bash
ssh user@server-ip
```

---

## Real-World Example

Connecting to AWS EC2 Linux servers remotely.

---

## DevOps Relevance

SSH is heavily used for:
- Server administration
- Infrastructure automation
- Ansible automation
- Git authentication
- Remote deployments

---

# 6. DNS (Domain Name System)

## Port Number

```text
53
```

---

## Purpose

DNS converts domain names into IP addresses.

---

## Real-World Example

Converting:

```text
google.com → 142.250.x.x
```

---

## DevOps Relevance

DNS is important for:
- Application routing
- Kubernetes service discovery
- Cloud networking
- Load balancing
- Domain management

---

# 7. SMTP (Simple Mail Transfer Protocol)

## Port Number

```text
25
```

---

## Purpose

SMTP is used for sending emails.

---

## Real-World Example

Applications sending:
- Password reset emails
- Notifications
- Alerts

---

## DevOps Relevance

Used in:
- Monitoring systems
- Alerting tools
- CI/CD notifications
- Logging systems

---

# 8. POP3 (Post Office Protocol Version 3)

## Port Number

```text
110
```

---

## Purpose

POP3 downloads emails from mail servers.

---

## DevOps Relevance

Used in enterprise mail systems and communication platforms.

---

# 9. IMAP (Internet Message Access Protocol)

## Port Number

```text
143
```

---

## Purpose

IMAP synchronizes emails across multiple devices.

---

## DevOps Relevance

Used in enterprise email infrastructure and cloud communication systems.

---

# 10. Telnet

## Port Number

```text
23
```

---

## Purpose

Telnet provides remote server access.

---

## Security Note

Telnet is insecure because it sends data in plain text.

SSH is preferred instead of Telnet.

---

## DevOps Relevance

Mostly used only for testing legacy systems.

---

# 11. LDAP (Lightweight Directory Access Protocol)

## Port Number

```text
389
```

---

## Purpose

LDAP provides directory and authentication services.

---

## DevOps Relevance

Used in:
- Active Directory
- Centralized authentication
- Enterprise user management

---

# 12. NTP (Network Time Protocol)

## Port Number

```text
123
```

---

## Purpose

Synchronizes time across systems and servers.

---

## DevOps Relevance

Important for:
- Kubernetes clusters
- Logging systems
- Distributed applications
- Monitoring tools

---

# 13. SNMP (Simple Network Management Protocol)

## Port Number

```text
161
```

---

## Purpose

SNMP monitors network devices and infrastructure.

---

## DevOps Relevance

Used for:
- Infrastructure monitoring
- Router monitoring
- Switch monitoring
- Observability systems

---

# Database Ports

# MySQL

## Port Number

```text
3306
```

---

## Purpose

MySQL database communication.

---

## DevOps Relevance

Used by:
- Web applications
- Backend systems
- Cloud applications

---

# PostgreSQL

## Port Number

```text
5432
```

---

## Purpose

PostgreSQL database communication.

---

## DevOps Relevance

Widely used in:
- Cloud-native applications
- Kubernetes environments
- Enterprise applications

---

# Redis

## Port Number

```text
6379
```

---

## Purpose

Redis in-memory database communication.

---

## DevOps Relevance

Used for:
- Caching
- Session management
- Message queues

---

# MongoDB

## Port Number

```text
27017
```

---

## Purpose

MongoDB database communication.

---

## DevOps Relevance

Used in scalable NoSQL applications.

---

# DevOps Tools and Their Ports

# Jenkins

## Port Number

```text
8080
```

---

## Purpose

Jenkins automation server.

---

## DevOps Relevance

Used for:
- CI/CD pipelines
- Build automation
- Deployment automation

---

# Kubernetes API Server

## Port Number

```text
6443
```

---

## Purpose

Communication with Kubernetes control plane.

---

## DevOps Relevance

Used by:
- kubectl
- Automation tools
- Kubernetes administrators

---

# Docker Daemon

## Port Numbers

```text
2375 / 2376
```

---

## Purpose

Docker daemon communication.

---

## DevOps Relevance

Used for:
- Container management
- Remote Docker API communication

---

# Importance of Protocols and Ports in DevOps

Protocols and ports are extremely important because DevOps engineers work with:
- Linux servers
- Cloud infrastructure
- Containers
- Kubernetes
- APIs
- Databases
- CI/CD tools

Common tasks include:
- Opening firewall ports
- Configuring Security Groups
- Troubleshooting network issues
- Testing APIs
- Securing infrastructure

---

# Real-World DevOps Scenario

Suppose a DevOps engineer deploys an application on AWS.

The setup may involve:
- HTTPS (443) for secure web traffic
- SSH (22) for server access
- DNS (53) for domain resolution
- Jenkins (8080) for CI/CD
- MySQL (3306) for database connectivity
- Kubernetes API (6443) for cluster management

This demonstrates how protocols and ports are used together in real-world DevOps environments.

---

# Security Best Practices

- Use HTTPS instead of HTTP
- Restrict unnecessary ports
- Avoid Telnet and use SSH
- Secure databases using firewall rules
- Use Security Groups and firewalls properly
- Monitor open ports regularly

---

# Conclusion

Protocols and ports form the foundation of networking and DevOps infrastructure.

Every application, cloud service, API, container, and deployment pipeline depends on network communication.

Understanding protocols and ports helps DevOps engineers:
- Secure infrastructure
- Troubleshoot networking issues
- Configure cloud environments
- Manage CI/CD pipelines
- Deploy scalable applications

Mastering these concepts is an essential step toward becoming a successful DevOps engineer.