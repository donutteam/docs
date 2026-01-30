---
title: "CloseObjective"
description: "Closes an objective in a stage in a mission."
authors: [ 2 ]
---

Closes an objective in a stage in a mission.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("dummy");
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("dummy")
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}