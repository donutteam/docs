---
title: "Known Issues"
description: "Known issues in Lucas' Simpsons Hit & Run Mod Launcher and their status."
authors: [ 2, 6310 ]
---

This page documents known issues in Lucas' Simpsons Hit & Run Mod Launcher.

The known issues here are reflective of the current version of the Mod Launcher.

# Launcher
## About Window
* The ampersand is missing from the title of the program on this window.
	* **Introduced**: Version 1.27
	* **Status**: Fixed in Future Update

# Hacks
## Aspect Ratio Support
* The new Analogue Speedometer and Frame Rate Counter hacks are scaled incorrectly with certain aspect ratios.
	* **Introduced**: Version 1.27
	* **Status**: Investigating

## Cheat Keys
* The Toggle Vehicle Visibility key does not persist through changing the current camera.
	* **Introduced**: Version 1.27
	* **Status**: Investigating

## Custom Reward Quest Support
* Skin shops will sometimes show the wrong level's rewards (which are any skins besides `forsale` skins, including `defaultskin` skins).
	* What level's rewards are shown is determined by what level you were in the last time something queried the number of unlocked cars, such as opening the "Level Progress" menu.
	* **Introduced**: Version 1.27
	* **Status**: Fixed in Future Update

## Dear Imgui
* Certain elements or text, such as the chat box in the Multiplayer hack, may overflow ImGui related containers slightly in Direct3D 8.
	* **Introduced**: Version 1.27
	* **Status**: Fixed in Future Update

## Discord Rich Presence
* The game will crash on startup if you have a main mod enabled that does not have a `Title` set in its Meta.ini
	* **Introduced**: Version 1.27
	* **Status**: Fixed in Future Update

## Free Camera and No Clip
* Interacting with an InteriorEntrance Locator while in No Clip mode will result in being stuck on the loading screen.
	* **Introduced**: Version 1.27
	* **Status**: Investigating

## Multiplayer
* The game may crash when certain HUD icons are updated at the server's request.
	* **Introduced**: Version 1.27
	* **Status**: Fixed in Future Update

## No Explosion Exit Delay
* Blowing up your car by entering the UFO’s tractor beam creates a vehicle you cannot enter.
	* **Introduced**: Version 1.27
	* **Status**: Investigating
