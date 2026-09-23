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

### Scope Configuration

Configured the DHCP scope with an appropriate address range and subnet mask for the virtual network.

![DHCP Scope Configuration](./screenshots/dhcp-scope-configuration.png)

### DHCP Options

Configured DHCP options to provide network configuration to DHCP clients, including the default gateway and DNS server.

![DHCP Options](./screenshots/dhcp-options.png)

---

## DHCP Validation

### Client IP Configuration

Used `ipconfig /all` on the Windows 11 client to verify that the client received its network configuration from DHCP.

![Client IP Configuration](./screenshots/dhcp-ipconfig.png)

### DHCP Lease

Verified the active DHCP lease assigned to the Windows 11 client.

![DHCP Lease](./screenshots/dhcp-lease.png)

### Connectivity Validation

Verified that the Windows 11 client could communicate with the network after receiving its DHCP configuration.

![Connectivity Test](./screenshots/dhcp-connectivity.png)

---

## DHCP Verification

Verified that the DHCP server successfully assigned an IP address and network configuration to the Windows 11 client.

The client received its network configuration from the Windows Server 2022 DHCP service, confirming successful DHCP operation.
