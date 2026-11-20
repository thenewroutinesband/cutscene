# CUTSCENE — The New Routines

The complete static web game for **Cut Scene**. It includes the fox level, the supplied petrol-station artwork, and the looping song extract.

## Contents

- `index.html` — the whole game
- `assets/cut-scene-remix.mp3` — the looping music
- `assets/petrol-station-still.png` — the supplied visual

## Put it on GitHub

1. Create a new empty repository on GitHub, such as `cut-scene`.
2. Upload the **contents of this folder** (not the outer ZIP folder). `index.html` and the `assets` folder must sit at the repository root.
3. Commit the upload.

The project has no install or build step: it is ready to publish as-is.

## Publish from GitHub with Netlify

1. In Netlify, choose **Add new project** → **Import an existing project** → **GitHub**.
2. Select this repository.
3. Leave the build command empty. Netlify uses the included `netlify.toml` to publish the repository root.
4. Deploy.

## Publish with GitHub Pages (optional)

On GitHub, open **Settings** → **Pages**, choose **Deploy from a branch**, then select `main` and `/(root)`. GitHub will give you a shareable URL.

## Audio note

Modern phone and desktop browsers do not permit music to start before a person interacts with a page. The game deliberately begins the song after the player taps **YES** on the opening screen. The MP3 is already included in this package; no separate asset upload is needed.
