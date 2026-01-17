---
title: "SuppressDriver"
description: "Prevents a character from appearing as the driver of the player's vehicles in a level."
authors: [ 2 ]
---

Prevents a character from appearing as the driver of the player's vehicles in a level

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/LevelLoad.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SuppressDriver( character );
```
{{ endtab }}
{{ tab Lua }}
```js
Game.SuppressDriver( character )
```
{{ endtab }}
{{ endtabs }}

* **character**: The name of the character who will be unavailable as a driver in the level.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
// Used in Level 1 to prevent Homer appearing in his cars since he's the player character
SuppressDriver("homer");
```
{{ endtab }}
{{ tab Lua }}
```lua
-- Used in Level 1 to prevent Homer appearing in his cars since he's the player character
Game.SuppressDriver("homer")
```
{{ endtab }}
{{ endtabs }}

# Notes
There is a limit of 32 suppressed drivers in a level.