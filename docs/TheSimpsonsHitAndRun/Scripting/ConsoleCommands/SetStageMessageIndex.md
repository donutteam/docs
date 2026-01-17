---
title: "SetStageMessageIndex"
description: "Sets the stage objective text message index to use."
authors: [ 2 ]
---

Sets the stage message index to use.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStageMessageIndex( index, [unused] );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStageMessageIndex( index, [unused] )
```
{{ endtab }}
{{ endtabs }}

* **index**: The message index to use.
	* For standard mission objective messages, valid values are 0 to 299 and these refer to the game's `MISSION_OBJECTIVE_00` through `MISSION_OBJECTIVE_299` text strings.
	* For locked stage messages, valid values are 0 to 19 and refer to the game's `INGAME_MESSAGE_00` through `INGAME_MESSAGE_19` text strings.
* **unused**: Unused parameter.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
    SetStageMessageIndex(174);

    AddObjective("dummy");
    CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
    Game.SetStageMessageIndex(174)

    Game.AddObjective("dummy")
    Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}

# Notes
To customize text strings in a mod, use the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomText.md]] hack.