# Course Notes

### Blender Low Poly Landscapes: Model Your Own Stylized Landscapes!

- [Course Page](https://www.gamedev.tv/courses/blender-low-poly-landscapes/welcome-to-the-course/1692)

# Random Notes

- Set distance between points to 0
  - Scale X-axis to 0 `S + X + 0`
  - Example: Setting a roof to a triangle
  - Does NOT delete any of the vertices
- Turn on User Perspective statistics
  - Top right of viewport: "Overlays"
  - Check "Statistics" box
- Merge selected vertices
  - Select all vertices to be merged
    - Setting view to wireframe in the top right
  - Check the statistics for number of vertices selected
  - Click `M`
  - Merge at center
- Insert new object/mesh
  - `SHIFT + A`
- Local Scale
  - Use the local scale instead of the global scale for scale/rotate/etc
  - Hit direction twice
  - `S + Y + Y`
  - Line should change
- Move 3D Cursor
  - `SHIFT + RMB`
- Focus view port on selected object
  - `NUMPAD .`
- Reset Object Rotation
  - sets selected object to 0 degree rotation in all directions
  - `ALT + R`
- Loop Cut
  - Only works on quad shapes (not triangle)
  - `CTRL + R` in edit mode
  - Click once to adjust where the cut is made
  - Right click after to auto place at the middle
- Add more Loops
  - `Scroll Wheel` while in loop menu to add more loops
- Select Loop Cut
  - `ALT + LMB` click on edge
- Delete Loop cut
  - Select Loop
  - `DEL` > Dissolve Edges
  - Removes edges without deleting faces
- Duplicate selected object
  - `SHIFT + D`
  - Duplicate object still part of original, not separate
- Separate Object
  - `P` > Selection
- Move Origin Point
  - Go in Object Mode
  - Top Right > "Options"
  - Check "Origins" box
  - Move with Grab `G` like normal
- Local View
  - Hides everything except for selected object
  - `NUMPAD /`
- Knife/Cut Tool
  - `K`
  - Hit `Enter` when done cutting
- Apply Scale
  - `CTRL + A` > Scale






# Python Answer

```
import folium
import pandas as pd

# Read the CSV file
csv_file = 'coordinates.csv'  # Replace with your CSV file path
data = pd.read_csv(csv_file)

# Convert the DataFrame to a list of coordinate tuples
coordinates = list(zip(data['latitude'], data['longitude']))

# Create a Folium map object
# You can set the initial location and zoom level as per your requirement
m = folium.Map(location=[data['latitude'].mean(), data['longitude'].mean()], zoom_start=10)

# Add a polygon to the map
folium.Polygon(locations=coordinates, color='blue', fill=True, fill_color='blue', fill_opacity=0.2).add_to(m)

# Save the map to an HTML file
m.save('map.html')
```










































