# Device Configurations

This folder contains IP configuration screenshots for all end devices and key network tables.

## Screenshots

| # | File Name | Device | Purpose |
|---|-----------|--------|---------|
| 1 | `01-server-pc-ipconfig.png` | SERVER-PC | Server IP settings |
| 2 | `02-staff-pc1-ipconfig.png` | STAFF-PC1 | Staff workstation 1 |
| 3 | `03-staff-pc2-ipconfig.png` | STAFF-PC2 | Staff workstation 2 |
| 4 | `04-guest-pc-ipconfig.png` | GUEST-PC | Guest workstation |
| 5 | `05-mac-address-table.png` | CORE-SWITCH | MAC table |
| 6 | `06-isp-router-routing.png` | ISP-ROUTER | Routing table |

## IP Configuration Details

### SERVER-PC (VLAN 30)
| Setting | Value |
|---------|-------|
| IP Address | 192.168.33.34 |
| Subnet Mask | 255.255.255.240 |
| Default Gateway | 192.168.33.33 |
| DNS Server | 8.8.8.8 |

### STAFF-PC1 (VLAN 20)
| Setting | Value |
|---------|-------|
| IP Address | 192.168.33.18 |
| Subnet Mask | 255.255.255.240 |
| Default Gateway | 192.168.33.17 |
| DNS Server | 8.8.8.8 |

### STAFF-PC2 (VLAN 20)
| Setting | Value |
|---------|-------|
| IP Address | 192.168.33.19 |
| Subnet Mask | 255.255.255.240 |
| Default Gateway | 192.168.33.17 |
| DNS Server | 8.8.8.8 |

### GUEST-PC (VLAN 40)
| Setting | Value |
|---------|-------|
| IP Address | 192.168.33.50 |
| Subnet Mask | 255.255.255.240 |
| Default Gateway | 192.168.33.49 |
| DNS Server | 8.8.8.8 |

## MAC Address Table

Shows which devices are communicating on which ports:
- Fa0/1 → STAFF-PC1 (VLAN 20)
- Fa0/2 → STAFF-PC2 (VLAN 20)
- Fa0/3 → GUEST-PC (VLAN 40)
- Fa0/4 → SERVER-PC (VLAN 30)
- Gig0/1 → Edge Router (Trunk)
