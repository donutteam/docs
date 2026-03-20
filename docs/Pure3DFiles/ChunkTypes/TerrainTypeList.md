---
title: "Terrain Type List (0x300000E)"
description: "TODO"
authors: [ 6310 ]
---

TODO

# Data Structure
| Property | Data Type             | Description |
|----------|-----------------------|-------------|
| Version  | uint32                | TODO        |
| NumTypes | uint32                | TODO        |
| Types    | TerrainType[NumTypes] | TODO        |

## TerrainType
| Property | Data Type | Description                                                                  |
| -------- | --------- | ---------------------------------------------------------------------------- |
| Type     | Types     | Terrain type. Stored in bits 0–6 of the underlying byte value (`0x7F` mask). |
| Interior | bool      | Indicates interior terrain. Stored in bit 7 (`0x80`). `true` = bit set.      |

## Types
**1 byte**
| Name   | Value |
|--------|-------|
| Road   | 0     |
| Grass  | 1     |
| Sand   | 2     |
| Gravel | 3     |
| Water  | 4     |
| Wood   | 5     |
| Metal  | 6     |
| Dirt   | 7     |

# Parents
TODO

# Children
TODO
