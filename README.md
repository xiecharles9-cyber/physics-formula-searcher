# ⚛︎ Physics Formula Searcher

A free, fast, in-browser reference and calculator for **170+ physics formulas** — searchable by the *quantity* you care about. Type a variable like `displacement`, `force`, or `energy` and instantly see every equation that uses it.

**🔗 Live site:** https://xiecharles9-cyber.github.io/physics-formula-searcher/

---

## Features

- **Search by variable name** — find every formula containing a quantity (e.g. all equations with *velocity*), with the matching variable highlighted.
- **Search by symbol** — look things up by their math symbol instead (`λ`, `v`, `X_C`, `m₁`). Matches subscripted variants too.
- **Clickable variable chips** — click any variable under a formula to jump to all the other formulas that share it.
- **Built-in "solve for" calculators** — 165 of the formulas can solve for any variable: fill in what you know, leave one blank, press Solve. Physical constants (c, G, h, k_B, …) are pre-filled.
- **Unit conversion** — enter values in km/h, grams, eV, degrees, etc.; inputs convert to SI before solving and results convert back to your chosen unit.
- **5 languages** — full interface, category, variable, and formula translations in **English, Spanish, French, German, and Chinese**. Search works in the active language.
- **Category filter** — browse one topic at a time.
- **Zero dependencies** — a single self-contained HTML file. No build step, no frameworks, works offline.

## How to use

1. Open the [live site](https://xiecharles9-cyber.github.io/physics-formula-searcher/) (or open `index.html` locally).
2. Type a variable or formula name in the search box.
3. Optional toggles:
   - **Search by symbol** — switch matching to mathematical symbols.
   - **Show calculators** — reveal a 🧮 Calculator on each supported formula.
   - **Category** — narrow results to one branch of physics.
   - **Language** — switch the whole UI (remembered for next visit).

## Topics covered

Kinematics · Dynamics · Momentum · Energy & Work · Rotational motion · Gravitation ·
Waves & Sound · Optics · Fluids · Electricity & Magnetism · AC Circuits ·
Thermodynamics · Modern/Relativity · Nuclear · Astrophysics

## Run locally

It's a static site — no build needed. Just open the file, or serve the folder:

```bash
# option 1: open directly
open index.html

# option 2: serve (so relative links like the privacy page work cleanly)
python3 -m http.server 8137
# then visit http://localhost:8137/
```

## Project structure

| File | Purpose |
|------|---------|
| `index.html` | The entire app — markup, styles, formula data, translations, and logic. |
| `privacy.html` | Privacy policy (required for advertising). |
| `DOMAIN-SETUP.md` | How to attach a custom domain and enable Google AdSense. |
| `LICENSE` | Usage terms. |

## Custom domain & ads

See **[DOMAIN-SETUP.md](DOMAIN-SETUP.md)** for connecting a custom domain via GitHub Pages and wiring up Google AdSense (the ad code is already scaffolded in `index.html` — you just add your publisher and slot IDs).

## License

© 2026 — All Rights Reserved. You're welcome to use the live site; see [LICENSE](LICENSE) for terms on copying or reusing the code.

## Disclaimer

This is an educational reference tool. The calculators use exact algebraic rearrangements and standard constant values, but always verify important results and mind significant figures.
