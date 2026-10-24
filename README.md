# Multi-Branch Enterprise Network Implementation

## Project Overview
A simulated enterprise network connecting two office branches, Mumbai and Pune, using Cisco Packet Tracer. The project demonstrates IPv4 configuration, router setup, static routing, and end-to-end connectivity testing.

## Network Topology
- 2 routers
- 2 switches
- 4 PCs
- 2 branch LANs connected through a router-to-router WAN link

## Technologies Used
- Cisco Packet Tracer
- IPv4 addressing and subnetting
- LAN and WAN networking
- Static routing
- ICMP ping testing

## IP Addressing

| Device | Interface | IP Address |
|---|---|---|
| Mumbai Router | G0/0 | 192.168.10.1/24 |
| Mumbai Router | G0/1 | 10.0.0.1/30 |
| PC0 | NIC | 192.168.10.10/24 |
| PC1 | NIC | 192.168.10.11/24 |
| Pune Router | G0/0 | 192.168.20.1/24 |
| Pune Router | G0/1 | 10.0.0.2/30 |
| PC2 | NIC | 192.168.20.10/24 |
| PC3 | NIC | 192.168.20.11/24 |

## Static Routing

**Mumbai Router**
```text
ip route 192.168.20.0 255.255.255.0 10.0.0.2
```

**Pune Router**
```text
ip route 192.168.10.0 255.255.255.0 10.0.0.1
```

## Testing Results
- Mumbai to Pune: 4 packets received, 0% packet loss.
- Pune to Mumbai: 4 packets received, 0% packet loss.

## Key Learnings
- Configuring router interfaces and PC network settings.
- Understanding subnet masks and default gateways.
- Implementing static routes between two LANs.
- Testing and troubleshooting connectivity with ping.

## Future Improvements
- DHCP configuration
- VLAN implementation
- OSPF dynamic routing
- Access Control Lists (ACLs)

*This is a simulated learning project built using Cisco Packet Tracer.*

## How to Run
Download the `.pkt` file from this repository and open it using Cisco Packet Tracer.
