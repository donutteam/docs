---
title: "Override Shader Parameters"
description: "This hack allows mods to override shader parameter values globally or for specific shaders."
authors: [ 2 ]
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/MustBeRequiredByMod.md }}

This hack allows mods to override shader parameter values globally or for specific shaders.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=OverrideShaderParameters
```

Your mod must provide a configuration file when requiring this hack.

# Configuring This Hack
To configure this hack, create a file named `OverrideShaderParameters.xml` and add the parameters necessary for your mod inside it.

```xml
<?xml version="1.0" encoding="utf-8"?>
<OverrideShaderParameters>
	<!--
	<Shader>
		Name: The name of the shader want to override.
			Optional. Not specifying a name will apply the overrides to every shader.
			This name can use * and ? wildcards. * matches any amount of characters, ? matches a specific amount.

		<Parameter>
			Name: The name of the parameter to override.

			(For Shader Colour Parameters):
				Value: A hex representation of a color.
				  (OR)
				Red: The red value. 0 to 255.
				Green: The green value. 0 to 255.
				Blue: The blue value. 0 to 255.
				Alpha: The alpha value.
					Optional. Defaults to 255.

			(For Shader Float Parameters):
				Value: A floating point number.

			(For Shader Integer Parameters):
				Value: An integer value, "false" for 0 or "true" for 1.

			(For Shader Texture Parameters):
				Value: The name of a texture.

			(For ALl Parameters):
				Value (or Red/Green/Blue/Alpha) are optional. Not specifying indicates to use the value from the P3D file(s).
	-->
	
	<!--
		<Shader> Element with no "Name" attribute
		This overrides the specified parameters for EVERY shader
	-->
	<Shader>
		<!-- No value specified so use whatever the shaders say instead of forcing it -->
		<Parameter Name="2SID" />
	</Shader>
	
	<Shader Name="shadername1">
		<!-- Force 2SID off regardless of what the shader specifies -->
		<Parameter Name="2SID" Value="false"/>
	</Shader>
	
	<Shader Name="shadername2">
		<!-- Force 2SID on regardless of what the shader specifies -->
		<Parameter Name="2SID" Value="true"/>
	</Shader>
	
	<Shader Name="famil_v*">
		<!-- Apply a red diffuse color to most of the shaders of the Family Sedan -->
		<Parameter Name="DIFF" Value="0xFFFF0000" />
	</Shader>
	
	<Shader Name="marge_v*">
		<!-- Apply a blue diffuse color to most of the shaders of the Canyonero -->
		<Parameter Name="DIFF" Red="0" Green="0" Blue="255" Alpha="255" />
	</Shader>
</OverrideShaderParameters>
```

# Version History
## Version 1.23.4
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.4/OverrideShaderParameters.md }}

## Version 1.20.2
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.20.2/OverrideShaderParameters.md }}

## Version 1.20.1
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.20.1/OverrideShaderParameters.md }}