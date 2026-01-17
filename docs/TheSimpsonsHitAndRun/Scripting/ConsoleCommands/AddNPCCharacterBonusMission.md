---
title: "AddNPCCharacterBonusMission"
description: "Adds a bonus mission NPC character to a level."
authors: [ 2, 104 ]
---

Adds a bonus mission NPC character to a level

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/LevelInit.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
AddNPCCharacterBonusMission( character, skeleton, locator, bonus_mission, drawable, conversation, no_replay, [completed_drawable] );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddNPCCharacterBonusMission( character, skeleton, locator, bonus_mission, drawable, conversation, no_replay, [completed_drawable] )
```
{{ endtab }}
{{ endtabs }}

* **character**: The internal name of the character hosting the mission.
	* See [[/TheSimpsonsHitAndRun/Characters.md]] for the list of available characters in the base game.
* **skeleton**: The skeleton and animation set that character will use.
* **locator**: The name of a [[/Pure3DFiles/ChunkTypes/Locator.md|CarStart Locator]] that the character will spawn on.
* **bonus_mission**: The internal name of bonus mission that the character is hosting.
* **drawable**: The name of the drawable floating above the character's head when their mission has not been completed yet.
* **conversation**: The name of the dialogue conversation that will be used when talking to the character.
	* When the **mission** is "gr1", there is no conversation.
* **no_replay**: Disallows replaying the mission until the level is fully reloaded.
* **completed_drawable**: The name of the drawable floating above the character's head when their mission has been completed.
    * Optional, defaults to **drawable**.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
// Street Race NPCs
// Replayable, "checkeredfinish" drawable when completed
AddNPCCharacterBonusMission("milhouse", "npd", "sr1_mhouse_sd", "sr1", "checkered", "intro", 0, "checkeredfinish");
AddNPCCharacterBonusMission("nelson", "npd", "sr2_nelson_sd", "sr2", "checkered", "intro", 0, "checkeredfinish");
AddNPCCharacterBonusMission("ralph", "npd", "sr3_ralph_sd", "sr3", "checkered", "intro", 0, "checkeredfinish");

// Wager Race NPC
// Replayable, no completed drawable (see Notes)
AddNPCCharacterBonusMission("louie", "npd", "sr4_louie_sd", "gr1", "dice", "intro", 0);

// Bonus Mission NPC
// Not replayable, "exclamation_shadow" drawable when completed
AddNPCCharacterBonusMission("cletus", "npd", "bm1_cletus_sd", "bm1", "exclamation", "jug", 1, "exclamation_shadow");
```
{{ endtab }}
{{ tab Lua }}
```lua
-- Street Race NPCs
-- Replayable, "checkeredfinish" drawable when completed
Game.AddNPCCharacterBonusMission("milhouse", "npd", "sr1_mhouse_sd", "sr1", "checkered", "intro", 0, "checkeredfinish")
Game.AddNPCCharacterBonusMission("nelson", "npd", "sr2_nelson_sd", "sr2", "checkered", "intro", 0, "checkeredfinish")
Game.AddNPCCharacterBonusMission("ralph", "npd", "sr3_ralph_sd", "sr3", "checkered", "intro", 0, "checkeredfinish")

-- Wager Race NPC
-- Replayable, no completed drawable (see Notes)
Game.AddNPCCharacterBonusMission("louie", "npd", "sr4_louie_sd", "gr1", "dice", "intro", 0)

-- Bonus Mission NPC
-- Not replayable, "exclamation_shadow" drawable when completed
Game.AddNPCCharacterBonusMission("cletus", "npd", "bm1_cletus_sd", "bm1", "exclamation", "jug", 1, "exclamation_shadow")
```
{{ endtab }}
{{ endtabs }}

# Notes
There are various nuances to these arguments depending on the value of **bonus_mission**.

When it is set to `sr1` or `sr2`, a mod will need to use the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomBonusMissionSupport.md]] hack to change the **character** from `milhouse` or `nelson` respectively.

When it is set to `bm1` and the bonus mission has already been completed, the character will be removed from the world when a vehicle they drive is summoned at a phone booth. They will also no longer spawn on level load. A Mod can use the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/ReplayableBonusMissions.md]] to prevent this behaviour.

When it is set to `gr1`, there will be no conversation regardless of what **conversation** is set to. Additionally, the **completed_drawable** will not be used.