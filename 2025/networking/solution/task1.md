# OSI & TCP/IP Models

## Introduction

Networking models are frameworks that help us understand how data travels from one device to another over a network or the internet. The two most important networking models are:

1. OSI Model (Open Systems Interconnection Model)
2. TCP/IP Model (Transmission Control Protocol/Internet Protocol Model)

These models divide networking into layers. Each layer performs a specific task during communication.

---

# OSI Model

The OSI model contains 7 layers.

```text
7. Application Layer
6. Presentation Layer
5. Session Layer
4. Transport Layer
3. Network Layer
2. Data Link Layer
1. Physical Layer



1. Physical Layer (Layer 1)
Purpose

The Physical Layer is responsible for transmitting raw bits (0s and 1s) over physical media.

Functions
Data transmission through cables or wireless signals
Converts data into electrical or optical signals
Defines hardware specifications
Devices
Hub
Repeater
Ethernet Cable
Fiber Cable
Real-World Example

When an Ethernet cable connects your computer to a router, the Physical Layer transfers electrical signals between devices.

Technologies
Ethernet
Fiber Optics
Wi-Fi Signals
2. Data Link Layer (Layer 2)
Purpose

Provides communication between devices on the same network.

Functions
Uses MAC addresses
Error detection
Frame creation
Devices
Switch
Bridge
Address Used

MAC Address

Real-World Example

When your laptop sends data to a switch in the same office network, the Data Link Layer identifies the correct destination using MAC addresses.

Protocols
Ethernet
PPP
ARP
3. Network Layer (Layer 3)
Purpose

Responsible for routing packets between different networks.

Functions
Path selection
Logical addressing
Packet forwarding
Devices
Router
Address Used

IP Address

Real-World Example

When you access a website hosted in another country, routers use IP addresses to send packets across the internet.

Protocols
IP
ICMP
OSPF
4. Transport Layer (Layer 4)
Purpose

Provides end-to-end communication between systems.

Functions
Segmentation
Error recovery
Flow control
Reliable communication
Protocols
TCP
UDP
Real-World Examples
TCP Example

HTTP websites use TCP because reliable data transfer is required.

UDP Example

Online games and video streaming use UDP because speed is more important than reliability.

5. Session Layer (Layer 5)
Purpose

Manages communication sessions between applications.

Functions
Session establishment
Session maintenance
Session termination
Real-World Example

When you log into a banking website and remain connected until logout, the Session Layer manages that session.

6. Presentation Layer (Layer 6)
Purpose

Responsible for data formatting, encryption, and compression.

Functions
Encryption
Decryption
Compression
Data translation
Real-World Example

HTTPS encrypts browser data using SSL/TLS before sending it over the internet.

Formats and Technologies
SSL/TLS
JPEG
MP3
GIF
7. Application Layer (Layer 7)
Purpose

Provides services directly to end users.

Functions
File transfer
Email services
Web browsing
Protocols
HTTP/HTTPS
FTP
SMTP
DNS
Real-World Example

When you open Google Chrome and access a website using HTTPS, the Application Layer provides the service.

Real-World Example of OSI Model

Suppose a user opens:

https://google.com
OSI Layer	Real-World Activity
Application	Browser sends HTTP/HTTPS request
Presentation	Data encrypted using SSL/TLS
Session	Session established with server
Transport	TCP ensures reliable delivery
Network	IP routes packets
Data Link	MAC addresses used in local network
Physical	Data transmitted through Wi-Fi/cable
TCP/IP Model

The TCP/IP model is the practical networking model used on the internet.

It contains 4 layers.

4. Application Layer
3. Transport Layer
2. Internet Layer
1. Network Access Layer
1. Application Layer
Purpose

Combines OSI Application, Presentation, and Session layers.

Protocols
HTTP
HTTPS
FTP
DNS
SMTP
Real-World Example

Using a browser to access websites.

2. Transport Layer
Purpose

Provides end-to-end communication.

Protocols
TCP
UDP
Real-World Example

TCP ensures complete and reliable file downloads.

3. Internet Layer
Purpose

Handles routing and logical addressing.

Protocols
IP
ICMP
ARP
Real-World Example

Routers use IP addresses to transfer packets across the internet.

4. Network Access Layer
Purpose

Responsible for physical data transmission.

Technologies
Ethernet
Wi-Fi
Real-World Example

Data travels through Ethernet cables or wireless networks.

Difference Between OSI and TCP/IP Models
Feature	OSI Model	TCP/IP Model
Number of Layers	7	4
Developed By	ISO	DARPA
Usage	Reference Model	Practical Internet Model
Session Layer	Separate	Combined
Presentation Layer	Separate	Combined
Real Internet Usage	Limited	Widely Used
Mapping Between OSI and TCP/IP Models
OSI Model	TCP/IP Model
Application	Application
Presentation	Application
Session	Application
Transport	Transport
Network	Internet
Data Link	Network Access
Physical	Network Access
Common Networking Protocols and Their Layers
Protocol	Layer
HTTP/HTTPS	Application
FTP	Application
DNS	Application
TCP	Transport
UDP	Transport
IP	Network
Ethernet	Data Link
Wi-Fi	Physical/Data Link
Why OSI & TCP/IP Models Are Important

These models help in:

Network troubleshooting
Cloud computing
DevOps engineering
Cybersecurity
System administration
Understanding internet communication
Conclusion

The OSI and TCP/IP models are fundamental concepts in networking. The OSI model explains networking in a structured and theoretical way, while the TCP/IP model is the practical model used on the internet today.

Understanding these models helps engineers troubleshoot network problems and understand how devices communicate across networks.