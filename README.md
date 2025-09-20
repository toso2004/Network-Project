# Network Topologies Design

## Overview
This project demonstrates the design and simulation of **five basic network topologies** (Bus, Star, Ring, Mesh, Extended Star) and a **Hybrid topology** using Cisco Packet Tracer. Each topology is configured with IPv4 and IPv6, VLAN segmentation, and includes at least one server for DHCP/DNS/HTTP services.  


## 1. Network Topologies

A **network topology** defines the layout of devices and connections in a network. It affects data flow, fault tolerance, and scalability.

### Bus Topology
- **Description:** All devices share a single backbone cable.
- **Pros:** Simple, cost-effective for small networks.
- **Cons:** Single point of failure; performance decreases with more devices.
- **Use Case:** Small or legacy networks.

### Star Topology
- **Description:** All devices connect to a central switch or hub.
- **Pros:** Easy to manage; device failures do not affect others.
- **Cons:** Central device failure affects the network; more cabling needed.
- **Use Case:** Modern LANs in offices and schools.

### Ring Topology
- **Description:** Devices form a closed loop, passing data sequentially.
- **Pros:** Predictable performance; simple paths.
- **Cons:** Single device failure can disrupt network; requires redundancy for reliability.
- **Use Case:** Token Ring networks, specialized LANs.

### Mesh Topology
- **Description:** Every device connects to every other device.
- **Pros:** High redundancy; fault-tolerant.
- **Cons:** Expensive and complex; requires many ports and cables.
- **Use Case:** Backbones, critical networks.

### Extended Star Topology
- **Description:** Multiple star topologies connected via central distribution switches.
- **Pros:** Scalable; combines reliability of star topology.
- **Cons:** Central node failure affects multiple segments.
- **Use Case:** Large campus or enterprise LANs.

### Hybrid Topology
- **Description:** Combines two or more topologies for maximum advantage.
- **Example:** Star for PCs, mesh for servers, bus segment for legacy devices.
- **Pros:** Flexible, scalable, fault-tolerant.
- **Use Case:** Enterprise networks, data centers.

---



