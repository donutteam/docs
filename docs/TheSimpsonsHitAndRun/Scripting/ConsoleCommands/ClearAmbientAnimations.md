---
title: "ClearAmbientAnimations"
description: "Clears conversation animations registered to bonus missions to make room for new ones."
authors: [ 104 ]
---

Clears conversation animations registered to bonus missions to make room for new ones.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/LevelInit.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
ClearAmbientAnimations( bonus_mission_name );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.ClearAmbientAnimations( bonus_mission_name )
```
{{ endtab }}
{{ endtabs }}

* **bonus_mission_name**: The name of the bonus mission for which ambient animations are being cleared.
    * Valid arguments are `bm1`, `sr1`, `sr2`, and `sr3`.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddNPCCharacterBonusMission("milhouse", "npd", "sr1_mhouse_sd", "sr1", "checkered", "intro", 0, "checkeredfinish");
SetBonusMissionDialoguePos("sr1", "sr1_player", "sr1_mhouse_sd", "level1_carstart");

ClearAmbientAnimations(                        "sr1"); // Clear any animations stored for SR1.
// Then register new animations.
AddAmbientNpcAnimation("dialogue_no",          "sr1");
AddAmbientPcAnimation("dialogue_shaking_fist", "sr1");
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddNPCCharacterBonusMission("milhouse", "npd", "sr1_mhouse_sd", "sr1", "checkered", "intro", 0, "checkeredfinish")
Game.SetBonusMissionDialoguePos("sr1", "sr1_player", "sr1_mhouse_sd", "level1_carstart")

Game.ClearAmbientAnimations(                        "sr1") -- Clear any animations stored for SR1.
-- Then register new animations.
Game.AddAmbientNpcAnimation("dialogue_no",          "sr1")
Game.AddAmbientPcAnimation("dialogue_shaking_fist", "sr1")
```
{{ endtab }}
{{ endtabs }}