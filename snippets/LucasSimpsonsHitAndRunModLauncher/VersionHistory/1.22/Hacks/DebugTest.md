### General
* Made it only check if the "H" key is down once each frame instead of once for every possible collision.
* Made it only check if the "H" key is down when the game window is focused.
* Made the vehicle controller used when possessing vehicles with the 8 key only get the key states once each frame.
    * Did you know about this feature? We didn't.
* Made possessing vehicles with the 8 key still use their old controller when not accelerating or steering, not switch them to in-car physics until accelerating or steering and take traffic cars off rails when not accelerating or steering.
    * No seriously, Lucas found out he did this recently. I wonder what other secrets there are...
    * Loren should really document Debug Test sometime.

### Graphics Page
* Added "Software Vertex Processing".
* Added "Flip > X", "Flip > Y", "Flip > Z" and "Flip > Cull Mode" to flip the viewport in wacky ways.

### Vehicles Page
* Added "Air Vent Force". Now your car can soar like a candy wrapper in an updraft.
    * This suppresses the new "Vehicles > No Air Vent Audio" feature of Bug Fixes if the force is not 0.
* Added "Override Maximum Traffic".
* Added "No Load Properties" to disable the game loading CON files.
    * Also added "Set Up Vehicle Handling" and "Create Driver" to make the game do some initialization stuff it would've done if it loaded the CON file.
* Removed the limit of 5 on "Vehicles > Road Nodes > Maximum Cars".

### Miscellaneous Page
* Added "Gravity" settings. Far out!
    * Screen might go blue if you set some of these numbers the wrong way. No warranty included.
* Added "Heaps > No Temp Heap".
* Moved "Use Tracking Heaps" into the new "Heaps" group.