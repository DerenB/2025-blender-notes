
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


















































