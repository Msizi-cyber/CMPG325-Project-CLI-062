# Router Configuration Screenshots

This folder contains configuration evidence from the **EDGE-ROUTER** and **ISP-ROUTER** (Cisco 1941).

## Screenshots

| # | File Name | What It Shows |
|---|-----------|---------------|
| 1 | `01-edge-router-ip-brief.png` | All interfaces up/up |
| 2 | `02-edge-router-routes.png` | Routing table with default route |
| 3 | `03-edge-router-subinterfaces.png` | Router-on-a-Stick sub-interfaces |
| 4 | `04-edge-router-internet.png` | Ping 8.8.8.8 successful |
| 5 | `05-isp-router-config.png` | ISP Router configuration |
| 6 | `06-access-lists.png` | ACL 100 for Guest isolation |
| 7 | `07-rsa-keys.png` | Crypto keys for SSH |
| 8 | `08-ssh.png` | SSH enabled |
| 9 | `09-vty-config.png` | VTY configuration |

## Key Configuration

**EDGE-ROUTER Sub-interfaces:**
| Interface | VLAN | IP Address |
|-----------|------|------------|
| Gi0/1.10 | 10 | 192.168.33.1/28 |
| Gi0/1.20 | 20 | 192.168.33.17/28 |
| Gi0/1.30 | 30 | 192.168.33.33/28 |
| Gi0/1.40 | 40 | 192.168.33.49/28 |

**WAN:**
- Gi0/0: 192.168.33.253/29 (to ISP)

**Default Route:**
- `ip route 0.0.0.0 0.0.0.0 192.168.33.254`

**ISP-ROUTER:**
- Gi0/0: 192.168.33.254/29
- Loopback0: 8.8.8.8/32
- Route to LAN: `ip route 192.168.33.0 255.255.255.0 192.168.33.253`
