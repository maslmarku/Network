RCOMP 2023-2024 Project - Sprint 2 planning
===========================================

### Sprint master: 1201958

(This file is to be created/edited by the sprint master only)

# 1. Sprint's backlog

| Task  | Task description                                                                                                                                                                                              |
| ----- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| T.2.1 | Development of a layer two and layer three Packet Tracer simulation for building one, encompassing the campus backbone. </br>Integration of every member’s Packet Tracer simulation into a single simulation. |
| T.2.2 | Development of a layer two and layer three Packet Tracer simulation for building two, encompassing the campus backbone.                                                                                       |                                                                               |

# 2. Technical decisions and coordination

In this section, all technical decisions taken in the planning meeting should be mentioned. Most importantly, all technical decisions impacting on the subtasks implementation must be settled on this meeting and specified here.

**Packet Tracer Version to be adopted - 8.2.2**

### Devices

Device names should follow the following structure: **DeviceName-BuildingNr.FloorNr.RoomNr**

- **DeviceNameNr**: Designation of the cross connect, ex: IC, HC, CP;
- **BuildingNr**: Number of each building.
- **Floor**: Designation of the floor where the device is located.
- **RoomNr**: Designation of the room.

> Examples: MC-1.0.2, IC-2.0.1

### VLANs

For each building **N** (code 1, 2, 3, 4):

| Designation   | Designation Code | VLAN name        |
| ------------- | ---------------- | ---------------- |
| Ground floor  | F0               | **VLAN-BN-F0**   |
| Floor 1       | F1               | **VLAN-BN-F1**   |
| Wi-fi network | WIFI             | **VLAN-BN-WIFI** |
| Building DMZ  | DMZ              | **VLAN-BN-DMZ**  |
| VoIP          | VOIP             | **VLAN-BN-VOIP** |

For the Backbone: **VLAN-BK**

For the default VLAN: **VLAN-DEFAULT**

## VLAN IDs

VLANIDs range to be used: **428 – 449**.

### Default VLANID

The default VLANID is 428

### Campus backbone:

| VLANID | Description (coverage) |
| ------ | ---------------------- |
| 429    | Building 1             |
| 430    | Building 2             |


### Distribution by buildings:

#### Building 1

| VLANID | Description (coverage)                                             |
| ------ | ------------------------------------------------------------------ |
| 431    | all end-user outlets on the ground floor                           |
| 432    | all end-user outlets on floor one of the building                  |
| 433    | Wi-Fi network (for all access-points’ outlets within the building) |
| 434    | building DMZ (for servers and administration workstations)         |
| 435    | VoIP (for IP-phones)                                               |

#### Building 2

| VLANID | Description (coverage)                                             |
| ------ | ------------------------------------------------------------------ |
| 436    | all end-user outlets on the ground floor                           |
| 437    | all end-user outlets on floor one of the building                  |
| 438    | Wi-Fi network (for all access-points’ outlets within the building) |
| 439    | building DMZ (for servers and administration workstations)         |
| 440    | VoIP (for IP-phones)                                               |


## VTP domains

VTP domain name to be used: **r2324nag5**

### IPv4 Addresses

#### Backbone

![BACKBONE_NETWORK.png](BACKBONE_NETWORK.png)

#### Building 1

![B1_NETWORK.png](B1_NETWORK.png)

#### Building 2

![B2_NETWORK.png](B2_NETWORK.png)


## Internet Address
172.26.112.0/20

ISP Node Address: **5.60.38.129/30**

# 3. Subtasks assignment

- 1200657 - Development of a layer two and three Packet Tracer simulation for building 2
- 1201958 - Development of a layer two and three Packet Tracer simulation for building 1 and integration of every member's simulation into a single simulation.


# 4. Sprint 1 updates

- **Building 1** - 1201958
-

- **Building 2** - 1200657

  - Added missing CP.
