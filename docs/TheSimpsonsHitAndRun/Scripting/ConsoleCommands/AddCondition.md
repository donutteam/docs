---
title: "AddCondition"
description: "Adds a condition for failing to a mission stage."
authors: [ 2 ]
---

Adds a condition for failing to a mission stage.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
AddCondition( condition_type, [keepbarrel_fail_stage_count] );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddCondition( condition_type, [keepbarrel_fail_stage_count] )
```
{{ endtab }}
{{ endtabs }}

* **type**: The type of condition to add.
* **keepbarrel_fail_stage_count**: The number of stages to go back when failing a [[../MissionConditions/keepbarrel.md]] condition.

# Examples
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Examples/TimeoutCondition.md }}

# Notes
No additional notes.