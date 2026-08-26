# Physical Topology Design

## Client: Dikgatlong Adventure Tourism (Kimberley)

## Building Layout & Device Placement

### Floor 1 (Ground Floor) - Public/Staff Area
- **Staff Workstations (2-3 PCs):** Located in the main office area.
- **Guest Wi-Fi Access:** Simulated by a PC in the reception area.
- **Network Cabling:** Uses existing building risers to connect to the communications room.

### Floor 2 (Server/Management Area)
- **Server Room:** Contains the main business server (booking system, email, files).
- **Communications Room:** Contains the edge router and core switch.

### Cable Path (Shared Risers)
All cables run through **existing vertical risers** between floors. No new cabling is installed.
- Floor 2 (Comms Room) → Riser → Floor 1 (Staff Area)
- Floor 2 (Comms Room) → Riser → Floor 1 (Reception)

## Constraint: Shared Risers, No Civil Works
- **Constraint:** The organisation rents part of the building. New cabling or infrastructure changes are not allowed.
- **Solution:** Use existing network risers to connect devices between floors. All cabling uses standard copper cables available in the existing infrastructure.

## Device Inventory

| Device | Model | Quantity | Location | Purpose |
|--------|-------|----------|----------|---------|
| Edge Router | Cisco 1941 | 1 | Comms Room (Floor 2) | Connect to ISP, handle routing |
| Core Switch | Cisco 2960 | 1 | Comms Room (Floor 2) | Connect all internal devices |
| ISP Router | Cisco 1941 | 1 | Simulated (ISP side) | Simulate internet service provider |
| Staff PC 1 | Generic PC | 1 | Floor 1 - Office | Staff workstation |
| Staff PC 2 | Generic PC | 1 | Floor 1 - Office | Staff workstation |
| Admin PC | Generic PC | 1 | Off-site (simulated) | Remote administrator access |
| Server | Generic PC | 1 | Floor 2 - Server Room | Business server |
| Guest PC | Generic PC | 1 | Floor 1 - Reception | Simulate guest Wi-Fi access |

## Physical Diagram

