# Lab Screenshot Checklist

This directory is where visual evidence of the completed lab should be stored.

## Important
Before uploading a screenshot, inspect it carefully. Do **not** publish passwords, private keys, API tokens, product keys, recovery codes, sensitive personal information, or anything else that should remain private.

## VMware
Save under `images/vmware/`:
- `01-virtual-network.png` - VMware network configuration
- `02-dc01-settings.png` - domain-controller VM settings
- `03-client01-settings.png` - Windows client VM settings
- `04-linux01-settings.png` - Linux VM settings
- `05-running-vms.png` - lab machines running

## Windows Server
Save under `images/windows-server/`:
- `01-server-desktop.png`
- `02-server-manager.png`
- `03-hostname.png`
- `04-ip-configuration.png`
- `05-updates.png`

## Active Directory
Save under `images/active-directory/`:
- `01-ad-ds-role.png`
- `02-domain-controller.png`
- `03-ou-structure.png`
- `04-users.png`
- `05-security-groups.png`
- `06-group-policy.png`

## Networking
Save under `images/networking/`:
- `01-dns-manager.png`
- `02-forward-zone.png`
- `03-dns-test.png`
- `04-dhcp-scope.png`
- `05-dhcp-options.png`
- `06-client-lease.png`

## Domain Client
Save under `images/domain-client/`:
- `01-client-network.png`
- `02-domain-join.png`
- `03-domain-login.png`
- `04-computer-in-ad.png`
- `05-gpresult.png`

## Linux
Save under `images/linux/`:
- `01-linux-vm.png`
- `02-ip-address.png`
- `03-updates.png`
- `04-user-management.png`
- `05-ssh-status.png`
- `06-connectivity-test.png`

## Security
Save under `images/security/`:
- `01-windows-firewall.png`
- `02-account-policy.png`
- `03-event-viewer.png`
- `04-linux-security.png`
- `05-updates.png`

## Troubleshooting
Save under `images/troubleshooting/`:
- `01-problem.png`
- `02-diagnostics.png`
- `03-root-cause.png`
- `04-fix.png`
- `05-validation.png`

## Screenshot Quality
Crop screenshots around the relevant interface while leaving enough context to understand what is being shown. Use readable resolution and consistent filenames. A short caption can be added to the corresponding guide after each screenshot is uploaded.

## Embedding an Image

Example Markdown:

```markdown
![Active Directory OU structure](../images/active-directory/03-ou-structure.png)
```

Once the real screenshots are available, the guides can be updated so each image appears directly underneath its corresponding step.
