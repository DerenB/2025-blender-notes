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
- Apply Solidify modifier
- Add bulge to bottom of drips
  - Enter Sculpt mode
  - Use "Inflate" Brush
  - Change brush size: `F`
  - Change brush strength: `SHIFT + F`
- Apply subdivision modifier
  - Level 2
  - Render 6
- Use "Grab" brush to modifier droplets 
  - Can open with `G`
- Use "Mask" brush
  - Can open with `M`
  - Brush areas
- Show Brush Menu
  - Click "View" beneath main task bar
  - Check "Tool Settings" box
- Edit only front
  - Can accidently edit opposite side of object
  - Enable Tool Settings > Brush > "Front Faces Only"
- Erase marking errors
  - `CTRL + LMB` 
- Flip the shaded areas
  - `CTRL + I`
- Smooth Mask
  - Sub Task Bar > Mask > "Smooth Mask"
- Add thiccness
  - Use "Mesh Filter"
  - Set strength to 0.1
  - Drag to Left to increase
- Clear Mask
  - Mask
  - Clear Mask
- Smooth edges
  - Use smooth brush
  - Clean up artifacting areas.



# Part 5: Shading

- Add temporary shading to icing and donut
  - Properties Window
  - Materials 
  - New
  - Set color
  - Set Roughness
- Add Plane for Marble
  - `SHIFT + A`
- Set Donut parent
  - Donut the parent of the icing
  - Select icing
  - Hold `SHIFT`
  - Select Donut
  - `CTRL + P`
  - "Object Keep Transform"



# Part 5.1 Import custom texture ***

- Set Texture
  - Material 
  - New
  - Click the yellow dot by color
  - Texture > Image Texture
  - Add the image for the marble (the base color jpg)
- Shading Tab
  - Drag off from Principled BSDF > Roughness 
  - Add "Image Texture Color"
- Roughness Node
  - Set "Color Space" to "Non-Color"
- Principled BSDF node
  - Drag off Normal
  - Add "Image Texture Color
  - Open Purple image with "normal"
  - Set to Non Color
- Normal Map
  - `SHIFT + A`
  - Add Vector > Normal Map
  - Drop between Image Texture Color Normal and BSDF
- Texture Paint
  - Open Texture paint tab
  - Go to Materials tab
  - Yellow dot > Image Texture
  - New Image
  - Set donut color
- Add donut color to left side at the top
  - Paint onto donut the rim
- Save the image
  - Have to separately save the image



# Part 6: Geometry Nodes

- Open "Geometry Nodes" menu at the top
- Add points
  - Adds points to the icing
  - `SHIFT + A`
  - Point > Distribute Points of Faces
- Join the geometry
  - Adding the points removes the icing
  - `SHIFT + A`
  - Join > Join Geometry
- Circle shape on nodes can only accept one input
- Oval/Pill shape can accept many inputs
- Points won't render, need to indicate what to render as
- Add a mesh to the scene 
  - shift + a
  - Add a sphere
- Add mesh to geometry nodes
  - Drag into geometry nodes from outline
- Delete Geometry Node connection
  - `CTRL + RMB`
- Add Instance Points
  - Instances > Instance on Points
- Points too close together
  - Set the "Distribute Points on Faces" to "Poisson Disk"
- Remove points from underside
  - Add weight painting
  - Go to Data Tab
  - Rename vertex group from the painting
- Add to Geometry Nodes
  - Drag off from "Distribute points on faces" from Density Factor
  - Add "Named Attribute"
  - Set name to the name given to the vertex group
- Fix brush to single face
  - Tool toolbar > Brush > Front Faces Only
- "Expose" data point
  - Drag "density factor into "Group Input"
  - Then if the donut is duplicated, you can change the value per donut
  - Value changed in the modifier 
- Rename node item
  - Select node (ex Group Input)
  - Click `N`, opens a side menu
  - Can double click node item to rename it
- Scale donut/everything down to actual size, 0.1m
- Can hold `CTRL` while scaling for incremental adjustments
- Show side menu: `N`
- Apply the scale
  - Select all
  - `CTRL + A`
  - Apply Scale
- Add Math to density
  - Multiplication math node to simplify the quantity adjustment



# Part 7: Sprinkles

- Move 3D cursor
  - `SHIFT + RMB`
- Set clipping distance
  - Side Menu
  - View
  - Set Clip Start
- Add Sprinkle
  - 12 sides
  - 0.001 size
- Round edges of sprinkle
  - Select top and bottom face
  - add bevel: `CTRL + B`
  - Use mousewheel scroll to increase number of bevels
- Add bend to the sprinkle
  - Add modifier: SimpleDeform
- Set origin point of objects to middle
  - Select objects
  - Right Click
  - Set Origin > Origin to Geometry
- Apply the bend modifier
- Duplicate Donut with icing
- Edit the Geometry Nodes for Long Sprinkles
  - Remove the sphere collection
  - Drag in the long sprinkles collection
- Fix position
  - Check "Separate Children"
  - Check "Reset Children"
  - Check "Pick Instance"
  - Rotate sprinkles so they are parallel to plane
- Add random rotation
  - `SHIFT + A`
  - Utilities > Rotation > Rotation Rotation



# Part 8: Sprinkle Colors

- Apply same material to multiple objects
  - Shift select all objects
  - Make item with material last
  - `CTRL + L` > Link Materials
  - Material pane shows count of objects with the material
- Add Node Frame
  - Select Nodes
  - Hit `F`
  - Add Title
- Edit Node Frame Title
  - Select Frame
  - Hit `F2`
- Cut Node connection
  - `CTRL + RMB`
- Shading tab
  - Add Input > Object Info
  - Add Converter > Color Ramp



# Part 8.5 Set up Camera & Render

