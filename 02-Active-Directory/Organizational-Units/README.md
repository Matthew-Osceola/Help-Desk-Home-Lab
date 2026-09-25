# Organizational Units Configuration & Validation

## Overview

Created and organized Organizational Units (OUs) in Active Directory to separate users, groups, computers, and departmental resources. This structure provides a clean administrative hierarchy and prepares the environment for Group Policy deployment.

## Environment

- **Hypervisor:** Oracle VirtualBox
- **Server:** Windows Server 2022
- **Domain Controller:** `OK-DC-01`
- **Domain:** `mattosceola.com`
- **Client:** Windows 11 VM


## Objectives

- Create a structured OU hierarchy.
- Separate administrative objects from lab-created objects.
- Organize users and security groups by department.
- Prepare the domain for targeted Group Policy Objects (GPOs).

## Configuration

### 1. Created the Primary Organizational Units

Created top-level OUs to organize Active Directory objects.

![Primary Organizational Units](./screenshots/primary-ous.png)

### 2. Created Departmental Organizational Units

Created department-specific OUs to separate resources by business function.

Departments include:

- Finance
- Human Resources
- Information Technology
- Management
- Marketing

![Departmental Organizational Units](./screenshots/department-ous.png)

### 3. Created User Organizational Units

Created a dedicated Users OU and separate departmental user OUs to isolate lab-created accounts from built-in Active Directory objects.

![User Organizational Units](./screenshots/user-ous.png)

### 4. Created Security Group Organizational Units

Created a dedicated Groups OU to organize department security groups separately from default Active Directory groups.

![Groups Organizational Units](./screenshots/groups-ous.png)

### 5. Moved Lab Objects into the New Structure

Moved users and security groups into their appropriate Organizational Units while preserving Active Directory functionality.

![New Structure](./screenshots/new-structure.png)

## Validation

Verified that:

- All Organizational Units were created successfully.
- Department users appear in their assigned OUs.
- Security groups are organized under the Groups OU.
- Built-in Active Directory objects remain separate from lab-created objects.
- The OU structure is ready for Group Policy deployment.

![Primary Organizational Units](./screenshots/fnal-structure.png)
