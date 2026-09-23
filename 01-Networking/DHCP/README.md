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

Tested DHCP functionality by renewing the client's lease:

ipconfig /release
ipconfig /renew

Confirmed that the Windows 11 client received the expected IPv4 address, subnet mask, gateway, and DNS server from the DHCP server.

## Evidence

### DHCP Scope


### DHCP Address Lease


### Client IP Configuration
