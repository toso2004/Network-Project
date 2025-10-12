# Blatjang Smart City Network Topology

This project showcases a **Smart City network topology** designed to connect and manage different sectors of a city efficiently. The network is divided into **five LANs**, each representing a different department of the city. Each LAN uses a specific network topology based on its operational requirements.

## Overview

The smart city network connects the following LANs:

1. **Traffic Management LAN** – Ring Topology
2. **Police Station LAN** – Star Topology
3. **Fire Station LAN** – Star Topology
4. **Library LAN** – Bus Topology
5. **Power Grid Monitoring LAN** – Mesh Topology

A central distribution layer connects all these LANs to ensure communication between departments and provide internet access through a router (not shown in this diagram yet).

![Smart City Topology](./hybrid%20topology.png)

---

## 1. Traffic Management LAN – Ring Topology

The **ring topology** is used for the Traffic Management LAN. This is because traffic lights, sensors, and monitoring devices need a **continuous and reliable data flow**. In a ring topology, each device is connected to two others, forming a closed loop. If one link fails, data can still flow in the opposite direction, ensuring smooth operation of traffic systems.

**Why Ring Topology?**

* Offers **high reliability** through looped paths.
* Ensures **real-time communication**, which is crucial for traffic monitoring.
* Suitable for systems where **data needs to circulate continuously**.

---

## 2. Police Station LAN – Star Topology

The **star topology** connects all police department devices to a central switch. This is ideal for environments where **many devices communicate through a single point**, such as workstations and IP phones.

**Why Star Topology?**

* **Easy to manage** and set up.
* **Failure of one device** doesn’t affect the entire network.
* Centralized structure makes **maintenance and troubleshooting simpler**.

---

## 3. Fire Station LAN – Star Topology

Similar to the police station, the Fire Station LAN also uses a **star topology**. It allows for **efficient coordination** between fire personnel, control rooms, and emergency devices.

**Why Star Topology?**

* Simple to **expand** as the station grows.
* Each device has a **dedicated connection**, reducing collisions.
* Central switch improves **network performance and reliability**.

---

## 4. Library LAN – Bus Topology

The **bus topology** is used for the Library LAN. This topology is cost-effective and works well for smaller networks where devices share the same communication line.

**Why Bus Topology?**

* **Economical** and requires less cabling.
* Good for **simple networks** with minimal traffic.
* Easy to **add or remove devices** without major changes.

---

## 5. Power Grid Monitoring LAN – Mesh Topology

The **mesh topology** is implemented for the Power Grid Monitoring LAN. Since the power grid is a **critical infrastructure**, mesh provides **redundancy and high reliability**. Each device is interconnected, ensuring there’s no single point of failure.

**Why Mesh Topology?**

* Offers **maximum fault tolerance**.
* Allows **multiple communication paths**, which improves reliability.
* Suitable for critical systems where **continuous monitoring** is essential.

---

## Summary Table

| Department            | Topology | Key Benefit                          |
| --------------------- | -------- | ------------------------------------ |
| Traffic Management    | Ring     | Reliability and continuous data flow |
| Police Station        | Star     | Easy management and troubleshooting  |
| Fire Station          | Star     | Reliable and expandable structure    |
| Library               | Bus      | Cost-effective for small networks    |
| Power Grid Monitoring | Mesh     | High fault tolerance and redundancy  |

---

## Conclusion

This smart city network topology combines **multiple topologies** to suit the needs of different departments. By doing this, the network achieves a **balance between cost, reliability, and scalability**, making it a solid foundation for a beginner-level smart city project.

