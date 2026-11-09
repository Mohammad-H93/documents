# Getting started

## 1. Sign in to the portal

Create an account or sign in at [termite.tools](https://termite.tools). The portal is your account page. It has four tabs:

| Tab | What it is for |
|---|---|
| **Overview** | Your Termites balance, your **access token** and your plan |
| **Plugins** | Download the plugins for Rhino, Revit, Archicad and Grasshopper |
| **Usage** | A history of every Termite you received or used |
| **Billing** | Buy more Termites |

### Your access token

The access token connects a plugin to your account. Find it on the **Overview** tab, then click **Show** or **Copy token**.

!!! warning "Keep your token private"
    Anyone who has your token can use your account. Do not share it or post it online.

### Termites and plans

**Termites** are credits. Termite uses them when it generates something, for example a unit mix or a plan layout. The **Overview** tab shows your balance and the current cost of each action.

- Every account gets **20 free Termites per month**.
- If you need more, buy a package on the **Billing** tab (payment through Stripe). Buying Termites also upgrades your account to **Pro**.
- The **Usage** tab lists every action and how many Termites it used.

---

## 2. Install a plugin

1. Open the **Plugins** tab in the portal.
2. Click **Download** next to your CAD tool.
3. Run the installer. When it asks for your **access token**, paste the token you copied from the **Overview** tab.
4. Start your CAD tool. The Termite panel is now available.

!!! note "Windows warning"
    Windows may show a "Windows protected your PC" message while you install. Click **More info** → **Run anyway**.

### Where to find Termite in each tool

| CAD tool | How Termite shows up |
|---|---|
| **Rhino** | A Termite panel inside Rhino |
| **Revit** | A Termite pane inside Revit |
| **Archicad** | A separate **Termite** app (Start menu or desktop shortcut). It connects to the open Archicad project. Supported versions: Archicad 26–29. |
| **Grasshopper** | A set of Termite components on the canvas. Each step in these docs is one component. |

The panel looks and works the same way in Rhino, Revit and Archicad. The screens in these docs use Rhino.

---

## 3. The Termite panel

The panel has three parts, from top to bottom:

1. **Termite bar**: a collapsible bar with notifications and the Stop, Refresh, Update and Profile buttons. See [Settings](settings.md#the-termite-bar).
2. **Context bar**: three dropdowns that pick what you are working on:
    - **Project**: the active project
    - **Mass**: the building mass the floors belong to
    - **Floor**: the active floor
3. **Tabs**:
    - **Units**: define floors, hallways and staircases, then generate a unit mix. See [Generate a unit mix](unit-mix.md).
    - **Plan**: generate a floor plan for one unit. See [Generate a plan](plan.md).
    - **Settings**: the dataset program. See [Settings](settings.md).

Next, read [Core concepts](concepts.md).
