# Termite Documentation

**Termite** is an AI design assistant for the early design phase. It works inside the CAD tool you already use (**Rhino**, **Revit**, **Archicad** or **Grasshopper**). You draw a floor boundary, and Termite splits it into units and generates apartment or hotel-room layouts for you.

---

## How Termite works

There are three steps:

1. **Sign in to the portal.** On [termite.tools](https://termite.tools) you get your access token, download the plugins and manage your plan.
2. **Install the plugin** for your CAD tool and enter your access token.
3. **Design inside your CAD tool.** Create a project, define floors, generate a unit mix and then generate floor plans for the units.

```
Portal  ──►  Plugin (Rhino / Revit / Archicad / Grasshopper)
             │
             └─ Project
                 └─ Floors ──► Unit mix ──► Plan layouts
```

All your work is saved under a **project** on the Termite server. You can close your CAD tool and come back to it later.

---

## Where to go next

| Page | What you learn |
|---|---|
| [About Termite](about.md) | Current version, the T_QUEEN_1 engine, Free / Pro / Enterprise engines |
| [Getting started](getting-started.md) | Portal, access token, plans and Termites, installing a plugin |
| [Core concepts](concepts.md) | What projects, floors, hallways, staircases, units and spaces are |
| [Generate a unit mix](unit-mix.md) | The **Units** tab: split a floor into units |
| [Generate a plan](plan.md) | The **Plan** tab: Explore mode and Sketch mode |
| [Settings](settings.md) | The **Settings** tab and the Termite bar |
| [Modeling tips](modeling-tips.md) | Polylines vs. curves, edge sizes, levels in Revit/Archicad, layers in Rhino |

---

Questions? Email us at [info@termite.tools](mailto:info@termite.tools).
