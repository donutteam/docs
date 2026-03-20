---
title: "Texture (0x19000)"
description: "Represents a texture that can be referenced by a Shader."
authors: [ 2, 6310 ]
---

A Texture chunk represents a texture that can be referenced by a [[Shader.md]].

# Data Structure
| Property    | Data Type    | Description |
|-------------|--------------|-------------|
| Name        | string       | TODO        |
| Version     | uint32       | TODO        |
| Width       | uint32       | TODO        |
| Height      | uint32       | TODO        |
| Bpp         | uint32       | TODO        |
| AlphaDepth  | uint32       | TODO        |
| NumMipMaps  | uint32       | TODO        |
| TextureType | TextureTypes | TODO        |
| UsageHint   | UsageHints   | TODO        |
| Priority    | uint32       | TODO        |

## TextureTypes
**4 bytes**
| Name         | Value |
|--------------|-------|
| RGB          | 0     |
| Palettized   | 1     |
| Luminance    | 2     |
| BumpMap      | 3     |
| DXT1         | 4     |
| DXT2         | 5     |
| DXT3         | 6     |
| DXT4         | 7     |
| DXT5         | 8     |
| IPU          | 9     |
| Z            | 10    |
| Linear       | 11    |
| RenderTarget | 12    |
| PS2_4Bit     | 13    |
| PS2_8Bit     | 14    |
| PS2_16Bit    | 15    |
| PS2_32Bit    | 16    |
| GC_4Bit      | 17    |
| GC_8Bit      | 18    |
| GC_16Bit     | 19    |
| GC_32Bit     | 20    |
| GC_DXT1      | 21    |

## UsageHints
**4 bytes**
| Name    | Value |
|---------|-------|
| Static  | 0     |
| Dynamic | 1     |
| NoCache | 2     |

# Parents
TODO

# Children
* [[Image.md]]