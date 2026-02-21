---
title: "Version 1.1.3"
description: "Changelog for Version 1.1.3 of Lucas' Pure3D Editor Model XML Format Blender Add-on."
---

**This version was released on February 28, 2020.**

* Fixed an issue where exporting an object with an empty material slot would fail.
* Fixed an issue where importing a model with a Shader element that had no Name attribute would fail.
	* This addon could not create models like this without the previous change.
* Added support for the following versions of Blender:
	* 2.63
	* 2.64
	* 2.65
	* 2.66
	* 2.67
	* 2.68
	* 2.69
	* 2.70
	* 2.71
	* 2.72
	* 2.73
	* 2.80
	* 2.81
	* 2.82
	* Blender versions lower than 2.74 cannot import normals. Blender will generate normals instead, which happens anyways when editing models in any version.
* Changed the target version of the add-on to Blender 2.80. 
	* This change is required for Blender 2.80 or newer to load the add-on.
	* This will cause older versions of Blender to show [a warning](/img/lucaspure3deditor/blender-target-version-warning.png) about this when first enabled but the addon will still work properly in those versions.
* Added the "Use Modifiers Render Settings" tickbox when exporting. This is disabled by default.
	* Also renamed the "Apply modifiers (preview resolution)" tickbox to "Apply modifiers".
	* This change is copied from [a change in Blender's OBJ exporter](https://github.com/blender/blender-addons/commit/a746a84f8aaf3a4843eb3f4ce3f5a0464872077a) in Blender 2.79.
	* This setting is not available in Blender 2.80 or newer as this feature was [removed in Blender 2.80](https://github.com/blender/blender-addons/commit/0abe5a6a37d0014d5881f34543fa84f0bd0f66cc).
* Made it so transformations are applied after triangulating faces when exporting instead of before.
	* This change is copied from [a change in Blender's OBJ exporter](https://github.com/blender/blender-addons/commit/ce7685695e9aedc2852289f772c8400674fd1025#diff-bb9105e4533d56a13c4a7c8e580233b7) in Blender 2.79.
* Made it so normals get inverted on meshes with negative scaling.
	* This change is copied from [a change in Blender's OBJ exporter](https://github.com/blender/blender-addons/commit/473d074b34b66d6f674bb2f06153533c9b636fd1) in Blender 2.79.
* Greatly improved the speed of exporting.