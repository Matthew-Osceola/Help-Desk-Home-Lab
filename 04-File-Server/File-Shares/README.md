# File Shares Configuration & Validation

## Overview

Configured Windows Server 2022 SMB file shares to provide centralized access to department and user-specific folders within an Active Directory environment.

Department shares were published for group-based access, while user shares were created to provide dedicated storage for individual domain users.

## Environment

* **Hypervisor:** Oracle VirtualBox
* **Server:** Windows Server 2022
* **Domain Controller:** `OK-DC-01`
* **Client:** Windows 11 Pro
* **Domain:** `mattosceola.com`

## Configuration

### Department Shares

Created SMB shares for department resources.

* Information Technology
* Finance
* Human Resources
* Marketing
* Management

These shares were designed to work with Active Directory security groups for centralized access management.

### User Shares

Created individual SMB shares to provide each user with dedicated network storage.

User shares were configured to support user-specific access through Active Directory.

### Share Configuration

* Created shared folders on the Windows Server file server.
* Enabled SMB sharing for department and user folders.
* Configured share permissions for the intended access level.
* Used Active Directory security groups to support department-based access management.

> **Note:** NTFS permission configuration is documented separately in the **NTFS Permissions** README.

## Validation

Verified that the file shares functioned correctly from the Windows 11 client.

* Confirmed department shares were accessible.
* Confirmed user shares were accessible.
* Tested access using domain user accounts.
* Verified the shares were published from `OK-DC-01`.

### Department Shares

*Server showing the configured department SMB shares.*

![Department Shares](./screenshots/department-shares.png)

### User Shares

*Server showing the configured user SMB shares.*

![User Shares](./screenshots/user-shares.png)

### Shared Folders

*Windows Server displaying the published SMB shares through Shared Folders.*

![Shared Folders](./screenshots/shared-folders.png)

### File Explorer Access

*Windows 11 client accessing shared folders from `OK-DC-01`.*

![File Explorer Access](./screenshots/file-explorer-access.png)
