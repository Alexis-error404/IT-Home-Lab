# 02 - Windows Server Deployment

## Goal
Deploy a Windows Server VM and prepare it to become the central infrastructure server for the lab.

## Procedure

### 1. Install Windows Server
Boot DC01 from the Windows Server ISO and complete the operating-system installation.

### 2. Rename the server
Use Server Manager, Settings, or PowerShell to rename the system to a descriptive hostname such as `DC01`. Restart when required.

### 3. Configure a static IP
A domain controller/DNS server should have a predictable address.

Record:
- IPv4 address
- subnet mask/prefix
- default gateway
- preferred DNS server

Once DC01 provides DNS, its DNS configuration should reflect the intended AD DNS design.

### 4. Install updates
Apply current Windows updates before adding production-like roles.

### 5. Verify configuration

Useful commands:

```powershell
hostname
ipconfig /all
Get-NetIPConfiguration
```

## Validation
- Hostname is correct
- Static IP configuration is correct
- Network connectivity works
- Server is patched
- Server Manager opens without unexpected errors

## Screenshots to Capture
1. `images/windows-server/01-server-desktop.png`
2. `images/windows-server/02-server-manager.png`
3. `images/windows-server/03-hostname.png`
4. `images/windows-server/04-ip-configuration.png`
5. `images/windows-server/05-updates.png`

Mask any information you do not want public.

## Skills Demonstrated
Windows Server installation, hostname management, static IP configuration, patching, PowerShell.
