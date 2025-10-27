# Active Directory Integration Project: Windows Server & Linux Database Server

## Project Overview

This project demonstrates a comprehensive enterprise integration scenario where a Linux server running a database service successfully joins a Windows Active Directory domain. The implementation includes Windows Server with AD DS, DNS, and DHCP roles, and a Linux server with PostgreSQL/MySQL database, fully integrated into the Active Directory domain.

## Network Architecture

```
┌───────────────────────────────────────────────────────┐
│                    CORPORATE NETWORK                  │
│                                                       │
│  ┌──────────────────────┐    ┌──────────────────┐     │
│  │   Windows Server     │    │   Linux Server   │     │
│  │   (Domain Controller)│    │  (Database Server)│    │
│  │                      │    │                  │     │
│  │ • AD DS Domain       │    │ • PostgreSQL/    │     │
│  │   Controller         │    │   MySQL Database │     │
│  │ • DNS Server         │    │ • Domain Joined  │     │
│  │ • DHCP Server        │    │ • Samba Winbind  │     │
│  │ • IP: 192.168.1.10   │    │ • IP: 192.168.1.20│    │
│  │ • Domain: Xpandcs.local│  │                  │     │
│  └──────────────────────┘    └──────────────────┘     │
│           ↑                           ↑               │
│           └───────────┬───────────────┘               │
│                       │                               │
│                 ┌─────────────┐                       │
│                 │   Switch    │                       │
│                 └─────────────┘                       │
│                       ↑                               │
│                 ┌─────────────┐                       │
│                 │   Clients   │                       │
│                 │ (DHCP)      │                       │
│                 └─────────────┘                       │
└───────────────────────────────────────────────────────┘
![alt text](image-1.png)
```

### System Specifications

#### Windows Server
- **Role**: Domain Controller
- **IP Address**: 192.168.1.10/24
- **Hostname**: WIN-DC01
- **Domain**: Xpandcs.local
- **Services**: AD DS, DNS, DHCP

#### Linux Server
- **Role**: Database Server
- **IP Address**: 192.168.1.20/24
- **Hostname**: linux-db01
- **Services**: PostgreSQL/MySQL, Samba Winbind
- **Domain Joined**: Xpandcs.local

## Implementation Guide

### Phase 1: Windows Server Setup

#### 1.1 Install Windows Server 2019/2022
- Install Windows Server with Desktop Experience
- Set static IP: 192.168.1.10/24
- Configure computer name: WIN-DC01

#### 1.2 Install AD DS, DNS, and DHCP
- Install Active Directory Domain Services
- Install DNS Server role
- Install DHCP Server role
- Configure domain: Xpandcs.local
- Set up DHCP scope for client computers

### Phase 2: Linux Server Setup

#### 2.1 Install Linux (Ubuntu/CentOS)
- Install Ubuntu Server 20.04/22.04 or CentOS 8
- Set static IP: 192.168.1.20/24
- Configure hostname: linux-db01

#### 2.2 Install and Configure Database
- Install PostgreSQL or MySQL database
- Create sample database: companydb
- Configure database users and permissions

### Phase 3: Active Directory Integration

#### 3.1 Prepare AD for Linux Integration
- Create service account for Linux machine join
- Create Organizational Unit for Linux servers
- Configure necessary permissions

#### 3.2 Configure Linux for AD Join
- Install required packages: realmd, sssd, samba
- Configure DNS to point to Windows DC
- Join Linux machine to Active Directory domain
- Configure SSSD for authentication

## Script Case

### PowerShell Domain Health Monitoring
```powershell
# DomainHealthCheck.ps1
# Monitors AD DS, DNS, and DHCP services for Xpandcs domain
# Checks domain joined computers
# Generates health reports
```

### Bash AD Integration Checking
```bash
#!/bin/bash
# ad-integration-check.sh
# Verifies AD connectivity for Xpandcs.local
# Tests Kerberos authentication
# Monitors domain join status
```

### Python Integration Testing
```python
# db_ad_test.py
# Tests database connectivity with Xpandcs domain
# Verifies AD integration
# Creates test records in database
```

## Project Deliverables

1. **Network Diagram** - Visual representation of the Xpandcs infrastructure
2. **Windows Server Configuration** - Fully configured AD DS, DNS, DHCP services for Xpandcs.local
3. **Linux Server** - Database server integrated with Xpandcs Active Directory
4. **Script Case** - Automation and monitoring scripts including:
   - PowerShell domain health monitoring for Xpandcs
   - Bash AD integration checking for Xpandcs.local
   - Python integration testing
5. **Documentation** - Complete implementation guide for Xpandcs domain
6. **Verification Procedures** - Steps to validate the integration with Xpandcs domain

## Prerequisites

- Windows Server 2019/2022 ISO
- Ubuntu Server 20.04/22.04 or CentOS 8 ISO
- Virtualization platform (VMware, Hyper-V, or VirtualBox)
- Sufficient hardware resources (RAM, CPU, storage)
- Network connectivity between servers

## Success Criteria

- Linux server successfully joined to Xpandcs Active Directory domain
- Database services running on Linux server
- Xpandcs AD users can authenticate to Linux server
- DNS resolution working between servers
- DHCP serving IP addresses to clients
- All scripts executing without errors

## Troubleshooting Areas

- DNS configuration and resolution for Xpandcs.local
- Kerberos authentication issues
- Firewall and network connectivity
- Service account permissions in Xpandcs domain
- Time synchronization between servers
- SSSD configuration problems

## Domain Information
- **Domain Name**: Xpandcs.local
- **NetBIOS Name**: XPANDCS
- **Domain Controller**: WIN-DC01.Xpandcs.local
- **DNS Server**: 192.168.1.10

## File Information
- **Filename**: AD-Integration-Project-Xpandcs-README.md
- **Project Name**: Xpandcs Domain Integration Project
- **Version**: 1.0
- **Created**: Documentation for Xpandcs domain implementation

