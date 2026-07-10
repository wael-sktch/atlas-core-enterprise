# Atlas Core Enterprise

> A production-inspired enterprise infrastructure lab demonstrating identity management, network security, and Windows Server administration using industry-standard technologies.

---

## Overview

Atlas Core Enterprise is a hands-on enterprise lab designed to simulate a modern corporate IT environment. The project focuses on secure infrastructure deployment, centralized identity management, network segmentation, and policy-based administration.

The environment is built to reflect real-world enterprise practices used by system administrators, network engineers, and security professionals.

---

## Technologies

- pfSense Firewall
- Windows Server Active Directory
- DNS
- DHCP
- Group Policy (GPO)
- OpenVPN
- SMB File Services
- NTFS Permissions
- Role-Based Access Control (RBAC)
- VLAN Segmentation

---

# Infrastructure

```
                    Internet
                        │
                  ┌────────────┐
                  │  pfSense   │
                  └─────┬──────┘
                        │
        ┌───────────────┼────────────────┐
        │               │                │
     USERS          SERVERS            DMZ
   10.10.10.0     10.10.20.0       10.10.30.0
                        │
                ┌───────────────┐
                │     DC01      │
                │ ActiveDirectory│
                │ DNS / DHCP     │
                └───────────────┘
                        │
                ┌───────────────┐
                │     FS01      │
                │ File Services │
                └───────────────┘

              MGMT Network
             10.10.40.0/24
```

---

# Network Design

| Network | Subnet | Purpose |
|---------|---------|---------|
| USERS | `10.10.10.0/24` | Employee workstations |
| SERVERS | `10.10.20.0/24` | Domain controllers and servers |
| DMZ | `10.10.30.0/24` | Public-facing services |
| MGMT | `10.10.40.0/24` | Administrative management |

---

# Active Directory

The Active Directory environment provides centralized authentication and authorization.

### Domain Services

- Active Directory Domain Services (AD DS)
- DNS
- Organizational Units (OUs)
- Security Groups
- User & Computer Management

### Organizational Structure

```
Atlas.local
│
├── Users
├── Computers
├── Servers
├── IT
├── HR
└── Finance
```

---

# Group Policy

Implemented security baselines include:

- Password Policy
- Account Lockout Policy
- Windows Firewall Configuration
- Desktop Restrictions
- Drive Mapping
- Security Hardening
- Automatic Updates

---

# File Services

Dedicated file server with:

- SMB Shares
- NTFS Permissions
- Departmental Shares
- Role-Based Access Control
- Least Privilege Access

Example:

| Department | Access |
|------------|--------|
| HR | HR Only |
| Finance | Finance Only |
| IT | Full Control |
| Public | Read Only |

---

# pfSense Firewall

The firewall provides:

- Stateful Packet Inspection
- Network Segmentation
- DNS Resolver
- NAT
- Firewall Rules
- VPN Gateway
- Logging & Monitoring

---

# Network Segmentation

Traffic between VLANs is restricted using firewall rules.

Examples:

- Users → DNS Server
- Users → File Server
- Users → Internet
- Block lateral movement
- Restricted management access

---

# Remote Access

Secure remote administration is provided using OpenVPN.

Features include:

- Encrypted VPN Tunnel
- Remote User Authentication
- Internal Resource Access
- Secure Administrative Access

---

# Security Features

- Active Directory Authentication
- Least Privilege Access
- Network Segmentation
- Role-Based Access Control
- Group Policy Enforcement
- Secure Remote Access
- Windows Firewall Policies
- DNS Security
- SMB Permissions

---

# Project Deliverables

-  Active Directory Deployment
-  DNS Configuration
-  Organizational Unit Design
-  Security Groups
-  Group Policy Baseline
-  File Server Deployment
-  SMB Share Permissions
-  NTFS Permissions
-  pfSense Firewall Configuration
-  VLAN Segmentation
-  DNS Resolver
-  NAT Configuration
-  OpenVPN Remote Access

---

# Skills Demonstrated

- Windows Server Administration
- Active Directory
- Group Policy Management
- Network Administration
- pfSense Firewall
- VPN Deployment
- DNS & DHCP
- File Server Administration
- Access Control
- Enterprise Networking
- Cybersecurity Fundamentals
- Infrastructure Design

---

# Future Enhancements

- Microsoft Certificate Services (AD CS)
- Windows Deployment Services (WDS)
- Microsoft Defender for Endpoint
- WSUS
- RADIUS Authentication
- Sysmon
- Centralized SIEM Logging
- Azure AD Hybrid Integration
- Multi-Factor Authentication (MFA)

---

## License

This project is intended for educational and portfolio purposes to demonstrate enterprise systems administration, networking, and cybersecurity skills.
