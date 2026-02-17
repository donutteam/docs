---
title: "Custom Reward Quest Support"
description: "This hack expands base game reward quest types, adds several new ones and more."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 294 # 1.27
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/MustBeRequiredByMod.md }}

This hack expands base game reward quest types, adds several new ones and more.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=CustomRewardQuestSupport
```

# Base Game Quest Types
## General
This hack reimplements all base game quest types to support multiple rewards per quest type, such as having multiple default cars/skins or multiple street race rewards. 

Additionally, all quest types (except `defaultcar`) can now be used with `skin` rewards, enabling many new ways to unlock skins.

## cards
The `cards` quest type exists in the base game, but does not function properly. With this hack, you can use it to bind a reward to collecting all cards in a level and it will actually unlock immediately upon doing so.

Here is an example of using the `cards` quest type:
{{ tabs }}
{{ tab MFK }}
```js
// Unlock the Electaurus upon collecting all of Level 1's cards
BindReward("elect_v", "art\cars\elect_v.p3d", "car", "cards", 1);
```
{{ endtab }}
{{ tab Lua }}
```lua
-- Unlock the Electaurus upon collecting all of Level 1's cards
Game.BindReward("elect_v", "art\\cars\\elect_v.p3d", "car", "cards", 1)
```
{{ endtab }}
{{ endtabs }}

Additionally, you can also now bind a reward to a specific card in a level by specifying the card number after the level number:
{{ tabs }}
{{ tab MFK }}
```js
// Unlock the Electaurus upon collecting Level 1's third card
BindReward("elect_v", "art\cars\elect_v.p3d", "car", "cards", 1, 3);
```
{{ endtab }}
{{ tab Lua }}
```lua
-- Unlock the Electaurus upon collecting Level 1's third card
Game.BindReward("elect_v", "art\\cars\\elect_v.p3d", "car", "cards", 1, 3);
```
{{ endtab }}
{{ endtabs }}

## streetrace
With this hack, the `streetrace` quest type can take an extra parameter to bind a reward to a specific street race.

Here is an example:
{{ tabs }}
{{ tab MFK }}
```js
// Unlock the Electaurus upon completing Level 1's second street race
BindReward("elect_v", "art\cars\elect_v.p3d", "car", "streetrace", 1, 2);
```
{{ endtab }}
{{ tab Lua }}
```lua
-- Unlock the Electaurus upon completing Level 1's second street race
Game.BindReward("elect_v", "art\\cars\\elect_v.p3d", "car", "streetrace", 1, 2)
```
{{ endtab }}
{{ endtabs }}

# Additional Quest Types
## wasps
Unlocks a reward when a player destroys all wasps in a level.
{{ tabs }}
{{ tab MFK }}
```js
// Unlock the Electaurus upon destroying all wasps in Level 1
BindReward("elect_v", "art\cars\elect_v.p3d", "car", "wasps", 1);
```
{{ endtab }}
{{ tab Lua }}
```lua
-- Unlock the Electaurus upon destroying all wasps in Level 1
Game.BindReward("elect_v", "art\\cars\\elect_v.p3d", "car", "wasps", 1)
```
{{ endtab }}
{{ endtabs }}

## gags
Unlocks a reward when a player completes all gags in a level.
{{ tabs }}
{{ tab MFK }}
```js
// Unlock the Electaurus upon completing all gags in Level 1
BindReward("elect_v", "art\cars\elect_v.p3d", "car", "gags", 1);
```
{{ endtab }}
{{ tab Lua }}
```lua
-- Unlock the Electaurus upon completing all gags in Level 1
Game.BindReward("elect_v", "art\\cars\\elect_v.p3d", "car", "gags", 1)
```
{{ endtab }}
{{ endtabs }}

## mission
Unlocks a reward when a player completes either a specific story mission or ALL story missions in a level.
{{ tabs }}
{{ tab MFK }}
```js
// Unlock the WWII Car upon completing Level 7 Mission 1
BindReward("gramp_v", "art\cars\gramp_v.p3d", "car", "mission", 7, 1);

