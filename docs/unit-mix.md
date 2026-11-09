# Generate a unit mix

The **Units** tab splits a floor into units. You give Termite the floor outline, any hallways and staircases, and the mix of unit types you want. Termite returns several options.

Make sure a **project** is selected in the context bar first. See [Core concepts](concepts.md#project).

Not sure which geometry to select? See [What to select in each CAD tool](modeling-tips.md#what-to-select-in-each-cad-tool).

The tab has four steps. **All four are required**: a floor needs a boundary, hallways and staircases before Termite can generate units.

---

## Video: project, floors, staircases and hallways

<div class="video-embed">
  <iframe src="https://www.youtube-nocookie.com/embed/6YNZEUb26Cc" title="Create a project, floors, staircases and hallways" loading="lazy" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
<p class="video-note">Shown in Archicad. The steps are the same in Rhino and Revit. For what to select in your tool, see <a href="../modeling-tips/#what-to-select-in-each-cad-tool">What to select in each CAD tool</a>.</p>

---

## Step 1: Floor boundary

1. Type a **Floor Name**, for example `Level 01`. If you leave it empty, Termite names it `Floor 1`, `Floor 2` and so on.
2. Click **Pick Boundary** and select the closed polyline of the floor in your model.
3. Click **Send Floor**.

The new floor appears in the **Floor** dropdown and is selected.

!!! note
    If a floor with the same name already exists, Termite asks whether to **update** it.

---

## Step 2: Hallways

!!! warning "Required"
    Every floor needs at least one hallway. Termite places the units along the hallways.

1. Click **Select Centerlines** and select one or more lines that run through the middle of your corridors.
2. Every hallway appears as a row. Change its **name** and **width** if needed.
3. Click **Submit**.

Row buttons:

- **Remove**: removes the row from this list only. The saved hallway stays on the server.
- **Delete**: deletes the hallway permanently.
- **↻ Refresh**: reloads the saved hallways for the current floor.

---

## Step 3: Staircases

!!! warning "Required"
    Every floor needs at least one staircase. Termite uses it as the escape route for the fire safety distance.

1. Choose the **Scope**:
    - **Mass**: the staircase is on every floor of the current mass.
    - **Project**: the staircase is on every floor of the project.
2. Click **Select Staircase Regions** and select one closed polyline for each staircase.
3. To limit a staircase to certain floors, type their IDs in **Floors (ids, blank = all)**.
4. Click **Submit**.

**Remove**, **Delete** and **↻ Refresh** work the same way as for hallways.

---

## Step 4: Preferences and generate

<div class="video-embed">
  <iframe src="https://www.youtube-nocookie.com/embed/pbCTqdv-l3w" title="Generate a unit mix for each floor" loading="lazy" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
<p class="video-note">Shown in Archicad. The steps are the same in Rhino and Revit. For what to select in your tool, see <a href="../modeling-tips/#what-to-select-in-each-cad-tool">What to select in each CAD tool</a>.</p>

### Unit mix table

Add one row for each unit type you want:

| Column | Meaning |
|---|---|
| **Name** | The unit type, for example Residential or Office |
| **Percentage %** | The share of the floor for this type |
| **Area** | The target area of one unit, in m² |

!!! warning
    The percentages must add up to **100%**. If they don't, Termite shows a warning and does not generate.

**Example:** 80% Residential at 45 m² and 20% Retail at 80 m².

### Constraints

| Setting | Default | Meaning |
|---|---|---|
| **Min unit width (m)** | 3.5 | No unit is narrower than this |
| **Fire safety distance (m)** | 15 | The maximum distance from a unit to an escape route |

### Advanced (optional)

Click **▸ Advanced** to fine-tune the generator. The defaults work well for most cases.

| Setting | Default | Meaning |
|---|---|---|
| **Number of Results** | 3 | How many options you get (1–10) |
| **Exploration per Iteration** | 10% | How much each round tries new ideas. Higher means more variety. |
| **Iterations** | 100 | How long Termite searches (50–250). More iterations give better results but take longer. |

### Generate

Click **Generate Units**. The status line shows the progress. When the run is done, the results appear as thumbnails.

---

## Use the results

- Every result is a tile named `Result #…`.
- Click **Load Units** on a tile to draw that result into your model. Each unit gets its own outline and a label (`Unit 1`, `Unit 2`, …).
- To try other options, change the mix or the constraints and generate again.

Next: pick a unit and [generate a plan](plan.md) for it.
