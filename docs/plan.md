# Generate a plan

The **Plan** tab generates a room layout for **one unit**: where the bedrooms, kitchen, bathroom and other spaces go.

The tab has two modes. Switch between them with the buttons at the top of the tab:

| Mode | In short |
|---|---|
| **Explore** | Choose a unit type (for example a two-bedroom apartment). Termite proposes layouts. |
| **Sketch** | Define your own list of rooms and constraints. *Coming soon.* |

---

## Explore mode

Use Explore when you want quick layout options for a standard unit type.

### Step 1: Boundary

For the geometry types each CAD tool accepts, see [What to select in each CAD tool](modeling-tips.md#what-to-select-in-each-cad-tool).

1. Click **Select / Update Boundary**. A selection bar opens.
2. Click **Select Unit Boundary** and select the closed outline of the unit. This can be a unit from your [unit mix](unit-mix.md) or any closed polyline.
3. Click **Select Entry Edge** and select the edge where the front door goes.
4. Click **Select Daylight Edge** and select the edges on the facade (where windows can go).
5. Click **Finish**.

!!! tip
    Termite puts rooms that need daylight, such as living rooms and bedrooms, along the daylight edges. Choose these edges carefully.

### Step 2: Topology and generate

1. Pick a **Category**:
    - **apartment**: studio, one bedroom, two bedrooms, three bedrooms or any
    - **hotel-room**: one to five beds, or any
2. Pick a **Type** from that category. Choose **any** to let Termite decide.
3. Options:
    - **With loggia**: add a loggia (a covered balcony).
    - **Furnished**: add furniture to the layout.
4. **Threshold**: the snapping tolerance Termite uses to clean up the lines of the layout. The default is fine in most cases.
5. Click **Generate Plan**.

A progress display shows what Termite is doing. When it is done, the layouts appear as thumbnails.

### Use the results

Click **Load in Rhino** (or **Load in Revit**, and so on) on a tile to draw the plan into your model: walls, rooms and labels, on separate layers.

To get other options, change the type or the boundary edges and generate again.

---

## Sketch mode

!!! info "Coming soon"
    Sketch mode is not available yet. Use **Explore** mode for now.

Sketch mode gives you full control over the layout. You will be able to:

- set your own list of rooms (the **topology**), with the area of each room and which rooms connect to each other
- add **preferred locations** (points that show roughly where a room should be)
- add **fixed geometries** (rooms whose shape and position are fixed)
- add an **axis grid** that the walls follow

Termite will then generate a plan that follows these inputs.
