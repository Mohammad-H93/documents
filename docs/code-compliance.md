# Code compliance

Every office works with its own rules: building codes for the region, fire safety distances, and internal standards built up over years. Termite can follow these rules, so the plans it generates fit your regulations and your way of working.

There are three ways to set this up. You can use them on their own or together.

| | What Termite follows | Best for |
|---|---|---|
| **Learn from your drawings** | Your own plans: sizes, relations, design style | Offices with a library of past projects |
| **Custom rule dataset** | Rules we extract from your data: min/max sizes, fire safety distances | A default for your office that you can adjust per project |
| **Wall types in the settings** | The wall types you choose for each space | Drafting that must match technical standards |

---

## Learn from your drawings

Send us a set of your own drawings (DWG files of past projects). Termite is trained on them and learns how **you** design:

- **Sizes**: how large you make each type of room
- **Relations**: which spaces you put next to each other
- **Design style**: the layouts and proportions you prefer
- **Circulation**: how you organize hallways, entries and movement through a unit
- **Spatial arrangement**: how you place and group the spaces inside a unit

The result is a custom engine trained only on your data and used only by you. Your drawings are never shared or used to train Termite for anyone else. The plans it generates already look like your office's work and fit your workflow, so you spend less time correcting them.

Termite needs only a small set of plans to learn from (see [the generative core](about.md#the-generative-core-t_queen_1)). Custom engines run on a dedicated server and are part of the **Enterprise** plan (see [engines per plan](about.md#engines-per-plan)).

---

## Custom rule dataset

You don't need to write your rules down. We extract them from your data for you, and build a custom rule base that Termite follows when it generates plans. For example:

- the **minimum and maximum width** of each space
- the **minimum and maximum area** of each space
- **fire safety distances**, for example the longest allowed distance to an exit

From this rule base we make a **default** for your office, in the same way as the default of the general Termite dataset (Termite_General). Every new project starts with your default values.

In addition, you can change the default values for each project, depending on:

- the **region** and its regulations
- the **context** of the site
- the **type of project**, for example housing or hotel

When a value changes, the next plans Termite generates follow the new value. You can see the values Termite uses for a project in the [dataset program](settings.md#dataset-program) in the Settings tab.

---

## Wall types in the settings

Some rules are about how a plan is drafted, not only about its layout. For example, a toilet may need a wall of a certain type and thickness behind it for the plumbing, or your office may have internal standards for the walls around bathrooms or between units.

In the Termite **Settings** you can choose, per project, which wall types Termite uses: for the exterior walls, the default interior walls, and the walls of each space. When you load a generated plan into your model, Termite draws the walls with these types, so the drafting already follows the regulations you work with.

---

## Get started

To set up a custom engine or a custom rule dataset for your office, contact us at [info@termite.tools](mailto:info@termite.tools). Tell us which regions and project types you work on and which rules matter most to you, and we will prepare the setup with you.
