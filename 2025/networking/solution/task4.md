# Networking Commands Cheat Sheet for DevOps Engineers

# Introduction

Networking commands are essential tools for DevOps Engineers, System Administrators, Cloud Engineers, and Network Engineers. These commands help troubleshoot connectivity issues, inspect DNS records, monitor ports, test APIs, and verify network communication between systems.

In modern DevOps environments such as:
- AWS
- Kubernetes
- Docker
- Linux Servers
- CI/CD Pipelines

network troubleshooting is a daily task. Understanding networking commands is therefore a fundamental skill for every DevOps engineer.

This guide explains the purpose, syntax, examples, and real-world usage of the most important networking commands.

---

# 1. ping Command

## Purpose

The `ping` command checks network connectivity between two systems.

It sends ICMP (Internet Control Message Protocol) Echo Request packets to the destination host and waits for a response.

---

## Syntax

```bash
ping <hostname-or-ip>
```

---

## Example

```bash
ping google.com
```

---

## Sample Output

```text
64 bytes from google.com: icmp_seq=1 ttl=117 time=24 ms
64 bytes from google.com: icmp_seq=2 ttl=117 time=22 ms
```

---

## Important Information

| Field | Meaning |
|---|---|
| icmp_seq | Packet sequence number |
| ttl | Time To Live |
| time | Response time |

---

## Useful Options

### Send Limited Packets

```bash
ping -c 4 google.com
```

This sends only 4 packets instead of continuous pinging.

---

## Real-World DevOps Usage

- Check server connectivity
- Verify internet access
- Test communication between cloud instances
- Troubleshoot Kubernetes pod communication
- Diagnose network outages

---

# 2. traceroute Command

## Purpose

The `traceroute` command shows the complete path packets travel from source to destination.

It helps identify:
- Network delays
- Routing problems
- Failed network hops

---

## Syntax

```bash
traceroute <hostname-or-ip>
```

---

## Example

```bash
traceroute google.com
```

---

## Sample Output

```text
1  router.local
2  isp-gateway
3  regional-router
4  google.com
```

---

## Windows Equivalent

```cmd
tracert google.com
```

---

## Real-World DevOps Usage

- Diagnose slow internet routes
- Identify failed routers
- Troubleshoot cloud networking issues
- Analyze packet routing paths

---

# 3. netstat Command

## Purpose

The `netstat` command displays:
- Active network connections
- Listening ports
- Routing tables
- Network statistics

It is one of the most useful troubleshooting commands in Linux networking.

---

## Syntax

```bash
netstat [options]
```

---

## Common Examples

### Show Active Connections

```bash
netstat -an
```

---

### Show Listening Ports

```bash
netstat -tulnp
```

---

## Option Explanation

| Option | Meaning |
|---|---|
| -t | TCP connections |
| -u | UDP connections |
| -l | Listening ports |
| -n | Numeric addresses |
| -p | Process information |

---

## Sample Output

```text
tcp   0   0 0.0.0.0:22   0.0.0.0:*   LISTEN
```

This indicates:
- SSH service is listening on port 22.

---

## Real-World DevOps Usage

- Verify running services
- Check open ports
- Detect suspicious connections
- Troubleshoot application networking

---

## Modern Alternative

Many Linux distributions now prefer:

```bash
ss -tulnp
```

instead of `netstat`.

---

# 4. curl Command

## Purpose

The `curl` command transfers data using URLs.

It is heavily used for:
- API testing
- Downloading files
- Testing websites
- Automation scripts

---

## Syntax

```bash
curl <url>
```

---

## Example

```bash
curl https://google.com
```

---

## Get HTTP Headers

```bash
curl -I https://google.com
```

---

## API Request Example

```bash
curl https://api.github.com
```

---

## POST Request Example

```bash
curl -X POST https://example.com/api
```

---

## Download a File

```bash
curl -O https://example.com/file.zip
```

---

## Real-World DevOps Usage

- Test REST APIs
- Perform health checks
- Validate Kubernetes services
- Automate deployments
- Troubleshoot web applications

