#  Cybersecurity Practical Lab & Interview Portfolio

> A practical cybersecurity learning and project portfolio covering networking, Linux security, Windows security, SOC operations, SIEM, IAM, Microsoft Entra ID, Azure security, vulnerability management, threat intelligence, incident response, and an AI-Based Intrusion Detection System.

---

# About Me

I am a BCA graduate interested in:

- Cybersecurity
- Identity and Access Management (IAM)
- Security Operations Center (SOC)
- Microsoft Entra ID
- Azure Security
- Cloud Security
- Networking
- Linux and Windows Security
- Incident Response
- Threat Detection

This repository documents my cybersecurity learning, practical labs, security concepts, projects, and interview preparation.

---

# Table of Contents

- Authentication and Authorization
- Access Control
- Network Security
- Linux Security
- Windows Security
- SOC
- SIEM
- Incident Response
- Threat Intelligence
- IAM
- Microsoft Entra ID
- Azure Security
- Vulnerability Management
- Security Tools
- AI-Based Intrusion Detection System

---

# 1.  Cybersecurity Fundamentals

## What is Cybersecurity?

Cybersecurity is the practice of protecting:

- Computers
- Servers
- Networks
- Applications
- Cloud resources
- Identities
- Data

from unauthorized access, attacks, damage, or disruption.

---

## Threat

A threat is a potential cause of harm to a system, network, application, or data.

### Examples

- Malware
- Phishing
- Unauthorized access
- Denial-of-Service attacks
- Credential theft

---

## Vulnerability

A vulnerability is a weakness in a system that can potentially be exploited by an attacker.

### Example

An outdated application with a known security vulnerability.

---

## Risk

Risk is the possibility that a threat may exploit a vulnerability and cause damage.

Simple relationship:

Threat + Vulnerability + Impact = Risk

---

## Attack

An attack is an attempt to exploit a vulnerability or compromise a system.

---

# 2.  CIA Triad

The CIA Triad is one of the fundamental concepts of cybersecurity.

## Confidentiality

Confidentiality ensures that information is accessible only to authorized users.

### Example

Only authorized employees should be able to access confidential company data.

---

## Integrity

Integrity ensures that information is not modified or deleted without authorization.

### Example

A financial transaction should not be changed by an unauthorized user.

---

## Availability

Availability ensures that systems and data are available when authorized users need them.

### Example

A company's website should remain available to customers.

---

# 3.  Authentication and Authorization

## Authentication

Authentication verifies the identity of a user.

Examples:

- Username and password
- Multi-Factor Authentication
- Biometrics
- Security token
- Digital certificate

### Simple Question

> Who are you?

---

## Authorization

Authorization determines what an authenticated user is allowed to access or perform.

### Simple Question

> What are you allowed to do?

---

## Example

A user logs into a company application.

```text
Username + Password
        ↓
Authentication
        ↓
Identity Verified
        ↓
Authorization
        ↓
Access Based on Permissions
```

---

# 4.  Access Control

Access control determines who can access which resources.

Important principles:

- Least Privilege
- Need to Know
- Role-Based Access Control
- Separation of Duties
- Access Reviews

---

## Least Privilege

Users should receive only the permissions required to perform their job.

### Example

A normal employee should not have Domain Administrator privileges unless there is a legitimate business requirement.

---

## Need to Know

Users should have access to information only when they need that information to perform their job.

---

## Role-Based Access Control

Permissions are assigned based on a user's role.

### Example

```text
Employee
   ↓
Employee Role
   ↓
Required Permissions
   ↓
Company Resources
```

---

## Separation of Duties

Important tasks should be divided between different users or roles to reduce the risk of unauthorized actions.

---

## Access Review

Access reviews verify whether users still need their assigned permissions.

```text
User
 ↓
Current Access
 ↓
Review
 ↓
Business Requirement
 ↓
Keep or Remove Access
```


# 5.  Network Security

Network security is the practice of protecting networks, devices, systems, and data from unauthorized access, attacks, and misuse.

