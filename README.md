# clinic-network-infrastructure
Enterprise clinic network designed and configured in Cisco Packet Tracer using CCNA and CCNP networking concepts.

## Project Overview

This project is an enterprise style clinic network designed and configured in Cisco Packet Tracer. The network provides segmented access for different departments while incorporating redundancy, routing, switching, and network services.

## Network Topology

The network consists of an Internet connection, an edge router, redundant Layer 3 core switches, access switches, departmental VLANs, and a dedicated server VLAN.

### Network Design

- R1 provides connectivity toward the Internet.
- CORE-SW1 and CORE-SW2 provide the core switching and routing infrastructure.
- Access switches provide connectivity to end-user devices.
- EtherChannel provides redundant and higher-bandwidth connections between the core and access layers.
- VLANs separate users by department.
- HSRP and STP provide network redundancy.
- A dedicated Server VLAN provides DNS, DHCP, and Web services.

## Technologies Used

- VLANs
- 802.1Q Trunking
- Inter-VLAN Routing
- EtherChannel
- HSRP
- STP / PVST
- DHCP
- DNS
- Web Server
- Layer 2 Switching
- Layer 3 Switching
- Static Routing
- Network Redundancy

## Network Segmentation

|    Network   |          Purpose           |
|--------------|----------------------------|
| Admin VLAN   |     Administrative users   |
| Doctors VLAN |      Doctor workstations   |
| Nurses VLAN  |        Nursing staff       |
| Guest VLAN   |        Guest devices       |
| Server VLAN  | DNS, DHCP and Web services |

## Redundancy

The network uses redundant core switching and multiple paths between network devices.

HSRP provides first-hop gateway redundancy, while STP helps prevent Layer 2 loops.

EtherChannel is used to combine multiple physical links into logical connections, providing increased bandwidth and link redundancy.

## Verification

The following Cisco commands were used to verify the network configuration:

```text
show vlan brief
show interfaces trunk
show etherchannel summary
show spanning-tree
show standby
show ip interface brief
show ip route
