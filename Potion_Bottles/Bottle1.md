
# Video Link

- https://youtu.be/-LDptWxkG8Q?si=fsmXFoddrp8gEQBV

# Notes

# Create Bottle

- Add UV-sphere mesh
- Remove top faces
  - Edit Mode
  - Select first 3 "rows" of faces
    - can drag and click first row
    - `CTRL + +` to select next rows
  - Remove faces
    - `x` > Delete Faces
- Extrude top rim
  - Select top rim (the rim that forms after deleting the top face rows)
  - Extrude upwards
    - `E` to extrude
    - `Z` for z-axis
- Thicken shape
  - Object mode
  - Properties > Modifiers > Solidify Modifier
  - Keep offset at -1 (thicken inwards)
  - Set thickness to 0.12m
  - Apply modifier
- Add rim to top
  - Back to edit mode
  - Select faces around the top
  - `RMB` > Extrude Faces Along Normals
  - Can either drag to size or start typing on numpad for size (0.12)
- Bevel edges
  - Bevel the the 4 edges
  - `CTRL + B` + mouse wheel for more edges
- Add subdivision
  - `CTRL + 3`
  - Set both Levels Viewport and Render to 3
- `RMB` > Shade Auto Smooth



# Create Rope

- Add Circle
  - `SHIFT + A` > Mesh > Circle
  - Move to the side
  - Duplicate circles so that there are 3
  - Arrange them into a triangle shape
  - Select all circles 
  - Join together: `SHIFT + J`
- Go into edit mode on the circle
  - delete the inner vertices
  - Join the vertices at the corner intersections: `M` > Join at Center
  - Select all `A` > `RMB` > Smooth Vertices
- Go to Object Mode
  - `RMB` > Set Origin > Origin to Geometry
- Screw Modifier
  - Add "Screw" modifier
  - Set "screw" to 6m
  - Set iterations to 3
- Add subdivision `CTRL + 2` modifier
- Scale down `S`
- `SHIFT + S` > Selection to Cursor
- `SHIFT + A` > Mesh > Circle
  - Duplicate, put 2nd around bottle neck
  - Scale down to almost size of bottle
- Select rope
  - Add "Curve" modifier
  - Select circle that will be used for curve
  - `RMB` > Convert To > Curve
  - Select circle with the rope curve modifier
  - Set axis to Z
  - Increase iterations on screw modifier and scale to size
- Duplicate Rope and repeat for upper section
- Apply all 3 modifiers for both ropes
  - Screw
  - Subdivision
  - Curve
- Delete the 2 curve circles
- Rotate ropes so that seam is behind the view
- Duplicate rope and rotate so it forms an X



# Create Potion

- Select bottle
- Edit mode > face select
- Select bottom faces with drag and click
  - `CTRL + +` to go up the side
  - Duplicate the selection `SHIFT + D` > `RMB`
  - Seperate `P` > By Selection
- Enter edit mode on the potion
  - Select upper rim
  - Top Bar > Face > Grid Fill
  - `RMB` > Subdivide
  - `CTRL + I` invert selection
  - `H` hide the inverted selection
- Add waves
  - vertex select mode
  - select vertices with porpotional editing
  - move up or down









