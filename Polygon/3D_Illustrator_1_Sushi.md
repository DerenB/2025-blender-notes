# Sushi

- Create cube
- Squish height to size
- Subdivide
  - Edit mode
  - `RMB` > subdivide
  - Do Twice
- Extrude interior
  - extrude `e` the interior squares inward to create layer
- Extrude perimeter
  - `alt` select all of the exterior faces
  - Warning:
    - using extrude `e` then cancelling with `RMB` still creates the new vertices
    - have to be careful or merge at distance afterwards to fix
  - `ALT + E` > Extrude Faces ALong Normals
    - Normals are the direction that an object is facing
  - Use `S` scale to extrude out evenly
- Extrude new perimeter upwards



# Add Material

- Remove default material
- Set multiple colors in edit mode
  - select faces > assign



# Duplicate the Sushi

- Add modifier
  - Generate > Array
  - Set Count to 3
  - Set relative offset x to 1.2
- Add 2nd Array modifier to created 2nd row
  - Set count to 2
  - Set relative offset y to 1.2



# Add Plate

- Add plane
- Change scale in edit mode
- extrude upwards
- Inset the plate `I`



# Chop Sticks

- Move Cursor: `SHIFT + RMB`
- Reset to world 0,0,0 origin:
  - `SHIFT + S` > Cursor to world origin
- Create chopstick from cube
- Create linked duplicate with `ALT + D`
  - Linked allows for material and size to be applied to both
  - Size must be adjusted in edit mode to change the data



# Camera Setup

- Set to orthographic mode
- Setup camera
  - Select camera, got to output properties
  - Set to 4:3 aspect ratio for resolution
    - Set to 1600x1200
  - Camera tab
    - Change from "Perspective" to "Orthographic"
- Move Camera In/Out
  - Camera > Data Properties > Change "Orthographic Scale"
- Rotate about axis easier
  - Top of Screen > Transform Pivot Point > 3D Cursor
- Rotate the camera
  - Set Transform Pivot Point to "Median Point"
    - Can also set to "3D Cursor" to pivot around it
  - Set Transform Orientation to "Local"
- Can change from Global to Local by clicking the axis twice
  - `R + X + X`



# Lighting

- Set up render settings
  - cycles
  - gpu compute
  - set samples
  - 
- Set up World Light Settings



# Group Items

- Select all items
- Select main parent item last
- Group them: `CTRL + P`









