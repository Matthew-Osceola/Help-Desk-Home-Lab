# NTFS Permissions Configuration & Validation

## Overview

Configured and validated **NTFS permissions** in a Windows Server 2022 Active Directory environment to control access to department and personal folders.

Permissions were assigned using **AGDLP (Accounts → Global Groups → Domain Local Groups → Permissions)**, allowing access to be managed through Active Directory groups instead of assigning permissions directly to individual users.

## Environment

* **Hypervisor:** Oracle VirtualBox
* **Server:** Windows Server 2022
* **Client:** Windows 11 Pro
* **Domain:** `mattosceola.com`
* **File Server:** `OK-DC-01`

## Configuration

### Department Folder Permissions

Configured department folders to grant access through **Domain Local security groups** instead of individual user accounts.

Examples include:

- `DL-Finance-Modify`
- `DL-Finance-Read`
- Department-specific Modify and Read groups

Each folder inherited permissions from the parent where appropriate while retaining department-specific access.

### Personal Folder Permissions

Configured personal user folders so each user could access only their own folder.

Permissions were assigned through Active Directory group membership, preventing unauthorized access from other users while allowing administrators to retain management access.

### AGDLP Implementation

Implemented the AGDLP permission model by assigning:

- Users to **Global Groups**
- Global Groups to **Domain Local Groups**
- Domain Local Groups to NTFS permissions

This approach simplifies permission management by allowing future access changes through group membership rather than modifying folder permissions individually.

## Validation

Verified the NTFS permission configuration by:

- Confirming department groups were assigned to the correct folders.
- Testing access with users from different departments.
- Verifying authorized users could open permitted folders.
- Confirming unauthorized users were denied access.
- Verifying personal folders were accessible only to their assigned users.
- Confirming administrators retained management access.

### Department Folder Security

![Department Folder Security](department-folder-security.png)

### Personal Folder Security

![Personal Folder Security](personal-folder-security.png)

### Finance User Access

![Finance User Access](finance-user-access.png)

### Unauthorized Access Test

![Unauthorized Access Test](unauthorized-access-test.png)

### Personal Folder Access

![Personal Folder Access](personal-folder-access.png)
