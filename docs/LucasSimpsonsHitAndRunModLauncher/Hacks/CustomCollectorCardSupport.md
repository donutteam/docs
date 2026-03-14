---
title: "Custom Collector Card Support"
description: "This hack adds support for customizing various aspects of collector cards."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 294 # 1.27
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/MustBeRequiredByMod.md }}

This hack adds support for customizing various aspects of collector cards on a per card basis:
* The drawable shown in the world when the card has not been collected.
* The collection drawable shown right after collecting the card.
* The number of character quotes and which character icons are shown for them.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=CustomCollectorCardSupport
```

Your mod must provide a configuration file when requiring this hack.

# Configuring This Hack
To configure this hack, create a file named `CustomCollectorCardSupport.xml` and add the parameters necessary for your mod inside it.

```xml
<?xml version="1.0" encoding="utf-8"?>

<!--
	<CustomCharacters>
		<CustomCharacter>
			Name: The name of the character.
			Index: The index the name maps to.
				
	<Level>
		Index: The index of the level. 0-6.
		 OR
		Number: The number of the level. 1-7.

		<CollectorCard>
			Index: The index of the card. 0-6.
			 OR
			Number: The number of the card. 1-7.

			Drawable: The drawable to use for the card. Optional, defaults to "card_idle".
			CollectDrawable: The drawable to use when the player collects the card. Optional, defaults to "card_collect".

			<Quotes>
				This element existing will overwrite *all* base game quotes.
				Leaving it empty is valid and will simply make a card have no quotes.

				You can also declare up to 3 <Quote> elements inside a card to have up to 3 quotes spoken by whoever you like.

				<Quote>
					Name: The name of the character saying the quote. Case-insensitive.
					 OR
					Index: The index of the character saying the quote.

-->

<CustomCollectorCardSupport>
	<CustomCharacters>
		<CustomCharacter Name="Loren" Index="32" />
		<CustomCharacter Name="maz" Index="33" />
	</CustomCharacters>

    <Level Number="1">
		<!-- Custom Drawable/CollectDrawable, Default Quotes -->
        <CollectorCard Number="1" Drawable="phone_icon" CollectDrawable="bonestorm_explosion" />
		
		<!-- Custom Drawable/CollectDrawable, No Quotes -->
        <CollectorCard Number="2" Drawable="phone_icon" CollectDrawable="bonestorm_explosion">
            <Quotes />  <!-- Removes Base Game Quotes -->
         </CollectorCard>
		
		<!-- Default Drawables, No Quotes -->
        <CollectorCard Number="3">
            <Quotes />  <!-- Removes Base Game Quotes -->
         </CollectorCard>
		
		<!-- Default Drawables, Custom Quotes -->
        <CollectorCard Number="4">
            <Quotes>
				<Quote Name="Homer" />
				<Quote Name="Marge" />
				<Quote Name="Milhouse" />
			</Quotes>
         </CollectorCard>
		
		<!-- Default Drawables, Custom Quotes, Using Custom Characters -->
        <CollectorCard Number="5">
            <Quotes>
				<Quote Name="Loren" />
				<Quote Name="maz" />
			</Quotes>
         </CollectorCard>
    </Level>
</CustomCollectorCardSupport>
```

# Characters
Characters refer to [[/Pure3DFiles/ChunkTypes/FrontendMultiSprite.md]] indices found in the game's `art\frontend\scrooby\frontend.p3d` and `art\frontend\scrooby\ingame.p3d`.

## Default Characters
The game's default quote characters are mapped with friendly names by default for convenience:

| Character    | Index |
|--------------|-------|
| ANNOUNCER    | 0     |
| APU          | 1     |
| BART         | 2     |
| BROCKMAN     | 3     |
| BURNS        | 4     |
| CARL         | 5     |
| CHILD        | 6     |
| DRWOLFF      | 7     |
| DR WOLFF     | 7     |
| DR. WOLFF    | 7     |
| GIL          | 8     |
| HOMER        | 9     |
| JASPER       | 10    |
| JIMBO        | 11    |
| KANG         | 12    |
| KRUSTY       | 13    |
| LENNY        | 14    |
| LISA         | 15    |
| MAGGIE       | 16    |
| MANJULA      | 17    |
| MARGE        | 18    |
| MEYERS       | 19    |
| MILHOUSE     | 20    |
| MOTHER       | 21    |
| MRSPARKLE    | 22    |
| MR SPARKLE   | 22    |
| MR. SPARKLE  | 22    |
| OTTO         | 23    |
| PHOTOGRAPHER | 24    |
| RALPH        | 25    |
| SKINNER      | 26    |
| SMITHERS     | 27    |
| STACY        | 28    |
| WIGGUM       | 29    |
| WILLIE       | 30    |

## Custom Characters
You can also register custom characters and modify frontend files to add sprites for them.

Doing so requires adding custom sprites and including them in specific [[/Pure3DFiles/ChunkTypes/FrontendMultiSprite.md]] chunks located in `art\frontend\scrooby\frontend.p3d` and `art\frontend\scrooby\ingame.p3d`:
* `D:\Radical\Projects\Simpsons2\game\exportart\frontend\scrooby\_pc\frontend.prj` / `ingame.prj` ([[/Pure3DFiles/ChunkTypes/FrontendProject.md]]) 
	* `ViewCard.pag` ([[/Pure3DFiles/ChunkTypes/FrontendPage.md]])
		* `ViewCard` ([[/Pure3DFiles/ChunkTypes/FrontendLayer.md]])
			* `Quotes` ([[/Pure3DFiles/ChunkTypes/FrontendGroup.md]])
				* `Quote2` ([[/Pure3DFiles/ChunkTypes/FrontendGroup.md]])
					* `Quote2` ([[/Pure3DFiles/ChunkTypes/FrontendMultiSprite.md]])
				* `Quote1` ([[/Pure3DFiles/ChunkTypes/FrontendGroup.md]])
					* `Quote1` ([[/Pure3DFiles/ChunkTypes/FrontendMultiSprite.md]])
				* `Quote0` ([[/Pure3DFiles/ChunkTypes/FrontendGroup.md]])
					* `Quote0` ([[/Pure3DFiles/ChunkTypes/FrontendMultiSprite.md]])

Adding additional characters requires modifying both frontend files:
* Add a [[/Pure3DFiles/ChunkTypes/Sprite.md]] chunk inside file above the [[/Pure3DFiles/ChunkTypes/FrontendProject.md]].
* Add a [[/Pure3DFiles/ChunkTypes/FrontendImageResource.md]] chunk inside the `ViewCard.pag` [[/Pure3DFiles/ChunkTypes/FrontendPage.md]] referencing it.
* Add the name of the [[/Pure3DFiles/ChunkTypes/FrontendImageResource.md]] to the `ImageNames` list inside the `Quote2`/`Quote1`/`Quote0` [[/Pure3DFiles/ChunkTypes/FrontendMultiSprite.md]] chunks.
* Declare a `<CustomCharacter>` in a `<CustomCharacters>` element in your `CustomCollectorCardSupport.xml` that maps a friendly name to the index in the `ImageNames` lists.
	* You can also use the index directly, though you probably shouldn't.