---
title: "Persistent Objects"
description: "Information about persistent objects saved to the save game."
authors: [ 2, 6310 ]
---

Persistent objects are objects that, when collected or destroyed, have that fact saved to the user's saved game.

Such objects include coins placed in the world, certain types of prop (including, but not limited to, cola machines and cola crates), and wasp cameras.

The game has a hardcoded list of sectors, each of which corresponds to a particular region of a level (such as `l1z1.p3d`) or the level itself.

Each sector can save up to 128 objects and what object is saved where depends entirely on the order of chunks in the region's P3D file or the order of actors in the level's initialisation script.

# Base Game Sectors
The tables below outline each sector in the base game and what objects occupy each slot.

Empty slots are omitted for brevity, none of the sectors in the base game come close to occupying all 128 slots. Object indices can go up to 127 per sector.

## Sector 0 (l1r1.p3d)
| Object Index | Object Type                                         | Object Name                          |
|--------------|-----------------------------------------------------|--------------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_lemonade_Shape` -> `l1_lemonade` |
| 1            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                               |
| 2            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                              |
| 3            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`                              |
| 4            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                              |
| 5            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin5`                              |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin6`                              |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`                              |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin7`                              |

## Sector 1 (l1r2.p3d)
| Object Index | Object Type                                 | Object Name                     |
|--------------|---------------------------------------------|---------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]] | `l1_crate_Shape` -> `l1_crate3` |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]] | `l1_crate_Shape` -> `l1_crate4` |

## Sector 2 (l1r3.p3d)
| Object Index | Object Type                                         | Object Name                          |
|--------------|-----------------------------------------------------|--------------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_crate_Shape` -> `(no name)`      |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_vending_Shape` -> `l1_vending_1` |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_gaspump_Shape` -> `l2_gaspump_2` |
| 3            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_gaspump_Shape` -> `l2_gaspump_1` |
| 4            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R3C1Coin1`                          |
| 5            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R3C1Coin0`                          |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R3C1Coin2`                          |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R3C1Coin3`                          |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R3C2Coin1`                          |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R3C1Coin5`                          |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R3C2Coin0`                          |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R3C2Coin2`                          |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R3C2Coin3`                          |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                              |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                               |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                              |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin5`                              |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`                              |
| 18           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`                              |
| 19           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin7`                              |
| 20           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin6`                              |
| 21           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R3C1Coin4`                          |

## Sector 3 (l1r4a.p3d)
| Object Index | Object Type                                         | Object Name  |
|--------------|-----------------------------------------------------|--------------|
| 0            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin7`      |
| 1            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R4AC1Coin0` |
| 2            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`      |
| 3            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`      |
| 4            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R4AC1Coin1` |
| 5            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin5`      |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`      |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`      |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin6`      |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`       |

## Sector 4 (l1r4b.p3d)
| Object Index | Object Type                                         | Object Name                     |
|--------------|-----------------------------------------------------|---------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_crate_Shape` -> `(no name)` |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_crate_Shape` -> `(no name)` |
| 2            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin1`           |
| 3            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin3`           |
| 4            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin4`           |
| 5            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin5`           |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin0`           |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin6`           |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin7`           |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin8`           |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin9`           |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin10`          |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin11`          |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin12`          |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin13`          |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin14`          |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin15`          |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin16`          |
| 18           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin18`          |
| 19           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin28`          |
| 20           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin17`          |
| 21           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin21`          |
| 22           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin19`          |
| 23           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin20`          |
| 24           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin24`          |
| 25           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin22`          |
| 26           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin23`          |
| 27           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin27`          |
| 28           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin29`          |
| 29           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin25`          |
| 30           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin26`          |
| 31           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin2`           |

## Sector 5 (l1r6.p3d)
| Object Index | Object Type                                         | Object Name                                       |
|--------------|-----------------------------------------------------|---------------------------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_fence_Shape` -> `l1_fence_`                   |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_fence_Shape` -> `l1_fence_2`                  |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_fence_Shape` -> `l1_fence_3`                  |
| 3            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_haybale_Shape` -> `l1_haybale_1`              |
| 4            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_haybale_Shape` -> `l1_haybale_2`              |
| 5            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_haybale_Shape` -> `l1_haybale_3`              |
| 6            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_haybale_Shape` -> `l1_haybale_4`              |
| 7            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_haybale_Shape` -> `l1_haybale_5`              |
| 8            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1r6_tomaccostand_Shape` -> `l1r6_tomaccostand_` |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R6C1Coin0`                                       |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R6C1Coin1`                                       |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R6C1Coin2`                                       |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R6C1Coin3`                                       |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                                            |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                                           |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`                                           |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                                           |

## Sector 6 (l1r7.p3d)
| Object Index | Object Type                                         | Object Name                          |
|--------------|-----------------------------------------------------|--------------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_vending_Shape` -> `l1_vending_1` |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_vending_Shape` -> `l1_vending_3` |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_gaspump_Shape` -> `l2_gaspump_2` |
| 3            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_gaspump_Shape` -> `l2_gaspump_1` |
| 4            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_crate_Shape` -> `l1_crate_2`     |
| 5            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_crate_Shape` -> `l1_crate_3`     |
| 6            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_crate_Shape` -> `l1_crate_4`     |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin0`                          |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin1`                          |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin2`                          |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin3`                          |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin4`                          |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin5`                          |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin6`                          |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin7`                          |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin8`                          |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin9`                          |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin10`                         |
| 18           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin11`                         |
| 19           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin12`                         |
| 20           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin6`                              |
| 21           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin15`                         |
| 22           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin8`                              |
| 23           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin13`                         |
| 24           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin14`                         |
| 25           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin18`                         |
| 26           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin16`                         |
| 27           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin17`                         |
| 28           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin9`                              |
| 29           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin19`                         |
| 30           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                              |
| 31           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                               |
| 32           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                              |
| 33           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin5`                              |
| 34           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`                              |
| 35           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`                              |
| 36           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin7`                              |

## Sector 7 (l1z1.p3d)
| Object Index | Object Type                                         | Object Name                      |
|--------------|-----------------------------------------------------|----------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_crate_Shape` -> `l1_crate_2` |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_crate_Shape` -> `l1_crate_3` |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_crate_Shape` -> `l1_crate_5` |
| 3            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_crate_Shape` -> `l1_crate_6` |
| 4            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_crate_Shape` -> `l1_crate_7` |
| 5            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_crate_Shape` -> `l1_crate_9` |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C4Coin1`                      |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C4Coin2`                      |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C4Coin0`                      |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C4Coin4`                      |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C4Coin5`                      |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C4Coin3`                      |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C4Coin7`                      |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                          |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C4Coin6`                      |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C3Coin1`                      |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C3Coin2`                      |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C3Coin0`                      |
| 18           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C3Coin6`                      |
| 19           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C3Coin3`                      |
| 20           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C3Coin5`                      |
| 21           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                          |
| 22           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C3Coin4`                      |
| 23           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                           |
| 24           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin5`                          |
| 25           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C3Coin7`                      |
| 26           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`                          |
| 27           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin8`                          |
| 28           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`                          |
| 29           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin7`                          |
| 30           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin6`                          |

## Sector 8 (l1z2.p3d)
| Object Index | Object Type                                         | Object Name                          |
|--------------|-----------------------------------------------------|--------------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_crate_Shape` -> `l1_crate2`      |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_gaspump_Shape` -> `l2_gaspump_2` |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_gaspump_Shape` -> `l2_gaspump_1` |
| 3            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_vending_Shape` -> `l1_vending_1` |
| 4            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_vending_Shape` -> `l1_vending_2` |
| 5            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_vending_Shape` -> `l1_vending_3` |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C3Coin2`                          |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C3Coin0`                          |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C3Coin5`                          |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C3Coin3`                          |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C3Coin1`                          |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C4Coin0`                          |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C3Coin6`                          |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C3Coin4`                          |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C4Coin3`                          |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C4Coin1`                          |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C3Coin7`                          |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                              |
| 18           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                               |
| 19           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C4Coin2`                          |
| 20           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin5`                              |
| 21           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`                              |
| 22           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                              |
| 23           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`                              |
| 24           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin8`                              |
| 25           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin6`                              |
| 26           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin10`                             |
| 27           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin9`                              |
| 28           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin7`                              |
| 29           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin13`                             |
| 30           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin11`                             |
| 31           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin16`                             |
| 32           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin14`                             |
| 33           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin12`                             |
| 34           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin17`                             |
| 35           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin15`                             |

