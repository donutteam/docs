---
title: "Custom Shop Support"
description: "This hack allows mods to specify custom NPCs for car shops."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 379 # 1.18
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/MustBeRequiredByMod.md }}

This hack allows mods to specify custom NPCs for car shops.
   
It also allows mods to include and exclude specific cars and skins at specific phone booths and skin shops respectively.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=CustomShopSupport
```

Your mod must provide a configuration file when requiring this hack.

# Configuring This Hack
To configure this hack, create a file named `CustomShopSupport.xml` and add the parameters necessary for your mod inside it.

{{ tabs }}
{{ tab Current Features }}
```xml
<?xml version="1.0" encoding="utf-8"?>
<CustomShopSupport>
	<!--
	
	<CarShop>
		Level: The level the charshop is in.
		Character: The name of the character that runs the shop (including the "reward_" prefix).
		Conversation: The name of the conversation to use when talking to the character. Leave blank to disable the conversation.
	<PhoneBooth>
		Drawable: Change the drawable that displays above the phonebooth. Optional.
		<Selector>
			Level: The level to use this phonebooth on.
			Locator: The Type 9 SummonVehiclePhone locator to use this phonebooth on.
		<FreeItems>
			<Car>
				[Contents]: Specify the name of the car.
				Path: The path to the car. Defaults to "art\cars\CARNAME.p3d".
				RepairCost: The cost to repair this car.
		<ExcludedItems>
			<Car>
				[Contents]: Specify the name of the car.
		<IncludedItems>
			<Car>
				[Contents]: Specify the name of the car.
				RepairCost: The cost to repair this car.
	<SkinShop>
		Drawable: Change the drawable that represents this shop. Optional.
		<Selector>
			Level: The level to use this SkinShop on.
			Locator: The Type 9 PurchaseSkin locator to use this SkinShop on.
		<FreeItems>
			<Skin>
				[Contents]: Specify the name of the character.
				Path: The path to the character. Defaults to "art\chars\CHARNAME.p3d".
		<ExcludedItems>
			<Skin>
				[Contents]: Specify the name of the character.
		<IncludedItems>
			<Skin>
				[Contents]: Specify the name of the character.
		
	-->

	<!-- Default Car Shops -->
	<CarShop Level="1" Conversation="plowking" Character="reward_barney" />
	<CarShop Level="2" Conversation="son" Character="reward_homer" />
	<CarShop Level="3" Conversation="bus" Character="reward_otto" />
	<CarShop Level="4" Conversation="tractor" Character="reward_tractor" />
	<CarShop Level="5" Conversation="borrowing" Character="reward_homer" />
	<CarShop Level="6" Conversation="swine" Character="reward_kearney" />
	<CarShop Level="7" Conversation="" Character="zombie" />
	
	<!-- Custom Phone Booth Examples -->
	<PhoneBooth>
		<!-- Use this Phonebooth in Level 1 and Level 7 -->
		<Selector Level="1" />
		<Selector Level="7" />
		
		<!--  Make it so Homer can't use Apu's car -->
		<ExcludedItems>
			<Car>apu_v</Car>
		</ExcludedItems>
	</PhoneBooth>
	
	<PhoneBooth Drawable="wrench"> 
		<!-- Use this PhoneBooth in Level 1 on the locator named "Z1p1" -->
		<Selector Level="1" Locator="Z1p1"/>
		
		<!-- Specify an empty IncludedItems to exclude all Reward Cars -->
		<IncludedItems />
		
		<FreeItems>
			<!-- And then here we add a couple cars to the phonebooth -->
			<Car>bart_v</Car>
			<Car>homer_v</Car>
		</FreeItems>
	</PhoneBooth>
	
	<!-- Custom Skin Shop Examples -->
	<SkinShop Drawable="dice">
		<Selector Level="1" Locator="z1_skin2"/>
		
		<FreeItems>
			<Skin>h_fat</Skin>
			<Skin>h_scuzzy</Skin>
		</FreeItems>
	</SkinShop>
	
	<SkinShop Drawable="wrench">
		<Selector Level="1" Locator="z1_skin3"/>
		
		<FreeItems>
			<Skin>h_stcrobe</Skin>
			<Skin>h_undrwr</Skin>
		</FreeItems>
	</SkinShop>
</CustomShopSupport>
```
{{ endtab }}
{{ tab Deprecated Features }}
These properties have been superseded by new properties in other sections. They are still supported for backwards compatibility but we don't recommend mods targetting newer versions use these.

```xml
<?xml version="1.0" encoding="utf-8"?>
<CustomShopSupport>
	<!--
	
	<PhoneBooth>
		<Blacklist> (Use <ExcludedItems> instead)
		<Whitelist> (Use <IncludedItems> instead)
		
	<SkinShop>
		<Blacklist> (Use <ExcludedItems> instead)
		<Whitelist> (Use <IncludedItems> instead)
		
	-->
</CustomShopSupport>
```
{{ endtab }}
{{ endtabs }}

# Version History
## Version 1.25
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.25/Hacks/CustomShopSupport.md }}

## Version 1.22
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22/Hacks/CustomShopSupport.md }}

## Version 1.18.2
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18.2/Hacks/CustomShopSupport.md }}