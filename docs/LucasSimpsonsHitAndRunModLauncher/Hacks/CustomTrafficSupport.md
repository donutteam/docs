---
title: "Custom Traffic Support"
description: "This hack that allows you to have dynamic traffic groups, more than 5 traffic cars, custom traffic colors and more."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 388 # 1.22
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/MustBeRequiredByMod.md }}

This hack that allows you to have dynamic traffic groups, more than 5 traffic cars, custom traffic colors and more.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=CustomTrafficSupport
```

Your mod must provide a configuration file when requiring this hack.

# Configuring This Hack
To configure this hack, create a file named `CustomTrafficSupport.xml` and add the parameters necessary for your mod inside it.

```xml
<?xml version="1.0" encoding="utf-8"?>
<CustomTrafficSupport>
	<!--
		
	<DynamicTraffic>
		Type: Set the type of dynamic traffic to use. Defaults to "None".
			None: Dynamic groups are not enabled.
			Models: Dynamic Models means that when the game goes to use a slot, the hack changes the model in the slot if necessary.
			Slots: Dynamic Slots means that the hack picks a random model and gives the game a slot to use. This is required for Weights to work and is generally better but slightly more advanced.
	
	<PreallocatedCars>
		Amount: Set the amount of traffic cars that are created during level load. Defaults to the total amount of AllocatedCars. Any additional cars will be created when they're first needed.
			When using the "Models" DynamicTraffic type, it is probably optimal to set this to "0".
			When using the "Slots" DynamicTraffic type, this is currently ignored altogether and no cars are Preallocated.

	<AllocatedCars>
		Amount: Set the amount of allocated traffic cars. Defaults to 5.
			This limit is also the maximum amount of parked cars that can exist in the level.
		
	<MaxTraffic>
		Amount: Set the default amount of traffic cars that will spawn on the roads. This is then controlled with SetMaxTraffic in mission scripts. Defaults to 5.
		
	<MaxTrafficOnFoot>
		Amount: Set the amount of traffic cars that will spawn when the player is not in their car. Defaults to 5.
		
	<RoadTrafficLimitMultiplier>
		Amount: The amount to multiply the car limit on Roads in P3D files by. Defaults to 1.
		
	<RoadLaneMaxTrafficLimit>
		Amount: Set the maximum amount of cars allow in any lane of any road. Defaults to 2.
			"Road" chunks in the P3D file define a "Maximum Cars" value.
			That number is then multiplied by the RoadTrafficLimitMultiplier if one is defined.
			And then this is finally divided by the number of lanes the "Road" chunk has.
			If the number obtained by that math is greater than this limit, it will be capped.
		
	<RemoveInterval>
		Value: The amount of time the game waits to remove cars outside
		
	<AddInterval>
		Value: The amount of time between attempts to spawn a traffic car.
		
	<PopulationDuration>
		Value: TODO
		
	<FadeDistance> 
		Value: Set the distance from the camera at which traffic starts fading out. Defaults to 85.0.
		
	<CentreOffset>
		Value: Set the distance in front the camera that's considered the centre of the radius where they don't spawn traffic. Defaults to 40.0.
	
	<AddDistance>
		Value: Set the distance from the CentreOffset required to spawn a car. Defaults to 65.0.
	
	<RemoveDistance>
		Value: Set the distance from the CentreOffset required to delete a car. Defaults to 75.0.
	
	<PopulateAddDistance>
		Value: TODO
		
	<DecelerationSpeed>
		Value: TODO
		
	<AccelerationSpeed>
		Value: TODO
		
	<DecelerationBrakeThreshold>
		Value: TODO
	
	<Colours>
		Inherit: Set whether or not this element inherits from other defined Colours.
			Inheritence flows like this:
				Car specific colours in Level > Colours in Level > Colours in root > Base game
				Car specific colours in Root > Colours in root > Base game
			Inheritence stops at the level that stops inheriting.
		<Colour>
			Red: Define the red value of the colour.
			Green: The green value of the colour.
			Blue: The blue value of the colour.
		
	<Group>
		Index: The index of the traffic group.
		Multiplier: The amount to multiply the car counts specified in the traffic group by.
		<Car>
			Name: The name of the car.
			Weight: Set a weight for how likely this car is to spawn over other cars.
				This defaults to the amount of this car allowed in the traffic group.
				For each instance that already exists, the weighting is reduced to give other cars a better chance at spawning.
	
	<Car>
		Name: The name of the car.
		
		This element can contain Colours elements to define them for a specific car.
	
	<Level>
		Index: The index of the level. 0-6.
		 OR
		Number: The number of the level. 1-7.
		
		This element can contain all other elements to make them level specific.
		
	-->

	<DynamicTraffic Type="Slots" />
	
	<PreallocatedCars Amount="5" />
	
	<AllocatedCars Amount="5" />
	
	<MaxTraffic Amount="5" />
	<MaxTrafficOnFoot Amount="5" />
	
	<RoadTrafficLimitMultiplier Value="1.0" />
	<RoadLaneMaxTrafficLimit Amount="2" />
	
	<RemoveInterval Value="200" />
	<AddInterval Value="200" />
	<PopulationDuration Value="200" />
	
	<FadeDistance Value="85.0" />
	<CentreOffset Value="40.0" />
	<AddDistance Value="65.0" />
	<RemoveDistance Value="75.0" />
	<PopulateAddDistance Value="100.0" />
	
	<DecelerationSpeed Value="-10.0" />
	<AccelerationSpeed Value="3.5" />
	<DecelerationBrakeThreshold Value="1.0" />
	
	<Colours Inherit="false">
		<!-- Defaults from the base game as an example -->
		<!-- Inheritence is disabled in this example for that reason -->
		<Colour Red="148" Green="45" Blue="12" />
		<Colour Red="133" Green="124" Blue="4" />
		<Colour Red="110" Green="84" Blue="145" />
		<Colour Red="170" Green="43" Blue="74" />
		<Colour Red="48" Green="11" Blue="102" />
		<Colour Red="110" Green="30" Blue="32" />
		<Colour Red="140" Green="125" Blue="207" />
		<Colour Red="195" Green="98" Blue="31" />
		<Colour Red="122" Green="50" Blue="69" />
		<Colour Red="148" Green="191" Blue="229" />
		<Colour Red="0" Green="159" Blue="123" />
		<Colour Red="0" Green="75" Blue="132" />
		<Colour Red="43" Green="177" Blue="166" />
		<Colour Red="250" Green="166" Blue="23" />
		<Colour Red="172" Green="81" Blue="127" />
		<Colour Red="185" Green="162" Blue="232" />
		<Colour Red="229" Green="222" Blue="33" />
		<Colour Red="163" Green="203" Blue="60" />
		<Colour Red="213" Green="142" Blue="210" />
		<Colour Red="255" Green="239" Blue="158" />
		<Colour Red="122" Green="43" Blue="103" />
		<Colour Red="181" Green="133" Blue="70" />
		<Colour Red="68" Green="106" Blue="171" />
		<Colour Red="59" Green="149" Blue="36" />
		<Colour Red="205" Green="94" Blue="0" />
	</Colours>

	<Level Number="1">	
		<AllocatedCars Amount="25" />
		
		<MaxTraffic Amount="25" />
		<MaxTrafficOnFoot Amount="25" />
		
		<RoadTrafficLimitMultiplier Value="5" />
		<RoadLaneMaxTrafficLimit Amount="25" />
		
		<Colours Inherit="true">
			 <Colour Red="255" Green="155" Blue="155" />
			 <Colour Red="155" Green="255" Blue="155" />
			 <Colour Red="155" Green="155" Blue="255" />
		</Colours>
		
		<Car Name="minivanA">
			<Colours Inherit="false">
				 <Colour Red="0" Green="255" Blue="0" />
				 <Colour Red="0" Green="0" Blue="255" />
			</Colours>
		</Car>
	</Level>
</CustomTrafficSupport>
```

# Version History
## Version 1.23.5
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.5/Hacks/CustomTrafficSupport.md }}