## Sector 9 (l1z3.p3d)
| Object Index | Object Type                                         | Object Name                          |
|--------------|-----------------------------------------------------|--------------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_crate_Shape` -> `l1_crate2`      |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_crate_Shape` -> `l1_crate3`      |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_crate_Shape` -> `l1_crate4`      |
| 3            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_crate_Shape` -> `l1_crate5`      |
| 4            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_vending_Shape` -> `l1_vending_1` |
| 5            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C1Coin0`                          |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C1Coin1`                          |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C1Coin2`                          |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C1Coin3`                          |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C1Coin5`                          |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C2Coin0`                          |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C2Coin1`                          |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C2Coin2`                          |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C3Coin0`                          |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C3Coin1`                          |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C3Coin2`                          |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C3Coin3`                          |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C3Coin4`                          |
| 18           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C3Coin5`                          |
| 19           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C3Coin6`                          |
| 20           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C3Coin7`                          |
| 21           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C3Coin8`                          |
| 22           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C3Coin9`                          |
| 23           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                               |
| 24           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                              |
| 25           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                              |
| 26           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`                              |
| 27           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`                              |
| 28           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C1Coin4`                          |

## Sector 10 (l1z4.p3d)
This sector has no objects.

## Sector 11 (l1z6.p3d)
| Object Index | Object Type                                         | Object Name                                  |
|--------------|-----------------------------------------------------|----------------------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_tunnelfence_Shape` -> `l1_tunnelfence_1` |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_vending_Shape` -> `l1_vending_1`         |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_vending_Shape` -> `l1_vending_2`         |
| 3            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1z6_powerbox_Shape` -> `powerbox1`         |
| 4            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1z6_powerbox_Shape` -> `powerbox2`         |
| 5            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1z6_powerbox_Shape` -> `powerbox3`         |
| 6            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1z6_powerbox_Shape` -> `powerbox4`         |
| 7            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1z6_powerbox_Shape` -> `powerbox5`         |
| 8            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1z6_powerbox_Shape` -> `powerbox6`         |
| 9            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1z6_powerbox_Shape` -> `powerbox7`         |
| 10           | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1z6_powerbox_Shape` -> `powerbox8`         |
| 11           | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1z6_powerbox_Shape` -> `powerbox9`         |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z6C1Coin1`                                  |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z6C1Coin2`                                  |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z6C1Coin0`                                  |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z6C1Coin4`                                  |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z6C1Coin5`                                  |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z6C1Coin3`                                  |

## Sector 12 (l1z7.p3d)
| Object Index | Object Type                                         | Object Name                      |
|--------------|-----------------------------------------------------|----------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l1_crate_Shape` -> `l1_crate_2` |
| 1            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                          |
| 2            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                           |
| 3            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                          |
| 4            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin15`                         |
| 5            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin13`                         |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin14`                         |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin18`                         |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin16`                         |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin17`                         |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin21`                         |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin19`                         |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin20`                         |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin24`                         |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin22`                         |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin23`                         |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin27`                         |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin25`                         |
| 18           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin26`                         |

## Sector 13 (l2r1.p3d)
| Object Index | Object Type                                         | Object Name                          |
|--------------|-----------------------------------------------------|--------------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l2_vending_Shape` -> `l2_vending_1` |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l2_crate_Shape` -> `l2_crate_8`     |
| 2            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                              |
| 3            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                               |
| 4            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                              |
| 5            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`                              |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`                              |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin5`                              |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin6`                              |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin7`                              |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin8`                              |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin11`                             |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin9`                              |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin10`                             |

## Sector 14 (l2r2.p3d)
| Object Index | Object Type                                         | Object Name                          |
|--------------|-----------------------------------------------------|--------------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l2_vending_Shape` -> `l2_vending_1` |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l2_crate_Shape` -> `l2_crate_1`     |
| 2            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                              |
| 3            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                               |
| 4            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin7`                              |
| 5            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                              |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`                              |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin6`                              |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`                              |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin5`                              |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin10`                             |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin8`                              |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin18`                             |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin13`                             |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin11`                             |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin12`                             |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin15`                             |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin14`                             |
| 18           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin17`                             |
| 19           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin9`                              |
| 20           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin16`                             |

## Sector 15 (l2r3.p3d)
This sector has no objects.

## Sector 16 (l2r4.p3d)
| Object Index | Object Type                                         | Object Name                          |
|--------------|-----------------------------------------------------|--------------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l2_vending_Shape` -> `l5_vending_1` |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l2_vending_Shape` -> `l5_vending_2` |
| 2            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`                              |
| 3            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                               |
| 4            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                              |
| 5            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                              |

## Sector 17 (l2z1.p3d)
| Object Index | Object Type                                         | Object Name                          |
|--------------|-----------------------------------------------------|--------------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l2_monkiesgag_Shape` -> `mokey_gag` |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l2_vending_Shape` -> `l5_vending_2` |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l2_crate_Shape` -> `l5_crate_1`     |
| 3            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l2_crate_Shape` -> `l5_crate_2`     |
| 4            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l2_crate_Shape` -> `l5_crate_3`     |
| 5            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l2_crate_Shape` -> `l5_crate_4`     |
| 6            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l2_crate_Shape` -> `l5_crate_5`     |
| 7            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l2_crate_Shape` -> `l5_crate_6`     |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                              |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                               |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin5`                              |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`                              |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`                              |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin8`                              |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin6`                              |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin7`                              |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin11`                             |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin9`                              |
| 18           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin10`                             |
| 19           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C1Coin2`                          |
| 20           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C1Coin0`                          |
| 21           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C1Coin1`                          |
| 22           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C1Coin5`                          |
| 23           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C1Coin3`                          |
| 24           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C1Coin4`                          |
| 25           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                              |
| 26           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin12`                             |
| 27           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin13`                             |
| 28           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin16`                             |
| 29           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin14`                             |
| 30           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin15`                             |
| 31           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin19`                             |
| 32           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin17`                             |
| 33           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin18`                             |
| 34           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin22`                             |
| 35           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin20`                             |
| 36           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin21`                             |
| 37           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin23`                             |
| 38           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin24`                             |

## Sector 18 (l2z2.p3d)
| Object Index | Object Type                                         | Object Name                          |
|--------------|-----------------------------------------------------|--------------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l2_gaspump_Shape` -> `l2_gaspump_1` |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l2_gaspump_Shape` -> `l2_gaspump_2` |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l2_crate_Shape` -> `l5_crate_2`     |
| 3            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l2_crate_Shape` -> `l5_crate_3`     |
| 4            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l2_crate_Shape` -> `l5_crate_4`     |
| 5            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l2_crate_Shape` -> `l5_crate_7`     |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C1Coin0`                          |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C1Coin1`                          |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C1Coin2`                          |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C1Coin3`                          |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                              |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                              |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`                              |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin6`                              |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin7`                              |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin8`                              |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin9`                              |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin10`                             |
| 18           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin11`                             |
| 19           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin12`                             |
| 20           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin13`                             |
| 21           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin20`                             |
| 22           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin21`                             |
| 23           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin22`                             |
| 24           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin23`                             |
| 25           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin24`                             |
| 26           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin25`                             |
| 27           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin26`                             |
| 28           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin27`                             |
| 29           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin28`                             |

## Sector 19 (l2z3.p3d)
| Object Index | Object Type                                 | Object Name                                |
|--------------|---------------------------------------------|--------------------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]] | `l2_vending_Shape` -> `l2_vending_1`       |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]] | `l2_gatesmasha_Shape` -> `l2_gatesmasha_1` |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]] | `l2_crate_Shape` -> `l2_crate_1`           |

