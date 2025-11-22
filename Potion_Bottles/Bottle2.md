# YouTube Tutorial

- [Link to the Tutorial](https://youtu.be/e4CW6MInaas?si=AYrG1MO6VVx0tgRc)



# Create the Bottle

- Add UV Sphere `SHIFT + A`
- From top, delete the first 3 "row" circles
  - Sphere has an open top now
- Shape Neck
  - Extrude `E` and Scale `S` the top sections to create neck
  - Create tear drop shape
  - Add/Extrude about 5 sections
  - Last section more straight
  - Can circle cut `CTRL + R` if more sections needed
- Add Thickness
  - Add Solidify modifier
  - Set Thickness to 0.08m
  - Keep offset at -1 (so thickness goes inwards)
  - Apply it (so it creates the vertices)
- Add Bottle Lip
  - Select outer faces of the top
  - `RMB` > "Extrude Faces Along Normals"
  - Can type in for the same size 0.08
  - Select inner edges created
  - `RMB` > Disolve Edges
  - Bevel top rim
- Set up the Bottom
  - Select first 3 "rows" of circles (like with the top)
  - Delete
  - Inside faces will still be there
  - Extrude `E` bottom rim downward
  - Select new bottom rim
  - Extude Outward: `E` > `ESC` > `S`
  - Extrude new outer rim 
  - Fill base around final outer rim `F`
- Bevel Bottom
  - Select edges to be beveled
  - Bevel `CTRL + B`
  - Clamp with `C` if you want two bevel edges to meet
  - Bevel not working
    - Go into X-RAY mode, select a vertex
    - See if multiple vertices are stacked on top of each other
  - Bevel remaining edges to desired shape
- Inset bottom
  - Inset `I` two additional circles
  - `CTRL + R` edge loop ~3 lines between the 2 new circles
  - Proportional edit, raise center inwards a bit
- Shade Auto Smooth
- Add subdivision modifier



# Create Cork

- Select inner faces of bottle rim
- Duplicate `SHIFT + D` > `RMB`
- Separate with `P` > By Selection
- Extrude upwards and downwards to create cork shape
- Select top rim > `F` to add a top face
- Repeat on bottom
- Add 2 insets to the top and the bottom faces




































