# DHCP Configuration & Validation

## Overview

Configured and validated DHCP on Windows Server 2022 within an Active Directory environment.

### Environment

* **Server:** Windows Server 2022
* **Domain Controller:** `OK-DC-01`
* **Domain:** `mattosceola.com`
* **DHCP Server:** `10.0.2.10`
* **Client:** Windows 11 VM
* **Virtualization:** Oracle VirtualBox

---

## DHCP Configuration

### DHCP Server Role

Installed and configured the DHCP Server role on the Windows Server 2022 Domain Controller.

![DHCP Server Role](./screenshots/dhcp-server-role.png)

### DHCP Scope

Created an IPv4 DHCP scope for the `10.0.2.0/24` network.

![DHCP Scope](./screenshots/dhcp-scope.png)

### DHCP Scope Configuration

Configured the DHCP scope with an appropriate address range and subnet mask for the virtual network.

![DHCP Scope Configuration](./screenshots/dhcp-scope-configuration.png)

---

## DHCP Validation

### DHCP Lease

Verified the active DHCP lease assigned to the Windows 11 client.

![Active DHCP Lease](./screenshots/dhcp-lease.png)

### Client IP Configuration

Used `ipconfig /all` on the Windows 11 client to verify that the client received its network configuration from DHCP.

![Client IP Configuration](./screenshots/dhcp-ipconfig.png)
