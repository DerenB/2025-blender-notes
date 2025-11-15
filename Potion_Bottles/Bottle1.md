
# Video Link

- https://youtu.be/-LDptWxkG8Q?si=fsmXFoddrp8gEQBV

# Notes

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










