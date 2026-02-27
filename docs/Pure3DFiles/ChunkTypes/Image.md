---
title: "Image (0x19001)"
description: "Represents metadata for an image within a Sprite chunk or a Texture chunk."
authors: [ 2, 6310 ]
---

An Image chunk represents metadata for an image within a [[Sprite.md]] chunk or a [[Texture.md]] chunk.

# Data Structure
| Property   | Data Type | Description |
|------------|-----------|-------------|
| Name       | string    | TODO        |
| Version    | uint32    | TODO        |
| Width      | uint32    | TODO        |
| Height     | uint32    | TODO        |
| Bpp        | uint32    | TODO        |
| Palettized | bool      | TODO        |
| HasAlpha   | bool      | TODO        |
| Format     | Formats   | TODO        |

## Formats
**4 bytes**
| Name     | Value |
|----------|-------|
| Raw      | 0     |
| PNG      | 1     |
| TGA      | 2     |
| BMP      | 3     |
| IPU      | 4     |
| DXT      | 5     |
| DXT1     | 6     |
| DXT2     | 7     |
| DXT3     | 8     |
| DXT4     | 9     |
| DXT5     | 10    |
| PS24Bit  | 11    |
| PS28Bit  | 12    |
| PS216Bit | 13    |
| PS232Bit | 14    |
| GC4Bit   | 15    |
| GC8Bit   | 16    |
| GC16Bit  | 17    |
| GC32Bit  | 18    |
| GCDXT1   | 19    |
| Other    | 20    |
| Invalid  | 21    |
| PSP4Bit  | 25    |

# Parents
* [[Sprite.md]]
* [[Texture.md]]

# Children
* [[ImageData.md]]