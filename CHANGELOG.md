# Changelog

All notable changes to this project are documented in this file.
The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.5.0] - 2026-10-19
> Commits: `6f9ab2f`

### Script
- **Changed**: Rewritten around the `data-cloze` attribute rendered by Anki; clozes are no longer converted into links.
- **Changed**: Event listeners are scoped per card with an `AbortController`, preventing duplicated listeners across cards on Anki Desktop.
- **Changed**: Native smooth scrolling replaces the custom scroll animation; the first action scrolls to an off-screen cloze, the next one reveals it.
- **Removed**: `scrollDuration` setting.
- **Added**: `ankiMobileTapZone` setting to choose the AnkiMobile tap zone used by auto flip.
- **Fixed**: Front-side shortcuts no longer act on the back side when the back template has no script.
- **Fixed**: The last cloze can be hidden when auto flip is off.
- **Fixed**: Vertical scrolling on touchscreens no longer counts as a swipe.
- **Fixed**: Shortcuts with Ctrl, Alt or Cmd (e.g. Alt+←) are passed to the browser and Anki.
- **Fixed**: Holding a key down no longer reveals every cloze and flips the card at once.
- **Fixed**: Shortcuts are ignored while typing in an answer field.
- **Fixed**: AnkiWeb detected by its domain instead of page text; AnkiDroid also detected through `window.ankiPlatform`.

### Styling
- **Added**: Touch rules for hidden clozes (`touch-action`, `pointer-events`) so tapping a cloze containing MathJax no longer opens AnkiDroid's editor.
- **Added**: Hidden clozes stay tappable above overlays covering the card, such as AnkiDraw's canvas.
- **Fixed**: AnkiDroid no longer shifts the page vertically when the card is flipped after scrolling to a cloze.
- **Changed**: The next cloze is highlighted with an underline; long clozes now wrap across lines.
- **Changed**: Softer cloze color in light mode (`#9b2c2c`).
