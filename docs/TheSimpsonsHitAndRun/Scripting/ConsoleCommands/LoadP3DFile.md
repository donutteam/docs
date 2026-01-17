---
title: "LoadP3DFile"
description: "Loads a P3D file in a level or a mission."
authors: [ 2 ]
---

Loads a P3D file in a level or a mission.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/AnyLoad.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
LoadP3DFile( file_path, heap_name, section_name );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.LoadP3DFile( file_path, heap_name, section_name )
```
{{ endtab }}
{{ endtabs }}

* **file_path**: The path to the P3D file to load.
    * The following 6 paths are ignored since the game preloads them at startup:
        * `art\phonecamera.p3d`
        * `art\cards.p3d`
        * `art\wrench.p3d`
        * `art\missions\generic\missgen.p3d`
        * `art\cars\common.p3d`
        * `art\cars\huskA.p3d`
* **heap_name**: Set the memory allocator to use for this P3D file.
	* Supported heaps for this argument are:
		* **GMA_DEFAULT**
		* **GMA_TEMP**
		* **GMA_GC_VMM**
			* Only on GameCube.
		* **GMA_PERSISTENT**
		* **GMA_LEVEL**
		* **GMA_LEVEL_MOVIE**
		* **GMA_LEVEL_FE**
		* **GMA_LEVEL_ZONE**
		* **GMA_LEVEL_OTHER**
			* This is the only heap Radical explicitly uses with this command, for each level's FX file (`art\l01_fx.p3d`, etc.).
		* **GMA_LEVEL_HUD**
    	* **GMA_LEVEL_MISSION**
   		* **GMA_LEVEL_AUDIO**
    	* **GMA_DEBUG**
    	* **GMA_SPECIAL**
		* **GMA_XBOX_SOUND_MEMORY**
			* Only on Xbox.
	* Defaults to **GMA_LEVEL_MISSION**.
* **section_name**: TODO.

# Examples
{{ tabs }}
{{ tab MFK }}
```text
// Load the level's locators.
LoadP3DFile("art\missions\level01\level.p3d");

// Load the Level's FX file into GMA_LEVEL_OTHER
LoadP3DFile("art\l01_fx.p3d", "GMA_LEVEL_OTHER");

// Will be ignored.
LoadP3DFile("art\cars\huskA.p3d");
```
{{ endtab }}
{{ tab Lua }}
```lua
-- Load the level's locators.
Game.LoadP3DFile("art\\missions\\level01\\level.p3d")

-- Load the Level's FX file into GMA_LEVEL_OTHER
Game.LoadP3DFile("art\\l01_fx.p3d", "GMA_LEVEL_OTHER")

-- Will be ignored.
Game.LoadP3DFile("art\\cars\\huskA.p3d")
```
{{ endtab }}
{{ endtabs }}