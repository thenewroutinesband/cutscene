# Cut Scene — Levels 1 + 2 (Field Maze)

This is the GitHub Pages build for The New Routines' *Cut Scene*.

## What is deliberately unchanged

`index.html`, Level 1, the opening screen, Level 1 controls, Level 1 music and Level 1 visual UI start from the approved `CS - V3 - Final` source. The only Level 1 menu change is the existing **02 / THE STORM FIELD** card: it unlocks once Level 1 is completed and opens `level2.html`.

## Level 2

- A top-down, rain-soaked field maze with subtle dirt paths rather than a bright visible grid.
- The fox begins in the bottom-left, automatically heads north after a 3–2–1 countdown, and keeps moving until directed elsewhere.
- Four-way D-pad plus Arrow keys/WASD. A blocked direction makes the fox wait for a new direction.
- Frankie is a friendly combine harvester who follows the same valid paths, slightly more slowly than the fox.
- Five hearts = five attempts. A catch plays a light failure cue, removes one heart, and restarts after a fresh countdown. At zero hearts the game returns to the level-selection screen.
- The shelter completes the level, shows the lyric, then unlocks the **PRE-SAVE CUTSCENE** reward screen.
- The supplied Level 2 clip plays only during Level 2 gameplay, loops while running, and restarts from the beginning after a catch.

## Files

```text
index.html                         Level 1 + level-selection integration
level2.html                        Standalone Level 2 maze
level-01-environment.png           Original Level 1 background
fox-sprite-sheet.png               Original Level 1 fox animation sheet
bin-open.png                       Original Level 1 bin
cutscene-video-game-sound.mp3      Original Level 1 music
assets/level2/fox-topdown-v1.png   New top-down Level 2 fox
assets/level2/frankie-combine-topdown-v1.png
assets/level2/cutscene-level-2.mp3 Supplied Level 2 music clip
```

## Pre-save link

Open `level2.html` and edit the value at the top of its script:

```js
const PRESAVE_URL = '';
```

Paste the final pre-save URL between the quotes. Until then, the reward button safely says **LINK COMING SOON** and opens nothing.

## Progress

The game stores completion locally in the browser:

- `cutscene-level-one`
- `cutscene-level-two`
- `cutscene-level-two-presave-opened` (only once a real pre-save URL is set)

This keeps unlocked levels after refreshes and returning from a pre-save visit. To test as a completely new player, clear the website data for the GitHub Pages site in the browser.

## Local preview

From this folder, run:

```bash
python3 -m http.server 4173
```

Then open `http://localhost:4173/`. A local server is preferable to opening the files directly because browser audio rules are closer to GitHub Pages and Instagram's in-app browser.

## Deploy to GitHub Pages

Upload the **contents of this folder** to the root of `thenewroutinesband/cutscene` on the `main` branch. Do not upload the enclosing folder or a ZIP file.

The important difference from the previous rejected combined build is that this package begins from the approved Level 1 source. It restores the original Level 1 interface and adds Level 2 in `level2.html` rather than rebuilding Level 1.

After committing, GitHub Pages should publish from `main` / `(root)` at:

`https://thenewroutinesband.github.io/cutscene/`
