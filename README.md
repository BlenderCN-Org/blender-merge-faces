# Blender Merge Faces

In this repository I try to figure out how to merge coplanar faces in Blender 2.8.

The setup is as follows:

- Keep the default cube as is
- Create another cube (Shift + A > Mesh > Cube) and translate it by 1 m on X and Y axes
- [ ] Find out if there is a shortcut for moving focus into the first field of the properties panel
- Select both cubes and join them (Ctrl + J)
- Go to edit mode (Tab) and deselect all (Alt + A or double A)
- Select the two overlapping coplanar top faces
- Switch to face select mode by pressing 2 in edit mode
  - [ ] Find out if there is a shortcut for cycling / switching these
    - https://blender.stackexchange.com/questions/60758/hotkey-to-change-select-mode#comment236267_60759
- [ ] Find out why Dissolve Faces is not it
- [ ] Find out how to introduce an edge where the vertical facesoverlap so that the top faces could be removed and a new one connecting the six points added
  - https://github.com/TomasHubelbauer/blender-edge-at-face-intersection

## Dissolve Edges

Selecting the edges belonging to the top faces of the cylinders contained within the area of the cube top face
except for the ones that are touching the cube top face edges and dissolving them works to a degree and provides
close to the desired result, however extending this selection to the edges of the cube's top face and dissolving
further collapses the whole mesh on itself.
