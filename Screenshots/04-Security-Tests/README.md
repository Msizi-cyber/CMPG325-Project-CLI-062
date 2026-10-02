# Security Tests

This folder contains evidence that security features are working, specifically **Guest isolation** and **SSH remote management**.

## Screenshots

| # | File Name | What It Shows |
|---|-----------|---------------|
| 1 | `01-guest-pc-internet.png` | Guest can access internet |
| 2 | `02-guest-pc-isolation-staff.png` | Guest CANNOT reach staff |
| 3 | `03-guest-pc-isolation-server.png` | Guest CANNOT reach server |
| 4 | `04-acl-verification.png` | ACL 100 configured on router |
| 5 | `05-ssh-verification.png` | SSH enabled on router |

## Security Tests Summary

| Test | Source | Destination | Result |
|------|--------|-------------|--------|
| 1 | GUEST-PC | 192.168.33.49 (Gateway) | ✅ Pass |
| 2 | GUEST-PC | 8.8.8.8 (Internet) | ✅ Pass |
| 3 | GUEST-PC | 192.168.33.18 (STAFF-PC1) | ❌ Blocked |
| 4 | GUEST-PC | 192.168.33.34 (SERVER-PC) | ❌ Blocked |
| 5 | GUEST-PC | 192.168.33.2 (Switch) | ❌ Blocked |

## ACL Configuration

**Extended ACL 100 (Applied to Guest VLAN):**
