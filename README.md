# Cut Scene — Art-first Level 1

This is the revised **GitHub Pages** build for The New Routines' *Cut Scene*. It is not a Netlify project.

The game contains:

- A new, original square pixel-art petrol-station scene made as a separate game environment.
- A separate animated fox sprite sheet and a clearly readable interactive wheelie bin.
- Level 1 unlocked and playable; Levels 2–4 visible but locked.
- An animated health reward: one heart becomes five in the centre of the screen, then returns to the top-left HUD.
- The supplied `Cutscene - Video game sound.mp3` music, with local-file fallback playback and the tighter hosted loop path.

## Upload to the existing GitHub repository

1. Download and unzip `cut-scene-github-pages-level-1-art-first-v3.zip`.
2. Open `thenewroutinesband/cutscene` on GitHub.
3. Choose **Add file → Upload files**.
4. Upload the files **inside** the unzipped folder, not the enclosing folder and not the ZIP itself.
5. When GitHub asks, choose to replace the existing `index.html` and any matching assets, then commit directly to `main`.

The important web files are all in this folder's root:

- `index.html`
- `level-01-environment.png`
- `fox-sprite-sheet.png`
- `bin-open.png`
- `cutscene-video-game-sound.mp3`

`README.md` and `.nojekyll` can be uploaded too. If Finder hides `.nojekyll`, GitHub Pages will still serve this plain static website correctly.

In **Settings → Pages**, use **Deploy from a branch**, then select `main` and `/(root)`. GitHub Pages republishes automatically after every later commit to `main`.

## Future vignettes

For Level 2, Level 3, and Level 4, use this same repository. Each new complete package will add the new scene and update the menu logic; once committed to `main`, the public GitHub Pages game automatically updates.
