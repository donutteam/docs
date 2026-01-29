### General
* Made debug class names cleaner. For example ".?AVVehicle@@" will now show up as "class Vehicle".
* Added a `-debugtextmode` command line argument. This can be used to launch the game with a specific debug mode enabled.
* Added a `-noscaledebugtext` command line argument. This disables the debug text being scaled according to the size of the window.
* Made the debug text scale down to fit the screen.
    * Also added a `-nofitdebugtext` command line argument to disable this.
* Made it so pages that are not built in are grouped by what Mod/Hack added them.
    * Grouped pages can be cycled by holding Shift+T/Shift+R.
    * Also added a `-nodebugtextgroups` command line argument to disable this.
* Made the "traffic" and "road segments" pages show intersections as blue spheres in the world as well as their names.
* Removed the "root tree node and animated icons" page and moved its contents to the "tree" and "miscellaneous" pages respectively.

### "miscellaneous" Page
* Added "Action buttons" to show the amount of action buttons that exist out of the maximum.
* Added "Playing sound clip players" and "Playing sound stream players" which show the current amounts out of the maximums.

### "cars" Page
* Added "Parked car count" to show how many parked cars currently exist.
* Moved the listed traffic cars to the "traffic" page.

### "mission" Page
* Now shows "Time" in stages with a timer. This is shown in milliseconds.
* Now shows the current time and duration on "timer" objectives in milliseconds.

### "traffic" Page
* Added "Count" to show the amount of traffic cars currently in existence out of the maximum.
* Added "In-car limit" to show what the in-car limit is currently set to.
* Added "Group" to show what traffic group is currently in use.
* Added a list of all models in the current traffic group with the current amount of each one out of their maximum.
* Added a list of all current traffic cars and whether or not they're active (in the world).

### "music" Page
Fixed a crash when viewing this page when the current region had multiple layers in it.

### "paths" Page
* Made this page only show the models of the current ped group and not show an "x" after each count.
* Made this page show characters and which ones are in use.