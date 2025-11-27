# YouTube Tutorial

- [Link to the Tutorial](https://youtu.be/e4CW6MInaas?si=AYrG1MO6VVx0tgRc)



# Create the Bottle

- Add UV Sphere `SHIFT + A`
- From top, delete the first 3 "row" circles
  - Sphere has an open top now.
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
- Bevel top and bottom edges



# Create Rope

- Add Mesh > Curve > Circle
- Move up to the neck
- Scale down close to size of neck
- Set thickness
  - Properties > Data > Geometry > Bevel
  - Set "Depth" to 0.1m
- Rotate rope so it looks like the picture
- Repeat for as many ropes as needed
- Add 2 loops for the knot
- Add the large loop for the tag
- Add Long ropes
  - Mesh > Curve > Bezier
  - Can Extrude for more vertices
  - Can fill the ends with "Fill caps" next to the thickness bevel



# Create Label

- Add a Plane mesh
- Rotate 90 degrees so you can see
- Resize to a rectangle
- Go to Edit Mode
- Add 2 circle cuts `CTRL + R` (divide into thirds)
- `S` in X-axis so the middle section is the size of the tag
- Circle cut down the middle
- Circle cut the tag
- Should be 4 columns on the main tag and a 2x2 grid on the tag
- Got back to object mode
  - `CTRL + A` > Apply scale
- Back to Edit Mode
- Tag Hole
  - Select vertex in center of 2x2 grid
  - `CTRL + SHIFT + B` to add a bevel, scroll to level 2 so there are 4 sections
  - In the bevel window, set "Profile Shape" to 0.104 (make circular)
- Round corners
  - select top 2 vertives of the tab
  - `CTRL + SHIFT + B` to bevel them
  - Reset "Profile Shape" to 0.500 so that they are round
- Add 6 loop cuts so that the edges of the label are protected
- Add 3 additional vertical loop cuts (so the paper can be curved)
- Add modifiers
  - Solidify
  - Subdivision surface
- Delete 4 faces inside tag (to create hole in tag)
- Use vertices to bend the tag around
- Move tag into position on the rope loop



# Rotate the Ropes

- Move cursor to World Origin
  - `SHIFT + S` > Cursor to World Origin
- Select all of the ropes/tags
- Set pivot point
  - Click "Transform Pivot Point" at the top
  - Set to "3D Cursor" (defaults to median point)
- Can now rotate about the axis



# Make the Liquid

- Isolate object
  - Select an object
  - Hit `/`
  - Hides everything except selected object
  - Repeat to show everything again
- Select inside bottom faces of bottle
- Increase amount selected `CTRL + +` until needed height
- Duplicate > Separate `P`
- Edit mode fluid
  - Select upper edge of fluid
  - `CTRL + F` > Grid Fill
- Duplicate potion as a backup
- Add Latice
  - `SHIFT + A` > Lattice > Lattice
  - Properties > Data > Set Resolution U,V,W to 7 each
- Select Fluid
  - Modifiers > add Lattice modifier
  - Dropper select the added lattice
- Go To Lattice in Edit mode
  - move the vertices up and down until you get a curve
- Turn on backup to compare to original size
  - Can add materials to the fluid to see clipping easier
- Check normals
  - Unhide everything with `/`
  - Top > Overlays > Face Orientation
  - Turn on Blue:
    - Edit > Preferences > Themes > 3D Viewport > Face Orientation Front
    - Set the alpha to something higher than 0
  - Fix red
    - Select red object
    - go to edit mode
    - Select all with `A`
    - `ALT + N` > Flip



# Rotate the bottle

- Select everything except the fluid
  - If child/parent issue > `ALT + P` > Clear Parent
- `CTRL + P` > Object (Keep Transform)
- Apply Fluid
  - Select fluid
  - Apply Lattice modifier
  - Add Bevel modifier
    - Place first, above subsurface
    - Set Amount to 0.014m
    - Set segments to 2



# Set up camera

- Focal Length 100mm
- Set render to Cycles, GPU compute
- Enable viewport Denoise, set to 50
- Disable render denoise
- Film > Transparent > Transparent Glass
- View Layer > Passes > Data > Denoising Data
- Add background Plane



# Shading Tab

- Reset Pivot Point
  - Top > Pivot Point > Individual Origins
- Go to shading tab at top
- Set Material to "World"
- Add an HDRI image with "Image Texture
  - Drag the color into the background color
- Set plane color
  - Add new material
  - set to Black #000000
  - Set roughness to 0.4
  - Hide in camera view
    - Properties > Object Properties > Visability > uncheck Camera
- Bottle
  - Set Transmission to 1
  - Set color to white #ffffff
  - Set roughness to 0
  - Add "volume absorption" node
    - Connect to "Material Output" volume pointer
    - Set color to whatever
    - Set density to 2
- Potion
  - Set to white #ffffff
  - Transmission to 1
  - Roughness to 0.01
  - Add "volume absorption" node
    - Connect to "Material Output" volume pointer
    - Set color to whatever
    - Set density to 2
- Rope
  - Set to brown
  - Set roughness to 0.6
- Cork
  - Add node "Voronoi Texture"
    - Connects color to color ramp factor
  - Add node "Color Ramp"
    - Connects color to principled base color
  - Set colors on ramp
    - Set points to 0.35 and 0.555



# Apply Modifiers

- Apply the modifiers
  - On Bottle
  - On Potion Fluid
  - On Cork
  - On Tag



# Add Label Image

- Go to UV Editing
- Select all polygons of the Tag
- Open the image (open icon at the top)



# Add the Bubbles

- Uses particle system
- Select fluid
- Properties > Particle
- Add a new one
- Hide the bottle
- Add UV Sphere
  - Used for the bubble
  - Create Material for sphere
    - Set to white
    - Roughness: 123
    - IQR: 1.3
    - Transmission: 1
    - Emission: 0.01
- Settings
  - Emission
    - Number: 100 (adjust for quantity)
    - Frame Start: 1
    - Frame End: 1
    - Lifetime: 250
  - Source
    - Emit From: Volume
    - Use Modifier Stack
  - Render
    - Render As: Object
    - Eyedropper select bubble sphere

































