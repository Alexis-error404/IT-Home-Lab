# IT Infrastructure Home Lab

A hands-on IT infrastructure portfolio project documenting the deployment and administration of a small enterprise-style virtual environment.

## Overview

This lab is designed to demonstrate practical skills in virtualization, Windows Server, Active Directory, DNS, DHCP, Windows domain administration, Linux, networking, security hardening, and troubleshooting.

```text
                         IT HOME LAB
                              |
                     VMware Virtual Network
                              |
          +-------------------+-------------------+
          |                   |                   |
   Windows Server DC     Windows Client      Linux Server
   AD DS / DNS / DHCP    Domain Joined       Linux Services
          |
   Users / Groups / OUs
          |
      Group Policy
```

## Objectives

- Build and configure virtual machines using VMware
- Install and administer Windows Server
- Deploy Active Directory Domain Services
- Create Organizational Units, users, and security groups
- Configure DNS and DHCP
- Join Windows clients to the domain
- Configure and test Group Policy
- Deploy and administer a Linux server
- Practice TCP/IP and name-resolution troubleshooting
- Apply basic system and account security controls
- Document the environment with repeatable procedures and screenshots

## Technologies

| Area | Technologies |
|---|---|
| Virtualization | VMware |
| Server Administration | Windows Server |
| Identity | Active Directory Domain Services |
| Networking | DNS, DHCP, TCP/IP |
| Endpoint Administration | Windows client |
| Linux | Linux server administration |
| Security | Least privilege, firewall, patching, account controls |
| Troubleshooting | ping, ipconfig, nslookup, PowerShell, Linux CLI |

## Lab Guides

1. [VMware Lab Setup](docs/01-vmware-setup.md)
2. [Windows Server Deployment](docs/02-windows-server.md)
3. [Active Directory](docs/03-active-directory.md)
4. [DNS and DHCP](docs/04-dns-dhcp.md)
5. [Domain Join](docs/05-domain-join.md)
6. [Linux Server](docs/06-linux-server.md)
7. [Security Hardening](docs/07-security-hardening.md)
8. [Troubleshooting](docs/08-troubleshooting.md)
9. [Screenshot Checklist](images/README.md)

## Skills Demonstrated

- Virtual machine deployment and configuration
- Windows Server administration
- Active Directory domain deployment
- OU, user, and group administration
- DNS name resolution
- DHCP configuration
- Windows domain enrollment
- Group Policy fundamentals
- Linux command-line administration
- Network configuration and troubleshooting
- Security hardening and least privilege
- Technical documentation

## Screenshot Documentation

Each guide includes suggested evidence to capture. Screenshots should be saved under the matching folder in `images/`. Never publish passwords, product keys, API tokens, private keys, or other secrets.

## Why I Built This Lab

I built this environment to strengthen my practical systems-administration and cybersecurity skills beyond theory. It provides a controlled environment where I can deploy enterprise technologies, make configuration changes, troubleshoot failures, validate solutions, and document the results.

## Future Improvements

- PowerShell administration and automation
- Centralized logging
- Additional Group Policies
- Vulnerability scanning
- Backup and recovery testing
- Network segmentation
- Additional Linux services
- Security monitoring

---

**Author:** Alexis Wiscovitch  
**GitHub:** @Alexis-error404
