---
title: "Road (0x3000003)"
description: "Represents road data used by the navigation system and AI cars."
authors: [ 2, 6310 ]
---

A Road chunk represents road data used by the navigation system.

These are used in conjunction with [[Intersection.md]] chunks to form a road network.

# Data Structure
| Property          | Data Type | Description |
|-------------------|-----------|-------------|
| Name              | string    | TODO        |
| Type              | uint32    | TODO        |
| StartIntersection | string    | TODO        |
| EndIntersection   | string    | TODO        |
| MaximumCars       | uint32    | TODO        |
| Speed             | uint8     | TODO        |
| Intelligence      | uint8     | TODO        |
| Shortcut          | bool      | TODO        |

# Parents
No valid parents.

# Children
* [[RoadSegment.md]]