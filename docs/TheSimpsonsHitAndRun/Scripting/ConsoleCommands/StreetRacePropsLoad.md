---
title: "StreetRacePropsLoad"
description: "Executes a dyna load data string when a mission begins."
authors: [ 2 ]
---

Executes a [[/TheSimpsonsHitAndRun/DynaLoadData.md]] string when a mission begins.

This will also cause pedestrians and parked cars to be disabled when the mission begins. [[StreetRacePropsUnload.md]] must also be called for these to be re-enabled when the mission ends.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitInner.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
StreetRacePropsLoad( dyna_load_data );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.StreetRacePropsLoad( dyna_load_data )
```
{{ endtab }}
{{ endtabs }}

* **dyna_load_data**: [[/TheSimpsonsHitAndRun/DynaLoadData.md]] string to execute.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
StreetRacePropsLoad("l1m7door.p3d;");
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.StreetRacePropsLoad("l1m7door.p3d;")
```
{{ endtab }}
{{ endtabs }}

# Notes
While not technically required, it is recommended to call [[StreetRacePropsUnload.md]] to re-enable pedestrians and parked cars when the mission ends or they **will remain disabled**.

You can also use the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/AdditionalScriptFunctionality/ConsoleCommands/SetPedsEnabled.md]] and/or [[/LucasSimpsonsHitAndRunModLauncher/Hacks/AdditionalScriptFunctionality/ConsoleCommands/SetParkedCarsEnabled.md]] commands provided by the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/AdditionalScriptFunctionality/Intro.md]] hack to enable them throughout the mission, but this will not cause them to remain enabled after the mission ends.