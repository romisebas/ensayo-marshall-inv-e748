# Design

Visual system of the Marshall study guide (`site/index.html`). Direction: "Columna del núcleo". The page reads like a core log: each section is a stratum with its own hatch, and the reader goes down the specimen.

## Color

Restrained strategy: an asphalt frame, a calm reading ground and a single heat accent.

| Token | Light | Dark | Use |
|---|---|---|---|
| `--asphalt` | `#1c1b19` | same | Masthead, rail, simulator, footer |
| `--asphalt-2` / `-3` | `#262420` / `#34312b` | same | Active layer, hatch ground, frame lines |
| `--bone` / `--bone-2` | `#e9e6df` / `#a9a49a` | same | Text on asphalt |
| `--stone` | `#e6e8e6` | `#1f2120` | Reading ground (cool limestone) |
| `--paper` | `#f3f4f2` | `#252826` | Tables, definitions, calculator |
| `--ink` / `--ink-2` | `#191b1a` / `#4a504e` | `#e7e9e7` / `#a9b0ad` | Body and secondary text |
| `--rule` | `#c3c8c5` | `#3c413e` | Hairlines |
| `--heat` | `#e8590c` | `#f07a3a` | Hot-mix orange: temperatures, the active layer, the "aquí quedé" flag |
| `--heat-ink` | `#b23f00` | `#ff9a5e` | Heat values set as text |
| `--agg-1..3` | `#6f726f` `#9a9e9a` `#c4c7c3` | same | Aggregate grays for hatches |

Rule: orange only marks heat or "where you are". Text on orange is `--asphalt`, never white.

## Type

- Display: Archivo, width axis around 68 to 85 %, weights 700 to 850. h1 uppercase at up to 10.5rem.
- Reading: Atkinson Hyperlegible, 17px (16.5px on phones), measure up to 72ch. Picked for legibility on a phone in the lab.
- Numbers and units: JetBrains Mono, tabular figures. Only for data, never for prose.

## Components

- Strata rail: a sticky column of layers whose height follows section length. Each layer carries a hatch (dots for asphalt, diagonals, gravel, horizontal lines, crosshatch, fine dots, sand). On screens under 1000px it turns into a horizontal strip at the top.
- Section opener: a 14px band with the section's hatch, then the h2.
- Steps: a numbered circle plus a vertical line. Dashed = pending, solid = done. State is line form, not color. Saved in localStorage.
- Alert: a heat-washed box with a 1px heat outline and the flag icon. No side stripe.
- 3D: three.js r160 from jsDelivr. Procedural asphalt texture (canvas) with bump. Hero specimen 102 x 63.5 mm at scale 1 unit = 100 mm; failure simulator with steel jaws.

## Motion

One authored moment: the hero specimen settles from a tilt in 1.4s (ease-out quart), then rotates slowly. Buttons press to `scale(.97)`. Everything respects `prefers-reduced-motion`. Canvases render only while visible.
