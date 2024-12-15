RCOMP 2023-2024 Project - Sprint 2 - Member 1200657 folder

===========================================
(This folder is to be created/edited by the team member 1200657 only)

# Building 1

## 1. Virtual LAN's

| VLANID | Description (coverage)                                             |
| ------ | ------------------------------------------------------------------ |
| 436    | all end-user outlets on the ground floor                           |
| 437    | all end-user outlets on floor one of the building                  |
| 438    | Wi-Fi network (for all access-points’ outlets within the building) |
| 439    | building DMZ (for servers and administration workstations)         |
| 440    | VoIP (for IP-phones)                                               |




### VTP

VTP Domain Name -> **r2324nag5**

## 2. IPv4 Networks

| VLANID    | Description                                                       | Maximum Nodes |
|-----------|-------------------------------------------------------------------|---------------|
| 436       | End user outlets on the ground floor                              | 90            |
| 437       | End user outlets on floor one                                     | 120           |
| 438       | Wi-Fi network                                                     | 220           |
| 439       | Local servers and administration workstations and machines (DMZ)  | 50            |
| 440       | VoIP (IP-phones)                                                  | 110           |
| **TOTAL** |                                                                   | 590           |



| Building 2 Network     |                           |
|------------------------|---------------------------|
| Network Address        | 172.26.129.0/20           |
| Broadcast Address      | 172.26.144.255            |
| Network Mask           | 255.255.240.0 (*20 bits*) |
| First Node Address     | 172.26.129.1              |
| Last Node Address      | 172.26.144.254            |

Backbone's Network IPv4 Building 2 Address -> **172.26.129.0**

> *Used by the building’s IC (router) connection to MC.*

ISP Node Address -> **5.60.38.134/30**


##  Some CLI Configuration Notes

### Switch

Switch#vlan database

| Switch(vlan)#              |
|----------------------------|
| vlan 436 name VLAN-B2-WIFI |
| vlan 437 name VLAN-B2-F1   |
| vlan 438 name VLAN-B2-F0   |
| vlan 439 name VLAN-B2-DMZ  |
| vlan 440 name VLAN-B2-VOIP |


Switch(config)#do show vlan

* *Remaining VLANs, from other buildings, added to the local VLAN database.*



### VTP Domain

Switch#show vtp status

Switch#config t

Switch(config)#vtp domain r2324nag5

- _Change the VTP mode of every switch to client, except the server mode switch (MC)._

Switch(config)#vtp mode client

### Router

**Sub-Interfaces Configuration:**

![B2_SUBINF.png](B2_SUBINF.png)


**DHCP Configuration:**

![B2_DHCP.png](B2_DHCP.png)

## 4. Test Scenarios

### Scenario 0

IC Connection between MC and ISP Router.

### Scenario 1

Connection between end-devices from different floors and VLAN's.

### Scenario 2

Connection between end-devices and ISP Router.