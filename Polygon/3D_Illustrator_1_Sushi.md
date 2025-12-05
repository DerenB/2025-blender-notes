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











