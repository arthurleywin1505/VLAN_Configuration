# IP Addressing Table

| Endpoint | VLAN | IPv4 | Subnet Mask | Gateway |
|---|---:|---|---|---|
| PC-HR | 10 | 192.168.10.10 | 255.255.255.0 | 192.168.10.1 |
| PC-IT | 20 | 192.168.20.10 | 255.255.255.0 | 192.168.20.1 |
| PC-Finance | 30 | 192.168.30.10 | 255.255.255.0 | 192.168.30.1 |
| PC-Management | 40 | 192.168.40.10 | 255.255.255.0 | 192.168.40.1 |

## Gateway interface plan
| Router subinterface | VLAN tag | Gateway IP |
|---|---:|---|
| G0/0.10 | 10 | 192.168.10.1/24 |
| G0/0.20 | 20 | 192.168.20.1/24 |
| G0/0.30 | 30 | 192.168.30.1/24 |
| G0/0.40 | 40 | 192.168.40.1/24 |

Interface names depend on the device model. This table is a design template.
