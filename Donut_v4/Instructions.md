# Blender Tutorial v4

- [YouTube Playlist](https://www.youtube.com/playlist?list=PLjEaoINr3zgEPv5y--4MKpciLaoQYZB1Z)



# Video 1: Intro



# Video 2: Donut Creation

- Add the mesh
  - `SHIFT + A`
- Set the settings before clicking off
  - Major 32
  - Minor 12
  - Radius 0.39m
  - Radius 0.25m
- View the texture as smooth
  - `RMB`
  - "Shade Smooth"
- Add Subdivision Modifier
  - Properties Window
  - Modifiers (wrench icon)
  - Add Modifier
  - Generate
  - Subdivision Modifier
- Enter "Edit" Mode
  - `TAB`
- Proportionally Edit Donut
  - Toggle on proportional editing at the top of the ViewPort
  - Edit donut to make it lumpy
- Add Center crease
  - center of donut is inset a bit
  - Select all with `ALT`
  - Should turn off proportional editing



# Video 3: Icing

- Duplicate Donut
  - Select Object
  - `SHIFT + D`
- Delete the bottom half of icing vertices
- Thicken icing
  - Properties Window
  - Add Modifier
  - Generate > Solidify
  - Set Offset to 1
  - Set thickness to 0.025m
- Hide modifier in Edit mode
  - click box on the modifier to hide in edit
- Snap the vertices to the donut
  - Click magnet icon at the top of the view port
  - set to "face" snapping
  - set to "face project"
- Apply subdivision modifier (increase vertices)
- Select inner vertices to hide them
  - Select inner ring with `ALT`
  - Auto select next tier `CTRL + +`
  - Hide with `H`
  - Unhide with `ALT + H`
- Do all of the dragging for the wavy affects
- Add Modifier to round edges
  - Add subdivision modifier
  - Rounds the edges so they aren't 90 degrees
- Fix icing edge issue
  - Icing is rounded and not pinned to donut
  - Change Solidify modifier
    - Set Edge Data > Crease Inner : 1
- Extrude Icing Drips
  - Select verticies
  - Extrude with `E`



# Step 4: Sculpting

- Fix any issues with the vertices and face layering
- Add Modifier
  - Deform > Shrinkwrap
  - Set target to donut
  - Put it first in modifier order
  - Apply it







