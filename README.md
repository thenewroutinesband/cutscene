# Cut Scene — Levels 1, 2 + 3

This is the GitHub Pages build for The New Routines' *Cut Scene*.

## What remains unchanged

Level 1, Level 2, their visual design, their gameplay, their existing sound files, and their existing asset folders are preserved. Level 3 is a separate page and its files live only in `assets/level3/`.

## Level flow

1. **01 / THE PETROL STATION** is the original approved level.
2. **02 / THE STORM FIELD** unlocks after Level 1.
3. **03 / WHO DO YOU LOVE?** unlocks after Level 2 and opens `level3.html`.
4. **04 / THIS SUCKER IS NUCLEAR!** remains locked. It is not unlocked by completing Level 3, because future levels will be released on their own calendar schedule.

## Level 3 — Who Do You Love?

- A portrait-first, faux-isometric concert venue where the fox travels from the rear of a packed crowd to the female fox at the stage barrier.
- The venue keeps the established dark purple, magenta, amber and teal *Cut Scene* look. The final concert reference informs the stage, audience density, lighting and four-member band layout.
- Eight fair crowd rows alternate between stationary people and slow moving people. The crowd has generous gaps and multiple routes so the level remains approachable on a phone.
- Arrow keys, WASD and the four-way D-pad move the fox one grid space at a time. Higher rows sit further back in the concert perspective, while the controls remain intuitive: up is towards the stage.
- A person moving into the fox causes a gentle reset to the rear of the venue. There are no hearts or lives to lose. The message **NOW YOU'RE FEELING FUNNY IN A MOSHPIT** appears for three seconds before play resumes automatically.
- The four on-stage band members retain the supplied concert composition and receive lightweight instrument, microphone, drum and lighting animations. The supplied pixel **THE NEW ROUTINES** logo now sits on the rear wall behind them. The stage uses soft amber, purple and teal sweeps rather than harsh strobing; the **LIGHTS** button can disable them.
- The supplied Level 3 *Cutscene* clip starts after **START SHOW**, loops continuously during play, keeps playing through a moshpit reset, and fades naturally at the end. The **SOUND** button can mute it.
- Reaching the tile beside the female fox pauses the crowd, shows **WHO DO YOU LOVE THAT YOU CAN'T SEE?** for three seconds, then presents the final message: **NOT LONG NOW — CUTSCENE OUT JANUARY 15TH 2027**. The final card stays onscreen until the player selects **LEVELS**.

## Files

```text
index.html                                Original Level 1 + level-selection integration
level2.html                               Standalone Level 2 maze (unchanged by Level 3)
level3.html                               Standalone Level 3 concert-crowd level
level-01-environment.png                  Original Level 1 background
fox-sprite-sheet.png                      Original Level 1 fox animation sheet
bin-open.png                              Original Level 1 bin
cutscene-video-game-sound.mp3             Original Level 1 music
assets/level2/                            Existing Level 2 files (unchanged by Level 3)
assets/level3/concert-venue.png           Supplied concert venue artwork
assets/level3/concert-mockup.png          Supplied final concert visual reference / title backdrop
assets/level3/crowd-sprite-sheet.png      Supplied human crowd source artwork
assets/level3/fox-sprite-sheet.png        Supplied male and female fox source artwork
assets/level3/cutscene-level-3.mp3        Approved Level 3 Cutscene promotional clip
```

Level 3 removes the baked checkerboard from the supplied crowd and fox sheets in the browser, caches the resulting pixel sprites, and renders the venue in one canvas. This keeps the original source art untouched, avoids blurry scaling, and is lightweight enough for mobile browsers.

## Progress

The game stores completion locally in the browser:

- `cutscene-level-one`
- `cutscene-level-two`
- `cutscene-level-two-presave-opened` (only once a real pre-save URL is set)
- `cutscene-level-three`

Progress is per browser/device. To test as a completely new player, clear the GitHub Pages site's website data in that browser.

## Updating an existing Level 1 + 2 build with Level 3

For the Level 3 release, add or replace only these items at the repository root:

```text
index.html
level3.html
README.md
assets/level3/   (upload this new folder and its five files)
```

Do **not** delete or replace `level2.html`, any Level 1 files, `assets/level2/`, or the Level 1 and Level 2 music files.

## Local preview

From this folder, run:

```bash
python3 -m http.server 4173
```

Then open `http://localhost:4173/`. A local server is preferable to opening the files directly because browser audio behaviour is closer to GitHub Pages and Instagram's in-app browser.

## Deploy to GitHub Pages

Upload the contents of this folder to the root of `thenewroutinesband/cutscene` on the `main` branch. Do not upload the enclosing folder or a ZIP file.

After committing, GitHub Pages should publish from `main` / `(root)` at:

`https://thenewroutinesband.github.io/cutscene/`
