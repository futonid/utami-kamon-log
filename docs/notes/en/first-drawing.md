## First Drawing
**Context:** My template is ready, but I don't know how to start drawing, [22/06/26 / GIMP 3.2.0]
### Problem

- **p1-first-drawing-where**
Will the first drawing be done digitally or on paper?
- **p2-drawing-on-grid**
How will the drawing be done on the grid?
- **p3-maru-and-motif**
How close will the motif come to the edges of the circle?
- **p4-how-to-name-it**
How should I name the drawing once it's finished?

### Solution
#### p1-first-drawing-where
- [Müller-Brockmann's](/docs/workbook/references/research.md#grid-system) design process strongly recommends starting with small-scale sketches on paper.
- My materials are as follows:
    - Ballpoint pen,
    - Pencil,
    - Eraser,
    - Grid or dot-grid notebook/paper.
    - Compass
    - Ruler

- Measure the total area of the paper in cm.
- Draw an 8x8 grid on grid or dot-grid paper (I have dot-grid).
- Optionally, do a guide calculation and constrain the working area the same way as in the digital environment (preferred).
- Example:
    - Total Area   : 14cm
    - Active Area  : (14/1.618) ≈ 8.65
    - Margins      : 2.675 / 11.325 (right/top, left/bottom)
    - Grid Size    : 8.65 / 8 = 1.08125 ≈ 1.1 (this is how I rounded it on paper, since I don't have a precise ruler).
    - [Example Images](/docs/workbook/references/own-resources.md#first-drawing-stages)
- **Source:** [Plant Motif](/docs/notes/tr/bitki-motifi-sablon.md#p1-template)

#### p2-drawing-on-grid
- **On paper:**
    - For the drawing, I worked out the grid piece by piece, counting squares as I drew. After a few repetitions, the logic becomes clear; no need to overthink the details.
- **In GIMP:**
    - Include the paper drawing as a reference image in your project file (optional).
    - Draw with the `Paths Tool` (Path Tool): Use the `Paths Tool` (B) to snap the anchor points of the plant motif exactly onto the intersection points of the grid lines (Snap to Grid).
    - Path each piece separately.
    - For a rational layout, draw the motif up to the halfway point first; then duplicate this layer (or all of them together) and flip it with `Shift + F` (Flip Tool) to achieve symmetry.
    - **The cleanest way to do this by selecting everything together:**
        - Select all parts `Ctrl + A` > remove the ones you don't want mirrored from the selection `Ctrl + LeftClick` > apply `Shift + F` (Flip Tool) to mirror.

        - I noticed that following this exact method lets me use GIMP much more smoothly; otherwise the mirroring process gets messy and you may need extra adjustments.

    ---
    - **Black-and-White Border Lines**
    - For each piece you've pathed, create a new transparent layer.
    - For the selected path, follow this sequence: `Select Path` > `Fill Path (White)` > `Shrink` > `Fill (Black)`. This way, the borders of the motifs you want on top don't stick to each other, and **a carved-out look is created**.

#### p3-maru-and-motif
- I didn't do deep research into how this should be calculated; the various kamon I examined each have different maru, and often different maru thicknesses are chosen even for the same kamon. So I decided to go by eye/taste.

- To keep the maru circle from overflowing outward, I produced the circle this way:
    - For drawing the circle, Tool: `Ellipse Select Tool` (E); check the `Fixed Aspect Ratio (1:1)` option in Tool Options. Enable the `Expand from center` checkbox.
    - Fill it with black using the Bucket Fill Tool (Shift + B).
    - `Select` > `Shrink` > preferably `30-35px` > `OK` > clear the area (Del)


#### p4-how-to-name-it

- I looked into this with Google and Claude, and as far as I understand, there really is a specific naming standard.

- The most common pattern: **"Maru ni ○○"** — meaning placing a motif inside a circle.
    - maru (丸) = "the encircling circle" — functions as a frame/border
    - ni (に) = the particle meaning "inside/in"
    - motif name = the actual thing being drawn (leaf, flower, animal, geometric pattern)
- **Number/repetition prefixes** — before the motif there is usually a numeral adjective indicating how many there are.
- + `[enclosing shape if any: maru]` + `Number/variation` + `[Motif name]` + `(mon suffix, used in formal contexts)`

[Related Article](https://cocoro.faag.co.jp/en/what-is-a-japanese-family-crest-meaning-history-and-design/)

---
### Result:

- The first kamon I designed in GIMP [maru-one-tilsu-mon.png](/exports/maru-one-tilsu-mon.png)
    - **Ocimum tenuiflorum (Tulsi)**: An aromatic plant of the mint family (Lamiaceae). A medicinal green-leafed plant with adaptogenic properties, used in Ayurvedic medicine for over 3000 years as the "elixir of life."


- I did quite a lot of drawing on paper and worked in the most effortless and abstract way; it was very useful for deciding what kind of thing I basically wanted to see, but when I moved to digital, I really tried to add detail to the design and also changed its composition.

- If you want to work with precise measurements on paper, you absolutely need a precise ruler — even a rounding like 1.1 seriously damaged the proportions. If you look at the images, you'll notice how curved the lines became and how imperfect the squares are; probably my somewhat lazy ruler skills also played a significant part in that.

- GIMP might not be the right tool for this job; you could work much more comfortably with other free, open-source tools, but I'll continue with GIMP.

**Note:** [First Drawing References](/docs/workbook/references/research.md#first-drawing-references)

---
