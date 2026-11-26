# Project Overview — VLAN Configuration & Inter-VLAN Routing

## What is this project?
This is a small-office network design that uses Virtual LANs (VLANs) to divide one switched network into separate logical departmental networks. Four departments are represented: HR, IT, Finance, and Management.

## Why is it used?
Without segmentation, devices on a shared LAN may all belong to the same broadcast domain. VLANs allow a network administrator to group devices logically even when they connect to the same physical switch.

Typical benefits:
- **Organization:** separate departments and device groups.
- **Broadcast-domain separation:** broadcast traffic is confined to its VLAN.
- **Administration:** easier to map switch ports to teams or functions.
- **Policy foundation:** inter-VLAN traffic can be controlled at a router or Layer-3 switch. VLANs alone are not a complete security control.

## How this design works
1. The managed switch defines VLAN 10, 20, 30, and 40.
2. Endpoint-facing switch ports are configured as access ports and assigned to a VLAN.
3. The switch uplink to the router is configured as a trunk so it can carry multiple VLANs.
4. Router subinterfaces use 802.1Q VLAN tags and act as default gateways for the four IP subnets.
5. A router can route between these subnets; in a production design, ACLs/firewall policies should determine which departments may communicate.

## Department plan
| Department | VLAN | Subnet | Gateway |
| HR | 10 | 192.168.10.0/24 | 192.168.10.1 |
| IT | 20 | 192.168.20.0/24 | 192.168.20.1 |
| Finance | 30 | 192.168.30.0/24 | 192.168.30.1 |
| Management | 40 | 192.168.40.0/24 | 192.168.40.1 |

## Tools / concepts
- Network topology diagrams (visual design)
- Cisco IOS-style CLI syntax (configuration examples)
- VLAN segmentation
- IEEE 802.1Q trunking
- Router-on-a-stick routing
- IPv4 addressing and subnet masks
- Common verification commands are included as a checklist but have not been run.

## Portfolio status
This package is a design and documentation project, not a validated simulation. It includes no `.pkt` file or authentic command/ping screenshots.
