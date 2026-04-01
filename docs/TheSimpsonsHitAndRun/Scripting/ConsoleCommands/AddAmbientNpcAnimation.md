---
title: "AddAmbientNpcAnimation"
description: "Adds a conversation animation for the NPC involved in the conversation."
authors: [ 104 ]
---

Adds a conversation animation for the NPC involved in the conversation.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/AnyInit.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
AddAmbientNpcAnimation( animation, [bonus mission name] );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddAmbientNpcAnimation( animation, [bonus mission name] )
```
{{ endtab }}
{{ endtabs }}

* **animation**: The name of the animation to play as defined in the character's .cho file.
* **bonus mission name**: The name of the bonus mission for which the animation is being registered.
    * This argument is only used for bonus missions and street races, valid arguments are `bm1`, `sr1`, `sr2`, and `sr3`.

# Examples
{{ tabs }}
{{ tab MFK }}
# Normal Mission
```js
AddStage();
	AddObjective("dialogue");
		AddAmbientNpcAnimation("dialogue_shaking_fist"); // Marge shakes her fist at Homer for some reason.
		AddAmbientPcAnimation("dialogue_hands_in_air");
		SetDialogueInfo("homer", "marge", "shake", 0);
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	Game.AddObjective("dialogue")
		Game.AddAmbientNpcAnimation("dialogue_shaking_fist") -- Marge shakes her fist at Homer for some reason.
		Game.AddAmbientPcAnimation("dialogue_hands_in_air")
		Game.SetDialogueInfo("homer", "marge", "shake", 0)
	Game.CloseObjective()
Game.CloseStage()
```

# Bonus Mission (leveli.mfk)
```js
AddNPCCharacterBonusMission("milhouse", "npd", "sr1_mhouse_sd", "sr1", "checkered", "intro", 0, "checkeredfinish");
SetBonusMissionDialoguePos("sr1", "sr1_player", "sr1_mhouse_sd", "level1_carstart");

ClearAmbientAnimations(                        "sr1"); // Radical always include this.
AddAmbientNpcAnimation("dialogue_no",          "sr1"); // Milhouse shakes his head in disapproval.
AddAmbientPcAnimation("dialogue_shaking_fist", "sr1");
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddNPCCharacterBonusMission("milhouse", "npd", "sr1_mhouse_sd", "sr1", "checkered", "intro", 0, "checkeredfinish")
Game.SetBonusMissionDialoguePos("sr1", "sr1_player", "sr1_mhouse_sd", "level1_carstart")

Game.ClearAmbientAnimations(                        "sr1") -- Radical always include this.
Game.AddAmbientNpcAnimation("dialogue_no",          "sr1") -- Milhouse shakes his head in disapproval.
Game.AddAmbientPcAnimation("dialogue_shaking_fist", "sr1")
```
{{ endtab }}
{{ endtabs }}