## Sector 20 (l2z4.p3d)
| Object Index | Object Type                                         | Object Name                                |
|--------------|-----------------------------------------------------|--------------------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l2_newsstand_Shape` -> `l2_newsstand_1`   |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l2_newsstand_Shape` -> `l2_newsstand_2`   |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l2_newsstand_Shape` -> `l2_newsstand_3`   |
| 3            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l2_newsstand_Shape` -> `l2_newsstand_4`   |
| 4            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l2_newsstand_Shape` -> `l2_newsstand_5`   |
| 5            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l2_crate_Shape` -> `l5_crate_4`           |
| 6            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l2_crate_Shape` -> `l5_crate_5`           |
| 7            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l2_gatesmasha_Shape` -> `l2_gatesmasha_1` |
| 8            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l2_gatesmasha_Shape` -> `l2_gatesmasha_2` |
| 9            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l2_gatesmasha_Shape` -> `l2_gatesmasha_3` |
| 10           | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l2_gatesmasha_Shape` -> `l2_gatesmasha_7` |
| 11           | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l2_vending_Shape` -> `l5_vending_1`       |
| 12           | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l2_vending_Shape` -> `l5_vending_4`       |
| 13           | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l2_vending_Shape` -> `l5_vending_5`       |
| 14           | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l2_vending_Shape` -> `l5_vending_6`       |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                                    |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`                                    |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`                                    |
| 18           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                                    |
| 19           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin6`                                    |
| 20           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin7`                                    |
| 21           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin5`                                    |
| 22           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin9`                                    |
| 23           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin10`                                   |
| 24           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin8`                                    |
| 25           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin12`                                   |
| 26           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin11`                                   |
| 27           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin18`                                   |
| 28           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin19`                                   |
| 29           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin17`                                   |
| 30           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin21`                                   |
| 31           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin22`                                   |
| 32           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin20`                                   |
| 33           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin24`                                   |
| 34           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin25`                                   |
| 35           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin23`                                   |
| 36           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin27`                                   |
| 37           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin28`                                   |
| 38           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin26`                                   |
| 39           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin29`                                   |
| 40           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin30`                                   |
| 41           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                                     |

## Sector 21 (l3r1.p3d)
| Object Index | Object Type                                         | Object Name                          |
|--------------|-----------------------------------------------------|--------------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l3_vending_Shape` -> `(no name)`    |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l3_gaspump_Shape` -> `l2_gaspump_1` |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l3_gaspump_Shape` -> `l2_gaspump_2` |
| 3            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R1C01Coin2`                         |
| 4            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R1C01Coin0`                         |
| 5            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R1C01Coin1`                         |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R1C01Coin5`                         |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R1C01Coin3`                         |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R1C01Coin4`                         |

## Sector 22 (l3r2.p3d)
This sector has no objects.

## Sector 23 (l3r3.p3d)
| Object Index | Object Type                                         | Object Name                                |
|--------------|-----------------------------------------------------|--------------------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l3_crate_Shape` -> `l3_crate_1`           |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l3_crate_Shape` -> `l3_crate_2`           |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l3_crate_Shape` -> `l3_crate_3`           |
| 3            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l3_globexsign_Shape` -> `l3_globexsign_1` |
| 4            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                                     |
| 5            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`                                    |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                                    |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin6`                                    |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                                    |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin5`                                    |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin9`                                    |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`                                    |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin8`                                    |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin7`                                    |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin11`                                   |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin10`                                   |

## Sector 24 (l3r4.p3d)
This sector has no objects.

## Sector 25 (l3r5.p3d)
| Object Index | Object Type                                         | Object Name                      |
|--------------|-----------------------------------------------------|----------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l3_crate_Shape` -> `l3_crate_1` |
| 1            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin8`                          |
| 2            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin5`                          |
| 3            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                           |
| 4            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                          |
| 5            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                          |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`                          |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`                          |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin7`                          |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin6`                          |

## Sector 26 (l3z1.p3d)
| Object Index | Object Type                                         | Object Name                       |
|--------------|-----------------------------------------------------|-----------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l3_vending_Shape` -> `(no name)` |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l3_vending_Shape` -> `(no name)` |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l3_vending_Shape` -> `(no name)` |
| 3            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l3_crate_Shape` -> `l3_crate_1`  |
| 4            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C1Coin1`                       |
| 5            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C1Coin0`                       |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C1Coin4`                       |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C1Coin2`                       |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C1Coin3`                       |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C2Coin1`                       |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C1Coin5`                       |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C2Coin0`                       |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C2Coin4`                       |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C2Coin2`                       |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C2Coin3`                       |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C2Coin7`                       |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C2Coin5`                       |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C2Coin6`                       |
| 18           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C2Coin8`                       |
| 19           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C2Coin9`                       |
| 20           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                           |
| 21           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                            |

## Sector 27 (l3z2.p3d)
| Object Index | Object Type                                         | Object Name                       |
|--------------|-----------------------------------------------------|-----------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l3_vending_Shape` -> `(no name)` |
| 1            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin15`                          |
| 2            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                            |
| 3            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                           |
| 4            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                           |
| 5            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`                           |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`                           |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin5`                           |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin7`                           |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin14`                          |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin6`                           |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin8`                           |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin10`                          |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin9`                           |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin13`                          |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin11`                          |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin12`                          |

## Sector 28 (l3z3.p3d)
| Object Index | Object Type                                         | Object Name                                   |
|--------------|-----------------------------------------------------|-----------------------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l3_kickbird_Shape` -> `l3_kickbird2`         |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l3_kickbird_Shape` -> `l3_kickbird3`         |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l3_crate_Shape` -> `l3_crate_1`              |
| 3            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l3_crate_Shape` -> `l3_crate_2`              |
| 4            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l3_kickbirdaway_Shape` -> `l3_kickbirdaway1` |
| 5            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l3_kickbirdaway_Shape` -> `l3_kickbirdaway2` |
| 6            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l3_kickbirdaway_Shape` -> `l3_kickbirdaway3` |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`                                       |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                                       |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin17`                                      |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin20`                                      |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin18`                                      |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin19`                                      |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin23`                                      |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin21`                                      |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin22`                                      |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin26`                                      |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin24`                                      |
| 18           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin25`                                      |
| 19           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin29`                                      |
| 20           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin27`                                      |
| 21           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin28`                                      |
| 22           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin30`                                      |
| 23           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin31`                                      |

## Sector 29 (l3z4.p3d)
| Object Index | Object Type                                         | Object Name                       |
|--------------|-----------------------------------------------------|-----------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l3_gate_Shape` -> `l3_gate_1`    |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l3_gate_Shape` -> `l3_gate_2`    |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l3_gate_Shape` -> `l3_gate_3`    |
| 3            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l3_gate_Shape` -> `l3_gate_4`    |
| 4            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l3_vending_Shape` -> `(no name)` |
| 5            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l3_vending_Shape` -> `(no name)` |
| 6            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l3_vending_Shape` -> `(no name)` |
| 7            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l3_crate_Shape` -> `l3_crate_1`  |
| 8            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l3_crate_Shape` -> `l3_crate_2`  |
| 9            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l3_crate_Shape` -> `l3_crate_3`  |
| 10           | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l3_crate_Shape` -> `l3_crate_4`  |
| 11           | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l3_crate_Shape` -> `l3_crate_5`  |
| 12           | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l3_crate_Shape` -> `l3_crate_6`  |
| 13           | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l3_crate_Shape` -> `l3_crate_7`  |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`                           |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin6`                           |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`                           |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin5`                           |
| 18           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin9`                           |
| 19           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin8`                           |
| 20           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z4C1Coin2`                       |
| 21           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z4C1Coin0`                       |
| 22           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z4C1Coin1`                       |
| 23           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z4C1Coin5`                       |
| 24           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z4C1Coin3`                       |
| 25           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z4C1Coin4`                       |
| 26           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z4C1Coin6`                       |
| 27           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z4C1Coin7`                       |
| 28           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                           |
| 29           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                           |
| 30           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin15`                          |
| 31           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin13`                          |
| 32           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin14`                          |
| 33           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin18`                          |
| 34           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin16`                          |
| 35           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin17`                          |
| 36           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin21`                          |
| 37           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin19`                          |
| 38           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin20`                          |
| 39           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin7`                           |

## Sector 30 (l3z5.p3d)
| Object Index | Object Type                                         | Object Name                       |
|--------------|-----------------------------------------------------|-----------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l3_crate_Shape` -> `l3_crate_1`  |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l3_crate_Shape` -> `l3_crate_2`  |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l3_vending_Shape` -> `(no name)` |
| 3            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin10`                          |
| 4            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                            |
| 5            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                           |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                           |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`                           |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`                           |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin5`                           |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin6`                           |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin7`                           |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin8`                           |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin11`                          |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin9`                           |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin12`                          |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin13`                          |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin15`                          |
| 18           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin16`                          |
| 19           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin14`                          |
| 20           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin18`                          |
| 21           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin19`                          |
| 22           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin17`                          |
| 23           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin21`                          |
| 24           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin20`                          |
| 25           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin23`                          |
| 26           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin24`                          |
| 27           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin22`                          |
| 28           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin25`                          |

## Sector 31 (l4r1.p3d)
| Object Index | Object Type                                         | Object Name |
|--------------|-----------------------------------------------------|-------------|
| 0            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`     |
| 1            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`     |
| 2            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`     |
| 3            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`      |
| 4            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin7`     |
| 5            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin5`     |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin6`     |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`     |

## Sector 32 (l4r2.p3d)
| Object Index | Object Type                                 | Object Name                     |
|--------------|---------------------------------------------|---------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]] | `l4_crate_Shape` -> `l4_crate3` |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]] | `l4_crate_Shape` -> `l4_crate5` |

## Sector 33 (l4r3.p3d)
| Object Index | Object Type                                         | Object Name                          |
|--------------|-----------------------------------------------------|--------------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_crate_Shape` -> `(no name)`      |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_crate_Shape` -> `(no name)`      |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_crate_Shape` -> `(no name)`      |
| 3            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_vending_Shape` -> `l1_vending_1` |
| 4            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_gaspump_Shape` -> `l2_gaspump_2` |
| 5            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_gaspump_Shape` -> `l2_gaspump_1` |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R3C1Coin1`                          |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R3C1Coin0`                          |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R3C1Coin4`                          |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R3C1Coin2`                          |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R3C1Coin3`                          |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R3C3Coin1`                          |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R3C1Coin5`                          |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R3C3Coin0`                          |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R3C4Coin0`                          |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R3C3Coin2`                          |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R3C3Coin3`                          |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R3C4Coin3`                          |
| 18           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R3C4Coin1`                          |
| 19           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R3C4Coin2`                          |
| 20           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R3C5Coin2`                          |
| 21           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R3C5Coin0`                          |
| 22           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R3C5Coin1`                          |
| 23           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R3C5Coin3`                          |
| 24           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                               |
| 25           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`                              |
| 26           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                              |
| 27           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                              |
| 28           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`                              |
| 29           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin5`                              |
| 30           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin6`                              |
| 31           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin7`                              |

