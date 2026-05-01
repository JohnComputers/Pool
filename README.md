# The Velvet Cue — 8-Ball

A self-contained, top-down 8-ball pool game playable in any modern browser. Single HTML file. Zero dependencies. Drops straight onto GitHub Pages.

## Features

- **Full 8-ball rules**: open table assignment after the break, group lock-in (solids/stripes), proper foul detection (wrong-ball-first, no-rail-after-contact, scratch), ball-in-hand on fouls, and 8-ball win/loss conditions.
- **Real-feel physics**: per-frame friction, elastic ball-to-ball collisions, cushion bounces with realistic restitution, and pocket capture logic with a drop-in animation.
- **Three AI opponents** at different skill levels — Margaux (casual), Lucien (steady), Vivian (sharp). Each evaluates ghost-ball positions, checks for path obstructions, scores shots by cut angle and distance, and adds skill-appropriate aim/power jitter.
- **Aim assist line** that traces the cue's path until it hits a ball or cushion, plus a ghost-ball indicator showing the projected impact and target trajectory.
- **Pull-back-to-shoot controls**: hold and drag away from the cue ball to charge power, release to strike. Touch-supported.
- **Pocketed-ball racks** for each player and group badges that update live as the table state changes.
- **Saved progress**: lifetime wins, matches played, and longest run-out persist in `localStorage`.

## Deploy to GitHub Pages

1. Create a new GitHub repository (public).
2. Drop `index.html` (and optionally this `README.md`) into the repo root.
3. In the repo: **Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: `main` / `(root)`**.
4. Wait ~30 seconds. Your site is live at `https://<your-username>.github.io/<repo-name>/`.

No build step, no framework, no `package.json`.

## Run locally

Open `index.html` directly, or serve with anything:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Controls

- **Move mouse** — aim the cue stick toward your target.
- **Press and hold** — start charging power; drag *away* from the cue ball to increase power. The on-screen meter and the cue's pull-back animation track your input.
- **Release** — strike. Release with very little power to cancel the shot.
- **Ball in hand** — when awarded after a foul, click anywhere legal on the table to place the cue ball.

## Tech

- Vanilla HTML / CSS / JS in one file.
- Canvas 2D for the table, balls, cue stick, and aim assist.
- Pre-rendered background canvas (felt, rails, pockets, diamonds) for performance.
- Two Google Fonts loaded for the salon aesthetic (Playfair Display + Outfit + JetBrains Mono).
- No external libraries, no API keys, no build tools.

## License

Do whatever you want with it. Have fun.
