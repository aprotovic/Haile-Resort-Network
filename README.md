# 🏨 Haile Hotels & Resorts — Enterprise Network Architecture

[![Cisco Packet Tracer](https://img.shields.io/badge/Simulator-Cisco%20Packet%20Tracer%208.2.2-049fd9.svg)](https://www.netacad.com/)
[![OSPF](https://img.shields.io/badge/Routing-OSPF%20v2-blue.svg)]()
[![VLANs](https://img.shields.io/badge/Segmentation-802.1Q%20VLANs-orange.svg)]()
[![Security](https://img.shields.io/badge/Security-ACLs%20%7C%20SSH-red.svg)]()

A comprehensive enterprise network infrastructure simulation and architecture design engineered for **Haile Hotels and Resorts**. Supports **500+ network nodes** across multiple physical floors, departments, and guest wireless environments.

---

## 📸 Network Topology & Simulation Screenshots

<div align="center">
  <img src="docs/screenshots/network_topology_diagram.png" alt="3-Tier Hierarchical Network Topology" width="90%" />
  <p><i>Figure 1: Full 3-Tier Hierarchical Network Topology (Core, Distribution, and Access layers) in Cisco Packet Tracer.</i></p>
</div>

<div align="center">
  <img src="docs/screenshots/packet_tracer_simulation.png" alt="Packet Tracer Simulation & OSPF Routing Table" width="90%" />
  <p><i>Figure 2: Active simulation verifying inter-VLAN routing, OSPF neighbor states, and NAT/PAT translation.</i></p>
</div>

> **Tip:** Add your Packet Tracer screenshots to `docs/screenshots/network_topology_diagram.png` and `docs/screenshots/packet_tracer_simulation.png`.

---

## 🏛️ Network Hierarchy

Built using Cisco's industry-standard **3-Tier Hierarchical Model**:

```
           +-----------------------+
           |       CORE LAYER      |  <- Dual redundant Layer-3 switches (High-speed backplane)
           +-----------+-----------+
                       |
        +--------------+--------------+
        |                             |
+-------+-------+             +-------+-------+
|  DISTRIBUTION |             |  DISTRIBUTION |  <- Inter-VLAN routing, ACL security policies & QoS
+-------+-------+             +-------+-------+
        |                             |
+-------+-------+             +-------+-------+
|  ACCESS LAYER |             |  ACCESS LAYER |  <- Port security, end-user PC connectivity, APs
+---------------+             +---------------+
```

---

## 🌐 Departmental VLAN Architecture

| VLAN ID | Subnet Description | Department | Security Policy |
| :---: | :--- | :--- | :--- |
| **10** | `192.168.10.0/24` | Sales & Marketing | Standard employee access |
| **20** | `192.168.20.0/24` | HR & Logistics | Restricted database access |
| **30** | `192.168.30.0/24` | Restaurant & POS | Isolated POS payment terminals |
| **40** | `192.168.40.0/24` | Finance & Accounting | Strict ACL isolation; no guest access |
| **50** | `192.168.50.0/24` | Administration & PR | Executive access |
| **60** | `192.168.60.0/24` | ICT Department | Full network administration & monitoring |
| **70** | `192.168.70.0/24` | Server Room / DMZ | Static IPs, SSH-only, hardened firewalls |

---

## 🔒 Security Implementations

- **SSHv2 Only:** Telnet disabled across all managed switches and routers.
- **Access Control Lists (ACLs):** Extended ACLs preventing guest wireless and commercial subnets from reaching the Server Room or Finance VLAN.
- **NAT / PAT:** Dynamic overload translation hiding internal RFC 1918 private subnets behind ISP gateway IPs.
- **Redundancy:** Dual core switch links preventing single points of failure.

---

## 📂 Included Artifacts

- `project.pkt` — Native Cisco Packet Tracer 8.2.2 simulation file.
- `Report.pdf` — Complete engineering design report, subnet allocation tables, and routing configurations.

---

## 📄 Author
Goitom Shumey ([@aprotovic](https://github.com/aprotovic)) • Debre Berhan University