## Sector 34 (l4r4a.p3d)
| Object Index | Object Type                                         | Object Name |
|--------------|-----------------------------------------------------|-------------|
| 0            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`     |
| 1            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`     |
| 2            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`     |
| 3            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin5`     |
| 4            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`      |
| 5            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`     |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin6`     |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin7`     |

## Sector 35 (l4r4b.p3d)
| Object Index | Object Type                                         | Object Name                     |
|--------------|-----------------------------------------------------|---------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_crate_Shape` -> `(no name)` |
| 1            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R4BC1Coin0`                    |
| 2            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R4BC1Coin1`                    |
| 3            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R4BC1Coin2`                    |
| 4            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R4BC1Coin3`                    |
| 5            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R4BC1Coin4`                    |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R4BC1Coin5`                    |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R4BC1Coin6`                    |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R4BC1Coin7`                    |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R4BC1Coin8`                    |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R4BC1Coin9`                    |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin0`           |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin1`           |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin2`           |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin3`           |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin4`           |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin5`           |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin6`           |
| 18           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin7`           |
| 19           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin8`           |
| 20           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin9`           |
| 21           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin10`          |
| 22           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin11`          |
| 23           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin12`          |
| 24           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin13`          |
| 25           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin14`          |
| 26           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin15`          |
| 27           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin16`          |
| 28           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin17`          |
| 29           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin19`          |
| 30           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `burnsbackcoinsCoin18`          |

## Sector 36 (l4r6.p3d)
| Object Index | Object Type                                         | Object Name                                        |
|--------------|-----------------------------------------------------|----------------------------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4r6_tomaccostand_Shape` -> `l1r6_tomaccostand_1` |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_fence_Shape` -> `l1_fence_8`                   |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_fence_Shape` -> `l1_fence_9`                   |
| 3            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_fence_Shape` -> `l1_fence_10`                  |
| 4            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_haybale_Shape` -> `l1_haybale_`                |
| 5            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_haybale_Shape` -> `l1_haybale_7`               |
| 6            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_haybale_Shape` -> `l1_haybale_9`               |
| 7            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_haybale_Shape` -> `l1_haybale_11`              |
| 8            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_haybale_Shape` -> `l1_haybale_13`              |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R6C1Coin0`                                        |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R6C1Coin1`                                        |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R6C1Coin2`                                        |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R6C1Coin3`                                        |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                                            |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                                            |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                                             |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`                                            |

## Sector 37 (l4r7.p3d)
| Object Index | Object Type                                         | Object Name                          |
|--------------|-----------------------------------------------------|--------------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_crate_Shape` -> `l1_crate`       |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_vending_Shape` -> `l1_vending_2` |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_vending_Shape` -> `l1_vending_4` |
| 3            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_gaspump_Shape` -> `l1_gaspump_1` |
| 4            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_gaspump_Shape` -> `l1_gaspump_2` |
| 5            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin7`                              |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin9`                              |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin1`                          |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin0`                          |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin4`                          |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin2`                          |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin3`                          |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin7`                          |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin5`                          |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin6`                          |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin10`                         |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin8`                          |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin9`                          |
| 18           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin13`                         |
| 19           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin11`                         |
| 20           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin12`                         |
| 21           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin16`                         |
| 22           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin14`                         |
| 23           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin15`                         |
| 24           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin19`                         |
| 25           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin17`                         |
| 26           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin8`                              |
| 27           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                               |
| 28           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`                              |
| 29           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                              |
| 30           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                              |
| 31           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin6`                              |
| 32           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`                              |
| 33           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin5`                              |
| 34           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin18`                         |

## Sector 38 (l4z1.p3d)
| Object Index | Object Type                                         | Object Name                      |
|--------------|-----------------------------------------------------|----------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_crate_Shape` -> `l4_crate_2` |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_crate_Shape` -> `l4_crate_3` |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_crate_Shape` -> `l4_crate_5` |
| 3            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_crate_Shape` -> `l4_crate_6` |
| 4            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_crate_Shape` -> `l4_crate_7` |
| 5            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_crate_Shape` -> `l4_crate_9` |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C4Coin0`                      |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C4Coin2`                      |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C4Coin3`                      |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C4Coin1`                      |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C4Coin5`                      |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C4Coin6`                      |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C4Coin4`                      |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                          |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C3Coin0`                      |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C4Coin7`                      |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C3Coin2`                      |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C3Coin3`                      |
| 18           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C3Coin1`                      |
| 19           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C3Coin5`                      |
| 20           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C3Coin6`                      |
| 21           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C3Coin4`                      |
| 22           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                           |
| 23           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                          |
| 24           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C3Coin7`                      |
| 25           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`                          |
| 26           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin5`                          |
| 27           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`                          |
| 28           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin7`                          |
| 29           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin6`                          |
| 30           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin8`                          |

## Sector 39 (l4z2.p3d)
| Object Index | Object Type                                         | Object Name                          |
|--------------|-----------------------------------------------------|--------------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_gaspump_Shape` -> `l4_gaspump_1` |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_gaspump_Shape` -> `l4_gaspump_2` |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_vending_Shape` -> `l4_vending_1` |
| 3            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_vending_Shape` -> `l4_vending_2` |
| 4            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_vending_Shape` -> `l4_vending_3` |
| 5            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_crate_Shape` -> `l4_crate2`      |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C3Coin2`                          |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C3Coin0`                          |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C3Coin4`                          |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C3Coin5`                          |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C3Coin3`                          |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C3Coin7`                          |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C4Coin0`                          |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C3Coin6`                          |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C4Coin2`                          |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C4Coin3`                          |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C4Coin1`                          |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                              |
| 18           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                              |
| 19           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                               |
| 20           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`                              |
| 21           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin5`                              |
| 22           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`                              |
| 23           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin7`                              |
| 24           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin8`                              |
| 25           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin6`                              |
| 26           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin10`                             |
| 27           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin9`                              |
| 28           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin12`                             |
| 29           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin11`                             |
| 30           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin14`                             |
| 31           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin16`                             |
| 32           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin13`                             |
| 33           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C3Coin1`                          |
| 34           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin15`                             |
| 35           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin17`                             |

## Sector 40 (l4z3.p3d)
| Object Index | Object Type                                         | Object Name                          |
|--------------|-----------------------------------------------------|--------------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_crate_Shape` -> `l4_crate2`      |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_crate_Shape` -> `l4_crate4`      |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_crate_Shape` -> `l4_crate5`      |
| 3            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_crate_Shape` -> `l4_crate6`      |
| 4            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_vending_Shape` -> `l1_vending_1` |
| 5            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C1Coin0`                          |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C1Coin1`                          |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C1Coin2`                          |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C1Coin3`                          |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C1Coin4`                          |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C1Coin5`                          |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C2Coin0`                          |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C2Coin1`                          |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C2Coin2`                          |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C3Coin0`                          |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C3Coin1`                          |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C3Coin2`                          |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C3Coin3`                          |
| 18           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C3Coin4`                          |
| 19           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C3Coin5`                          |
| 20           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C3Coin6`                          |
| 21           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C3Coin7`                          |
| 22           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C3Coin8`                          |
| 23           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C3Coin9`                          |
| 24           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                               |
| 25           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                              |
| 26           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`                              |
| 27           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                              |
| 28           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`                              |

## Sector 41 (l4z4.p3d)
This sector has no objects.

## Sector 42 (l4z6.p3d)
| Object Index | Object Type                                         | Object Name                                  |
|--------------|-----------------------------------------------------|----------------------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_vending_Shape` -> `l4_vending_1`         |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_vending_Shape` -> `l4_vending_2`         |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l4_tunnelfence_Shape` -> `l1_tunnelfence_1` |
| 3            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z6C1Coin0`                                  |
| 4            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z6C1Coin2`                                  |
| 5            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z6C1Coin3`                                  |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z6C1Coin1`                                  |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z6C1Coin5`                                  |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z6C1Coin4`                                  |

