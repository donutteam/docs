---
title: "Confirm"
description: "Shows a Windows message box with an OK button and a Cancel button for debugging purposes."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 354 # 1.7
---

Shows a Windows message box with an **OK** button and a **Cancel** button for debugging purposes.

This returns true if **OK** was pressed and false if **Cancel** was pressed.

# Syntax
```lua
Confirm( message )
```

## Arguments
* **message** (string): The message to show in message box.

## Return Values
* (boolean): Whether the user clicked **OK**.

# Examples
```lua
local Result = Confirm("Something, something, skulls on Barts car.") 

if Result then
	-- User clicked OK
else
	-- User clicked Cancel
end
```