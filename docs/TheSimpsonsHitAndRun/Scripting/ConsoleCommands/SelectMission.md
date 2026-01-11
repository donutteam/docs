---
title: "SelectMission"
description: "Sets what mission is about to be initialised."
authors: [ 2 ]
---

This command sets what mission is about to be initialised.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/ConsoleCommands/Scopes/MissionInit.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SelectMission( mission );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SelectMission( mission )
```
{{ endtab }}
{{ endtabs }}

* **mission**: The ID of the mission that's about to be initialised.

# Examples
{{ Snippet:TheSimpsonsHitAndRun/ConsoleCommands/Examples/MinimalMission.md }}