---

# 5. dig Command

## Purpose

The `dig` command performs DNS lookups and displays detailed DNS information.

It is commonly used for:
- DNS troubleshooting
- Checking DNS records
- Verifying domain resolution

---

## Syntax

```bash
dig <domain>
```

---

## Example

```bash
dig google.com
```

---

## Query Specific Record Types

### A Record

```bash
dig google.com A
```

---

### MX Record

```bash
dig google.com MX
```

---

### NS Record

```bash
dig google.com NS
```

---

## Sample Output

```text
google.com.   300   IN   A   142.250.x.x
```

---

## Real-World DevOps Usage

- Verify DNS records
- Troubleshoot Kubernetes DNS
- Validate cloud networking
- Debug mail server issues

---

# 6. nslookup Command

## Purpose

The `nslookup` command is used to query DNS servers and retrieve domain-related information.

It is simpler than `dig` and commonly used for quick DNS checks.

---

## Syntax

```bash
nslookup <domain>
```

---

## Example

```bash
nslookup google.com
```

---

## Sample Output

```text
Name: google.com
Address: 142.250.x.x
```

---

## Real-World DevOps Usage

- Verify domain resolution
- Check DNS server configuration
- Troubleshoot networking issues
- Validate public and private DNS entries

---

# Difference Between dig and nslookup

| Feature | dig | nslookup |
|---|---|---|
| Detailed Output | Yes | Limited |
| Preferred in Linux | Yes | Basic Usage |
| Advanced DNS Queries | Supported | Limited |

---

# Additional Useful Networking Commands

# ip Command

## Purpose

Displays and manages network interfaces and IP addresses.

---

## Example

```bash
ip addr
```

---

# ifconfig Command

## Purpose

Displays network interface configuration.

---

## Example

```bash
ifconfig
```

---

# hostname Command

## Purpose

Displays the hostname of the system.

---

## Example

```bash
hostname
```

---

# ssh Command

## Purpose

Securely connects to remote servers.

---

## Example

```bash
ssh user@server-ip
```

---

# wget Command

## Purpose

Downloads files from the internet.

---

## Example

```bash
wget https://example.com/file.zip
```

---

# Common Networking Troubleshooting Workflow

Suppose a website hosted on AWS EC2 is not accessible.

A DevOps engineer may troubleshoot using the following commands:

| Command | Purpose |
|---|---|
| ping | Check connectivity |
| traceroute | Verify routing path |
| netstat | Check open ports |
| curl | Test HTTP response |
| dig | Verify DNS records |
| nslookup | Confirm domain resolution |

---

# Real-World DevOps Scenario

Suppose an application hosted on AWS is down.

A DevOps engineer may follow these steps:

---

## Step 1: Verify Connectivity

```bash
ping server-ip
```

---

## Step 2: Check Listening Ports

```bash
netstat -tulnp
```

---

## Step 3: Test Application Response

```bash
curl http://server-ip
```

---

## Step 4: Verify DNS Resolution

```bash
dig example.com
```

---

## Step 5: Trace Network Path

```bash
traceroute example.com
```

---

# Best Practices

- Use secure protocols such as HTTPS and SSH
- Monitor open ports regularly
- Restrict unnecessary network access
- Validate DNS configurations
- Use network monitoring tools for observability

---

# Importance of Networking Commands in DevOps

Networking commands help DevOps engineers:
- Troubleshoot infrastructure
- Monitor servers
- Test APIs
- Validate Kubernetes networking
- Secure systems
- Maintain application availability

These commands are part of daily DevOps operations.

---

# Conclusion

Networking commands are fundamental tools for every DevOps Engineer and System Administrator.

Commands such as:
- `ping`
- `traceroute`
- `netstat`
- `curl`
- `dig`
- `nslookup`

help troubleshoot connectivity issues, validate DNS records, test APIs, and maintain reliable infrastructure.

Mastering these commands is essential for managing modern cloud and DevOps environments effectively.