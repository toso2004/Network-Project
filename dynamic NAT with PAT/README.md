# Dynamic NAT with PAT - Cisco Packet Tracer Project

## 📌 Project Overview

This project demonstrates **Dynamic Network Address Translation (NAT) with Port Address Translation (PAT)** using Cisco Packet Tracer. The setup involves two routers, a switch, and multiple end devices. NAT with PAT allows multiple internal devices to share a single public IP address while maintaining unique port mappings to communicate with external networks.

---

## 🧠 Objectives

* Configure internal and external interfaces on the router
* Set up NAT with PAT to allow multiple internal hosts to access external networks simultaneously
* Verify connectivity between internal hosts and external networks

---

## 🖼️ Topology Description

The network consists of:

* **Router0** – Acts as the border router performing NAT with PAT
* **Router1** – Simulates the external/public network
* **Switch0** – Connects internal hosts (PC0, PC1) to Router0
* **PC0 & PC1** – Internal hosts using private IP addresses

The **Serial interface** connects Router0 and Router1 (external side), while the **FastEthernet0/0 interface** connects Router0 to the internal LAN.

---

## 🧱 IP Addressing Scheme

| Device / Interface | IP Address    | Subnet Mask   | Role            |
| ------------------ | ------------- | ------------- | --------------- |
| Router0 - Fa0/0    | 192.168.10.1  | 255.255.255.0 | Inside Network  |
| Router0 - S0/1/0   | 10.0.0.1      | 255.0.0.0     | Outside Network |
| Router1 - S0/1/0   | 10.0.0.2      | 255.0.0.0     | External Router |
| PC0                | 192.168.10.10 | 255.255.255.0 | Inside Host     |
| PC1                | 192.168.10.20 | 255.255.255.0 | Inside Host     |

---

## ⚙️ Configuration Steps

### 1. Enable Interfaces & Assign IPs (Router0)

```bash
Router> enable
Router# configure terminal
Router(config)# interface FastEthernet0/0
Router(config-if)# ip address 192.168.10.1 255.255.255.0
Router(config-if)# no shutdown
Router(config-if)# exit

Router(config)# interface Serial0/1/0
Router(config-if)# ip address 10.0.0.1 255.0.0.0
Router(config-if)# no shutdown
Router(config-if)# exit
```

### 2. Configure Inside and Outside NAT

```bash
Router(config)# access-list 1 permit 192.168.10.0 0.0.0.255
Router(config)# ip nat inside source list 1 interface Serial0/1/0 overload

Router(config)# interface FastEthernet0/0
Router(config-if)# ip nat inside
Router(config-if)# exit

Router(config)# interface Serial0/1/0
Router(config-if)# ip nat outside
Router(config-if)# exit
```

### 3. Configure Router1 (External)

```bash
Router> enable
Router# configure terminal
Router(config)# interface Serial0/1/0
Router(config-if)# ip address 10.0.0.2 255.0.0.0
Router(config-if)# no shutdown
Router(config-if)# exit
```

---

## 🧪 Testing

1. Assign IP addresses to PC0 and PC1.
2. Ping Router1’s Serial interface (10.0.0.2) from PC0 and PC1.
3. Both should succeed using a single translated public IP (10.0.0.1) through PAT.
4. Use the `show ip nat translations` command on Router0 to view active translations.

Example output:

```bash
Router# show ip nat translations
Pro  Inside global      Inside local       Outside local      Outside global
icmp  10.0.0.1:13      192.168.10.10:13  10.0.0.2:13        10.0.0.2:13
```

---

## 📝 Key Takeaways

* **Dynamic NAT with PAT** enables multiple hosts to share a single public IP through unique port numbers.
* Access Control Lists (ACLs) define which internal traffic is eligible for translation.
* Inside and outside interfaces must be clearly defined for NAT to work properly.
* PAT is commonly used by ISPs and enterprises to conserve public IP addresses.

---


