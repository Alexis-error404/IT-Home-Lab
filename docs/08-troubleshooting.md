# 08 - Troubleshooting Playbook

## Goal
Document a repeatable troubleshooting process rather than changing settings randomly.

## Method

### 1. Identify the symptom
Ask:
- What exactly is failing?
- When did it begin?
- What changed?
- Is one system affected or multiple?
- Can the issue be reproduced?

### 2. Check the local system

Windows:

```cmd
hostname
ipconfig /all
route print
```

Linux:

```bash
hostname
ip addr
ip route
```

### 3. Test the network progressively
Test from the closest dependency outward:
1. local TCP/IP configuration
2. gateway or local peer
3. domain controller/server
4. DNS resolution
5. required application/service

### 4. Test DNS

Windows:

```cmd
nslookup <hostname>
ipconfig /displaydns
```

Linux:

```bash
getent hosts <hostname>
```

Use the DNS tools available on the selected distribution.

### 5. Check services

Windows:

```powershell
Get-Service
```

Linux:

```bash
systemctl --failed
systemctl status <service>
```

### 6. Review logs
Use Windows Event Viewer and Linux journal/log files to correlate errors with the reported time.

### 7. Change one thing at a time
Record the hypothesis, action, result, and rollback path.

## Example: Domain Join Fails

Check:
- Is CLIENT01 on the correct VMware network?
- Does it have the expected IP configuration?
- Is its DNS server DC01?
- Can it resolve the AD domain?
- Is DC01 reachable?
- Are AD DS and DNS healthy?
- Is system time reasonably synchronized?
- Are the credentials authorized to perform the join?

## Example: Client Does Not Receive DHCP

Check:
- DHCP service status
- scope activation
- available addresses
- DHCP options
- virtual network configuration
- whether another DHCP service is unexpectedly serving the segment

## Example Incident Record

| Field | Entry |
|---|---|
| Symptom | CLIENT01 cannot resolve DC01 |
| Hypothesis | Incorrect DNS server |
| Test | Review `ipconfig /all` |
| Finding | Client points to wrong DNS server |
| Fix | Correct DHCP/DNS configuration |
| Validation | `nslookup`, domain access, `gpupdate` successful |

## Screenshots to Capture
1. `images/troubleshooting/01-problem.png`
2. `images/troubleshooting/02-diagnostics.png`
3. `images/troubleshooting/03-root-cause.png`
4. `images/troubleshooting/04-fix.png`
5. `images/troubleshooting/05-validation.png`

## Skills Demonstrated
Root-cause analysis, layered troubleshooting, DNS/DHCP diagnostics, Windows/Linux tooling, incident documentation.
