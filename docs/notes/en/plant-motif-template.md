## GIMP Plant Motif Template
**Context:** Specifically, how should a template be prepared for a plant motif using GIMP? **[19/06/26 / GIMP 3.2.0]**
### Problem

- **p1-template**
The working area size must be chosen and the general system determined.
- **p2-maru-decision**
It must be decided whether the design will be within a maru or freestanding.
- **p3-grid-structure**
The grid must be set specifically for the plant motif.

- **p4-motif-construction**
Even though plant motifs come from nature, in Kamon design they must be highly abstracted and made minimalist.
---

### Solution
#### p1-template:
- File > New: Set the Width and Height values to `1200 px`.
- Set the Color Space to Grayscale. `Image` > `Mode` > `Grayscale`
- Golden Ratio Calculation: `1200 px / 1.618 ≈ 742 px.` This is the "active" working area.
- Margin Calculation: `(1200 - 742) / 2 = 229 px`.
- Guides: Using Image > Guides > New Guide (by Pixels), add both vertical and horizontal guide lines at 229 px and 971 px (229+742) positions.
- **Source:** [Analysis](/docs/notes/tr/analiz-sablonlar.md)
**Alternative: Percent-Based Golden Ratio (valid for any canvas size)**
- Instead of calculating pixels, GIMP's percent-based guide feature can be used; this method is independent of canvas size because the constant φ (1.618) always translates to the same percentage: **19.1%** and **80.9%**.
- Using `Image > Guides > New Guide (by Percent)`:
  - Orientation: Vertical, Position: `19.1` → add
  - Orientation: Vertical, Position: `80.9` → add
  - Orientation: Horizontal, Position: `19.1` → add
  - Orientation: Horizontal, Position: `80.9` → add
- These 4 guides create 4 intersection points at the same ratio regardless of canvas size (e.g. 1080x400, 1200x1200, etc.); a text block or focal element can be aligned to one of these points.
- Note: 19.1% + 80.9% = 100; the two lines divide the canvas twice (19.1-80.9 and 80.9-19.1) under a "large piece – small piece" logic.

#### p2-maru-decision:
- Will be done within a circular frame.
- Kamon designs generally establish balance radiating out from the center.
- Create the main axis for the motif: go to `Image` > `Guides` > `New Guide (by Percent)` and place both Horizontal and Vertical center guides at the `50%` value.
- For drawing the circle, Tool: `Ellipse Select Tool` (E), check the `Fixed Aspect Ratio (1:1)` option in Tool Options. Enable the `Expand from center` checkbox.
    - Application: Place the cursor at the center intersection point and draw the circle so it touches the boundaries of your active area (the 742 px square). In [Müller-Brockmann's](/docs/workbook/references/research.md#grid-system) system, this circle must mathematically coincide exactly with the outer guides.


#### p3-grid-structure:
- A grid with fewer divisions, such as 8x8, makes it easier to focus on basic forms without getting bogged down in complex detail.
- 742 px (active area) / 8 units = 92.75 px.
- Go to `Edit` > `Preferences` > `Default Grid`, or for the current file, to the `Image` > `Configure Grid` menu.
- Enable `View` > `Show Grid` to see the grid, and `View` > `Snap to Grid` to snap to the lines.


#### p4-motif-construction
- Abstraction: Strip away all unnecessary detail from the plant (leaf, flower, stem). Keep only the basic forms.
- Grid Alignment: Snap the tips of the leaves or the joining points of the stem exactly onto the grid intersections.
- Symmetry: After drawing one leaf, use `Layer` > `Transform` > `Flip Horizontally` to reflect the other side with rational precision.




---
### Result

**[kamon-master-8Grid.xcf](/docs/workbook/templates/)**

**Note:**
(Balance and Negative Space)
In [Müller-Brockmann's](/docs/workbook/references/research.md#grid-system) system, empty (white) areas are just as active as the black forms.

Monochrome Balance: Count how many modules the black plant forms occupy on the grid. Make sure the white empty spaces create a "rhythm" with these forms.

Legibility: Look at the work at small scales like 10-20%; test whether, thanks to the grid, the Kamon retains its character (recognizability from a distance).

---
