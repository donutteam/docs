---
title: "Version 4.4"
description: "Changelog for Version 4.4 of Lucas' Pure3D Editor."
authors: [ 2, 395 ]
---

**This update was released on June 9, 2020.**

# General

* Added the Ctrl+N hotkey for "File > New".
* Added the Ctrl+O hotkey for "File > Open...".
* Made the open file dialogue used for "File > Open..." default to the directory containing the currently loaded P3D file (if one is loaded).
* Made the program set its working directory to the directory containing its executable when starting it with a command line argument to open a file.
	* One such case where this change makes a difference is when opening a file associated with the program. In that case, it makes it so the program doesn't keep the folder that file is in in use.
* Fixed an issue where "Vertex Type Unknown" was not set when loading a Primitive Group (0x10020) chunk.
* Fixed an issue where changing "Number of Strings" on a Frontend Language (0x1800E) chunk to a higher number would cause a crash and to a lower number would corrupt the chunk.
* Added more name mappings for hashes found in Frontend Language (0x1800E) chunks.
	* LEFTMOUSE
	* RIGHTMOUSE
	* MIDMOUSE
	* LEFTSHOULDER
	* RIGHTSHOULDER
	* SIDELEFT
	* SIDERIGHT
* Made importing over a Sprite (0x19005) chunk preserve the Image Width and Image Height being 0 if they're already 0.
* Made it so string padding warnings related to the "Shader" value on Sprite (0x19005) and Texture Font (0x22000) chunks are now messages instead.
	* This means these no longer show a message box and get highlighted in orange, instead they'll just be highlighted in yellow with a message in the Value Editor.
* Various performance improvements.

# Editors
## Frontend Language Editor
Made this editor support editing text strings by double clicking them.

## Texture Font Editor
Added support for viewing characters that ignore the text color specified by the game. These are used for button symbols in the game Scarface: The World is Yours.

# Tools
## General
Added the following new tools for working with P3DXML files:

* Import All Fence (0x3F00007)...
	* Removes all existing Fence (0x3F00007) chunks and adds the ones from the input P3DXML to the end of the file.
* Export All Fence (0x3F00007)...
	* Exports all Fence (0x3F00007) chunks to P3DXML.
* Import All Roads...
	* Removes all existing Road (0x3000003), Road Data Segment (0x3000009) and Intersection (0x3000004) chunks and imports the ones from the input P3DXML before the `darrow` and `warrow` Anim (0x3F0000C) chunks.
	* If neither of those chunks exist, the new chunks are added to the end of the file.
* Export All Roads...
	* Exports all Road (0x3000003), Road Data Segment (0x3000009) and Intersection (0x3000004) chunks in the file to P3DXML.
* Import All Path (0x300000B)...
	* Removes all existing Path (0x300000B) chunks and adds the ones from the input P3DXML to the end of the file.
* Export All Path (0x300000B)...
	* Exports all Path (0x300000B) chunks to P3DXML.

## Offset Positions... {{ id offset-positions }}
Made this tool support the following chunk types:

* Mesh (0x10000)
* Old Primitive Group (0x10002)
* Bounding Box (0x10003)
* Bounding Sphere (0x10004)
* Position List (0x10005)

## Export Language... {{ id export-language }}

* Fixed a bug where this tool did not tell the INI writer to escape strings with hashes.
	* This was necessary as hashes are supported for comments in INI files used by CustomText in the Mod Launcher.
* Made strings beginning or ending with a `"` get escaped.

## Import Language... {{ id import-language }}
Added this new tool to import an INI file over Frontend Language (0x1800E) chunks.

## Copy Car... {{ id copy-car }}
Made this tool also copy the BV Collision Object (0x7010000) and Physics Object (0x7011000) chunks.

# P3DXML

* Made the program remember if a loaded P3DXML file was in the "Pure3DFile" or "Pure3DChunk"/"Pure3DChunks" format and preserve this when saving it.
	* This does not apply to exporting, only saving.
* Changed it so Type 5 Zone Event Locator (0x3000005) chunks with extra garbage data after the null terminator at the end of their `DynaLoadData` strings are exported with an additional `Data` attribute that contains the entire `DynaLoadData` string as well as that garbage data as Base64 instead of including it in the `Value` attribute.
	* This is because it is apparently [not valid to include null terminators in XML strings](https://www.w3.org/TR/REC-xml/#charsets) and certain parsers that respect this part of the standard (such as Python's) refused to load files containing these (such as L2_TERRA).
	* When present, the `Data` attribute is only used when importing a file if the `Value` attribute contains equivalent data.
	* This attribute is only so the editor can preserve the exact state of the chunk and it's generally not recommended that you read or write it yourself.
* Made it so "Saved with Lucas' Pure3D Editor VERSION" comments are now included at the start of exported P3DXML files.
	* We recommend other people creating tools that export these files include their own comments indicating that it was saved with their tool.
	* Please do **not** indicate your files were created with the Pure3D Editor in your own tools.
* Fixed a bug where chunks with a display name that contained 2 consective dashes (-) or ended in a dash would make exporting fail.
	* Display name comments that would have contained 2 consecutive dashes are now omitted.
	* Display name comments that would have ended in a dash now have a space appended to the end.
	* One file that was affected by this was `art\frontend\scrooby\frontend.p3d`.