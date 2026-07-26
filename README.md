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
- Pip dots on every number token, red 6/8

## Keyboard

- `Space` or `R` — generate a new map
- Enter a seed and press **Use** (or `Enter`) to reproduce a specific map

## Tournament mode

`tournament.html` (linked from the generator via **🏆 Tournament Mode**) runs a full Catan tournament night:

- Enter players (or quick-fill "Player 1…N"), qualifying rounds, tables + seats (3–6 each), and one map style for the event.
- **Everyone plays the same map each round** — view it inline on the tournament page, open it full-screen, or reroll it before play starts.
- Players are **auto-rotated** across tables each round to minimise repeat opponents, with **Move players** (tap to swap two players, move into an empty seat, or bench someone) and **re-pair** to reshuffle.
- Record results by **typing each player's VP (capped at 10)** — finishing places are worked out automatically as you type; equal VP counts as a tied place with split points.
- Scoring is **placement points** (4-player 5·4·2·1, 3-player 5·3·1) summed across games, with **total VP as the tiebreaker** — matching real Catan tournament practice.
- A **Players panel** handles real life: add a late arrival (they start on the bench, ready to be seated), drop someone who leaves (their points stay), or fix a name.
- Choose a **playoff format**: top 2–6 into a single final, or top 8 / 12 / 16 snake-seeded into **semifinal tables** whose winners advance to the final. A **bracket view** shows seeds → semis → final → champion at any point in the night.
- Everything **auto-saves to the browser**, so a refresh mid-night resumes where you left off.

> Note: with only a few tables, some rematches are mathematically unavoidable after round 1 (four players can't be spread across three prior tables without a collision) — the pairing minimises them to the floor.
>
> Tip: the generator accepts `embed=1` in its URL hash to render just the board (no sidebar) — that's how the tournament page embeds its map preview.

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
