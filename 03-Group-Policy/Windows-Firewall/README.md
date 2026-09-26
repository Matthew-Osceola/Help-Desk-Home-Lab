# Windows Firewall Policy Configuration & Validation

## Overview

Configured Windows Firewall settings through Group Policy to create a consistent security baseline for domain-joined computers in a simulated Windows Server 2022 help desk environment. This project demonstrates centralized firewall management using Active Directory instead of configuring each workstation individually.

## Environment

* **Hypervisor:** Oracle VirtualBox
* **Server:** Windows Server 2022
* **Domain Controller:** `OK-DC-01`
* **Domain:** `mattosceola.com`
* **Client:** Windows 11 Pro VM
* **Management Tool:** Group Policy Management

## Configuration

### Firewall Group Policy

Configured Windows Firewall settings in the **GPO-Windows-Firewall** Group Policy Object.

**Configured settings:**

- Enabled Windows Defender Firewall for the Domain Profile.
- Managed firewall settings through Group Policy.
- Applied the policy to domain-joined workstations.

### Policy Deployment

Linked the GPO to the appropriate Organizational Unit so domain computers receive the firewall configuration automatically during Group Policy updates.

## Validation

Verified that the firewall policy was successfully applied to the Windows 11 client.

Validation includes:

- Verified the configuration of the **GPO-Windows-Firewall** GPO.
- Verified Windows Defender Firewall was enabled.
- Confirmed the workstation received **GPO-Windows-Firewall**.


### Firewall Group Policy

![Firewall Group Policy](./screenshots/firewall-gpo.png)

### Firewall Enabled

![### Firewall Enabled](./screenshots/firewall-enabled.png)

### Group Policy Results

![### Group Policy Results](./screenshots/gpresult-firewall.png)
