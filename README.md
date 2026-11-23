# Cut Scene — Levels 1 + 2

This is the editable GitHub Pages build for The New Routines' *Cut Scene*.

## What is included

- The opening **KEEP DRIVING?** choice: **YES** briefly loops the wet road and returns; **NO** enters Level 1.
- Level 1 petrol-station food / bin sequence, release-date reveal, animated health reward and saved completion.
- Level 2 **Storm Field**: three ordered lit points, heavy rain, Frankie the labelled combine harvester, fox shake animation, lyric and a separate pre-save button.
- Mobile tap controls, a thumb-sized D-pad, and desktop arrow/WASD plus Space/E controls.
- A compact **REWARDS** menu and `localStorage` progress, which survives refreshes and returning from an external link.

## Before publishing

Open `index.html` and edit the two empty values near the top:

```js
const LINKS = {
  presave: '',
  soundcloud: ''
};
```

They are deliberately blank in this preview. A visible preview warning appears instead of opening a broken link. Add the full URLs when they are ready. The player opens each in a new tab, so their saved game remains behind it.

## Uploading to the existing GitHub repository

Upload the contents of this folder to the **root** of `thenewroutinesband/cutscene`, replacing the existing `index.html` and Level 1 images where prompted. Keep the existing `cutscene-video-game-sound.mp3` in the repository root: this update still uses it, but it is not duplicated here because the existing deployed copy is retained.

The public root should contain at least:

```text
index.html
level-01-environment.png
fox-sprite-sheet.png
bin-open.png
level-02-storm-field.png
frankie-combine.png
cutscene-video-game-sound.mp3  ← keep the existing file
```

GitHub Pages should remain set to **Deploy from a branch → main → /(root)**. Do not upload unreleased Level 3/4 art or a private demo to a public Pages repository: files deployed there can be downloaded by visitors even if the interface marks them locked.

## Local preview

From this folder, run:

```bash
python3 -m http.server 4173
```

Then visit `http://localhost:4173`. Browser autoplay rules mean music starts only after the first tap/key press. Make sure the existing MP3 is present beside `index.html` to test the music locally.

## Release checks

1. Test the game at a narrow phone width and in Instagram's browser.
2. Complete Level 1, refresh, and confirm Storm Field is unlocked.
3. Follow the three lights in order; off-target taps must not progress it.
4. Use the pre-save and SoundCloud links in a signed-out/private browser before launch.
5. Refresh after visiting a link and confirm the rewards stay unlocked.

