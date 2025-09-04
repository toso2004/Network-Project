#1. Description

A bus topology consists of a connection in which all devices share a single central cable (the "bus"). The data within topology travels in both directions along the bus,to which each device checks if the data is for it. The bus topology is cheap, easy to set up and requires minimal cabling. The downside of this topology is that it has a single point of failure, if the main cable breaks the entire network fails and it tends to be slow when many devices send data. Examples include; early ethernet networks( using a coaxial cable).

#2. Devices Used

4 PCs were used
4 Switches were used imitate the backbone found in the bus topology. The switches allowed for the connection of the PCs together.
A coaxial cable was used. It is usually the cable that is used in to connect devices in the bus topology.

#3. IP Adressing Scheme

| Device | IPv4 Address| IPv6 Address     | Subnet Mask     | IPv4 Default Gateway    |IPv6 Default Gateway| IPv4 DNS Server | IPv6 DNS Server  |
|--------|-------------|------------------|-----------------|-------------------------|--------------------|-----------------|----------------- |
| PC0    | 192.168.1.2 | 2001:DB8:1::2/64 | 255.255.255.0   |192.168.1.1              |2001:DB8:1::1       | 192.168.1.100   | 2001:DB8:1::100  |
| -------|-------------|------------------|-----------------|-------------------------|--------------------|-----------------|------------------|
| PC1    | 192.168.1.3 | 2001:DB8:1::3/64 | 255.255.255.0   |192.168.1.1              |2001:DB8:1::1       | 192.168.1.100   | 2001:DB8:1::100  |
| -------|-------------|------------------|-----------------|-------------------------|--------------------|-----------------|------------------|
| PC2    | 192.168.1.4 | 2001:DB8:1::4/64 | 255.255.255.0   |192.168.1.1              |2001:DB8:1::1       | 192.168.1.100   | 2001:DB8:1::100  |
| -------|-------------|------------------|-----------------|-------------------------|--------------------|-----------------|------------------|
| PC3    | 192.168.1.5 | 2001:DB8:1::5/64 | 255.255.255.0   |192.168.1.1              |2001:DB8:1::1       | 192.168.1.100   | 2001:DB8:1::100  |


#4. Configuration

**PC0** > **IPv4**: 192.168.1.2 **IPv6**: 2001:DB8:1::2/64 **SM**: 255.255.255.0 **IPv4 GW**: 192.168.1.1 **IPv6 GW**: 2001:DB8:1::1 **IPv4 DNS**:192.168.1.100
**PC1** > **IPv4**: 192.168.1.3 **IPv6**: 2001:DB8:1::2/64 **SM**: 255.255.255.0 **IPv4 GW**: 192.168.1.1 **IPv6 GW**: 2001:DB8:1::1
**PC2** > **IPv4**: 192.168.1.4 **IPv6**: 2001:DB8:1::2/64 **SM**: 255.255.255.0 **IPv4 GW**: 192.168.1.1 **IPv6 GW**: 2001:DB8:1::1
**PC3** > **IPv4**: 192.168.1.5 **IPv6**: 2001:DB8:1::2/64 **SM**: 255.255.255.0 **IPv4 GW**: 192.168.1.1 **IPv6 GW**: 2001:DB8:1::1

#5. Testing
#6. Screenshots
#7. Observations
