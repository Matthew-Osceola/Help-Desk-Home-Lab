# Domain Controller Configuration & Validation

## Overview

Configured and validated a Windows Server 2022 Domain Controller using Active Directory Domain Services (AD DS). Established the `mattosceola.com` Active Directory domain and verified Active Directory, DNS integration, and Domain Controller health.

## Environment

* **Hypervisor:** Oracle VirtualBox (NAT Network)
* **Server:** Windows Server 2022
* **Domain Controller:** `OK-DC-01`
* **Domain:** `mattosceola.com`
* **Server IP:** `10.0.2.10`
* **Directory Service:** Active Directory Domain Services (AD DS)

## Configuration

### Active Directory Domain Services

Verified that the **Active Directory Domain Services (AD DS)** role is installed on the Windows Server.

![AD DS Installed](./screenshots/ad-ds-installed.png)

### Active Directory Users and Computers

Verified access to the `mattosceola.com` domain through **Active Directory Users and Computers (ADUC)**.

![Active Directory Users and Computers](./screenshots/ad-users-and-computers.png)

### Active Directory Domains and Trusts

Verified the `mattosceola.com` domain and Active Directory forest configuration using **Active Directory Domains and Trusts**.

![Active Directory Domains and Trusts](./screenshots/ad-domains-and-trusts.png)

## Validation

### Domain Controller Health

Ran `dcdiag /test:connectivity` and `dcdiag /test:dns` to validate Domain Controller functionality and identify potential issues.

```cmd
dcdiag /test:connectivity
```

```cmd
dcdiag /test:dns
```

Validated successful Domain Controller connectivity and services.

![DCDIAG Connectivity](./screenshots/dcdiag-connectivity.png)

![DCDIAG Connectivity](./screenshots/dcdiag-dns.png)

### FSMO Role Validation

Used `netdom` to verify the Flexible Single Master Operations (FSMO) roles held by the Domain Controller.

```cmd
netdom query fsmo
```

![FSMO Roles](./screenshots/fsmo-roles.png)
