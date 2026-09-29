# Password & Account Lockout Configuration & Validation

## Overview

Configured domain password and account lockout policies using Group Policy in a Windows Server 2022 Active Directory environment.

The policies strengthen account security by enforcing password requirements and temporarily locking accounts after repeated failed sign-in attempts.

## Environment

- **Hypervisor:** Oracle VirtualBox
- **Server:** Windows Server 2022
- **Domain Controller:** `OK-DC-01`
- **Domain:** `mattosceola.com`
- **Client:** Windows 11 Pro
- **Management Tool:** Group Policy Management

## Configuration

### Password Policy

Configured the following domain password requirements:

- Minimum password length
- Password complexity requirements
- Password history
- Maximum password age
- Minimum password age

### Account Lockout Policy

Configured account lockout settings to help protect against repeated failed authentication attempts:

- Account lockout threshold
- Account lockout duration
- Reset account lockout counter after

## Validation

Validated the configured policies through Group Policy Management and client-side policy results.

Confirmed that the Windows 11 client received the domain password and account lockout policies after Group Policy was applied.

### Password Policy

*Group Policy showing the configured domain password requirements.*

![Password Policy](./screenshots/password-policy.png)

### Account Lockout Policy

*Group Policy showing the configured account lockout settings.*

![Account Lockout Policy](./screenshots/account-lockout-policy.png)

### Group Policy Results

*`gpresult` confirming that the password and account lockout policies were successfully applied to the client.*

![Group Policy Results](./screenshots/gp-results.png)
