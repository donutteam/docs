---
title: "Custom Terra Files"
description: "This hack allowed you to define custom paths for each level's Terra file."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 341 # 1.2 (not technically *quite* accurate)
removedVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 347 # 1.5
  superseded_by: null
---

This hack allowed you to define custom paths for each level's Terra file.

# Requiring This Hack
This hack was required by adding this line to your mod's Meta.ini:

```ini
RequiredHack=CustomTerraFiles
```

Your mod had to have provided a configuration file when requiring this hack.

# Configuring This Hack
This hack was configured by creating a file named `CustomTerraFiles.ini` and then adding the parameters necessary for your mod inside it.

```ini
; [Miscellaneous]
    ; INDEX: Set the Terra file path for the specific level index.

[Miscellaneous]
; Normal Game Levels
0=ART\\L1_TERRA.P3D
1=ART\\L2_TERRA.P3D
2=ART\\L3_TERRA.p3d
3=ART\\L4_TERRA.P3D
4=ART\\L5_TERRA.P3D
5=ART\\L6_TERRA.P3D
6=ART\\L7_TERRA.P3D

; Unused
7=ART\\B00.P3D

; Bonus Game Maps
8=ART\\B01.P3D
9=ART\\B02.P3D
10=ART\\B03.P3D
11=ART\\B04.P3D
12=ART\\B05.P3D
13=ART\\B06.P3D
14=ART\\B07.P3D

; Unused 2: Electric Boogaloo
15=ART\\L1_INTER.P3D
16=ART\\L2_INTER.P3D
17=ART\\L3_INTER.p3d
18=ART\\L4_INTER.P3D
19=ART\\L5_INTER.P3D
20=ART\\L6_INTER.P3D
21=ART\\L7_INTER.P3D
22=
23=
24=
25=
26=
27=
28=
29=
30=everground.p3d
```