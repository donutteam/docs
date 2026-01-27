---
title: "SetTalkToTarget"
description: "Sets what NPC must be talked to in a talk to objective."
authors: [ 2 ]
---

Sets what NPC must be talked to in a [[../MissionObjectives/talkto.md]] objective.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStageObjective.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetTalkToTarget( npc, [icon, icon_y_offset, trigger_radius] );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetTalkToTarget( npc, [icon, icon_y_offset, trigger_radius] )
```
{{ endtab }}
{{ endtabs }}

* **npc**: The name of the NPC that must be talked to.
* **icon**: The type of 3D icon to show above the NPC's head.
	* **0**: Show the **exclamation** icon.
	* **1**: Show the **gift** icon.
		* Note: The base game has no such composite drawable, but this will work if one is loaded by a mod.
	* **2**: Show the **interior_icon** icon.
		* Note: The base game has no such composite drawable, but this will work if one is loaded by a mod.
	* Optional, defaults to **0**.
* **icon_y_offset**: An offset for the Y position of the 3D icon.
	* Optional, defaults to **0.0**.
* **trigger_Radius**: The radius of the trigger used to actually talk to the NPC.
	* Optional, defaults to **1.3**.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("talkto");
	AddNPC("ned", "m2_ned_sd");
	SetTalkToTarget("ned", 0, 0);
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("talkto")
	Game.AddNPC("ned", "m2_ned_sd")
	Game.SetTalkToTarget("ned", 0, 0)
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}