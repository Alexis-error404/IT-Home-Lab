# 07 - Security Hardening

## Goal
Apply baseline security practices to reduce unnecessary exposure and demonstrate security-minded administration.

## 1. Patch systems
Keep Windows Server, Windows clients, VMware, and Linux updated.

## 2. Least privilege
Use standard accounts for normal work and privileged accounts only for administrative tasks.

In Active Directory:
- separate administrative roles where practical
- use security groups for authorization
- avoid unnecessary Domain Admin membership

## 3. Account controls
Practice policies covering:
- password requirements
- account lockout
- screen locking
- disabling unused accounts

Changes should be tested in the lab before wider application.

## 4. Firewall
Keep host firewalls enabled and permit only traffic required for lab services.

Windows:

```powershell
Get-NetFirewallProfile
```

Linux tooling varies by distribution. Inspect the active firewall before making changes.

## 5. Service reduction
Disable or remove services and software that are not required for the lab's purpose.

## 6. Logging
Review:
- Windows Event Viewer
- Active Directory-related logs
- authentication events
- Linux system logs/journal

Linux example:

```bash
journalctl
last
```

## 7. Protect secrets
Never commit:
- passwords
- private keys
- API tokens
- recovery keys
- product keys
- sensitive configuration exports

## 8. Backups and snapshots
Use VM snapshots for controlled lab testing, while understanding that snapshots are not a replacement for a proper backup strategy.

## Validation
Document what was hardened, why it was changed, and how functionality was tested afterward.

## Screenshots to Capture
1. `images/security/01-windows-firewall.png`
2. `images/security/02-account-policy.png`
3. `images/security/03-event-viewer.png`
4. `images/security/04-linux-security.png`
5. `images/security/05-updates.png`

## Skills Demonstrated
Least privilege, defense in depth, patch management, firewall administration, logging, identity security, change validation.
