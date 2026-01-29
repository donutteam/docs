### General
* Made Ctrl+C copy the current page text to clipboard.
    * Also added "Allow Copying with Ctrl+C" to the "Advanced" tab of the hacks settings to disable that.

### "actors" Page
Added this page.

### "cams" Page
Made this page exclude null cameras.

### "characters" Paege
Added this page.

### "intersects" Page
Made this page not say "Y: " before the Y and "Z: " before the Z of "Intersect triangle pos 3".

### "loaded characters" Page
Added this page.

### "missions" Page
Made this page exclude null missions.

### "mission" Page
* Made this page show "null" for null objectives instead of crashing.
    * This is helpful for debugging in the event the stage's objective is not getting added.

### "traffic" Page
Made this page render the segments of the road the car is currently on (and the previous roads segments if the car is on an intersection).

### "triggers" Page
* Made this page include the type number of locators in brackets after the type name.
* Made sphere triggers render as spheres now instead of boxes.