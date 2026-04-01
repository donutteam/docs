---
title: "Dialog"
description: "Shows a Windows dialog box with a customisable icon and buttons."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 294 # 1.27
---

Shows a Windows dialog box with a customisable icon and buttons.

# Syntax
```lua
Dialog( icon, buttons, message, [title] )
```

## Arguments
* **icon** (integer): The icon to use.
	* For convenience, constants for all valid icons are provided in the [[../LuaTables/DialogIcon.md]] table.
* **buttons** (integer): The buttons to show.
	* For convenience, constants for all valid buttons are provided in the [[../LuaTables/DialogButtons.md]] table.
* **message** (string): The message to show.
* **title** (string): The dialog title.

## Return Values
* (integer): The result.
	* For convenience, constants for all valid results are provided in the [[../LuaTables/DialogResult.md]] table.

# Examples
```lua
local Result = Dialog(
	DialogIcon.Error,
	DialogButtons.OKClose,
	"Press OK to continue or Close to close the game."
) 
if Result == DialogResult.Close then
	os.exit()
end
```
