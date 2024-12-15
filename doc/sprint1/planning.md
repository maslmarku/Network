RCOMP 2022-2023 Project - Sprint 1 planning
===========================================
### Sprint master: 1201958 ###
(This file is to be created/edited by the sprint master only)
# 1. Sprint's backlog #
| Task   | description                                                |
|--------|------------------------------------------------------------|
| T.1.1  | Development of a structured cabling project for building 1, <br/>encompassing the backbone. |
| T.1.2  | Development of a structured cabling project for building 2. |

Only 2 buildings for 2 members were considered.

# 2. Technical decisions and coordination #

## 2.1 Decisions #
| General specifications                              | Decision                                                                    | Reason                                                                      |
|-----------------------------------------------------|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| Preferred backbone outdoor cables (campus/building) | Monomode optical fibre - 100Gbase-LR4                                       | *Ethernet – above 10 Gbps experience fewer losses and longer cable lengths* |
| Preferred indoor backbone cables (IC/HC/CP)         | Multimode optical fibre - 100Gbase-SR4                                      | *Ethernet – above 10 Gbps lower cable lengths in relation to 100Gbase-LR4*  |
| Fibre connectors                                    | Local Connector (LC)                                                        | No specific reason                                                          |
| Copper cable type                                   | CAT7 (10GbaseT)                                                             | *S/STP - signals up to 600 MHz (required for 10 Gbps)*                      |
| Copper cable wiring standard                        | T-568A                                                                      | No specific reason                                                          |
| Patch cord/cable connector and socket               | RJ45                                                                        | No specific reason                                                          |
| Telecommunication enclosures                        | 19'' rack  (10-16U)                                                         |                                                                             |
| Consolidation Points                                | 19'' rack  (4-6U)                                                           |                                                                             |
| Redundant links                                     | Add backbone redundant connections and use different pathways when possible |                                                                             |
| Preferred network topology                          | Star                                                                        | *Cable concentrator devices - more reliability*                             |

| Optical fibre requirements | Ethernet network                                   |
|----------------------------|----------------------------------------------------|
| Up to 10Gb Ethernet        | 10Gbase-LR                                         |
| More than 10Gb Ethernet    | 100Gbase-LR4 (monomode) / 100Gbase-SR4 (multimode) |


## 2.2 Coordination #
  * Base Excel done to work together with the same base file
  * Creation PowerPoint to work schemes for buildings
  * Definition of the same symbols for everyone uses in the schemes.

# 3. Subtasks assignment #
  * 1201958 - Structured cable design for building 1 and the backbone
  * 1200657 - Structured cable design for building 2