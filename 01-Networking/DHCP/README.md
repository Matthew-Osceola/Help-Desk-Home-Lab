# DHCP Configuration

## Overview

Configured the Windows Server 2022 DHCP Server role to provide automatic IPv4 network configuration to Windows client machines in the home lab environment.

## Configuration

| Setting | Configuration |
|---|---|
| DHCP Server | Windows Server 2022 |
| Client | Windows 11 VM |
| Address Assignment | DHCP |
| Scope |  |
| Subnet Mask |  |
| Default Gateway |  |
| DNS Server |  |
| Lease Duration |  |

## Verification

The Windows 11 client was configured to obtain its IPv4 configuration automatically.

Verification was performed using:

ipconfig /all

The DHCP lease was also verified in the DHCP management console under **Address Leases**.

Additional connectivity testing:

ping 

ping

nslookup


## Troubleshooting
