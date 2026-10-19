# Cloze Interactive

This is a script for Anki that enhances the functionality of cloze cards, allowing individual revelation and hiding of clozes still on the front of the card. It supports touch gestures and keyboard shortcuts. It is compatible with AnkiDroid, AnkiMobile and supports MathJax rendering.

![Demonstration of Cloze Interactive](https://github.com/huandney/Anki-Cloze-Interactive/assets/19948348/5c64a125-97ef-4ae8-9855-327765ccc5c6)

## Features

- **Individual Cloze Reveal:** No more revealing all clozes at once!
- **Touch Gestures:** Set your preferred gesture using User Action in AnkiDroid/AnkiMobile; swipe gestures are auto-enabled for AnkiWeb and AnkiDesktop with touchscreens.
- **Keyboard Shortcuts:** Use keyboard shortcuts to reveal or hide clozes.
- **Auto Scroll:** Enhance your reading experience with a smooth auto scroll to the next cloze.
- **Auto Flip:** The card is automatically flipped after revealing all the clozes, if enabled.
- **MathJax Support:** Include complex mathematical equations in your clozes with MathJax rendering.
- **Highlight Cloze:** Highlights the next cloze to guide your focus.

## Installation

There are two ways to install the Cloze Interactive script:

### Option 1: Import the Deck

1. Download the `.apkg` file from the [releases page](https://github.com/huandney/Anki-Cloze-Interactive/releases) on GitHub or from [AnkiWeb](https://ankiweb.net/shared/info/1523903214).
2. After the file is downloaded, double-click on it to open it in the desktop program. If asked which application to use, choose Anki.
3. The deck should now be imported into your Anki app.

### Option 2: Manual Installation

1. Navigate to the [card folder](https://github.com/huandney/Anki-Cloze-Interactive/tree/main/card) in the GitHub repository.
2. Copy the contents of the `front-template.html` file.
3. Open your Anki Desktop app. In the main Anki window, go to **Tools → Manage Note Types** and find the Cloze note type where you want to enable the Cloze Interactive script. Proceed by clicking on **Cards** to invoke the card template editor.
4. Replace your existing front template with the copied content.
5. Repeat the process for the `styling.css` file, replacing your existing styling. If you keep your own styling, copy only the rules under `CLOZE INTERACTIVE`; they are required for tapping clozes on touch devices.

> Please note that these instructions are for the Anki Desktop app. The process may vary slightly for AnkiMobile or AnkiDroid.

> **Using `{{FrontSide}}` on the back template?** Wrap the back template in an element with `class="back"` (e.g. `<div class="back">…</div>`), so the script knows it is on the answer side and stays inactive.

## Usage

- Click a cloze to reveal it.
- On touchscreen devices, tap a cloze to reveal or use gestures (for AnkiDroid/AnkiMobile, configure swipe gestures via User Actions; on AnkiDesktop and AnkiWeb, swipe right to reveal or left to hide clozes).
- Use keyboard shortcuts to reveal or hide clozes. Default keys: `W` or `→` for the next cloze, and `Q` or `←` to hide a cloze.

> Both gestures and keyboard shortcuts can be customized in the script's user settings.

## Configuration

You can customize the script's behavior by modifying the user settings at the top of the script. Here are the available options:

- `gesturesEnabled`: Enables or disables gestures on AnkiDesktop and AnkiWeb with touch screens.
- `invertGestures`: Inverts the touch gestures, only AnkiDesktop and AnkiWeb.
- `swipeThreshold`: Adjusts the swipe sensitivity (in pixels). Only mostly horizontal swipes are counted, so vertical scrolling never reveals or hides clozes.
- `autoFlip`: Controls whether the card automatically flips to the back after all clozes are revealed. Options include `"all"`, `"off"`, or specific platforms like `["AnkiDesktop", "AnkiDroid", "AnkiMobile", "AnkiWeb"]`. When the card does not flip, the last revealed cloze can still be hidden.
- `ankiMobileTapZone`: The AnkiMobile tap zone used by `autoFlip` (default `"midCenter"`). See the note below.
- `revealNextKeys`: Sets the keys to reveal the next cloze.
- `hideLastKeys`: Sets the keys to hide the last revealed cloze.
- `highlightCloze`: This option controls whether the next cloze to be revealed is visually highlighted. If enabled, the cloze will use the styles defined in the `.highlight-cloze` class from your CSS. You can customize these styles to suit your preferences.

> **Note for AnkiMobile users:** AnkiMobile offers no command for card scripts to show the answer, so `autoFlip` simulates a tap on a screen zone. In AnkiMobile's settings, map a tap zone to **Show Answer** and set `ankiMobileTapZone` to the same zone. Zone names combine a row (`top`, `mid`, `bottom`) with a column (`Left`, `Center`, `Right`), e.g. `"midCenter"` or `"bottomRight"`. This relies on AnkiMobile's private API and may break in future updates.

> Keyboard shortcuts ignore key combinations with Ctrl, Alt or Cmd, and holding a key down reveals only one cloze.

### User Actions: Gestures on AnkiDroid and AnkiMobile
Gestures are not automatically enabled on AnkiDroid and AnkiMobile. Follow these steps:

<details>
  <summary><strong>AnkiDroid</strong></summary>
  
  1. Go to **Settings**.
  2. Navigate to **Controls**.
  3. Enable gestures.
  4. Under **User Actions**, configure a preferred gesture. Set **User Action 1** to reveal the next cloze and **User Action 2** to hide the last revealed cloze.
</details>

<details>
  <summary><strong>AnkiMobile</strong></summary>
  
  1. Go to **Settings**.
  2. Navigate to **Review** settings.
  3. Open **Taps** or **Swipes**.
  4. Under "WHEN THE QUESTION IS SHOWN", select a preferred gesture and assign **User Action 1** to reveal and **User Action 2** to hide clozes.
</details>

## Compatibility

This script is compatible with:

- **Anki Desktop**: Version 2.1.55 or higher.
- **AnkiDroid**: Version 2.17.0 or higher.
- **AnkiWeb**: Compatible.
- **AnkiMobile**: Tested on version 25.09.
- **Overlays and drawing add-ons**: Hidden clozes stay tappable above overlays with a z-index below 1000 (tested with AnkiDraw); revealed clozes can be drawn over.

Clozes carry the `tappable` class, so tapping a cloze reveals it without triggering the app's tap gestures. AnkiMobile honors this class; AnkiDroid honors it only in its new reviewer, available since 2.21.0 ([ankidroid/Anki-Android#14303](https://github.com/ankidroid/Anki-Android/issues/14303)). In AnkiDroid's classic reviewer, tapping a cloze may also trigger the tap gesture assigned to that screen zone.

## License

This project is licensed under the GNU General Public License v3.0.

## Acknowledgements

### Inspiration

This script was inspired by the work of [ruin1990](https://github.com/ruin1990) and [kleinerpirat](https://github.com/kleinerpirat). For more details on their contributions, you can visit this [AnkiWeb forum discussion](https://forums.ankiweb.net/t/cloze-one-by-one-uncovering/12584). I also want to acknowledge [thiswillbeyourgithub](https://github.com/thiswillbeyourgithub) for creating the [Clozolkor](https://github.com/thiswillbeyourgithub/Clozolkor) script, which I used before developing this script.