## Sector 43 (l4z7.p3d)
| Object Index | Object Type                                         | Object Name  |
|--------------|-----------------------------------------------------|--------------|
| 0            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin25`     |
| 1            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin2`  |
| 2            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin0`  |
| 3            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin1`  |
| 4            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin5`  |
| 5            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin3`  |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin4`  |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin8`  |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin6`  |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin7`  |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin11` |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin9`  |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin10` |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin14` |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin12` |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin13` |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin17` |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin15` |
| 18           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin16` |
| 19           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin18` |
| 20           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin19` |
| 21           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin27`     |
| 22           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin8`      |
| 23           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin9`      |
| 24           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin10`     |
| 25           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin11`     |
| 26           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin12`     |
| 27           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin13`     |
| 28           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin14`     |
| 29           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin15`     |
| 30           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin26`     |
| 31           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin16`     |
| 32           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin17`     |
| 33           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin23`     |
| 34           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin24`     |

## Sector 44 (l5r1.p3d)
| Object Index | Object Type                                         | Object Name                          |
|--------------|-----------------------------------------------------|--------------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l5_vending_Shape` -> `l5_vending_2` |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l5_crate_Shape` -> `l5_crate_4`     |
| 2            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                               |
| 3            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                              |
| 4            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                              |
| 5            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`                              |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`                              |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin5`                              |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin6`                              |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin7`                              |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin8`                              |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin9`                              |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin10`                             |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin11`                             |

## Sector 45 (l5r2.p3d)
| Object Index | Object Type                                         | Object Name                            |
|--------------|-----------------------------------------------------|----------------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l5_crate_Shape` -> `l5_crate_2`       |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l5_vending_Shape` -> `l5l2_vending_2` |
| 2            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                                |
| 3            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                                 |
| 4            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin7`                                |
| 5            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                                |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`                                |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin6`                                |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`                                |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin5`                                |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin10`                               |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin8`                                |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin18`                               |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin13`                               |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin11`                               |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin12`                               |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin15`                               |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin14`                               |
| 18           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin17`                               |
| 19           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin9`                                |
| 20           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin16`                               |

## Sector 46 (l5r3.p3d)
This sector has no objects.

## Sector 47 (l5r4.p3d)
| Object Index | Object Type                                         | Object Name                          |
|--------------|-----------------------------------------------------|--------------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l5_vending_Shape` -> `l5_vending_1` |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l5_vending_Shape` -> `l5_vending_2` |
| 2            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                               |
| 3            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`                              |
| 4            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                              |
| 5            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                              |

## Sector 48 (l5z1.p3d)
| Object Index | Object Type                                         | Object Name                          |
|--------------|-----------------------------------------------------|--------------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l5_crate_Shape` -> `l5_crate_7`     |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l5_crate_Shape` -> `l5_crate_8`     |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l5_crate_Shape` -> `l5_crate_9`     |
| 3            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l5_crate_Shape` -> `l5_crate_10`    |
| 4            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l5_crate_Shape` -> `l5_crate_11`    |
| 5            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l5_crate_Shape` -> `l5_crate_12`    |
| 6            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l5_vending_Shape` -> `l5_vending_3` |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                               |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                              |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`                              |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`                              |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin5`                              |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin6`                              |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin7`                              |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin8`                              |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin9`                              |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin10`                             |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin11`                             |
| 18           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C1Coin0`                          |
| 19           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C1Coin1`                          |
| 20           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C1Coin2`                          |
| 21           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C1Coin3`                          |
| 22           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C1Coin4`                          |
| 23           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C1Coin5`                          |
| 24           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin12`                             |
| 25           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin13`                             |
| 26           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                              |
| 27           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin14`                             |
| 28           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin15`                             |
| 29           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin16`                             |
| 30           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin18`                             |
| 31           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin19`                             |
| 32           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin20`                             |
| 33           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin21`                             |
| 34           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin22`                             |
| 35           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin23`                             |
| 36           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin24`                             |
| 37           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin17`                             |

## Sector 49 (l5z2.p3d)
| Object Index | Object Type                                         | Object Name                              |
|--------------|-----------------------------------------------------|------------------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l5_crate_Shape` -> `l5_crate_2`         |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l5_crate_Shape` -> `l5_crate_3`         |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l5_crate_Shape` -> `l5_crate_4`         |
| 3            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l5_crate_Shape` -> `l5_crate_7`         |
| 4            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l5_gaspump_Shape` -> `l5l2_gaspump_3`   |
| 5            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l5_gaspump_Shape` -> `l5l2_gaspump_4`   |
| 6            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l5_stopsign_Shape` -> `l5l2_stopsign_6` |
| 7            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l5_stopsign_Shape` -> `l5l2_stopsign_7` |
| 8            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l5_stopsign_Shape` -> `l5l2_stopsign_8` |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin18`                                 |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                                  |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                                  |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`                                  |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin9`                                  |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin7`                                  |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin8`                                  |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin12`                                 |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin10`                                 |
| 18           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin11`                                 |
| 19           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z4C2Coin1`                              |
| 20           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin13`                                 |
| 21           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z4C2Coin0`                              |
| 22           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin14`                                 |
| 23           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z4C2Coin2`                              |
| 24           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z4C2Coin3`                              |
| 25           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin16`                                 |
| 26           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin22`                                 |
| 27           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin15`                                 |
| 28           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin21`                                 |
| 29           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin25`                                 |
| 30           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin20`                                 |
| 31           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin24`                                 |
| 32           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin28`                                 |
| 33           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin23`                                 |
| 34           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin27`                                 |
| 35           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin6`                                  |
| 36           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin26`                                 |

## Sector 50 (l5z3.p3d)
| Object Index | Object Type                                 | Object Name                                  |
|--------------|---------------------------------------------|----------------------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]] | `l5_gatesmasha_Shape` -> `l5l2_gatesmasha_2` |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]] | `l5_vending_Shape` -> `l5l2_vending_3`       |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]] | `l5_stopsign_Shape` -> `l5l1_stopsign_4`     |
| 3            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]] | `l5_stopsign_Shape` -> `l5l1_stopsign_5`     |
| 4            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]] | `l5_stopsign_Shape` -> `l5l1_stopsign_6`     |
| 5            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]] | `l5_stopsign_Shape` -> `l5l1_stopsign_7`     |
| 6            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]] | `l5_crate_Shape` -> `l5l2_crate_2`           |

## Sector 51 (l5z4.p3d)
| Object Index | Object Type                                         | Object Name                                |
|--------------|-----------------------------------------------------|--------------------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l5_crate_Shape` -> `l5_crate_4`           |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l5_crate_Shape` -> `l5_crate_5`           |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l5_gatesmasha_Shape` -> `l2_gatesmasha_4` |
| 3            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l5_gatesmasha_Shape` -> `l2_gatesmasha_5` |
| 4            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l5_gatesmasha_Shape` -> `l2_gatesmasha_6` |
| 5            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l5_newsstand_Shape` -> `l2_newsstand_6`   |
| 6            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l5_newsstand_Shape` -> `l2_newsstand_7`   |
| 7            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l5_newsstand_Shape` -> `l2_newsstand_8`   |
| 8            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l5_newsstand_Shape` -> `l2_newsstand_9`   |
| 9            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l5_newsstand_Shape` -> `l2_newsstand_10`  |
| 10           | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l5_vending_Shape` -> `l5_vending_1`       |
| 11           | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l5_vending_Shape` -> `l5_vending_4`       |
| 12           | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l5_vending_Shape` -> `l5_vending_5`       |
| 13           | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l5_vending_Shape` -> `l5_vending_6`       |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin17`                                   |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin30`                                   |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                                     |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                                    |
| 18           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                                    |
| 19           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`                                    |
| 20           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`                                    |
| 21           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin5`                                    |
| 22           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin6`                                    |
| 23           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin7`                                    |
| 24           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin8`                                    |
| 25           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin9`                                    |
| 26           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin10`                                   |
| 27           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin13`                                   |
| 28           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin14`                                   |
| 29           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin15`                                   |
| 30           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin18`                                   |
| 31           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin19`                                   |
| 32           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin16`                                   |
| 33           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin21`                                   |
| 34           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin22`                                   |
| 35           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin20`                                   |
| 36           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin24`                                   |
| 37           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin25`                                   |
| 38           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin23`                                   |
| 39           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin27`                                   |
| 40           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin28`                                   |
| 41           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin26`                                   |
| 42           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin29`                                   |

## Sector 52 (l6r1.p3d)
| Object Index | Object Type                                         | Object Name                          |
|--------------|-----------------------------------------------------|--------------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l6_vending_Shape` -> `(no name)`    |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l6_gaspump_Shape` -> `l3_gaspump_1` |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l6_gaspump_Shape` -> `l3_gaspump_2` |
| 3            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R1C01Coin0`                         |
| 4            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R1C01Coin2`                         |
| 5            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R1C01Coin3`                         |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R1C01Coin1`                         |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R1C01Coin4`                         |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R1C01Coin5`                         |

