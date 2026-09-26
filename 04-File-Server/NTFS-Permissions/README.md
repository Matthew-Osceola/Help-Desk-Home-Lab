# NTFS Permissions

## Overview

Configured and validated **NTFS permissions** in a Windows Server 2022 Active Directory environment to control access to department and personal folders.

Permissions were assigned using **AGDLP (Accounts → Global Groups → Domain Local Groups → Permissions)**, allowing access to be managed through Active Directory groups instead of assigning permissions directly to individual users.

## Environment

- **Server:** Windows Server 2022
- **Domain:** `mattosceola.com`
- **Domain Controller:** `OK-DC-01`
- **File Server:** `OK-DC-01`
- **Active Directory:** Users, Global Groups, Domain Local Groups
- **Permission Model:** AGDLP

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

*Department folder with Domain Local groups assigned to NTFS permissions.*

### Personal Folder Security

*Personal user folder showing restricted NTFS permissions.*

### Finance User Access

*Finance user successfully accessing the Finance folder.*

### Unauthorized Access Test

*User from another department receiving an Access Denied message.*

### Personal Folder Access

*User successfully accessing their own personal folder while other users are restricted.*
