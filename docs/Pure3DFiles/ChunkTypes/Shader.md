---
title: "Shader (0x11000)"
description: "Represents a material for a drawable."
authors: [ 2, 6310 ]
---

A Shader chunk represents a material for a drawable, such as a [[Mesh.md]].

# Data Structure
| Property        | Data Type    | Description |
|-----------------|--------------|-------------|
| Version         | uint32       | TODO        |
| PddiShaderName  | string       | TODO        |
| HasTranslucency | bool         | TODO        |
| VertexNeeds     | VertexMasks  | TODO        |
| VertexMask      | ~VertexMasks | TODO        |
| NumParams       | uint32       | TODO        |
| Name            | string       | TODO        |

## VertexMasks
| Name         | Value   |
|--------------|---------|
| None         | 0       |
| UVs          | 1       |
| UVs2         | 2       |
| UVs3         | 3       |
| UVs4         | 4       |
| UVs5         | 5       |
| UVs6         | 6       |
| UVs7         | 7       |
| UVs8         | 8       |
| Normals      | 1 << 4  |
| Colours      | 1 << 5  |
| Specular     | 1 << 6  |
| Matrices     | 1 << 7  |
| Weights      | 1 << 8  |
| Size         | 1 << 9  |
| W            | 1 << 10 |
| BiNormal     | 1 << 11 |
| Tangent      | 1 << 12 |
| Position     | 1 << 13 |
| Colours2     | 1 << 14 |
| ColourCount1 | 1 << 15 |
| ColourCount2 | 2 << 15 |
| ColourCount3 | 3 << 15 |
| ColourCount4 | 4 << 15 |
| ColourCount5 | 5 << 15 |
| ColourCount6 | 6 << 15 |
| ColourCount7 | 7 << 15 |

# Parents
TODO

# Children
* [[ShaderColourParameter.md]]
* [[ShaderFloatParameter.md]]
* [[ShaderIntegerParameter.md]]
* [[ShaderTextureParameter.md]]