## Sector 53 (l6r2.p3d)
| Object Index | Object Type                                 | Object Name                       |
|--------------|---------------------------------------------|-----------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]] | `l6_vending_Shape` -> `(no name)` |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]] | `l6_vending_Shape` -> `(no name)` |

## Sector 54 (l6r3.p3d)
| Object Index | Object Type                                         | Object Name                                |
|--------------|-----------------------------------------------------|--------------------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l3_globexsign_Shape` -> `l3_globexsign_1` |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l6_crate_Shape` -> `l3_crate_1`           |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l6_crate_Shape` -> `l3_crate_2`           |
| 3            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l6_crate_Shape` -> `l3_crate_3`           |
| 4            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin13`                                   |
| 5            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                                     |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`                                    |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                                    |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                                    |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin6`                                    |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`                                    |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin5`                                    |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin9`                                    |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin7`                                    |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin8`                                    |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin12`                                   |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin10`                                   |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin11`                                   |

## Sector 55 (l6r4.p3d)
This sector has no objects.

## Sector 56 (l6r5.p3d)
| Object Index | Object Type                                         | Object Name                      |
|--------------|-----------------------------------------------------|----------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l6_crate_Shape` -> `l6_crate_1` |
| 1            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                           |
| 2            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                          |
| 3            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`                          |
| 4            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                          |
| 5            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin5`                          |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin6`                          |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`                          |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin8`                          |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin7`                          |

## Sector 57 (l6z1.p3d)
| Object Index | Object Type                                         | Object Name                       |
|--------------|-----------------------------------------------------|-----------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l6_crate_Shape` -> `l3_crate_1`  |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l6_vending_Shape` -> `(no name)` |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l6_vending_Shape` -> `(no name)` |
| 3            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l6_vending_Shape` -> `(no name)` |
| 4            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C1Coin0`                       |
| 5            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C1Coin1`                       |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C1Coin2`                       |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C1Coin3`                       |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C1Coin4`                       |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C1Coin5`                       |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C2Coin0`                       |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C2Coin1`                       |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C2Coin2`                       |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C2Coin3`                       |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C2Coin4`                       |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C2Coin5`                       |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C2Coin6`                       |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C2Coin8`                       |
| 18           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C2Coin9`                       |
| 19           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                            |
| 20           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                           |
| 21           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C2Coin7`                       |

## Sector 58 (l6z2.p3d)
| Object Index | Object Type                                         | Object Name |
|--------------|-----------------------------------------------------|-------------|
| 0            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin15`    |
| 1            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin13`    |
| 2            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`      |
| 3            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`     |
| 4            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`     |
| 5            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`     |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`     |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin5`     |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin14`    |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin7`     |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin8`     |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin9`     |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin10`    |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin11`    |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin12`    |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin6`     |

## Sector 59 (l6z3.p3d)
| Object Index | Object Type                                         | Object Name                      |
|--------------|-----------------------------------------------------|----------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l6_crate_Shape` -> `l3_crate_1` |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l6_crate_Shape` -> `l3_crate_2` |
| 2            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin31`                         |
| 3            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                          |
| 4            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin18`                         |
| 5            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`                          |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin17`                         |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin21`                         |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin20`                         |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin24`                         |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin19`                         |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin23`                         |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin27`                         |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin22`                         |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin26`                         |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin30`                         |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin25`                         |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin29`                         |
| 18           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin28`                         |

## Sector 60 (l6z4.p3d)
| Object Index | Object Type                                         | Object Name                       |
|--------------|-----------------------------------------------------|-----------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l6_vending_Shape` -> `(no name)` |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l6_vending_Shape` -> `(no name)` |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l6_vending_Shape` -> `(no name)` |
| 3            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l6_gate_Shape` -> `l6_gate_1`    |
| 4            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l6_gate_Shape` -> `l6_gate_2`    |
| 5            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l6_gate_Shape` -> `l6_gate_3`    |
| 6            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l6_gate_Shape` -> `l6_gate_4`    |
| 7            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l6_crate_Shape` -> `l6_crate_1`  |
| 8            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l6_crate_Shape` -> `l6_crate_2`  |
| 9            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l6_crate_Shape` -> `l6_crate_3`  |
| 10           | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l6_crate_Shape` -> `l6_crate_4`  |
| 11           | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l6_crate_Shape` -> `l6_crate_5`  |
| 12           | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l6_crate_Shape` -> `l6_crate_6`  |
| 13           | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l6_crate_Shape` -> `l6_crate_7`  |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`                           |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin6`                           |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`                           |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin5`                           |
| 18           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin9`                           |
| 19           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin7`                           |
| 20           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin8`                           |
| 21           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z4C1Coin2`                       |
| 22           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z4C1Coin0`                       |
| 23           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z4C1Coin1`                       |
| 24           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z4C1Coin5`                       |
| 25           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z4C1Coin3`                       |
| 26           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z4C1Coin4`                       |
| 27           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z4C1Coin6`                       |
| 28           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z4C1Coin7`                       |
| 29           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                           |
| 30           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                           |
| 31           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin15`                          |
| 32           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin13`                          |
| 33           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin14`                          |
| 34           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin18`                          |
| 35           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin16`                          |
| 36           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin17`                          |
| 37           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin21`                          |
| 38           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin19`                          |
| 39           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin20`                          |

## Sector 61 (l6z5.p3d)
| Object Index | Object Type                                         | Object Name                       |
|--------------|-----------------------------------------------------|-----------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l6_crate_Shape` -> `l6_crate_1`  |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l6_crate_Shape` -> `l6_crate_2`  |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l6_vending_Shape` -> `(no name)` |
| 3            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin8`                           |
| 4            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                           |
| 5            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                            |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin5`                           |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`                           |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                           |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin7`                           |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin11`                          |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin6`                           |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin10`                          |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin9`                           |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin12`                          |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin15`                          |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin14`                          |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin18`                          |
| 18           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin13`                          |
| 19           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin17`                          |
| 20           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin21`                          |
| 21           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin16`                          |
| 22           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin20`                          |
| 23           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin25`                          |
| 24           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin19`                          |
| 25           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin22`                          |
| 26           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin24`                          |
| 27           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin23`                          |
| 28           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`                           |

## Sector 62 (l7r1.p3d)
| Object Index | Object Type                                         | Object Name |
|--------------|-----------------------------------------------------|-------------|
| 0            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin7`     |
| 1            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`      |
| 2            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`     |
| 3            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`     |
| 4            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`     |
| 5            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin6`     |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`     |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin5`     |

## Sector 63 (l7r2.p3d)
| Object Index | Object Type                                 | Object Name                     |
|--------------|---------------------------------------------|---------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]] | `l7_crate_Shape` -> `l7_crate3` |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]] | `l7_crate_Shape` -> `l7_crate6` |

## Sector 64 (l7r3.p3d)
This sector has no objects.

## Sector 65 (l7r4a.p3d)
This sector has no objects.

## Sector 66 (l7r4b.p3d)
This sector has no objects.

