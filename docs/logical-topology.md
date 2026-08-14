# Logical Topology Design

## Client: Dikgatlong Adventure Tourism (Kimberley)

## Overview
The logical topology defines how data flows through the network, including VLAN segmentation, IP addressing, routing, and security.

---

## VLAN Structure

| VLAN ID | VLAN Name | Subnet | Host Range | Purpose |
|---------|-----------|--------|------------|---------|
| 10 | Management | 192.168.33.0/28 | 192.168.33.1 - 14 | Network device management |
| 20 | Staff | 192.168.33.16/28 | 192.168.33.17 - 30 | Staff workstations |
| 30 | Servers | 192.168.33.32/28 | 192.168.33.33 - 46 | Business servers |
| 40 | Guest | 192.168.33.48/28 | 192.168.33.49 - 62 | Guest Wi-Fi access |

---

## Inter-VLAN Routing
- **Method:** Router-on-a-Stick (ROAS) using the edge router.
- **Sub-interfaces:** Each VLAN has a sub-interface on the edge router's Gig0/0 interface.
- **Benefits:** Centralizes routing, simplifies management, and improves security.

### Router-on-a-Stick Configuration

| Interface | VLAN | IP Address | Description |
|-----------|------|------------|-------------|
| Gig0/0.10 | VLAN 10 | 192.168.33.1/28 | Management Gateway |
| Gig0/0.20 | VLAN 20 | 192.168.33.17/28 | Staff Gateway |
| Gig0/0.30 | VLAN 30 | 192.168.33.33/28 | Server Gateway |
| Gig0/0.40 | VLAN 40 | 192.168.33.49/28 | Guest Gateway |

---

## Default Routing (Edge/ISP Path Design)

### Default Route Configuration
The edge router has a default route (gateway of last resort) pointing to the ISP router.

```cisco
ip route 0.0.0.0 0.0.0.0 192.168.33.254
