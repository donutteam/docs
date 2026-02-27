---
title: "Image Data (0x19002)"
description: "Represents raw image data."
authors: [ 2, 6310 ]
---

An Image Data chunk represents raw image data.

Metadata about the image is stored within the parent [[Image.md]] chunk.

# Data Structure
| Property  | Data Type        | Description |
|-----------|------------------|-------------|
| ImageSize | uint32           | TODO        |
| ImageData | uint8[ImageSize] | TODO        |

# Parents
* [[Image.md]]

# Children
No valid children.