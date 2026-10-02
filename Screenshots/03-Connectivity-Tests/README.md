# Connectivity Tests

This folder contains ping test evidence proving end-to-end connectivity across the network.

## Screenshots

| # | File Name | Source | Destination |
|---|-----------|--------|-------------|
| 1 | `01-staff-pc1-pings.png` | STAFF-PC1 | Gateway, PC2, Server, Internet |
| 2 | `02-staff-pc2-pings.png` | STAFF-PC2 | Gateway, PC1, Server, Internet |
| 3 | `03-server-pc-pings.png` | SERVER-PC | Gateway, Switch, Staff, Internet |
| 4 | `04-edge-router-pings.png` | EDGE-ROUTER | ISP, Internet |
| 5 | `05-isp-router-pings.png` | ISP-ROUTER | Edge Router, Staff PC |
| 6 | `06-full-topology.png` | Workspace | Complete network view |

## Test Results Summary

| Test | Source | Destination | Result |
|------|--------|-------------|--------|
| 1 | STAFF-PC1 | 192.168.33.17 (Gateway) | ✅ Pass |
| 2 | STAFF-PC1 | 192.168.33.19 (STAFF-PC2) | ✅ Pass |
| 3 | STAFF-PC1 | 192.168.33.34 (Server) | ✅ Pass |
| 4 | STAFF-PC1 | 8.8.8.8 (Internet) | ✅ Pass |
| 5 | SERVER-PC | 192.168.33.33 (Gateway) | ✅ Pass |
| 6 | SERVER-PC | 8.8.8.8 (Internet) | ✅ Pass |
| 7 | EDGE-ROUTER | 192.168.33.254 (ISP) | ✅ Pass |
| 8 | EDGE-ROUTER | 8.8.8.8 (Internet) | ✅ Pass |
| 9 | ISP-ROUTER | 192.168.33.253 (Edge) | ✅ Pass |
| 10 | ISP-ROUTER | 192.168.33.18 (STAFF-PC1) | ✅ Pass |

## Verification

All internal and external connectivity is working:
- ✅ Staff can reach each other, server, and internet
- ✅ Server can reach internet
- ✅ Routers can reach each other
- ✅ Internet simulation (8.8.8.8) is reachable
