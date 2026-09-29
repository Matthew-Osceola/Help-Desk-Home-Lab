# Help Desk Homelab

## Objective

Configured a Windows Server 2022 virtual machine and Windows 11 Pro virtual machine to create a simulated help desk environment and practice common IT support, system administration, and troubleshooting tasks.

## Technologies Used

* Oracle VirtualBox
* Windows Server 2022
* Windows 11 Pro
* Active Directory
* DNS
* DHCP
* Group Policy
* Jira
* Action1

## Tasks Performed

### Infrastructure & Networking

* Configured Windows Server 2022 as an Active Directory Domain Controller.
* Configured DNS and DHCP services.
* Configured static IP addressing and network connectivity.
* Joined Windows 11 Pro to the Active Directory domain.

### Active Directory & Group Policy

* Created and managed Active Directory users, security groups, and organizational units.
* Configured Group Policy for password policies, account lockout, screen inactivity, and other security settings.

### File Services & Permissions

* Configured departmental and user file shares.
* Implemented NTFS permissions using security groups and the AGDLP model.
* Configured network drive mappings for users and departments.

### Help Desk & Troubleshooting

* Created and resolved simulated Tier 1 help desk tickets using Jira.
* Troubleshot DNS, domain connectivity, Group Policy, and NTFS permission issues.
* Documented troubleshooting steps, resolutions, and validation results.

### Patch Management

* Used Action1 to deploy Windows updates and security patches.
* Validated patch deployment on the Windows 11 client.

## Project Documentation

Detailed configuration, troubleshooting, validation, and screenshots are organized by project:

| Project                                   | Topic                                                       |
| ----------------------------------------- | ----------------------------------------------------------- |
| [Networking](01-Networking)               | Static IP, NAT Network, DNS, and DHCP.                      |
| [Active Directory](02-Active-Directory)   | Domain Controller, users, groups, and organizational units. |
| [Group Policy](03-Group-Policy)           | Security policies and workstation configuration.            |
| [File Server](04-File-Server)             | File shares, NTFS permissions, and network drives.          |
| [Patch Management](05-Patch-Management)   | Windows update and patch deployment.                        |
| [Help Desk Tickets](06-Help-Desk-Tickets) | Simulated Tier 1 support tickets.                           |
| [Troubleshooting](07-Troubleshooting)     | Documented troubleshooting scenarios and resolutions.       |
