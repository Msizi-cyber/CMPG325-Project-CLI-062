# Switch Configuration Screenshots

This folder contains configuration evidence from the **CORE-SWITCH** (Cisco 2960).

## Screenshots

| # | File Name | What It Shows |
|---|-----------|---------------|
| 1 | `01-trunk-port.png` | Gi0/1 trunking with VLANs 10,20,30,40 allowed |
| 2 | `02-vlan-brief.png` | All 4 VLANs configured with port assignments |
| 3 | `03-mac-address-table.png` | MAC addresses learned on switch ports |
| 4 | `04-ip-interface-brief.png` | VLAN 10 management interface up/up |
| 5 | `05-rsa-keys.png` | Crypto keys for SSH |
| 6 | `06-ssh-enabled.png` | SSH version 2.0 enabled |
| 7 | `07-vlan-configuration.png` | Detailed VLAN configuration |
| 8 | `08-vty-config.png` | Line VTY configuration for SSH access |
| 9 | `09-access-lists.png` | Access list 11 for VTY restriction |

## Key Configuration

**VLANs:**
- VLAN 10 - Management (192.168.33.0/28)
- VLAN 20 - Staff (192.168.33.16/28) - Fa0/1, Fa0/2
- VLAN 30 - Servers (192.168.33.32/28) - Fa0/4
- VLAN 40 - Guest (192.168.33.48/28) - Fa0/3

**Trunk Port:**
- Gi0/1 - Trunk to Edge Router

**Management:**
- VLAN 10 IP: 192.168.33.2/28
- Default Gateway: 192.168.33.1