## Sector 67 (l7r6.p3d)
| Object Index | Object Type                                         | Object Name                                        |
|--------------|-----------------------------------------------------|----------------------------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_haybale_Shape` -> `l1_haybale_6`               |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_haybale_Shape` -> `l1_haybale_8`               |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_haybale_Shape` -> `l1_haybale_10`              |
| 3            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_haybale_Shape` -> `l1_haybale_12`              |
| 4            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_haybale_Shape` -> `l1_haybale_14`              |
| 5            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7r6_tomaccostand_Shape` -> `l1r6_tomaccostand_2` |
| 6            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_fence_Shape` -> `l1_fence_4`                   |
| 7            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_fence_Shape` -> `l1_fence_6`                   |
| 8            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_fence_Shape` -> `l1_fence_7`                   |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R6C1Coin0`                                        |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R6C1Coin1`                                        |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R6C1Coin2`                                        |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R6C1Coin3`                                        |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                                             |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                                            |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                                            |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`                                            |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin10`                                           |
| 18           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin11`                                           |
| 19           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin12`                                           |
| 20           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin15`                                           |
| 21           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin16`                                           |
| 22           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin17`                                           |
| 23           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin18`                                           |
| 24           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin19`                                           |
| 25           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin20`                                           |
| 26           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin21`                                           |
| 27           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin22`                                           |
| 28           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin23`                                           |
| 29           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin26`                                           |
| 30           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin27`                                           |
| 31           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin24`                                           |

## Sector 68 (l7r7.p3d)
| Object Index | Object Type                                         | Object Name                          |
|--------------|-----------------------------------------------------|--------------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_crate_Shape` -> `l1_crate1`      |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_vending_Shape` -> `l1_vending_`  |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_vending_Shape` -> `l1_vending_5` |
| 3            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_arch_Shape` -> `l7_arch_`        |
| 4            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_arch_Shape` -> `l7_arch_1`       |
| 5            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_gaspump_Shape` -> `l1_gaspump_`  |
| 6            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_gaspump_Shape` -> `l1_gaspump_3` |
| 7            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_spider_Shape` -> `l7_spider_4`   |
| 8            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_spider_Shape` -> `l7_spider_5`   |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin1`                          |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin0`                          |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin4`                          |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin2`                          |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin3`                          |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin7`                          |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin5`                          |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin6`                          |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin10`                         |
| 18           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin8`                          |
| 19           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin9`                          |
| 20           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin13`                         |
| 21           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin11`                         |
| 22           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin12`                         |
| 23           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin16`                         |
| 24           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin14`                         |
| 25           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin15`                         |
| 26           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin19`                         |
| 27           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin17`                         |
| 28           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `R7C1Coin18`                         |
| 29           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin9`                              |
| 30           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin7`                              |
| 31           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                               |
| 32           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin8`                              |
| 33           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`                              |
| 34           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                              |
| 35           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                              |
| 36           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin6`                              |
| 37           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`                              |
| 38           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin5`                              |

## Sector 69 (l7z1.p3d)
| Object Index | Object Type                                         | Object Name                      |
|--------------|-----------------------------------------------------|----------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_crate_Shape` -> `l7_crate_2` |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_crate_Shape` -> `l7_crate_3` |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_crate_Shape` -> `l7_crate_5` |
| 3            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_crate_Shape` -> `l7_crate_6` |
| 4            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_crate_Shape` -> `l7_crate_7` |
| 5            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_crate_Shape` -> `l7_crate_9` |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C4Coin2`                      |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C4Coin0`                      |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C4Coin5`                      |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C4Coin3`                      |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C4Coin1`                      |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                          |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C4Coin6`                      |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C4Coin4`                      |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C3Coin2`                      |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C3Coin0`                      |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C4Coin7`                      |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C3Coin5`                      |
| 18           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C3Coin3`                      |
| 19           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C3Coin1`                      |
| 20           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                           |
| 21           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C3Coin6`                      |
| 22           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C3Coin4`                      |
| 23           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`                          |
| 24           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                          |
| 25           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z1C3Coin7`                      |
| 26           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin8`                          |
| 27           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin5`                          |
| 28           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`                          |
| 29           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin7`                          |
| 30           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin6`                          |

## Sector 70 (l7z2.p3d)
| Object Index | Object Type                                         | Object Name                          |
|--------------|-----------------------------------------------------|--------------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_vending_Shape` -> `l7_vending_2` |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_vending_Shape` -> `l7_vending_3` |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_vending_Shape` -> `l7_vending_4` |
| 3            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_crate_Shape` -> `l7_crate2`      |
| 4            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_crate_Shape` -> `l7_crate3`      |
| 5            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_crate_Shape` -> `l7_crate4`      |
| 6            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_spider_Shape` -> `l7_spider_1`   |
| 7            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_spider_Shape` -> `l7_spider_3`   |
| 8            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_gaspump_Shape` -> `l2_gaspump_2` |
| 9            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_gaspump_Shape` -> `l2_gaspump_1` |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin16`                             |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C3Coin0`                          |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C3Coin1`                          |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C3Coin2`                          |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C3Coin3`                          |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C3Coin4`                          |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C3Coin5`                          |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C3Coin6`                          |
| 18           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C3Coin7`                          |
| 19           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C4Coin0`                          |
| 20           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C4Coin1`                          |
| 21           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C4Coin2`                          |
| 22           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z2C4Coin3`                          |
| 23           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                               |
| 24           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                              |
| 25           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                              |
| 26           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`                              |
| 27           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`                              |
| 28           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin5`                              |
| 29           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin6`                              |
| 30           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin7`                              |
| 31           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin8`                              |
| 32           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin9`                              |
| 33           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin17`                             |
| 34           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin11`                             |
| 35           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin12`                             |
| 36           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin13`                             |
| 37           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin14`                             |
| 38           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin15`                             |
| 39           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin10`                             |

## Sector 71 (l7z3.p3d)
| Object Index | Object Type                                         | Object Name                          |
|--------------|-----------------------------------------------------|--------------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_vending_Shape` -> `l1_vending_1` |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_spider_Shape` -> `l7_spider_1`   |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_spider_Shape` -> `l7_spider_2`   |
| 3            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_crate_Shape` -> `l7_crate2`      |
| 4            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_crate_Shape` -> `l7_crate5`      |
| 5            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_crate_Shape` -> `l7_crate6`      |
| 6            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_crate_Shape` -> `l7_crate7`      |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C1Coin0`                          |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C1Coin1`                          |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C1Coin2`                          |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C1Coin3`                          |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C1Coin4`                          |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C2Coin0`                          |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C2Coin1`                          |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C2Coin2`                          |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C3Coin0`                          |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C3Coin1`                          |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C3Coin2`                          |
| 18           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C3Coin3`                          |
| 19           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C3Coin4`                          |
| 20           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C3Coin5`                          |
| 21           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C3Coin6`                          |
| 22           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C3Coin7`                          |
| 23           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C3Coin8`                          |
| 24           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C3Coin9`                          |
| 25           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                               |
| 26           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                              |
| 27           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                              |
| 28           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`                              |
| 29           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`                              |
| 30           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z3C1Coin5`                          |

## Sector 72 (l7z4.p3d)
This sector has no objects.

## Sector 73 (l7z6.p3d)
| Object Index | Object Type                                         | Object Name                          |
|--------------|-----------------------------------------------------|--------------------------------------|
| 0            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_vending_Shape` -> `l7_vending_1` |
| 1            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_vending_Shape` -> `l7_vending_3` |
| 2            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_vending_Shape` -> `l7_vending_5` |
| 3            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_crate_Shape` -> `l7_crate_1`     |
| 4            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_crate_Shape` -> `l7_crate_2`     |
| 5            | [[/Pure3DFiles/ChunkTypes/AnimDynaPhys.md]]         | `l7_crate_Shape` -> `l7_crate_3`     |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin19`                             |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin10`                             |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin9`                              |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin22`                             |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin21`                             |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin20`                             |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin8`                              |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin18`                             |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin23`                             |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin17`                             |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin16`                             |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin15`                             |
| 18           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin14`                             |
| 19           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin13`                             |
| 20           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin12`                             |
| 21           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin11`                             |
| 22           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin1`                              |
| 23           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin7`                              |
| 24           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin6`                              |
| 25           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin5`                              |
| 26           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin4`                              |
| 27           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin3`                              |
| 28           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin2`                              |
| 29           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin`                               |

