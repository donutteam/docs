---
title: "Version 4.5"
description: "Changelog for Version 4.5 of Lucas' Pure3D Editor."
authors: [ 2, 395 ]
---

**This update was released on December 20th, 2020.**

# General

* Improved memory management.
* Made the Pure3D Editor support .NET 4.0 and use it if it's available.
	* .NET 4.0 is installed by default on Windows 8 and newer.
	* .NET 3.5 is installed by default on Windows 7.
	* This means the Pure3D Editor should no longer require a version of .NET that isn't installed by default on Windows 7 or newer.
	* Windows XP and Windows Vista users can install .NET 3.5 *or* .NET 4.0 to run the Pure3D Editor.
	* Windows 7 users can optionally install .NET 4.0.
	* You can delete "Lucas Pure3D Editor 4.exe.config" out of the folder to opt out of this change.
* Made the Pure3D Editor support running in Mono within Wine on Linux.
* Made the Pure3D Editor show a message and refuse to start if it's not running in a Windows environment (such as Mono on Linux but *not* within Wine).
* Made the Pure3D editor run as 64-bit on 64-bit Windows.
	* 32-bit Windows is still supported.
* Fixed an issue where Vertex Type Unknown on Old Primitive Group chunks had the wrong value by default (false) when importing.
* Fixed an issue with integer text boxes and negative signs on some locales.
* Fixed an issue with integer up/downs and decimal separators on some locales.
* Fixed an issue with numeric text boxes and decimal separators and negative signs on some locales.

# Editors
## General

* Added a refresh button to all editors when using the experimental Edit In New Window feature.
* Fixed an issue where Go To buttons on resource pickers with empty resources were not disabled when first opening the program.
	* This caused a crash if you were to click one in this circumstance.

## Car Camera Data Editor

* Made this editor support the experimental Edit In New Window feature.
* Renamed this editor to "Follow Camera Data Editor" when not using legacy names.

# Tools
## General

* Made the Find References tool support finding references to shaders in Old Sprite Emitter chunks.
* Added the ability to create Trigger Volume chunks from Edit and right click menus.
* Added a Wrap Around tickbox to the Find tool.

## Import All Static Entity Models XML... {{ id import-all-static-entity-models-xml }}
Added this new tool.

## Convert To Shop Preview {{ id convert-to-shop-preview }}

* Added a confirmation message to this tool.
* Fixed an issue where not all parts of the program were aware that the PDDI shader value on Shader chunks changed after using this tool.

## Make Wireframe {{ id make-wireframe }}

* Renamed this tool to "Convert to Wireframe".
* Added a confirmation message to this tool.
* Fixed an issue where not all parts of the program were aware that Index List chunks changed after using this tool.

# P3DXML

* Made it so all the Import All P3DXML tools handle errors in P3DXML files.
* Fixed an issue where you could not import or export Road Rage Grid chunks or files containing them.
* Made it so chunks no longer get automatically expanded when importing P3DXML files.
