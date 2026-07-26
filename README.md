# Catannis 🎲

A clean, fast **Catan map generator** — single HTML file, no build step, no dependencies.

👉 Live: `https://<your-username>.github.io/Catannis/`

## Features

- **3–4 player** (19 hexes) or **5–6 player expansion** (30 hexes)
- **Harbors/ports** on or off — docked to the actual coastline, with correct 2:1 / 3:1 mix
- **Balanced vs. fully random numbers**
  - *Balanced* (default): no two red numbers (**6** & **8**) ever touch
  - *Fully random*: anything goes
- **No same resource adjacent** (optional): avoids clumps of identical tiles
- **One-click / one-key regenerate** — `Space` or `R` for a fresh map
- **Seeds & shareable links** — every map has a seed; copy the link to share the exact board
- **Export PNG** — download the board as an image
- Pip dots on every number token, red 6/8, robber starts on the desert

## Keyboard

- `Space` or `R` — generate a new map
- Enter a seed and press **Use** (or `Enter`) to reproduce a specific map

## Tournament mode

`tournament.html` (linked from the generator via **🏆 Tournament Mode**) runs a full Catan tournament night:

- Enter players (or quick-fill "Player 1…N"), number of qualifying rounds, and the cut size (top N → final).
- Configure **each table independently** — seat count (3–6) and map settings — so one table can run the 5–6 expansion while others play the base game.
- Players are **auto-rotated** across tables each round to minimise repeat opponents (with a manual **swap** to override, and **re-pair** to reshuffle).
- Record results by **dragging players into finishing order** (1st at top) and typing each one's victory points — works with touch or mouse. Scoring is **placement points** (4-player 5·4·2·1, 3-player 5·3·1) summed across games, with **VP as the tiebreaker** — matching real Catan tournament practice.
- Live **standings** highlight who's in the cut; after the last round the top N seed into a single **Final**, then a champion + podium.
- Each table has a **Show map** button that opens the generator with that table's exact board.
- Everything **auto-saves to the browser**, so a refresh mid-night resumes where you left off.

> Note: with only a few tables, some rematches are mathematically unavoidable after round 1 (four players can't be spread across three prior tables without a collision) — the pairing minimises them to the floor.

## Publishing to GitHub Pages

1. Create a repo and push these files (`index.html` is all that's required).
2. Repo **Settings → Pages → Source: `main` branch, `/root`**.
3. Open the published URL — done.

The `.claude/` folder is only for local preview tooling and can be ignored or deleted.

## Ideas for later

- Pip-balance scoring / "fairness" meter per player position
- Lock individual tiles and reroll the rest
- Cities & Knights / Seafarers tile sets
- Light/dark themes and colorblind-friendly palettes
