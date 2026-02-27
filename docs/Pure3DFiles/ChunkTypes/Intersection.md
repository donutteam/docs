---
title: "Intersection (0x3000004)"
description: "Represents an intersection joining multiple roads together."
authors: [ 2, 6310 ]
---

An Intersection chunk represents an intersection joining multiple roads together.

These are used in conjunction with [[Road.md]] chunks to form a road network.

# Data Structure
| Property         | Data Type         | Description |
|------------------|-------------------|-------------|
| Name             | string            | TODO        |
| Position         | Vector3           | TODO        |
| Radius           | float             | TODO        |
| TrafficBehaviour | TrafficBehaviours | TODO        |

## TrafficBehaviours
**4 bytes**
| Name   | Value |
|--------|-------|
| NoStop | 0     |
| NWay   | 1     |

# Parents
No valid parents.

# Children
No valid children.