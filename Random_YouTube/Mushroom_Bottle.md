
# Create the Mushroom Stem

- Insert a cylinder 
  - 8 Vertices
  - Move to above the x/y plane (`G + Z`)
- Enter Edit Mode
  - Scale in x/y down to a stick
  - Add subsurf modifier `CTRL + 2`
    - Makes it look egg shaped
  - Add 3 Loop Cut Lines
- X-Ray View
  - Toggle X-Ray `ALT + Z` or at top
- Increase base shape
  - Select bottom vertices
  - Scale `S` with proportional scale `O`
  - Make it rounded bottom like a mushroom
- Drag middle areas around to get bent shape
- Bottom/Top Faces
  - Inset them slightly `I`



# Create the Mushroom Head

- Start with a cube
- Add subsurf modifier `CTRL + 2`
- Bring down to the top of the stem
- Bottom Face
  - Widen to width
  - Inset to make rim
  - Inset a 2nd time to make hole
  - Extrude up to deepen hole
- Position Head hole over Stem
- Scale to size



# Head Lattice

- Add a Lattice
  - Scale so that it covers the head completely
- Combine
  - Select Cap first, then lattice
  - Lattice is active (yellow)
  - `CTRL + P` > Lattice Deform
  - Cap will be affected by deforming the Lattice shape
- More Lattice Points
  - Properties > Data > Lattice > Resolution
  - Set the U/V/W to add more points
- Move Lattice points around to adjust head shape
- Select all 3 with stem selected last > `CTRL + P` > Object
- Shade both smooth



# Head Dots

- Add a cylinder
- Set vertices to 8
- Add a subsurface modifier
- Scale down
- Inset top and bottom faces (to make into hockey puck shape)
- Shade smooth
- Turn on "Snap" at top
- Turn on "Face" Snap Target
- Use `ALT + D` to duplicate so they are linked
- Freely rotate them with `R + R`



# Base

- add a cube
- add a subsurface modifier
- Scale up
- position under mushrooms
- Add an inset to top face
- Shape it into a bowl shape
- Shade smooth



# Add Large Grass

- add a "curve path"
- Rotate 90 degreess so it points up
- Properties > Data
  - Set depth to 0.102
  - Set resolution to 1
- Set size in edit mode
- drag points to make into curve shape
- Make top point
  - select top vertex
  - `ALT + S` to scale down
- Duplicate as much as you want `ALT + D`



# Add Small Grass

- Duplicate large grass with `SHIFT + D`
- Set to size
- Duplicate 4-6 times
- Join with `CTRL + J`
- `ALT + D` duplicate them



# Add Small Rocks

- Add a cube
- add a subsurf modifier
- Apply the modifier
- Move vertices around in edit mode with proportional editing `o`



# Add Bottle

- Add a cylinder
  - Set vertices to 8
- Add subsurf modifier
- Shape the cylinder into a bottle shape around the model
- Delete the top face of the bottle
- Add a solidify modifier
  - Make solidify first in hierarchy
  - Set the thiccness
  - Apply the solidify modifier
- Add the rim
  - Select the faces around the top
  - Extrude along the normals
  - Do a second loop in the middle
  - Add support Loop cuts `CTRL + R` to emphasis the edge
- Shade Smooth



# Create the Cork

- Select the inner loop 
- Duplicate `SHIFT + D` > RMB to keep it there
- Split from the bottle with `P`
- Add a face with `F`
- Use Extrude `E` and loop cuts `CTRL + R` to create the cork shape
- Inset `I` the top face
- Parent the cork to the bottle



# Add the Back Drop & Camera

- Add a plane
- Add a vertical section
- Bevel the border
- Camera
  - Set the resolution
  - Position the camera
  - Set world light to 0
- Split View 
  - In the render view, use `CTRL + B`
  - Drag select the camera view
  - This will only render what is in view



# Lighting

- Add an area light
- Add an area left and right light
- Turn off reflection on bottle
  - Select Light > Properties > Object > Ray Visibility
  - Turn off Glossy & Transmission



# Materials

- Bottle Material
  - Make sure render engine is set to cylces, will be black if eevee
  - Set to Glass BSDF
  - Set Roughness to 0
  - Set IQR to 1.5
- Ground Color (shading tab)
  - Geometry Nodes:
  - Texture Coordinate 
    - Generated > Mapping (Vector)
  - Mapping
    - Set Y-Rotation to 90
    - Vector > Gradient Texture (Vector)
  - Gradient Texture
    - Color > Color Ramp (Factor)
  - Color Ramp
    - Set the Colors
    - Color > Principled BSDF (Base Color)
  - Principled BSDF
    - BSDF > Material Output (Surface)
- Max Colors Pop more
  - Properties > Render > Color Management
  - Set View: Standard
  - Set Look: Very High Contrast














































