---
title: Path Handler Scripts
description: "This page documents what path handler scripts are and how to use them."
authors: [ 2 ]
---

Path Handler scripts are defined in the `CustomFiles.ini` configuration file.

These scripts get executed when the file or files (when using wildcards) are requested to load by the game.

These scripts can either redirect the file to a different path altogether or create a new file on the fly using the [[LuaFunctions/Output.md]] or [[LuaFunctions/UseCallbacks.md]]. This has a number of applications including but not limited to dynamically creating mission scripts with random elements or elements based on mod settings.

# Example
This is an example PathHandler definition and the script for it from Donut Mod 4.

```ini
[PathHandlers]
art\\frontend\\scrooby\\resource\\pure3d\\homer.p3d=Resources/scripts/handlers/mainmenuskins.lua
```

When `homer.p3d` is requested, the script redirects it to one of the files in the `MainMenuSkins` at random.

```lua
-- Table of main menu skin paths.
MainMenuSkins =
{
	GetModPath() .. "/Resources/art/mainmenuskins/h_work.p3d",
	GetModPath() .. "/Resources/art/mainmenuskins/h_pieman.p3d",
	GetModPath() .. "/Resources/art/mainmenuskins/h_sshield.p3d",
}

-- Redirect to one of them at random.
Redirect(MainMenuSkins[math.random(1, #MainMenuSkins)])
```