# VLAN Configuration & Inter-VLAN Routing — Portfolio Project

## Project status
**Design/documentation portfolio project.** This repository contains a network design diagram, VLAN plan, sample configuration templates, IP addressing, and verification/troubleshooting guidance. It was not run or verified in Cisco Packet Tracer. No simulated command outputs or ping results are represented as actual evidence.

## Summary
Virtual LANs (VLANs) logically segment a switched network into separate broadcast domains. This design divides a small-office network into HR, IT, Finance, and Management. A router-on-a-stick approach is documented to enable routing between the VLAN subnets using one router interface with 802.1Q-tagged subinterfaces.

## Intended use
- Separate departments logically without requiring a separate physical switch for each department.
- Organize endpoints and reduce unnecessary broadcast traffic.
- Make a basic network easier to administer.
- Demonstrate networking fundamentals for a learning portfolio.
- Provide a baseline design to adapt in a lab; real networks require security policies and validation.

## VLAN / subnet plan
| Department | VLAN ID | Network | Gateway |
|---|---:|---|---|
| HR | 10 | 192.168.10.0/24 | 192.168.10.1 |
| IT | 20 | 192.168.20.0/24 | 192.168.20.1 |
| Finance | 30 | 192.168.30.0/24 | 192.168.30.1 |
| Management | 40 | 192.168.40.0/24 | 192.168.40.1 |

Each sample endpoint uses `.10` in its subnet. Mask: `255.255.255.0`.

## Topology
See `Diagrams/VLAN_Network_Architecture.png` and `Diagrams/VLAN_Segmentation_Concept.png`.

## Tools / technologies documented
- Cisco IOS-style CLI configuration concepts (configuration templates only)
- VLANs and IEEE 802.1Q trunking
- Router-on-a-stick inter-VLAN routing
- IPv4 addressing and subnetting
- Network topology diagrams
- Verification commands (`show vlan brief`, `show interfaces trunk`, `show ip interface brief`, `ping`) — documented, not executed in this package

## Repository contents
- `Documentation/Project_Overview.md` — what VLANs are, why used, and project explanation
- `Documentation/IP_Addressing_Table.md` — IP plan
- `Documentation/Verification_and_Troubleshooting.md` — checks and common issues
- `Configuration/Sample_Configuration.txt` — illustrative Cisco IOS-style commands
- `Diagrams/` — architecture and segmentation concept diagrams
- `Screenshots/README.md` — explains why genuine simulator screenshots are not included
- `VLAN_Project_Report.pdf` — report

## Important honesty note
The design and configuration are documentation examples. No Packet Tracer project file is supplied and the configuration has not been simulated or tested. If you use this in a CV/interview, describe it as a **VLAN network design and configuration documentation project**, not as a completed hands-on Packet Tracer implementation.
