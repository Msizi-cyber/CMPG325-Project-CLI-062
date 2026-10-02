# Screenshots

This folder contains all testing, configuration, and verification screenshots for the Dikgatlong Adventure Tourism network (Milestone 2).

## Folder Structure

| Folder | Contents |
|--------|----------|
| `01-Switch-Configuration/` | VLAN, trunk, MAC table, SSH configs |
| `02-Router-Configuration/` | ROAS, routing table, ACL configs |
| `03-Connectivity-Tests/` | Ping test evidence |
| `04-Security-Tests/` | Guest isolation and ACL verification |
| `05-Device-Configurations/` | IP configurations, MAC table |

## Purpose

These screenshots provide **evidence** that:
- All devices are correctly configured
- The network is fully operational
- Security features (Guest isolation) are working
- All client requirements have been met

## Test Summary

| Test | Result |
|------|--------|
| Staff → Internet | ✅ Pass |
| Server → Internet | ✅ Pass |
| Guest → Internet | ✅ Pass |
| Guest → Staff | ✅ Blocked |
| Guest → Server | ✅ Blocked |

## How to Use

Each folder contains a `README.md` explaining the screenshots in detail.
