---
title: "Old Primitive Group (0x10002)"
description: "TODO"
authors: [ 6310 ]
---

TODO

# Data Structure
| Property      | Data Type      | Description |
|---------------|----------------|-------------|
| Version       | uint32         | TODO        |
| ShaderName    | string         | TODO        |
| PrimitiveType | PrimitiveTypes | TODO        |
| VertexType    | VertexTypes    | TODO        |
| NumVertices   | uint32         | TODO        |
| NumIndices    | uint32         | TODO        |
| NumMatrices   | uint32         | TODO        |

## PrimitiveTypes
**4 bytes**
| Name          | Value |
|---------------|-------|
| TriangleList  | 0     |
| TriangleStrip | 1     |
| LineList      | 2     |
| LineStrip     | 3     |
| Points        | 4     |

## VertexTypes
**4 bytes**
| Name             | Value   |
|------------------|---------|
| None             | 0       |
| UVs              | 1       |
| UVs2             | 2       |
| UVs3             | 3       |
| UVs4             | 4       |
| UVs5             | 5       |
| UVs6             | 6       |
| UVs7             | 7       |
| UVs8             | 8       |
| Normals          | 1 << 4  |
| Colours          | 1 << 5  |
| Specular         | 1 << 6  |
| Matrices         | 1 << 7  |
| Weights          | 1 << 8  |
| Size             | 1 << 9  |
| W                | 1 << 10 |
| Binormal         | 1 << 11 |
| Tangent          | 1 << 12 |
| Position         | 1 << 13 |
| Colours2         | 1 << 14 |
| ColourCount1     | 1 << 15 |
| ColourCount2     | 2 << 15 |
| ColourCount3     | 3 << 15 |
| ColourCount4     | 4 << 15 |
| ColourCount5     | 5 << 15 |
| ColourCount6     | 6 << 15 |
| ColourCount7     | 7 << 15 |
| ColourMaskOffset | 15      |

# Parents
TODO

# Children
TODO
