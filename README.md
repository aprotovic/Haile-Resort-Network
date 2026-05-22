# Haile Hotels and Resorts Network Design

Enterprise network design and simulation for Haile Hotels and Resorts using Cisco Packet Tracer.

## Project Overview

This project simulates a scalable and secure hotel network infrastructure supporting 500+ users across multiple departments and floors.

The network was designed using a three-tier hierarchical architecture:

- Core Layer
- Distribution Layer
- Access Layer

## Features

- VLAN Segmentation
- Inter-VLAN Routing
- OSPF Dynamic Routing
- DHCP Configuration
- NAT/PAT Internet Access
- SSH Secure Remote Access
- ACL-Based Access Control
- Wireless Network Integration
- Redundant Core Connections

## Technologies Used

- Cisco Packet Tracer 8.2.2
- Layer 3 Switching
- OSPF
- DHCP
- NAT
- VLANs
- ACLs
- SSH

## VLAN Structure

| VLAN | Department |
|------|-------------|
| 10 | Sales & Marketing |
| 20 | HR & Logistics |
| 30 | Restaurant |
| 40 | Finance & Accounts |
| 50 | Admin & Public Relations |
| 60 | ICT Department |
| 70 | Server Room |

## Security Implementations

- SSH-only remote management
- ACL restriction for administrative access
- VLAN isolation
- Static IPs for servers

## Testing Performed

- Inter-VLAN communication
- DHCP verification
- NAT internet access
- Wireless connectivity
- OSPF routing verification
- SSH access testing

## Files Included

- `project.pkt` → Cisco Packet Tracer simulation
- `Report.pdf` → Full project documentation

## Author
Goitom Shumey
