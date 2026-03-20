---
title: "Wall (0x3000000)"
description: "Represents vertical, infinitely tall, one-sided collision."
authors: [ 2, 6310 ]
---

A Wall chunk represents vertical, infinitely tall, one-sided collision.

These are typically placed facing inwards towards the playable area to keep the player within the bounds of the map.

# Data Structure
| Property | Data Type | Description                |
|----------|-----------|----------------------------|
| Start    | Vector3   | The wall's start position. |
| End      | Vector3   | The wall's end position.   |
| Normal   | Vector3   | The wall's normal.         |

The **Normal** determines which side of the wall is collidable and can be calculated from the **Start** and **End**.

# Parents
* [[Fence.md]]

# Children
No valid children.