# Cloze Interactive

This is a script for Anki that enhances the functionality of cloze cards, allowing individual revelation and hiding of clozes still on the front of the card. It supports touch gestures and keyboard shortcuts. It is compatible with AnkiDroid and supports MathJax rendering.

![Demonstration of Cloze Interactive](https://github.com/huandney/Anki-Cloze-Interactive/assets/19948348/5c64a125-97ef-4ae8-9855-327765ccc5c6)

## Features

- **Individual Cloze Reveal:** No more revealing all clozes at once!
- **Touch Gestures:** Swipe gestures are supported on touchscreen devices.
- **Keyboard Shortcuts:** Use keyboard shortcuts to reveal or hide clozes.
- **Auto Scroll:** Enhance your reading experience with a smooth auto scroll to the next cloze.
- **Flip to Back:** The card is automatically flipped after revealing all the clozes.
- **MathJax Support:** Include complex mathematical equations in your clozes with MathJax rendering.

## Installation

There are two ways to install the Cloze Interactive script:

### Option 1: Import the Deck

1. Download the `.apkg` file from the [releases page](https://github.com/huandney/Anki-Cloze-Interactive/releases) on GitHub or from [AnkiWeb](https://ankiweb.net/shared/info/1523903214).
2. After the file is downloaded, double-click on it to open it in the desktop program. If asked which application to use, choose Anki.
3. The deck should now be imported into your Anki app.

### Option 2: Manual Installation

1. Navigate to the [card folder](https://github.com/huandney/Anki-Cloze-Interactive/tree/main/card) in the GitHub repository.
2. Copy the contents of the `template-front.html` file.
3. Open your Anki Desktop app. In the main Anki window, go to **Tools → Manage Note Types** and find the Cloze note type where you want to enable the Cloze Interactive script. Proceed by clicking on **Cards** to invoke the card template editor.
4. Replace your existing front template with the copied content.
5. Repeat the process for the `styling.css` file, replacing your existing styling.

> Please note that these instructions are for the Anki Desktop app. The process may vary slightly for AnkiMobile or AnkiDroid.

## Usage

- Click a cloze to reveal it.
- On touchscreen devices, tap a cloze to open it or use swipe gestures (right to reveal, left to hide).
- Use keyboard shortcuts to reveal or hide clozes. Default keys: `W` or `→` for the next cloze, and `Q` or `←` to hide a cloze.

> Both gestures and keyboard shortcuts can be customized in the script's user settings.

## Configuration

You can customize the script's behavior by modifying the user settings at the top of the script. Here are the available options:

- `invertGestures`: Inverts the touch gestures.
- `swipeThreshold`: Adjusts the swipe sensitivity.
- `scrollDuration`: Adjusts the smooth scroll duration.
- `revealNextKeys`: Sets the keys to reveal the next cloze.
- `hideLastKeys`: Sets the keys to hide the last cloze.

:warning: To ensure compatibility with **AnkiDroid**, follow these steps:

1. Open AnkiDroid.
2. Go to **Settings**.
3. Navigate to **Advanced**.
4. Under the **Experimental** section, enable **Use the new backend**.

## Compatibility

This script is compatible with:

- **Anki Desktop**: version 2.1.55 or higher.
- **AnkiDroid**: version 2.16.2 or higher (requires experimental backend feature enabled).
- **AnkiWeb**: compatible, but without support for MathJax due to platform limitations.

> Compatibility with **AnkiMobile** has not been tested yet. Feedback from AnkiMobile users is welcome!

## License

This project is licensed under the GNU General Public License v3.0.

## Acknowledgements

### Inspiration

This script was inspired by the work of [ruin1990](https://github.com/ruin1990) and [kleinerpirat](https://github.com/kleinerpirat). For more details on their contributions, you can visit this [AnkiWeb forum discussion](https://forums.ankiweb.net/t/cloze-one-by-one-uncovering/12584). I also want to acknowledge [thiswillbeyourgithub](https://github.com/thiswillbeyourgithub) for creating the [Clozolkor](https://github.com/thiswillbeyourgithub/Clozolkor) script, which I used before developing this script.

### Functionality Reference

Thanks to [git9527](https://github.com/git9527) for the 'flip to back' functionality reference.
