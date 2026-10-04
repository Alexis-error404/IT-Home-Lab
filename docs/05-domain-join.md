# 05 - Join a Windows Client to the Domain

## Goal
Configure CLIENT01 to use the domain controller for DNS and join it to the Active Directory domain.

## Procedure

### 1. Verify client networking
On CLIENT01:

```cmd
ipconfig /all
ping <DC01-IP>
nslookup <your-domain-name>
```

The client must be able to reach DC01 and resolve the AD domain through the lab DNS server.

### 2. Configure DNS
If DHCP is being used, verify the DHCP scope distributes DC01 as the DNS server. If configuring the client manually, set its DNS server appropriately.

### 3. Join the domain
Open the Windows computer-name/domain settings and join the domain using authorized lab credentials.

Restart the computer when prompted.

### 4. Sign in with a domain account
After restart, sign in using one of the fictional test users created in Active Directory.

### 5. Verify the computer account
On DC01, open **Active Directory Users and Computers** and verify CLIENT01 appears. Move it into the intended Workstations OU if required.

### 6. Test Group Policy

```cmd
gpupdate /force
gpresult /r
whoami
```

Confirm the expected user/computer policies apply.

## Screenshots to Capture
1. `images/domain-client/01-client-network.png`
2. `images/domain-client/02-domain-join.png`
3. `images/domain-client/03-domain-login.png`
4. `images/domain-client/04-computer-in-ad.png`
5. `images/domain-client/05-gpresult.png`

## Skills Demonstrated
Windows endpoint administration, domain enrollment, DNS dependency troubleshooting, AD computer objects, Group Policy validation.
