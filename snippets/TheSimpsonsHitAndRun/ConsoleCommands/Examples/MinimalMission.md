{{ tabs }}
{{ tab MFK }}
```js
// This is the bare minimum required for a mission to function
SelectMission("m1");
	SetMissionResetPlayerOutCar("level1_homer_start", "level1_carstart");
	SetDynaLoadData("l1z1.p3d;l1r1.p3d;l1r7.p3d;");

	AddStage();
		AddObjective("dummy");

		CloseObjective();
	CloseStage();
CloseMission();
```
{{ endtab }}
{{ tab Lua }}
```lua
-- This is the bare minimum required for a mission to function
Game.SelectMission("m1");
	Game.SetMissionResetPlayerOutCar("level1_homer_start", "level1_carstart")
	Game.SetDynaLoadData("l1z1.p3d;l1r1.p3d;l1r7.p3d;")

	Game.AddStage()
		Game.AddObjective("dummy")

		Game.CloseObjective()
	Game.CloseStage()
Game.CloseMission()
```
{{ endtab }}
{{ endtabs }}