---
title: "hitandrunlost"
description: "This type of objective requires the player to lose their Hit & Run to pass the stage."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 379 # 1.18
---

This type of objective requires the player to lose their Hit & Run to pass the stage.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("hitandrunlost");

CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("hitandrunlost")

Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}

# Notes
This objective type is only completed if the player loses their Hit & Run *without* getting caught.

# Version History
## Version 1.18.1
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22.3/Hacks/AdditionalScriptFunctionality/MissionObjectives/hitandrunlost.md }}