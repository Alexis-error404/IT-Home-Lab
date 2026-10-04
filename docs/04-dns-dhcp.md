# 04 - DNS and DHCP

## Goal
Provide name resolution and automated IP configuration for the Windows lab.

# DNS

Active Directory relies heavily on DNS. Verify the DNS role and inspect the AD-integrated forward lookup zone.

Useful tests:

```cmd
ipconfig /all
nslookup DC01
nslookup <your-domain-name>
```

Create test records only when needed and verify forward name resolution.

# DHCP

## Install the role
Use **Add Roles and Features** to install **DHCP Server**.

## Create a scope
Choose a range appropriate for the virtual subnet.

Document:
- scope name
- starting address
- ending address
- subnet mask/prefix
- exclusions
- lease duration
- gateway option
- DNS server option
- DNS domain option

Activate the scope after validating the configuration.

## Client validation

On CLIENT01:

```cmd
ipconfig /release
ipconfig /renew
ipconfig /all
```

Confirm the client receives an address from the expected scope and uses the lab DNS server.

## Troubleshooting Checks
If DHCP fails:
- verify the DHCP service
- verify scope activation
- check address availability
- confirm VMware network placement
- inspect Windows Firewall where appropriate

If DNS fails:
- verify the client points to the lab DNS server
- inspect DNS records
- test with `nslookup`
- clear cached records if appropriate with `ipconfig /flushdns`

## Screenshots to Capture
1. `images/networking/01-dns-manager.png`
2. `images/networking/02-forward-zone.png`
3. `images/networking/03-dns-test.png`
4. `images/networking/04-dhcp-scope.png`
5. `images/networking/05-dhcp-options.png`
6. `images/networking/06-client-lease.png`

## Skills Demonstrated
DNS, DHCP, IPv4, Windows Server roles, client/server networking, troubleshooting.
