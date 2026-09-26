# Mapped Network Drives Configuration & Validation

## Overview

Configured Group Policy to automatically map department and personal network drives for domain users, providing consistent access to shared resources without requiring manual drive mapping.

## Environment

* **Hypervisor:** Oracle VirtualBox
* **Server:** Windows Server 2022
* **Domain Controller:** `OK-DC-01`
* **Domain:** `mattosceola.com`
* **Client:** Windows 11 Pro VM
* **Management Tool:** Group Policy Management

## Configuration

### Department Drive Mapping

Configured a Group Policy Preference to map the department shared folder.

- **Policy Location:** User Configuration → Preferences → Windows Settings → Drive Maps
- **Action:** Create
- **Drive Letter:** `S:`
- **Path:** `\\OK-DC-01\Department Shares\Information Technology`
- **Reconnect:** Enabled

### Personal Home Drive Mapping

Configured a second Group Policy Preference to automatically map each user's personal folder.

- **Policy Location:** User Configuration → Preferences → Windows Settings → Drive Maps
- **Action:** Create
- **Drive Letter:** `P:`
- **Path:** `\\OK-DC-01\User Shares\IT Users\%USERNAME%`
- **Reconnect:** Enabled

### Group Policy Deployment

- Linked the mapped drive policy to the appropriate Organizational Unit.
- Updated Group Policy on the client using `gpupdate /force`.
- Verified that the correct users received the assigned drives after signing in.

## Validation

Confirmed that:

- Department users automatically received the `S:` mapped drive.
- Users received their personal `P:` drive based on `%USERNAME%`.
- Drive mappings appeared without manual configuration.
- The mapped drives remained available after signing out and back in.
- Access respected NTFS and share permissions configured on the file server.

### Drive Maps Policy Configuration

![Drive Maps Policy Configuration](./screenshots/dmap-policy-config.png)

### Department Drive (S:)

![Department Drive](./screenshots/department-drive.png)

### Personal Drive (P:)

![Drive Maps Policy Configuration](./screenshots/personal-drive.png)

### File Explorer with Mapped Drives

![Drive Maps Policy Configuration](./screenshots/mapped-drives.png)

### Group Policy Applied (`gpresult`)

![Drive Maps Policy Configuration](./screenshots/gpo-applied.png)