// Unlock the WWII Rocket Car upon completing ALL story missions in Level 7
BindReward("gramR_v", "art\cars\gramR_v.p3d", "car", "mission", 7);
```
{{ endtab }}
{{ tab Lua }}
```lua
-- Unlock the WWII Car upon completing Level 7 Mission 1
Game.BindReward("gramp_v", "art\\cars\\gramp_v.p3d", "car", "mission", 7, 1);

-- Unlock the WWII Rocket Car upon completing ALL story missions in Level 7
Game.BindReward("gramR_v", "art\\cars\\gramR_v.p3d", "car", "mission", 7);
```
{{ endtab }}
{{ endtabs }}

## wager
Unlocks a reward when a player completes a wager race, optionally requiring a specific time to beat.
{{ tabs }}
{{ tab MFK }}
```js
// Unlock the Red Ferrini for beating Level 6's Wager Race
BindReward("bart_v", "art\cars\bart_v.p3d", "car", "wager", 6);

// Unlock the Black Ferrini for beating Level 6's Wager Race in less than 2 minutes
//	(This only works if the mission is actually a gamble race)
BindReward("cBlbart", "art\cars\cBlbart.p3d", "car", "wager", 6, 120);
```
{{ endtab }}
{{ tab Lua }}
```lua
-- Unlock the Red Ferrini for beating Level 6's Wager Race
Game.BindReward("bart_v", "art\\cars\\bart_v.p3d", "car", "wager", 6)

-- Unlock the Black Ferrini for beating Level 6's Wager Race in less than 2 minutes
--	(This only works if the mission is actually a gamble race)
Game.BindReward("cBlbart", "art\\cars\\cBlbart.p3d", "car", "wager", 6, 120)
```
{{ endtab }}
{{ endtabs }}

## coins
Unlocks a reward when a player has the specified amount of coins or greater.
{{ tabs }}
{{ tab MFK }}
```js
// Unlock the 70s Sports Car but only when the player is filthy rich in Level 1
BindReward("homer_v", "art\cars\homer_v.p3d", "car", "coins", 1, 9999);
```
{{ endtab }}
{{ tab Lua }}
```lua
-- Unlock the 70s Sports Car but only when the player is filthy rich in Level 1
Game.BindReward("homer_v", "art\\cars\\homer_v.p3d", "car", "coins", 1, 9999)
```
{{ endtab }}
{{ endtabs }}

The reward will **become locked again** if the player falls below this amount of coins. If you want the reward to stay unlocked, use the [maxcoins](#maxcoins) quest instead.

## hitandrun
Unlocks a reward when a player triggers the specified amount of Hit & Runs in a level.
{{ tabs }}
{{ tab MFK }}
```js
// Unlock the 70s Sports Car if the player pisses off the police 10 times in Level 1
BindReward("homer_v", "art\cars\homer_v.p3d", "car", "hitandrun", 1, 10);
```
{{ endtab }}
{{ tab Lua }}
```lua
-- Unlock the 70s Sports Car if the player pisses off the police 10 times in Level 1
Game.BindReward("homer_v", "art\\cars\\homer_v.p3d", "car", "hitandrun", 1, 10)
```
{{ endtab }}
{{ endtabs }}

## evaded
Unlocks a reward when a player successfully evades the specified number of Hit & Runs a level.
{{ tabs }}
{{ tab MFK }}
```js
// Unlock the 70s Sports Car if the player successfully avoids the police 10 times in Level 1
BindReward("homer_v", "art\cars\homer_v.p3d", "car", "evaded", 1, 10);
```
{{ endtab }}
{{ tab Lua }}
```lua
-- Unlock the 70s Sports Car if the player successfully avoids the police 10 times in Level 1
Game.BindReward("homer_v", "art\\cars\\homer_v.p3d", "car", "evaded", 1, 10)
```
{{ endtab }}
{{ endtabs }}

## busted
Unlocks a reward when a player gets busted during a Hit & Run the specified number of times in a level.
{{ tabs }}
{{ tab MFK }}
```js
// Unlock the 70s Sports Car if the player gets caught by the police 10 times in Level 1
BindReward("homer_v", "art\cars\homer_v.p3d", "car", "busted", 1, 10);
```
{{ endtab }}
{{ tab Lua }}
```lua
-- Unlock the 70s Sports Car if the player gets caught by the police 10 times in Level 1
Game.BindReward("homer_v", "art\\cars\\homer_v.p3d", "car", "busted", 1, 10)
```
{{ endtab }}
{{ endtabs }}

## getin
Unlocks a reward when the player enters the specified car (case-sensitive).
{{ tabs }}
{{ tab MFK }}
```js
// Unlock the Speed Rocket upon getting into it in Level 1
BindReward("rocke_v", "art\cars\rocke_v.p3d", "car", "getin", 1, "rocke_v");

