# Termite Documentation

**Termite** is an AI design assistant for the early design phase. It works inside the CAD tool you already use (**Rhino**, **Revit**, **Archicad** or **Grasshopper**). You draw a floor boundary, and Termite splits it into units and generates apartment or hotel-room layouts for you.

---

## Watch Termite in action

Three short videos, about 5 minutes in total, from an empty model to a finished floor plan.

<div class="video-grid">
<div class="video-card">
<div class="video-embed">
  <iframe src="https://www.youtube-nocookie.com/embed/6YNZEUb26Cc" title="Create a project, floors, staircases and hallways" loading="lazy" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
  <p><strong>1. Create a project, floors, staircases and hallways</strong><br><a href="unit-mix/">Read the steps →</a></p>
</div>
<div class="video-card">
<div class="video-embed">
  <iframe src="https://www.youtube-nocookie.com/embed/pbCTqdv-l3w" title="Generate a unit mix for each floor" loading="lazy" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
  <p><strong>2. Generate a unit mix for each floor</strong><br><a href="unit-mix/#step-4-preferences-and-generate">Read the steps →</a></p>
</div>
<div class="video-card">
<div class="video-embed">
  <iframe src="https://www.youtube-nocookie.com/embed/gZMrHFXYjZE" title="Generate a floor plan" loading="lazy" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
  <p><strong>3. Generate a floor plan</strong><br><a href="plan/#explore-mode">Read the steps →</a></p>
</div>
</div>

<p class="video-note">Shown in Archicad. The steps are the same in Rhino and Revit.</p>

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
