# 🌐 Network Topologies Design & NAT Simulation
📌 Project Overview

This project demonstrates the design and simulation of five basic network topologies and a Hybrid topology using Cisco Packet Tracer.

Features include:

IPv4 & IPv6 configuration

VLAN segmentation

At least one server per LAN (DHCP/DNS/HTTP)

Dynamic NAT with PAT configuration

**🏗️ Network Topologies**

A network topology defines how devices are connected in a network, influencing data flow, fault tolerance, and scalability.

**🚌 Bus Topology**

Description: Devices share a single backbone cable.
Pros: Simple & cost-effective for small networks
Cons: Single point of failure; performance drops as devices increase
Use Case: Small or legacy networks

**⭐ Star Topology**

Description: Devices connect to a central switch/hub
Pros: Easy to manage; device failures don’t affect others
Cons: Central device failure disrupts network; more cabling needed
Use Case: Modern LANs in offices and schools

**🔄 Ring Topology**

Description: Devices form a closed loop, passing data sequentially
Pros: Predictable performance; simple data paths
Cons: Single device failure can disrupt network; redundancy required
Use Case: Token Ring networks, specialized LANs

**🌐 Mesh Topology**

Description: Every device connects to every other device
Pros: High redundancy; fault-tolerant
Cons: Expensive & complex; many ports and cables needed
Use Case: Backbones, critical networks

**✨ Extended Star Topology**

Description: Multiple stars interconnected via central distribution switches
Pros: Scalable & reliable
Cons: Central node failure affects multiple segments
Use Case: Large campuses or enterprise LANs

**🏙️ Smart City Network – Topology Overview**

A Smart City network combines multiple LANs using the most suitable topology for each department:

Department	Topology	Purpose
🛑 Traffic Management	Ring	Continuous & reliable data flow for lights & sensors
👮 Police Station	Star	Centralized management & easy troubleshooting
🚒 Fire Station	Star	Reliable & scalable for emergency coordination
📚 Library	Bus	Simple & cost-effective for low-traffic networks
⚡ Power Grid Monitoring	Mesh	Maximum redundancy for critical infrastructure

All LANs connect to a central distribution layer and router for inter-department communication and internet access.

Goal: Balance cost, reliability, scalability, and performance for a beginner-level Smart City network project.

**🔄 Dynamic NAT with PAT**

Purpose: Allow multiple internal devices to share one public IP while keeping unique port mappings.

Setup:

Router0: NAT with PAT between internal LAN (192.168.10.0/24) and external network (10.0.0.0/8)

Router1: Simulated Internet

Connections: FastEthernet0/0 → LAN, Serial0/1/0 → External router

Configuration:

# Define internal IPs
access-list 1 permit 192.168.10.0 0.0.0.255

# Enable PAT
ip nat inside source list 1 interface Serial0/1/0 overload

# Mark interfaces
interface FastEthernet0/0
 ip nat inside
interface Serial0/1/0
 ip nat outside


Testing:

Assign IPs to PCs

Set Router0 as default gateway

Ping Router1’s interface

✅ Success verified with:

show ip nat translations


Benefits:

Conserves public IP addresses

Multiple users can access the Internet simultaneously

Hides internal IPs for basic security