// Unlock the Duff Truck for getting in the Traffic School Bus in Level 1
//	(random example to show it doesn't have to be the *same* car)
BindReward("cDuff", "art\cars\cDuff.p3d", "car", "getin", 1, "schoolbu");
```
{{ endtab }}
{{ tab Lua }}
```lua
-- Unlock the Speed Rocket upon getting into it in Level 1
Game.BindReward("rocke_v", "art\\cars\\rocke_v.p3d", "car", "getin", 1, "rocke_v")

-- Unlock the Duff Truck for getting in the Traffic School Bus in Level 1
--	(random example to show it doesn't have to be the *same* car)
Game.BindReward("cDuff", "art\\cars\\cDuff.p3d", "car", "getin", 1, "schoolbu")
```
{{ endtab }}
{{ endtabs }}

## doorbell
Unlocks a reward for pressing a doorbell with the given character (case-sensitive).
{{ tabs }}
{{ tab MFK }}
```js
// Unlock the Speed Rocket upon bothering Quimby in Level 1
BindReward("rocke_v", "art\cars\rocke_v.p3d", "car", "doorbell", 1, "quimby");
```
{{ endtab }}
{{ tab Lua }}
```lua
-- Unlock the Speed Rocket upon bothering Quimby in Level 1
Game.BindReward("rocke_v", "art\\cars\\rocke_v.p3d", "car", "doorbell", 1, "quimby")
```
{{ endtab }}
{{ endtabs }}

The character name for a doorbell is defined in the `ObjectName` field of an [[/Pure3DFiles/ChunkTypes/Locator.md|Action Locator]], prefixed with `DB_`. For example, the base game's `art\l1z4.p3d` contains such a locator with an `ObjectName` of `DB_quimby`, which is used in the above example.

## maxcoins
Unlocks a reward when a player reaches the specified amount of coins or greater.
{{ tabs }}
{{ tab MFK }}
```js
// Unlock the 70s Sports Car if the player is filthy rich at some point in Level 1
BindReward("homer_v", "art\cars\homer_v.p3d", "car", "maxcoins", 1, 9999);
```
{{ endtab }}
{{ tab Lua }}
```lua
-- Unlock the 70s Sports Car if the player is filthy rich at some point in Level 1
Game.BindReward("homer_v", "art\\cars\\homer_v.p3d", "car", "maxcoins", 1, 9999)
```
{{ endtab }}
{{ endtabs }}

The reward will **remain unlocked** if the player falls below this amount of coins. If you want the reward to become locked again if the player falls below the amount of coins, use the [coins](#coins) quest instead.

# Phonebooth Messages
This hack enables mods to show how to unlock a `car` reward in the phone booth.

To use this functionality, a mod must make manual changes to `art\frontend\ingame.p3d`.

Inside the [[/Pure3DFiles/ChunkTypes/FrontendProject.md]], navigate to:
* `Phonebooth.pag` ([[/Pure3DFiles/ChunkTypes/FrontendPage.md]])
	* `Foreground` ([[/Pure3DFiles/ChunkTypes/FrontendLayer.md]])
		* `Locked` ([[/Pure3DFiles/ChunkTypes/FrontendGroup.md]])

And, inside the `Locked` group, add a new [[/Pure3DFiles/ChunkTypes/FrontendMultiText.md]] named `CompleteQuest`. This chunk controls the position, justification, color and more of the text and how you set this up is up to you.

Then, inside the `Complete` quest multi text, add a new [[/Pure3DFiles/ChunkTypes/FrontendStringTextBible.md]] with the string identifier `COMPLETE_QUEST`.

In [[/LucasPure3DEditor/Intro.md]], your P3D file should look something like this:

![phonebooth message frontend changes in Lucas' Pure3D Editor 4](/img/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomRewardQuestSupport/PhoneboothMessage.png)

This message can then be customized by also requiring the [[CustomText.md]] hack and declaring one of the following strings:

* `COMPLETE_QUEST_` followed by the reward's name.
	* For example, the message shown on `elect_v` would be `COMPLETE_QUEST_ELECT_V`.
* `COMPLETE_QUEST_` followed by the quest type.
	* For example, the message shown on a car locked by a `cards` quest would be `COMPLETE_QUEST_CARDS`.
* `COMPLETE_QUEST`

If no string is found, the hack will fallback to showing "Complete quest".

# Skin Shop Messages
This hack enables mods to show how to unlock a `skin` reward in a skin shop.

Unlike phonebooth messages, this leverages existing frontend chunks in `art\frontend\ingame.p3d` so no modifications are needed.

The relevant frontend chunks are two [[/Pure3DFiles/ChunkTypes/FrontendMultiText.md]] chunks located inside the [[/Pure3DFiles/ChunkTypes/FrontendProject.md]]:
* `Rewards.pag` ([[/Pure3DFiles/ChunkTypes/FrontendPage.md]])
	* `Foreground` ([[/Pure3DFiles/ChunkTypes/FrontendLayer.md]])
		* `Locked` ([[/Pure3DFiles/ChunkTypes/FrontendGroup.md]])
			* `ToPurchase` ([[/Pure3DFiles/ChunkTypes/FrontendMultiText.md]])
			* `Price` ([[/Pure3DFiles/ChunkTypes/FrontendMultiText.md]])

The messages can then be customized by also requiring the [[CustomText.md]] hack and declaring one of the following strings to be shown in the `Price` [[/Pure3DFiles/ChunkTypes/FrontendMultiText.md]]:

* `COMPLETE_QUEST_` followed by the reward's name.
	* For example, the message shown on `elect_v` would be `COMPLETE_QUEST_ELECT_V`.
* `COMPLETE_QUEST_` followed by the quest type.
	* For example, the message shown on a car locked by a `cards` quest would be `COMPLETE_QUEST_CARDS`.
* `COMPLETE_QUEST`

If no string is found, the hack will fallback to showing "Complete quest".

You can also declare a `TO_UNLOCK` string to customize the text shown in the `ToPurchase` [[/Pure3DFiles/ChunkTypes/FrontendMultiText.md]]. If no string is found, the hack will fallback to showing "to unlock".

# Unlock Messages
Upon unlocking a reward, this hack will trigger a popup message similar to the one shown when completing all level gags or destroying all wasps in the base game.

This message can be customized by also requiring the [[CustomText.md]] hack and declaring one of the following strings:

* `QUEST_COMPLETE_` followed by the reward's name.
	* For example, unlocking `elect_v` would lookup `QUEST_COMPLETE_ELECT_V`.
* `QUEST_COMPLETE_` followed by the quest type.
	* For example, completing a `cards` quest would lookup `QUEST_COMPLETE_CARDS`.
* `QUEST_COMPLETE`

If no string is found, the hack will fallback to showing "QUEST COMPLETE!".

For rewards unlocked via the `gags` or `wasps` quest types, this message will take precedence over the message the game usually shows.

# Notes
If you're making a mod that adds additional rewards, you will most likely also want to use the [[CustomStatsTotals.md]] hack to adjust stats totals and potentially also the [[IncreasedRewardLimits.md]] hack if your added rewards exceed the base game's limitations.