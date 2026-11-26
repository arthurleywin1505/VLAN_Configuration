# Verification & Troubleshooting Guide (planned checks)

**These commands are suggested checks; they were not run for this project package.**

## Checks
| Goal | Command | What to inspect |
|---|---|---|
| VLANs/ports | `show vlan brief` | VLANs exist; access ports assigned |
| Trunk state | `show interfaces trunk` | Trunk operational; VLANs allowed |
| Router interfaces | `show ip interface brief` | Parent interface/subinterfaces up |
| Basic reachability | `ping <IP>` | Replies from gateway/other test host |

## Common faults
- Host cannot reach gateway: check host IP, mask, gateway, switch port VLAN, and router interface.
- Trunk does not carry VLAN: check trunk mode, allowed VLAN list, and link.
- Inter-VLAN routing fails: check VLAN tags, router subinterfaces, addressing, and interface state.
- VLAN/port mismatch: verify port assignment and endpoint connection.

## Results table — fill after actual testing
| Test | Expected | Actual | Status |
|---|---|---|---|
| HR PC to HR gateway | Reachable | Not tested | Pending |
| IT PC to IT gateway | Reachable | Not tested | Pending |
| HR PC to IT PC | Routed if policy permits | Not tested | Pending |
| Finance PC to Management PC | Routed if policy permits | Not tested | Pending |
