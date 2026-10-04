# 06 - Linux Server

## Goal
Deploy a Linux server in the same virtual environment and practice core Linux administration.

## Procedure

### 1. Install Linux
Create LINUX01 in VMware and install a server-oriented Linux distribution.

### 2. Update packages
Use the update procedure appropriate for the chosen distribution.

Ubuntu/Debian example:

```bash
sudo apt update
sudo apt upgrade
```

### 3. Inspect network configuration

```bash
ip addr
ip route
hostname
hostname -I
```

Configure addressing according to the lab design.

### 4. Create an administrative lab user

```bash
sudo adduser labadmin
```

Grant only the permissions required for the exercise.

### 5. Install and test SSH
If remote administration is part of the lab, install/enable OpenSSH using the distribution's package manager and service manager.

Check status:

```bash
systemctl status ssh
```

The service name can vary by distribution.

### 6. Practice Linux administration

Useful exercises:

```bash
pwd
ls -la
ip addr
ss -tulpn
df -h
free -h
ps aux
systemctl --failed
journalctl -p err
```

### 7. Test cross-platform connectivity
Test communication between LINUX01 and the Windows lab where firewall policy permits it.

## Security Notes
- Do not expose SSH directly to the public Internet for this lab
- Use strong unique credentials
- Prefer key-based SSH authentication when progressing beyond the basic exercise
- Patch the operating system
- Enable only required services

## Screenshots to Capture
1. `images/linux/01-linux-vm.png`
2. `images/linux/02-ip-address.png`
3. `images/linux/03-updates.png`
4. `images/linux/04-user-management.png`
5. `images/linux/05-ssh-status.png`
6. `images/linux/06-connectivity-test.png`

## Skills Demonstrated
Linux, CLI administration, users/groups, networking, package management, services, SSH, troubleshooting.
