# Troubleshooting Log

This folder documents issues encountered during network implementation and how they were resolved.

## Issues and Resolutions

| # | Issue | Cause | Solution |
|---|-------|-------|----------|
| 1 | Switch couldn't ping Server | Switch had no default gateway | Added `ip default-gateway 192.168.33.1` |
| 2 | Edge Router couldn't reach ISP | Wrong subnet mask on Gig0/0 (used /30 instead of /29) | Changed to `ip address 192.168.33.253 255.255.255.248` |
| 3 | PCs couldn't reach internet | ISP Router missing route back to LAN | Added `ip route 192.168.33.0 255.255.255.0 192.168.33.253` |
| 4 | Guest could access Staff network | Missing ACL on Guest sub-interface | Added ACL 100 to Gig0/1.40 |
| 5 | Server not appearing in MAC table | Server IP not configured | Set static IP 192.168.33.34 |
| 6 | Cables showed red in Packet Tracer | Wrong cable type used | Replaced with Copper Straight-Through |
| 7 | Configurations lost after restart | Not saved to NVRAM | Used `copy running-config startup-config` |

## Lessons Learned

1. **Always save configurations** - `copy run start` after every change
2. **Check subnet masks** - Mismatched masks cause routing issues
3. **Verify both directions** - Routing needs forward AND return paths
4. **Test incrementally** - Test after each configuration change
5. **Document as you go** - Easier than reconstructing later

## Common Commands Used

**Switch:**