Important network security concepts include:

- OSI Model
- TCP/IP
- IP Address
- MAC Address
- Ports
- Protocols
- DNS
- DHCP
- HTTP/HTTPS
- Firewall
- VPN
- IDS
- IPS
- Network Segmentation

---

## OSI Model

The OSI model has seven layers.

| Layer | Name | Examples |
|---|---|---|
| 7 | Application | HTTP, HTTPS, DNS |
| 6 | Presentation | Encryption, Encoding |
| 5 | Session | Session Management |
| 4 | Transport | TCP, UDP |
| 3 | Network | IP, Router |
| 2 | Data Link | MAC, Switch |
| 1 | Physical | Cable, Fiber |

### Simple Flow

```text
Application
     ↓
Presentation
     ↓
Session
     ↓
Transport
     ↓
Network
     ↓
Data Link
     ↓
Physical
```

---

# 6. TCP/IP Model

The TCP/IP model is commonly used for network communication.

| Layer | Examples |
|---|---|
| Application | HTTP, HTTPS, DNS, SSH |
| Transport | TCP, UDP |
| Internet | IP, ICMP |
| Network Access | Ethernet, Wi-Fi |

---

## TCP

TCP is a connection-oriented protocol.

It provides reliable and ordered delivery of data.

### Example

```text
Client
  ↓
TCP Connection
  ↓
Server
```

---

## UDP

UDP is connectionless and does not guarantee delivery.

It is commonly used where speed is more important than guaranteed delivery.

Examples:

- DNS
- Streaming
- VoIP

---

# 7. IP Address

An IP address identifies a device on a network.

There are two major versions:

- IPv4
- IPv6

### Example IPv4

```text
192.168.1.10
```

---

## Public IP

A public IP address can be used for communication over the Internet.

---

## Private IP

A private IP address is normally used inside internal networks.

### Private IPv4 ranges

```text
10.0.0.0/8

172.16.0.0/12

192.168.0.0/16
```

---

# 8. Ports

A port identifies a communication endpoint for a service.

### Important Ports

| Port | Protocol | Purpose |
|---:|---|---|
| 20/21 | FTP | File Transfer |
| 22 | SSH | Secure Remote Access |
| 23 | Telnet | Remote Access |
| 25 | SMTP | Email |
| 53 | DNS | Name Resolution |
| 67/68 | DHCP | IP Assignment |
| 80 | HTTP | Web |
| 110 | POP3 | Email |
| 143 | IMAP | Email |
| 389 | LDAP | Directory Services |
| 443 | HTTPS | Secure Web |
| 445 | SMB | File Sharing |
| 636 | LDAPS | Secure LDAP |
| 3389 | RDP | Remote Desktop |

---

# 9. DNS

DNS stands for Domain Name System.

DNS translates domain names into IP addresses.

### Example

```text
www.example.com
       ↓
DNS
       ↓
IP Address
```

Instead of remembering an IP address, users can use a domain name.

---

# 10. DHCP

DHCP stands for Dynamic Host Configuration Protocol.

DHCP automatically provides network configuration to devices.

It can provide:

- IP Address
- Subnet Mask
- Default Gateway
- DNS Server

### DHCP Process

```text
Discover
   ↓
Offer
   ↓
Request
   ↓
Acknowledgment
```

This is commonly called the **DORA process**.

---

# 11.  HTTP and HTTPS

## HTTP

HTTP is used for communication between web clients and web servers.

Default port:

```text
80
```

---

## HTTPS

HTTPS is HTTP secured using TLS.

Default port:

```text
443
```

HTTPS provides protection for data while it is transmitted between the client and server.

---

# 12.  Firewall

A firewall controls network traffic according to defined security rules.

A firewall can make decisions based on:

- Source IP
- Destination IP
- Source Port
- Destination Port
- Protocol
- Direction

### Example

```text
Internet
    ↓
 Firewall
    ↓
Allow / Deny
    ↓
Internal Network
```

