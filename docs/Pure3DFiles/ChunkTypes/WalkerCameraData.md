---
title: "Walker Camera Data (0x3000101)"
description: "TODO"
authors: [ 2, 6310 ]
---

Contains a list of parameters for a Walker Camera.

Due to support for dynamic data being scrapped during development, The Simpsons: Hit and Run only uses cameras with an Index 9.

During vanilla gameplay, only the MaxMagnitude and Elevation values are respected, however you can make all values load with the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/WalkerCameraDataSupport.md]] hack.

# Data Structure
| Property     | Data Type | Description              |
|--------------|-----------|--------------------------|
| Index        | uint32    | The index of the camera. |
| MinMagnitude | float     | TODO                     |
| MaxMagnitude | float     | TODO                     |
| Elevation    | float     | TODO                     |
| TargetOffset | Vector3   | TODO                     |

# Parents
No valid parents.

# Children
No valid children.