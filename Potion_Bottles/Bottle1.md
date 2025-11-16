
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



# Create Cork

- Select bottle and go into edit mode
- edge select inner edge of potion neck
- Duplicate and split
  - Duplicate with `SHIFT + D`
  - Drag up with `Z`
  - Seprate with `P` > By Selection
- Select cork circle and go into edit mode
  - Vertices select
  - Select all `A`
  - Fill with `F`
- Extrude cork upwards `E`
- Remove subdivision modifier
- Adjust size and position
- Face select top face
  - Rotate `R` to angle it
  - Inset face `I`
- Create chip
  - Select vertice
  - `CTRL + B` > `V` > scroll down until just 1 shape
  - If not working, might be multiple vertices. check xray
  - Drag with `G` until right size
  - Face select, delete face
  - Select 2 edges with edge select, create face with `F`
- Create 2nd chip if wanted
- Add Bevel modifier
  - Set amount to 0.01m
  - Set segments to 4
- Add subdivision modifier



# Camera

- Position camera so it's looking at potion
- Set output resolution size to square 1,920 x 1,920
- Rotate potion how you want it



# Background

- Add a plane
- Set size so it fills camera
- Edit mode > edge select backend
- Extrude `E` upwards
- Should be a 90 degree plane
- `CTRL + B` bevel the corner, adjust positioning
  - If Bevel not working, apply the scale of the plane with `CTRL + A` > Scale



# Set up Render and Lights

- Set render to Cycles
- Set to GPU Compute
- Set to 128 in Viewport and 512 in Render samples
- Render > Color Management
  - Set to Medium High Contrast
- Add Area Light
  - `SHIFT + A` > Light > Area Light
  - Drag it straight up, just outside of camera
- Light Settings
  - 300 Power
  - Disk Shape
  - 2m in size
  - Set color (#FFDAFD for demo)
- Add Lights
  - 3 Disc lights shining on potion (top, left, right)
  - 1 shining at the background plane



# Materials

- Set background color
  - Material > New
  - Demo used #FFB3A6FF
- Glass Bottle
  - Set surface to "Glass BSDF"
  - Set color (demo used #FFDEEBFF)
  - Set roughness to 0.01
- Set rope colors
  - Demo used #E78A66FF
- Set cork color
  - Demo used #B64C2FFF
  - Set roughness to 0.8
- Potion Color
  - Set color to #FEAEFEFF
  - Roughness to 0.1
  - IOR to 1.3
  - Transmission to 1
  - Emission of #F536FFFF
  - Emission strength of 5
  - If potion color coming through bottle, move back a bit
- World Color
  - Properties > World > Color
  - Set to #AD3C9FFF