- `SHIFT + ~` to put camera in fly mode
- `NUMPAD 0` to move to camera 
- Pin Camera to View: View > Camera to View
- Set up GPU render
  - Turn on preference if greyed out
  - Edit > Preferences > System > Cycles Render Devices
    - CUDA: NVIDIA 1080 and older
    - OptiX: Use for modern cards
- Move object to 0,0,0 orign: `ALT + G`
- Add sub surface scattering
  - Select object with material
  - Go to MATERIAL section in properties
  - Subsurface > Set weight to 1 (always use 1 or 0)
  - Fix the colors
    - The default radius values are for human skin colors
    - Set all 3 Radius values to 1
    - Set scale (thickness of the object)



# Part 9 Create the plate

- Add a window
  - move mouse to the edge of a view so drag icon shows
  - `RMB`
- Add a sphere
  - Extrude upwards
  - Scale outwards
- Extrude outwards:
  - `E` then `RMB` then `S` scale
- Add a face
  - go to wire frame mode
  - Select vertices
  - Hit `F`
- Add bevel
  - select edges
  - `CTRL + B`
- Add solidify modifier
- Apply modifier
- Add rounded bevel
  - Select both edges and start bevel `CTRL + B`
  - Click `C` while creating the bevel so that the edges meet
- Merge vertices
  - Vertices can be on top of each other
  - Select all with `A`
  - Open Merge window `M`
  - Merge by distance
  - Delect all with `ALT + A`



# Part 9.1 Camera Settings

- Adjust viewport size (the lines of the camera)
  - Select camera
  - Properties
  - Camera
  - Viewport Display
  - Change size



# Part 9.2 Duplicate donuts

- Select all donuts
  - Duplicate: `SHIFT + D`
- Position donuts
- Rotate around original axis
  - Rotate `R` and hit axis twice `Z + Z`
- Set up scene
  - Duplicate donuts
  - stack donuts
  - position camera
  - position light
- Duplicate floor pane, create background
- Create random colors



# Part 10 Lighting

- Add a sun lamp
  - properties
  - world
  - yellow dot
  - sky texture
- adjust hotness
  - render
  - color management
  - set exposure (-2)
- adjust sun size, elevation, rotation
- Add cube
  - pin to bottom corner
  - switch to wire frame
  - grab cube `G`
  - hit `B` to open pin function
  - pin to planes
- remove back and bottom sides of cube
  - `x`
  - faces
- cut opening
  - select face
  - inset `I`
  - delete new face
- Black fill cube
  - have basic white as default
  - create second material with + icon
  - set to Diffuse BSDF
  - Go to edit mode
  - select face
  - assign button on material
- take sun intensity down to 0.5



# Part 10.1 Import Model

- Web link for model: https://www.poliigon.com/model/wooden-utensils-jar-model/3441
- download, unzip
- File > Append > `.blend` file > collection > click



# Part 10.2 Install Addon

- Polygon addon download: https://www.poliigon.com/blender
- Don't unzip the file, blender installs from zip
- Edit > Preferences > Add-ons > drop down > Install from disk
- Click checkbox on addon to enable



# Part 11 Compositing

- Compositing tab at top
- Check "Use Nodes" box
- Set rendering max samples to low, 100
- Render an image
- Add image view in compositing
  - `CTRL + SHIFT + LMB`
- Close/open image on render layer node if can't see
- Move background image: `ALT + Middle Mouse Button`
- Zoom Image in/out
  - Zoom Out: `v`
  - Zoom in: `ALT + V`
- Can set color management in render menu
  - Properties > Render > Color Management
  - Set "Look"
  - Tutorial used Medium High Contrast



# Part 12 Animation

- Select object that will get keyframe
  - `K`
- Insert empty object at center of plate
  - `SHIFT + RMB` to move cursor
  - `SHIFT + A` > Empty > Plain Axes
- Set up empty object
  - properties > Data
- Attach camera to empty object
  - Select camera
  - `CTRL` select the empty object
  - `CTRL + P` > Object keep transform
- Roate camera by rotating the empty object
- Set timestamp at bottom
- Insert keyframe `k` and use "rotation"
- Open Animation tab
  - Make sure empty object is selected
  - delete y and z rotation
- Change animation tab window to "Graph editor"
- Use `HOME` to adjust view so whole graph is visible
  - `Middle Mouse` is pan
  - `CTRL + Middle Mouse` to manually adjust size
- Adjust transition
  - select keyframe
  - rotate with `r`
  - scale out with `s`
- Can move camera and insert a scale keyframe
- Change FPS
  - Properties > Output > Frame Rate



# Part 13 Rendering

- Use "Denoise"
- Uncheck "Noise Threshold"
- Sample count
  - 300 a good minimum
  - 500 is a good value
  - 1,000 is great with no time constraint
- Set up output settings
  - Properties > Output
  - NEVER output to a video format
    - If something goes wrong during render, whole thing is lost
  - Render to images, then combined into a video
  - PNG good option
  - TIFF slightly better
  - OpenEXR best but difficult if don't know what doing
  - NEVER jpeg
  - Color Depth
    - 8 is fine
    - 16 is for color grading or after affects



# Part 13.1 Pre-Render Error Checklist

- Check Face Direction
  - Solid viewport
  - Show Overlays > Face orientation
  - Blue is correct, red is incorrect
  - Turn on Blue:
    - Edit > Preferences > Themes > 3D Viewport > Face Orientation Front
    - Set the alpha to something higher than 0
  - Fix Red Items
    - Select red object
    - Go to Edit mode
    - Select all `A`
    - Hit `SHIFT + N`
    - For sprinkles, select the original sprinkle not the geometry nodes ones
- Hide objects in render
  - Click camera icon to make invisible in render but viewable in viewport






























