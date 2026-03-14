---
title: "IfCurrentCheckpoint"
description: "Returns whether or not the current stage is being resumed from a checkpoint."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 78 # 1.25
---

This conditional command returns whether or not the current stage is being resumed from a checkpoint.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

Additionally, **this must be called after** [[CHECKPOINT_HERE.md]] in the stage.

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
IfCurrentCheckpoint() 
{
	
}
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.IfCurrentCheckpoint()

Game.EndIf()
```
{{ endtab }}
{{ endtabs }}

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	SetStageTime(40);

	AddObjective("dummy");
	CloseObjective();
CloseStage();

AddStage();
	CHECKPOINT_HERE();
	
	!IfCurrentCheckpoint()
	{
		// Don't add any time when reaching this stage from the previous one.
		// Due to Radical programming AddStageTime() in an odd way, -1 adds no time and 0 adds one second.
		AddStageTime(-1);
	}
	
	IfCurrentCheckpoint()
	{
		// Set the time to 20 seconds when resuming from a checkpoint.
		SetStageTime(20);
	}

	AddObjective("dummy");
	CloseObjective();

	AddCondition("timeout")
	CloseCondition();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	Game.SetStageTime(40)

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()

Game.AddStage()
	Game.CHECKPOINT_HERE()
	
	Game.Not()
	Game.IfCurrentCheckpoint() -- Alternatively, you can omit the line with Game.Not() and use Game.Not_IfCurrentCheckpoint() here instead.
		-- Don't add any time when reaching this stage from the previous one.
		-- Due to Radical programming AddStageTime() in an odd way, -1 adds no time and 0 adds one second.
		Game.AddStageTime(-1)
	Game.EndIf()
	
	Game.IfCurrentCheckpoint()
	{
		-- Set the time to 20 seconds when resuming from a checkpoint.
		Game.SetStageTime(20)
	}

	Game.AddObjective("dummy")
	Game.CloseObjective()

	Game.AddCondition("timeout")
	Game.CloseCondition()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}

# Notes
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/ConditionalEvaluation.md }}