## Sector 74 (l7z7.p3d)
| Object Index | Object Type                                         | Object Name  |
|--------------|-----------------------------------------------------|--------------|
| 0            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin1`  |
| 1            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin4`  |
| 2            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin2`  |
| 3            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin0`  |
| 4            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin7`  |
| 5            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin5`  |
| 6            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin3`  |
| 7            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin10` |
| 8            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin8`  |
| 9            | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin6`  |
| 10           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin13` |
| 11           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin11` |
| 12           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin9`  |
| 13           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin11`     |
| 14           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin14` |
| 15           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin12` |
| 16           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin16` |
| 17           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin17` |
| 18           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin15` |
| 19           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin19` |
| 20           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `Z7C1Coin18` |
| 21           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin8`      |
| 22           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin12`     |
| 23           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin10`     |
| 24           | [[/Pure3DFiles/ChunkTypes/Locator.md;Coin Locator]] | `coin9`      |

## Sector 75 (Level 1)
| Object Index | Object Type | Object Name      |
|--------------|-------------|------------------|
| 0            | Wasp Camera | `w_lemon`        |
| 1            | Wasp Camera | `w_schoolroof1`  |
| 2            | Wasp Camera | `w_bonuscar`     |
| 3            | Wasp Camera | `w_stonetemple`  |
| 4            | Wasp Camera | `w_trailor1`     |
| 5            | Wasp Camera | `w_trailor2`     |
| 6            | Wasp Camera | `w_cardguard`    |
| 7            | Wasp Camera | `w_bridge1`      |
| 8            | Wasp Camera | `w_bridge2`      |
| 9            | Wasp Camera | `w_barn`         |
| 10           | Wasp Camera | `w_simpsons`     |
| 11           | Wasp Camera | `w_flanders`     |
| 12           | Wasp Camera | `w_wiggum`       |
| 13           | Wasp Camera | `w_kwickemart`   |
| 14           | Wasp Camera | `w_lardlad`      |
| 15           | Wasp Camera | `w_gasroof`      |
| 16           | Wasp Camera | `w_schoolroof2`  |
| 17           | Wasp Camera | `w_playground`   |
| 18           | Wasp Camera | `w_schoolstairs` |
| 19           | Wasp Camera | `w_tower`        |

## Sector 76 (Level 2)
| Object Index | Object Type | Object Name    |
|--------------|-------------|----------------|
| 0            | Wasp Camera | `w_hospital`   |
| 1            | Wasp Camera | `w_museum`     |
| 2            | Wasp Camera | `w_krusty1`    |
| 3            | Wasp Camera | `w_carwash`    |
| 4            | Wasp Camera | `w_railstair`  |
| 5            | Wasp Camera | `w_rail2`      |
| 6            | Wasp Camera | `w_mono1`      |
| 7            | Wasp Camera | `w_popcycle`   |
| 8            | Wasp Camera | `w_fountain`   |
| 9            | Wasp Camera | `w_townhall`   |
| 10           | Wasp Camera | `w_gazebo`     |
| 11           | Wasp Camera | `w_roof`       |
| 12           | Wasp Camera | `w_legitroof`  |
| 13           | Wasp Camera | `w_legitroof2` |
| 14           | Wasp Camera | `w_moesroof`   |
| 15           | Wasp Camera | `w_rail1`      |
| 16           | Wasp Camera | `w_roundroom`  |
| 17           | Wasp Camera | `w_police`     |
| 18           | Wasp Camera | `w_mono2`      |
| 19           | Wasp Camera | `w_mono3`      |

## Sector 77 (Level 3)
| Object Index | Object Type | Object Name     |
|--------------|-------------|-----------------|
| 0            | Wasp Camera | `w_comicroof`   |
| 1            | Wasp Camera | `w_bowl`        |
| 2            | Wasp Camera | `w_lighthouse`  |
| 3            | Wasp Camera | `w_shipcrane`   |
| 4            | Wasp Camera | `w_dockcrane`   |
| 5            | Wasp Camera | `w_duff2`       |
| 6            | Wasp Camera | `w_kstage1`     |
| 7            | Wasp Camera | `w_kstage2`     |
| 8            | Wasp Camera | `w_night`       |
| 9            | Wasp Camera | `w_culvert`     |
| 10           | Wasp Camera | `w_offramp`     |
| 11           | Wasp Camera | `w_dam1`        |
| 12           | Wasp Camera | `w_hype`        |
| 13           | Wasp Camera | `w_shipstairs`  |
| 14           | Wasp Camera | `w_duff1`       |
| 15           | Wasp Camera | `w_duff3`       |
| 16           | Wasp Camera | `w_dam2`        |
| 17           | Wasp Camera | `w_observatory` |
| 18           | Wasp Camera | `w_kamp1`       |
| 19           | Wasp Camera | `w_kamp2`       |

## Sector 78 (Level 4)
| Object Index | Object Type | Object Name      |
|--------------|-------------|------------------|
| 0            | Wasp Camera | `w_kwickemart`   |
| 1            | Wasp Camera | `w_gasroof`      |
| 2            | Wasp Camera | `w_schoolroof1`  |
| 3            | Wasp Camera | `w_schoolroof2`  |
| 4            | Wasp Camera | `w_tower`        |
| 5            | Wasp Camera | `w_burns1`       |
| 6            | Wasp Camera | `w_chess1`       |
| 7            | Wasp Camera | `w_chess2`       |
| 8            | Wasp Camera | `w_trailor1`     |
| 9            | Wasp Camera | `w_trailor2`     |
| 10           | Wasp Camera | `w_simpsons`     |
| 11           | Wasp Camera | `w_flanders`     |
| 12           | Wasp Camera | `w_neighbor1`    |
| 13           | Wasp Camera | `w_wiggum`       |
| 14           | Wasp Camera | `w_wiggum2`      |
| 15           | Wasp Camera | `w_gasroof2`     |
| 16           | Wasp Camera | `w_schoolstairs` |
| 17           | Wasp Camera | `w_burns2`       |
| 18           | Wasp Camera | `static_bee2`    |
| 19           | Wasp Camera | `static_bee6`    |

## Sector 79 (Level 5)
| Object Index | Object Type | Object Name    |
|--------------|-------------|----------------|
| 0            | Wasp Camera | `w_roof`       |
| 1            | Wasp Camera | `w_hospital`   |
| 2            | Wasp Camera | `w_museum`     |
| 3            | Wasp Camera | `w_railstair`  |
| 4            | Wasp Camera | `w_rail2`      |
| 5            | Wasp Camera | `w_rail3`      |
| 6            | Wasp Camera | `w_mono1`      |
| 7            | Wasp Camera | `w_mono4`      |
| 8            | Wasp Camera | `w_needle1`    |
| 9            | Wasp Camera | `w_needle2`    |
| 10           | Wasp Camera | `w_fountain`   |
| 11           | Wasp Camera | `w_townhall`   |
| 12           | Wasp Camera | `w_gazebo`     |
| 13           | Wasp Camera | `w_legitroof`  |
| 14           | Wasp Camera | `w_legitroof2` |
| 15           | Wasp Camera | `w_moesroof`   |
| 16           | Wasp Camera | `w_rail1`      |
| 17           | Wasp Camera | `w_police`     |
| 18           | Wasp Camera | `w_mono2`      |
| 19           | Wasp Camera | `w_mono3`      |

## Sector 80 (Level 6)
| Object Index | Object Type | Object Name      |
|--------------|-------------|------------------|
| 0            | Wasp Camera | `w_comicroof`    |
| 1            | Wasp Camera | `w_bowl`         |
| 2            | Wasp Camera | `w_lighthouse`   |
| 3            | Wasp Camera | `w_dockcrane`    |
| 4            | Wasp Camera | `w_kstage1`      |
| 5            | Wasp Camera | `w_kstage2`      |
| 6            | Wasp Camera | `w_night`        |
| 7            | Wasp Camera | `w_offramp`      |
| 8            | Wasp Camera | `w_observatory1` |
| 9            | Wasp Camera | `w_observatory2` |
| 10           | Wasp Camera | `w_kamp1`        |
| 11           | Wasp Camera | `w_kamp2`        |
| 12           | Wasp Camera | `w_comicroof2`   |
| 13           | Wasp Camera | `w_hype2`        |
| 14           | Wasp Camera | `w_shipcrane`    |
| 15           | Wasp Camera | `w_shipstairs`   |
| 16           | Wasp Camera | `w_duff2`        |
| 17           | Wasp Camera | `w_duff3`        |
| 18           | Wasp Camera | `w_dam1`         |
| 19           | Wasp Camera | `w_dam2`         |

## Sector 81 (Level 7)
| Object Index | Object Type | Object Name     |
|--------------|-------------|-----------------|
| 0            | Wasp Camera | `w_lemon`       |
| 1            | Wasp Camera | `w_krustyRC`    |
| 2            | Wasp Camera | `w_lardlads`    |
| 3            | Wasp Camera | `w_playground`  |
| 4            | Wasp Camera | `w_schoolroof1` |
| 5            | Wasp Camera | `w_schoolroof2` |
| 6            | Wasp Camera | `w_schoolroof3` |
| 7            | Wasp Camera | `w_blockade`    |
| 8            | Wasp Camera | `w_barn`        |
| 9            | Wasp Camera | `w_plantlot2`   |
| 10           | Wasp Camera | `w_simpsons`    |
| 11           | Wasp Camera | `w_simpsons2`   |
| 12           | Wasp Camera | `w_flanders`    |
| 13           | Wasp Camera | `w_wiggum`      |
| 14           | Wasp Camera | `w_kwickemart`  |
| 15           | Wasp Camera | `w_gasroof`     |
| 16           | Wasp Camera | `w_bridge1`     |
| 17           | Wasp Camera | `w_plantlot`    |
| 18           | Wasp Camera | `w_trailor1`    |
| 19           | Wasp Camera | `w_trailor2`    |

# Notes
These object lists are derived from the [PersistentObjectStates](https://github.com/Hampo/SHAR-Save-Game/blob/main/SHARSaveGameEditor/SHARSaveGameEditor/Names.cs) array in the [Project:119].