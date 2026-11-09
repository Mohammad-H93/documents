# Core concepts

Termite organizes your work like this:

```
Project
 └─ Floors
     ├─ Hallways
     ├─ Staircases   (can be shared by several floors)
     └─ Units  ──►  Spaces (bedroom, kitchen, ...)
```

---

## Project

A **project** is the container for one design. It holds your floors, hallways, staircases, generated units and plans. Everything is saved on the Termite server, so you can open the same project again later.

- **Create a project:** in the context bar, next to **Project**, click **+ New** and type a name.
- **Switch projects:** pick another project from the **Project** dropdown.
- The plugin remembers the last project you used and opens it next time.

A new project starts with the default list of spaces from the [dataset program](settings.md#dataset-program).

!!! note
    Deleting a project is not available yet.

---

## Floor

A **floor** is a closed outline: the footprint of one level of your building. Termite splits a floor into units.

- **Create a floor:** on the **Units** tab, type a floor name, click **Pick Boundary**, select a closed polyline and click **Send Floor**.
- **Pick a floor:** use the **Floor** dropdown in the context bar.
- **Draw it again in CAD:** click **⤓ Load** next to the Floor dropdown. The floor boundary is drawn into its own layer.
- **Rename or delete** a floor from the context bar.

!!! tip
    The boundary must be a **closed polyline**. Open shapes and true curves (arcs, splines) don't work. See [Modeling tips](modeling-tips.md).

---

## Hallway

A **hallway** is a corridor that runs through a floor. Termite keeps hallways free and places units along them.

- You draw a hallway as a **centerline**: a line through the middle of the corridor.
- Each hallway has a **name** and a **width** in meters. The default is 1.5 m.
- A hallway belongs to **one floor**.

Every floor **must** have at least one hallway before you generate a unit mix. See [Generate a unit mix → Hallways](unit-mix.md#step-2-hallways).

---

## Staircase

A **staircase** is a stair or core area that is not part of any unit, for example a stair or an elevator.

- You draw a staircase as a **closed polyline** around its footprint.
- One staircase can run through **several floors**. The **scope** sets which floors:
    - **Project**: every floor in the project
    - **Mass**: every floor of the current mass
    - Or type specific floor IDs to limit it to those floors.

Every floor **must** have at least one staircase before you generate a unit mix. See [Generate a unit mix → Staircases](unit-mix.md#step-3-staircases).

---

## Unit

A **unit** is one part of a floor: an apartment, an office, a shop and so on. Termite creates units for you when you [generate a unit mix](unit-mix.md).

Every unit has a **unit type**:

| Unit type | Default area | Daylight |
|---|---|---|
| Residential | 40 m² | preferred |
| Office | 60 m² | preferred |
| Retail | 80 m² | optional |
| Parking | 25 m² | none |
| Storage | 20 m² | none |

The **unit mix** is the share of each type on a floor, for example 70% residential and 30% retail.

---

## Space

A **space** is a room inside a unit: a living room, bedroom, kitchen, bathroom and so on. Termite places spaces when you [generate a plan](plan.md) for a unit.

Each space has an area, a daylight need (**required**, **preferred**, **optional** or **none**) and a minimum width. The full list of spaces is the **dataset program**. You can view it in [Settings](settings.md#dataset-program).
