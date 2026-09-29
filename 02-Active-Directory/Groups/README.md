# Active Directory Groups Configuration & Validation

## Overview

Created and configured Active Directory security groups to organize users and manage access to departmental resources using the AGDLP model.

## Environment

* **Hypervisor:** Oracle VirtualBox
* **Server:** Windows Server 2022
* **Domain Controller:** `OK-DC-01`
* **Domain:** `mattosceola.com`
* **Client:** Windows 11 Pro
* **Directory Service:** Active Directory Domain Services (AD DS)

## Configuration

Created security groups based on department and access requirements.

### Global Groups

* `GG-Finance`
* `GG-Human-Resources`
* `GG-Information-Technology`
* `GG-Marketing`
* `GG-Management`

### Domain Local Groups

* `DL-Finance-Read`
* `DL-Finance-Modify`
* `DL-Human-Resources-Read`
* `DL-Human-Resources-Modify`
* `DL-Information-Technology-Read`
* `DL-Information-Technology-Modify`
* `DL-Marketing-Read`
* `DL-Marketing-Modify`
* `DL-Management-Read`
* `DL-Management-Modify`

## Access Management

Implemented the **AGDLP (Accounts → Global Groups → Domain Local Groups → Permissions)** model to organize access and simplify permission management.

Users are assigned to appropriate Global Groups based on their department. Global Groups are then added to Domain Local Groups that correspond to the required resource permissions.

This structure separates user membership from resource permissions, making access easier to manage as users and departments change.

## Validation

Verified group creation, membership, scope, and type through **Active Directory Users and Computers (ADUC)**.

Confirmed that Global Groups could be assigned to the appropriate Domain Local Groups for resource access.

### Active Directory Groups

*Active Directory Users and Computers displaying the configured Global and Domain Local security groups.*

![Active Directory Groups](screenshots/ad-groups.png)

### Global and Domain Local Group Membership

*Global Group membership showing users assigned according to department.*

![Global Group Membership](screenshots/gg-group-membership.png)

*Domain Local Group membership showing a Global Group assigned for resource access.*

![Domain Local Membership](screenshots/dl-group-membership.png)

### Group Scope and Type

*Group properties showing the configured security group scope and group type.*

![Group Scope and Type](screenshots/group-scope.png)
