# About Termite

## Current version

| | |
|---|---|
| **Plugin version** | 0.1.0 (first public release) |
| **Generative core** | T_QUEEN_1 |
| **Dataset** | Termite_General |

You can always see the generative core and dataset you are using in the [Termite bar](settings.md#the-termite-bar).

---

## The generative core: T_QUEEN_1

**T_QUEEN_1** is the AI engine behind Termite. It generates floor plans for **residential buildings**, mainly **apartments**.

It was trained on Termite's own internal dataset of **100 architectural plans**.

### What makes it different

Most AI models need very large datasets. T_QUEEN_1 is built to:

- **learn from very little data**: a small set of plans is enough to train it
- **handle complex geometry**: irregular, angled and non-rectangular boundaries
- **predict shapes it has never seen**: it generates good layouts for boundaries that are not in its training data

This means Termite works on your real project shapes, not only on simple rectangles.

---

## Engines per plan

| Plan | Engine | Server |
|---|---|---|
| **Free** | General engine (T_QUEEN_1 on the Termite_General dataset) | Shared |
| **Pro** | General engine (T_QUEEN_1 on the Termite_General dataset) | Shared |
| **Enterprise** | Custom engine trained on **your own plans** | Dedicated server with dedicated resources |

### Enterprise: train on your own plans

Because T_QUEEN_1 needs only a small dataset, it can be trained on the plans of your office. Then the generated layouts follow your own design language, standards and typologies.

Enterprise customers get:

- a **dedicated server** with dedicated resources
- a **custom engine trained on their own dataset** of plans
- a **training service**: the Termite team prepares the data, trains the engine and sets it up for you

To discuss an Enterprise setup, contact us at [info@termite.tools](mailto:info@termite.tools).
