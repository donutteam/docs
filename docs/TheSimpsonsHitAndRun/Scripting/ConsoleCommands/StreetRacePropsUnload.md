---
title: "StreetRacePropsUnload"
description: "Executes a dyna load data string when a mission ends."
authors: [ 2, 8276 ]
---

Executes a [[/TheSimpsonsHitAndRun/DynaLoadData.md]] string when a mission ends.

This will also cause pedestrians and parked cars to be re-enabled when the mission ends.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitInner.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
StreetRacePropsUnload( dyna_load_data );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.StreetRacePropsUnload( dyna_load_data )
```
{{ endtab }}
{{ endtabs }}

* **dyna_load_data**: [[/TheSimpsonsHitAndRun/DynaLoadData.md]] string to execute.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
StreetRacePropsUnload("l1m7door.p3d:");
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.StreetRacePropsUnload("l1m7door.p3d:")
```
{{ endtab }}
{{ endtabs }}
