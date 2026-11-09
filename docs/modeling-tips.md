# Modeling tips

Termite reads geometry straight from your CAD model, so how you draw that geometry affects the result. Read this page before you start a real project.

---

## Use polylines, not curves

Termite understands **polylines**: shapes made of straight segments. It does **not** understand true curves such as arcs, circles or freeform splines.

This applies to everything you send to Termite: floor boundaries, unit boundaries, hallway centerlines and staircase outlines.

**If your design has a curved facade**, convert it to a polyline before you send it. For example:

- **Rhino:** use `Convert` (output: lines) or `Rebuild` to turn a curve into a polyline.
- **Revit:** draw the boundary with straight line segments.
- **Archicad:** draw the boundary as a **Polyline** made of straight segments.

---

## What to select in each CAD tool

Each input needs a specific type of geometry. If you select the wrong type, Termite shows an error or skips the element.

| Input | Shape | Rhino | Revit | Archicad | Grasshopper |
|---|---|---|---|---|---|
| **Floor boundary** (Units tab) | Closed outline | Closed polyline | **Floor** or **Area** element, or model/detail **lines** forming a closed loop | Closed **Polyline** or **Slab** | Closed polyline (`boundary` input) |
| **Hallway** (Units tab) | Straight centerline | Line | Model or detail **line** | **Line** | Lines (`hallway_curves` input) |
| **Staircase** (Units tab) | Closed outline | Closed polyline | Model or detail **lines** forming a closed loop | Closed **Polyline** | Closed polylines (`staircase_curves` input) |
| **Unit boundary** (Plan tab) | Closed outline | Closed polyline | **Floor** or **Area** element, or model/detail **lines** forming a closed loop | Closed **Polyline** or **Zone** | Closed polyline (`boundary` input) |
| **Entry edge** (Plan tab) | One or more straight edges | Line(s) | Model or detail **line(s)** | **Line(s)** or 2-point Polyline(s) | Lines |
| **Daylight edge** (Plan tab) | One or more straight edges | Line(s) | Model or detail **line(s)** | **Line(s)** or 2-point Polyline(s) | Lines (`daylights` input) |

!!! warning "Hallways are straight"
    Termite uses only the **start point and end point** of a hallway. If you select a polyline with several segments, Termite sends a straight line between its two ends. Draw an L-shaped or bent corridor as **several hallways**, one straight line for each segment.

!!! tip "Entry and daylight edges"
    Draw each edge as a line **on top of** the matching edge of the unit boundary. In most cases the easiest way is to explode a copy of the unit boundary and keep the segments you need.

---

## Edges are used exactly as you draw them

Termite does not simplify or redraw your boundary. **Every edge of your polyline is a real edge for Termite.** Walls, entries and windows are placed along those edges.

That is why the size of the segments matters:

| Your polyline | Result |
|---|---|
| Few, reasonably sized edges (for example 1 m or more) | Termite can place windows and doors along the edges without problems. |
| Many very small edges (for example a curve split into 10 cm pieces) | The edges are too short for windows. Window placement can fail, and the plan can get messy. |

!!! tip "Rule of thumb"
    When you turn a curve into a polyline, use **reasonable segment lengths**. Make each edge at least long enough to hold a window. Fewer, larger edges give cleaner plans.

The same applies to the **entry** and **daylight** edges you select in the [Plan tab](plan.md#step-1-boundary). Termite can only place a door or a window on an edge that is long enough for it.

---

## Levels in Revit and Archicad

In **Revit** and **Archicad**, every Termite floor is linked to a **level** (in Archicad: a **story**).

### How Termite finds the level

- When you send a floor, Termite reads the level from the elements you selected. For example, a floor or area in Revit, or a slab, zone or polyline in Archicad.
- If the elements have no level (for example plain lines in Revit), Termite uses the **height (Z)** of the lines.
- When you load a plan or units back into your model, Termite puts them on the level at that **same height**:
    - If a level exists at that height (within 2 mm), Termite uses it.
    - If not, Termite **creates a new level** at that height.

### What to watch out for

- **Draw on the correct level.** Draw or select your boundary in the plan view of the level you want to design. If the boundary is on the wrong level, the results load onto the wrong level.
- **Keep the floor and the view on the same level.** In Revit, Termite shows a warning when the active view is on a different level than the selected floor. Hallways and staircases belong to their floor's level, so they won't line up in another view.
- **Archicad: new stories go on top only.** Termite can only add a new story **above** the highest existing story. If it would need a story **between** two stories or **below** the lowest, it stops and asks you to create that story in Archicad yourself. That way your existing stories are never moved.
- **Don't change level heights after sending.** If you move a level, send the floor again so Termite has the new height.

---

## Layers in Rhino

Rhino has no levels, so Termite uses **layers** instead. The **floor name** works as the level: every floor gets its own parent layer, and everything Termite draws for that floor goes underneath it.

```
Level 01                        ← your floor name
 ├─ Floor                       ← the floor boundary
 ├─ Units
 │   ├─ Hallways
 │   └─ Result #12              ← one layer per "Load Units"
 └─ Plan
     └─ Layout_34               ← one layer per "Load in Rhino"
         ├─ Boundaries
         ├─ Walls
         ├─ Doors
         ├─ Windows
         ├─ Tags
         └─ Furniture
Staircases                      ← top level, shared by all floors
```

Things to know:

- **Staircases** have one top-level layer, because one staircase can belong to several floors.
- Termite creates these layers automatically and sets a default color for each. If you change a layer color, Termite keeps your color.
- **Pick the right floor first.** Results are drawn under the floor that is selected in the context bar. If no floor is selected, they go under a layer called `Default`.
- **Give floors clear names**, such as `Level 01` or `Level 02`. The name becomes the layer name.
- Keep your own drawings (input curves, context, site) on **your own layers**, not inside Termite's layers. Termite may clear and redraw its layers, for example the Hallways layer when you switch floors.
