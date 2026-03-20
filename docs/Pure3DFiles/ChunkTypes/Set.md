---
title: "Set (0x3000110)"
description: "Represents a set of Texture chunks, one of which is selected at random at load time."
authors: [ 2, 6310 ]
---

A Set chunk represents a set of [[Texture.md]] chunks, one of which is selected at random at load time.

When a set is loaded, one of the [[Texture.md]] chunks within is selected at random.

These can be referenced by [[Shader.md]] chunks in the same manner as [[Texture.md]] chunks.

# Data Structure
| Property    | Data Type | Description |
|-------------|-----------|-------------|
| Name        | string    | TODO        |
| Version     | uint32    | TODO        |
| NumTextures | uint8     | TODO        |

# Parents
TODO

# Children
* [[Texture.md]]