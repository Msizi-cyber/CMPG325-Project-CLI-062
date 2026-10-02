# Documentation

This folder contains all project documentation for the Dikgatlong Adventure Tourism network.

## Files

| File | Contents |
|------|----------|
| `ip-addressing-scheme.md` | Complete IP address plan |
| `vlan-configuration.md` | VLAN design details |
| `network-design.md` | Overall network design rationale |

## IP Addressing Scheme

### WAN Link
| Device | Interface | IP Address |
|--------|-----------|------------|
| EDGE-ROUTER | Gig0/0 | 192.168.33.253/29 |
| ISP-ROUTER | Gig0/0 | 192.168.33.254/29 |

### VLANs
| VLAN | Subnet | Gateway |
|------|--------|---------|
| 10 | 192.168.33.0/28 | 192.168.33.1 |
| 20 | 192.168.33.16/28 | 192.168.33.17 |
| 30 | 192.168.33.32/28 | 192.168.33.33 |
| 40 | 192.168.33.48/28 | 192.168.33.49 |

## Design Rationale

### VLAN Segmentation
- Separates departments for security
- Reduces broadcast domains
- Improves network performance

### Router-on-a-Stick
- Cost-effective routing solution
- Single physical interface handles all VLANs
- Easy to manage and scale

### Guest Isolation
- Protects internal resources
- Meets security best practices
- Complies with client requirements

## Client Requirements Met

| Requirement | Status |
|-------------|--------|
| Dikgatlong Adventure Tourism | ✅ |
| 192.168.33.0/24 block | ✅ |
| Default Routing | ✅ |
| Shared risers (no civil works) | ✅ |
| SSH remote management (CR9) | ✅ |
