---
title: "Refraction Shader Support"
description: "This hack reimplements the refract PDDI shader."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 397 # 1.23.4
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/MustBeRequiredByAMod.md }}

This hack reimplements the `refract` PDDI shader.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=RefractionShaderSupport
```

# Known Issues
While this hack is currently able to be required by mods, there are some issues with doing so when using the shader on multiple entities (like multiple cars or characters). This is due to the game only capturing the screen once the first time something with a `refract` shader is rendered on the frame.

The [[HoverCarRefraction.md]] hack uses this hack but has its own explicit support for multiple *Hover Cars* existing.

# Command Line Arguments
This hack is affected by certain [[../CommandLineArguments.md]] for the Mod Launcher.

# Version History
## Version 1.26
{{ snippet lucasmodlauncher/versions/1.26/hack_refraction-shader-support }}