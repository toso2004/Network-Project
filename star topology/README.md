#1. Description

All devices connect to a central hub or switch. All communtion goes through the central device. It is easy to manage, scalabe and is able to solate faults. The downside of this topology is that the whole network goes down if a hub/switch fails. Examples of this topology includes modern home/office networks with switches or wireless access points.

#2. Devices Used

6 PCs
4 switches 

#3. IP Adrssing Scheme

| Device | IPv4 Address| IPv6 Address     | Subnet Mask     | IPv4 Default Gateway    |IPv6 Default Gateway| IPv4 DNS Server | IPv6 DNS Server  |
|--------|-------------|------------------|-----------------|-------------------------|--------------------|-----------------|------------------|
| PC0    | 192.168.1.2 | 2001:DB8:1::2/64 | 255.255.255.0   |192.168.1.1              |2001:DB8:1::1       | 192.168.1.100   | 2001:DB8:1::100  |          
| PC1    | 192.168.1.3 | 2001:DB8:1::3/64 | 255.255.255.0   |192.168.1.1              |2001:DB8:1::1       | 192.168.1.100   | 2001:DB8:1::100  |
| PC2    | 192.168.1.4 | 2001:DB8:1::4/64 | 255.255.255.0   |192.168.1.1              |2001:DB8:1::1       | 192.168.1.100   | 2001:DB8:1::100  |
| PC3    | 192.168.1.5 | 2001:DB8:1::5/64 | 255.255.255.0   |192.168.1.1              |2001:DB8:1::1       | 192.168.1.100   | 2001:DB8:1::100  |


#4. Configuration

- PC0: IPv4: 192.168.1.2 SM: 255.255.255.0 IPv4 GW: 192.168.1.1 IPv6: 2001:DB8:1::2/64 IPv6 GW: 2001:DB8:1::1 DNS: 192.168.1.100

- PC1: IPv4: 192.168.1.3 SM: 255.255.255.0 IPv4 GW: 192.168.1.1 IPv6: 2001:DB8:1::3/64 IPv6 GW: 2001:DB8:1::1 DNS: 192.168.1.100

- PC2: IPv4: 192.168.1.4 SM: 255.255.255.0 IPv4 GW: 192.168.1.1 IPv6: 2001:DB8:1::4/64 IPv6 GW: 2001:DB8:1::1 DNS: 192.168.1.100

- PC3: IPv4: 192.168.1.5 SM: 255.255.255.0 IPv4 GW: 192.168.1.1 IPv6: 2001:DB8:1::5/64 IPv6 GW: 2001:DB8:1::1 DNS: 192.168.1.100

#5. Testing

Used ping command to check connectivity between PCs.
Example: ping 192.168.1.0 from PC2 → Success.

#6. Screenshots
#7. Observations
