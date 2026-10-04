# 03 - Active Directory Domain Services

## Goal
Turn DC01 into a domain controller and practice identity administration with Active Directory.

## 1. Install AD DS
In Server Manager:

1. Select **Add Roles and Features**
2. Choose **Role-based or feature-based installation**
3. Select DC01
4. Select **Active Directory Domain Services**
5. Add required features
6. Complete installation

## 2. Promote the server
After installation, select **Promote this server to a domain controller**.

For a new lab, create a new forest using a lab-only domain name of your choice. Do not publish real passwords in this repository.

Complete the wizard and restart.

## 3. Verify Active Directory
Open **Active Directory Users and Computers** and verify the domain is available.

PowerShell validation:

```powershell
Get-ADDomain
Get-ADForest
```

## 4. Build an OU structure
Create a simple organization structure such as:

```text
Lab
├── Users
├── Workstations
├── Servers
└── Groups
```

## 5. Create test users
Create several fictional lab accounts. Never publish real employee/user information.

Example:
- Test User 01
- Test User 02
- Help Desk Admin

## 6. Create security groups
Examples:
- IT-Admins
- Helpdesk
- Standard-Users

Use group membership to practice role-based access rather than assigning permissions individually.

## 7. Group Policy exercise
Create a test GPO and link it to an appropriate OU. Safe examples include:
- screen-lock policy
- password/account policy exercises
- desktop settings
- Windows security settings

Validate on a client with:

```cmd
gpupdate /force
gpresult /r
```

## Screenshots to Capture
1. `images/active-directory/01-ad-ds-role.png`
2. `images/active-directory/02-domain-controller.png`
3. `images/active-directory/03-ou-structure.png`
4. `images/active-directory/04-users.png`
5. `images/active-directory/05-security-groups.png`
6. `images/active-directory/06-group-policy.png`

## Skills Demonstrated
AD DS, domain controllers, forests/domains, OUs, user administration, security groups, Group Policy, RBAC concepts.
