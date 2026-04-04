---
title: "AddAmbientPcAnimation"
description: "Adds a conversation animation for the player character involved in the conversation."
authors: [ 104 ]
---

Adds a conversation animation for the player character involved in the conversation.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/AnyInit.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
AddAmbientPcAnimation( animation, [bonus_mission_name] );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddAmbientPcAnimation( animation, [bonus_mission_name] )
```
{{ endtab }}
{{ endtabs }}

* **animation**: The name of the animation to play as defined in the character's .cho file.
* **bonus_mission_name**: The name of the bonus mission for which the animation is being registered.
    * This argument is only used for bonus missions and street races, valid arguments are `bm1`, `sr1`, `sr2`, and `sr3`.

# Examples
# Normal Mission
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	AddObjective("dialogue");
		AddAmbientNpcAnimation("dialogue_shaking_fist");
		AddAmbientPcAnimation("dialogue_hands_in_air"); // Homer throws his hands in the air in defeat, not knowing why Marge is shaking her fist at him.
		SetDialogueInfo("homer", "marge", "shake", 0);
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	Game.AddObjective("dialogue")
		Game.AddAmbientNpcAnimation("dialogue_shaking_fist")
		Game.AddAmbientPcAnimation("dialogue_hands_in_air") -- Homer throws his hands in the air in defeat, not knowing why Marge is shaking her fist at him.
		Game.SetDialogueInfo("homer", "marge", "shake", 0)
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}

# Bonus Mission (leveli.mfk)
{{ tabs }}
{{ tab MFK }}
```js
AddNPCCharacterBonusMission("milhouse", "npd", "sr1_mhouse_sd", "sr1", "checkered", "intro", 0, "checkeredfinish");
SetBonusMissionDialoguePos("sr1", "sr1_player", "sr1_mhouse_sd", "level1_carstart");

ClearAmbientAnimations(                        "sr1"); // Radical always include this.
AddAmbientNpcAnimation("dialogue_no",          "sr1");
AddAmbientPcAnimation("dialogue_shaking_fist", "sr1"); // Homer shakes his fist at Milhouse, continuing the cycle of aggression begun by Marge.
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddNPCCharacterBonusMission("milhouse", "npd", "sr1_mhouse_sd", "sr1", "checkered", "intro", 0, "checkeredfinish")
Game.SetBonusMissionDialoguePos("sr1", "sr1_player", "sr1_mhouse_sd", "level1_carstart")

Game.ClearAmbientAnimations(                        "sr1") -- Radical always include this.
Game.AddAmbientNpcAnimation("dialogue_no",          "sr1")
Game.AddAmbientPcAnimation("dialogue_shaking_fist", "sr1") -- Homer shakes his fist at Milhouse, continuing the cycle of aggression begun by Marge.
```
{{ endtab }}
{{ endtabs }}