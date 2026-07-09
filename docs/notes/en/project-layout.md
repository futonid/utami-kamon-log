## In-Project Organization
**Context:** How should I set up the working environment hierarchy, [22/06/26 / GIMP 3.2.0]
### Problem
- **p1-modular-structure**
I need to build the whole project in as modular a structure as possible, both to keep it more organized and controlled, and to make it more sustainable given GIMP's technical infrastructure.

### Solution
#### p1-modular-structure
- Folder format inside GIMP:
    - `maru-one-example-mon` > Main project name. [Naming](/docs/notes/tr/ilk-cizim.md#p4-how-to-name-it)
        - `parts` > All the parts/layers of the motif.
        - `base`  > The surface files the motif is worked onto.
            - `paper` > The background of the motif.
            - `maru`  > The shape surrounding the motif, i.e. the circle.
            - `reflection` > I chose to take the mirror reflection of the motif and place it on this side.
- Keep `Path` names the same as `Layer` names, since they're on different layers, separate from each other. It makes it easier to follow the organization.

---
### Result

- **[kamon-master-8Grid.xcf](/docs/workbook/templates/)**

---
