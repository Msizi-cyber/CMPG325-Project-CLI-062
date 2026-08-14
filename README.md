# CMPG 325 - Computer Networks Project

## Project Information
- **Student Name: MAZIBUKO, MH
- **Student Number: 45066132
- **Project ID: CMPG325-2026-062
- **Client ID: CLI-062

## Client Overview
**Organisation:** Dikgatlong Adventure Tourism (Kimberley)  
**Industry:** Tourism  

This project involves designing and implementing a computer network for Dikgatlong Adventure Tourism, an adventure tourism company based in Kimberley. The network must provide reliable connectivity, support business operations, and meet specific technical requirements.


## Key Requirements

### Technical Challenge: Default Routing (Edge/ISP Path Design)
- Configure a default route on the edge router to provide internet connectivity.
- Implement a "gateway of last resort" for all internal traffic.
- Test and verify successful connectivity to the ISP.

### Change Request CR9: Secure Remote Management
- One off-site administrator requires secure remote access to network devices.
- Implementation: SSH (Secure Shell) with username/password authentication.
- Access Control List (ACL) to restrict access to the administrator's IP only.

### Design Constraint
- The organisation rents part of the building with shared risers.
- No civil works or new cabling infrastructure allowed.

---

## IP Addressing Plan
Assigned Block: 192.168.33.0/24

| Subnet | Network | Subnet Mask | VLAN | Purpose |
|--------|---------|-------------|------|---------|
| Management | 192.168.33.0 | /28 (255.255.255.240) | 10 | Network device management |
| Staff | 192.168.33.16 | /28 (255.255.255.240) | 20 | Staff workstations |
| Servers | 192.168.33.32 | /28 (255.255.255.240) | 30 | Business servers |
| Guest | 192.168.33.48 | /28 (255.255.255.240) | 40 | Guest Wi-Fi |
| Inter-router Link | 192.168.33.252 | /30 (255.255.255.252) | N/A | ISP connection |

---

## Repository Structure
