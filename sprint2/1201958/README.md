RCOMP 2023-2024 Project - Sprint 2 - Member 1201958 folder

===========================================
(This folder is to be created/edited by the team member 1201958 only)

# Building 1

## 1. Virtual LAN's

| VLANID | VLAN Name    | Description (coverage)                                             |
| ------ |--------------|--------------------------------------------------------------------|
| 431    | VLAN-B1-F0   | all end-user outlets on the ground floor                           |
| 432    | VLAN-B1-F1   | all end-user outlets on floor one of the building                  |
| 433    | VLAN-B1-WIFI | Wi-Fi network (for all access-points’ outlets within the building) |
| 434    | VLAN-B1-DMZ  | building DMZ (for servers and administration workstations)         |
| 435    | VLAN-B1-VOIP | VoIP (for IP-phones)                                               |



### VTP

VTP Domain Name -> **r2324nag5**

## 2. IPv4 Networks

| VLANID    | Description                                                       | Maximum Nodes |
|-----------|-------------------------------------------------------------------|---------------|
| 431       | End user outlets on the ground floor                              | 50            |
| 432       | End user outlets on floor one                                     | 50            |
| 433       | Wi-Fi network                                                     | 80            |
| 434       | Local servers and administration workstations and machines (DMZ)  | 100           |
| 435       | VoIP (IP-phones)                                                  | 67            |
| **TOTAL** |                                                                   | 347           |


172.26.128.0/20

| Building 1 Network     |                           |
|------------------------|---------------------------|
| Network Address        | 172.26.128.0/20           |
| Broadcast Address      | 172.26.143.255            |
| Network Mask           | 255.255.240.0 (*20 bits*) |
| First Node Address     | 172.26.128.1              |
| Last Node Address      | 172.26.143.254            |

Backbone's Network IPv4 Building 1 Address -> **172.26.128.0**

> *Used by the building’s IC (router) connection to MC.*

ISP Node Address -> **5.60.38.134/30**


##  Some CLI Configuration Notes

### Switch

Switch#vlan database

| Switch(vlan)#              |
|----------------------------|
| vlan 433 name VLAN-B1-WIFI |
| vlan 432 name VLAN-B1-F1   |
| vlan 431 name VLAN-B1-F0   |
| vlan 434 name VLAN-B1-DMZ  |
| vlan 435 name VLAN-B1-VOIP |


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
