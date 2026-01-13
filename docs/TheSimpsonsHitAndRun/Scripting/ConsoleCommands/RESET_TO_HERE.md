---
title: "RESET_TO_HERE"
description: "Tells the game to start at the stage this command is called in when selecting the mission or restarting it."
authors: [ 2 ]
---

Tells the game to start at the stage this command is called in when selecting the mission or restarting it.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
RESET_TO_HERE();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.RESET_TO_HERE()
```
{{ endtab }}
{{ endtabs }}

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
    RESET_TO_HERE();

    AddObjective("dummy");
    CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
    Game.RESET_TO_HERE()

    Game.AddObjective("dummy")
    Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}