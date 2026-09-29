# Windows Firewall Policy Configuration & Validation

## Overview

Configured Windows Defender Firewall settings through Group Policy to establish a consistent security baseline for domain-joined computers in a simulated Windows Server 2022 help desk environment. This project demonstrates centralized firewall management using Active Directory instead of configuring individual workstations manually.

## Environment

- **Hypervisor:** Oracle VirtualBox
- **Server:** Windows Server 2022
- **Domain Controller:** `OK-DC-01`
- **Domain:** `mattosceola.com`
- **Client:** Windows 11 Pro
- **Management Tool:** Group Policy Management

## Configuration

### Firewall Group Policy

Configured Windows Defender Firewall settings in the **GPO-Windows-Firewall** Group Policy Object.

**Configured settings:**

- Enabled Windows Defender Firewall for the Domain Profile.
- Managed firewall settings through Group Policy.
- Applied the policy to domain-joined workstations.

### Firewall Logging

Configured Windows Defender Firewall logging for the Domain Profile to support troubleshooting and security monitoring.

**Configured settings:**

- Log dropped packets: Enabled
- Log successful connections: Enabled
- Log file: `%systemroot%\system32\logfiles\firewall\pfirewall.log`

### Policy Deployment

- Linked **GPO-Windows-Firewall** to the appropriate Organizational Unit.
- Updated Group Policy on the client with `gpupdate /force`.
- Verified that the firewall configuration was applied to the domain-joined workstation.

## Validation

Verified that the firewall policy was successfully applied to the Windows 11 client.

- Confirmed the workstation received **GPO-Windows-Firewall**.
- Verified Windows Defender Firewall was enabled for the Domain Profile.
- Confirmed the Domain network profile was active.
- Verified Domain Profile logging settings were configured.

### Domain Firewall Policy

*Group Policy showing the configured Windows Defender Firewall and Domain Profile logging settings.*

![Firewall Group Policy](./screenshots/firewall-gpo.png)

### Firewall Enabled

*Windows Defender Firewall enabled on the Windows 11 client using the Domain Profile.*

![Firewall Enabled](./screenshots/firewall-enabled.png)

### Group Policy Results

*`gpresult` confirming that **GPO-Windows-Firewall** was successfully applied to the client.*

![Group Policy Results](./screenshots/gp-result.png)