---

## Firewall Example

Suppose an organization wants to allow HTTPS traffic but block unwanted traffic.

```text
HTTPS - 443
      ↓
    ALLOW

Unwanted Traffic
      ↓
    DENY
```

---

# 13.  VPN

VPN stands for Virtual Private Network.

A VPN creates a secure connection over an untrusted network such as the Internet.

### Common Uses

- Remote employee access
- Secure communication
- Site-to-site connectivity
- Access to private resources

### Example

```text
Employee
   ↓
Internet
   ↓
VPN
   ↓
Company Network
   ↓
Internal Resources
```

---

# 14.  IDS

IDS stands for Intrusion Detection System.

An IDS monitors network or system activity and identifies potentially suspicious activity.

When suspicious activity is detected, the IDS can generate an alert.

```text
Network Traffic
      ↓
     IDS
      ↓
Analyze Traffic
      ↓
Suspicious?
   ↙       ↘
 Yes        No
 ↓           ↓
Alert       Normal
```

---

# 15.  IPS

IPS stands for Intrusion Prevention System.

An IPS can detect suspicious activity and can also take preventive action according to its configuration.

### IDS vs IPS

| IDS | IPS |
|---|---|
| Detects suspicious activity | Detects suspicious activity |
| Generates alerts | Can take preventive action |
| Primarily monitoring | Monitoring + prevention |

---

# 16.  Network Segmentation

Network segmentation divides a network into separate sections.

Example:

```text
                 Network
                    |
        -------------------------
        |           |           |
       HR           IT        Security
        |           |           |
     Systems      Systems     Systems
```

Benefits include:

- Limiting access
- Reducing attack surface
- Containing incidents
- Improving network security

---

# 17.  Nmap

Nmap is a network discovery and security auditing tool.

>  Only scan systems that you own or have explicit permission to test.

---

## Basic Scan

```bash
nmap 192.168.1.10
```

---

## Host Discovery

```bash
nmap -sn 192.168.1.0/24
```

---

## Service Detection

```bash
nmap -sV 192.168.1.10
```

---

## OS Detection

```bash
nmap -O 192.168.1.10
```

---

## What Nmap Can Identify

- Live hosts
- Open ports
- Running services
- Service versions
- Network attack surface

---

# 18. Wireshark

Wireshark is a network packet-analysis tool.

It allows security professionals to inspect network traffic.

---

## Common Filters

### TCP

```text
tcp
```

### UDP

```text
udp
```

### DNS

```text
dns
```

### HTTP

```text
http
```

### Specific IP

```text
ip.addr == 192.168.1.10
```

### Specific Port

```text
tcp.port == 443
```

---

## What to Analyze

When analyzing packets, look at:

- Source IP
- Destination IP
- Source Port
- Destination Port
- Protocol
- TCP Flags
- DNS Requests
- Packet Size
- Communication Patterns

---

# 19.  Network Security Practical Workflow

A basic authorized lab workflow can be:

```text
Create Lab Environment
        ↓
Identify Lab Systems
        ↓
Check Network Configuration
        ↓
Perform Authorized Nmap Scan
        ↓
Identify Open Ports
        ↓
Identify Services
        ↓
Capture Traffic with Wireshark
        ↓
Analyze Packets
        ↓
Document Findings
```

---

# 20. Network Security Key Takeaways

### OSI

Seven-layer networking model.

### TCP

Reliable, connection-oriented communication.

### UDP

Fast, connectionless communication.

### IP Address

Identifies a device/interface on a network.

### Port

Identifies a service or communication endpoint.

### DNS

Converts domain names into IP addresses.

### DHCP

Automatically provides network configuration.

### Firewall

Controls network traffic.

### VPN

Provides a secure connection over an untrusted network.

### IDS

Detects suspicious activity.

### IPS

Detects and can prevent suspicious activity.

### Nmap

Used for authorized network discovery and scanning.

### Wireshark

Used for packet and network traffic analysis.
