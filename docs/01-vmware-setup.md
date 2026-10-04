# 01 - VMware Lab Setup

## Goal
Create an isolated virtual environment for the Windows Server, Windows client, and Linux systems used throughout the lab.

## Recommended Virtual Machines

| VM | Role | Suggested Resources |
|---|---|---|
| DC01 | Windows Server / Domain Controller | 2 vCPU, 4 GB RAM, 60 GB disk |
| CLIENT01 | Windows client | 2 vCPU, 4 GB RAM, 60 GB disk |
| LINUX01 | Linux server | 2 vCPU, 2-4 GB RAM, 30 GB disk |

Adjust resources to match the host computer.

## Procedure

### 1. Create the virtual network
Open VMware's virtual network settings and select a network mode suitable for an isolated lab. NAT is convenient when the VMs need Internet access. Host-only networking provides stronger isolation.

Document the subnet selected for the lab.

Example only:

```text
Lab subnet: 192.168.10.0/24
Gateway:    192.168.10.1
DC01:       192.168.10.10
CLIENT01:   DHCP
LINUX01:    192.168.10.20
```

Do not blindly reuse these addresses if they conflict with your network.

### 2. Create DC01
Create a VM for Windows Server, attach the Windows Server ISO, allocate CPU/RAM/storage, and connect its NIC to the lab network.

### 3. Create CLIENT01
Create a Windows client VM on the same virtual network.

### 4. Create LINUX01
Create a Linux VM and connect it to the same lab network.

### 5. Validate networking
After operating systems are installed, confirm each VM has an IP configuration and test connectivity between lab systems.

## Validation
- All three VMs boot successfully
- VMs are attached to the intended virtual network
- Systems can communicate as required by the lab design
- VM names and roles are documented

## Screenshots to Capture
1. `images/vmware/01-virtual-network.png` - VMware virtual network configuration
2. `images/vmware/02-dc01-settings.png` - DC01 VM hardware/settings
3. `images/vmware/03-client01-settings.png` - CLIENT01 settings
4. `images/vmware/04-linux01-settings.png` - LINUX01 settings
5. `images/vmware/05-running-vms.png` - all lab VMs visible/running

## Skills Demonstrated
VMware, virtualization, resource allocation, virtual networking, infrastructure planning.
