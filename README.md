# Cloze Interactive

This is a script for Anki that enhances the functionality of cloze cards, allowing individual revelation and hiding of clozes still on the front of the card. It supports touch gestures and keyboard shortcuts. It is compatible with AnkiDroid and supports MathJax rendering.

![Demonstration of Cloze Interactive](https://github.com/huandney/Anki-Cloze-Interactive/assets/19948348/5c64a125-97ef-4ae8-9855-327765ccc5c6)

## Installation

1. Download the script from this repository.
2. Open Anki and go to the card templates management section.
3. Add the script to the scripts section of your card template.

## Usage

- Click a cloze to reveal it.
- On touchscreen devices, tap a cloze to open it or use swipe gestures (right to reveal, left to hide).
- Use keyboard shortcuts to reveal or hide clozes. Default keys: `W` or `→` for the next cloze, and `Q` or `←` to hide a cloze.

Both gestures and keyboard shortcuts can be customized in the script's user settings.

## Configuration

You can customize the script's behavior by modifying the user settings at the top of the script. Here are the available options:

- `invertGestures`: Inverts the touch gestures.
- `swipeThreshold`: Adjusts the swipe sensitivity.
- `scrollDuration`: Adjusts the smooth scroll duration.
- `revealNextKeys`: Sets the keys to reveal the next cloze.
- `hideLastKeys`: Sets the keys to hide the last cloze.

To ensure compatibility with **AnkiDroid**, follow these steps:

1. Open AnkiDroid.
2. Go to **Settings**.
3. Navigate to **Advanced**.
4. Under the **Experimental** section, enable **Use the new backend**.

## Compatibility

This script is compatible with:

- **Anki Desktop**: version 2.1.55 or higher.
- **AnkiDroid**: version 2.16.2 or higher (requires experimental backend feature enabled).
- **AnkiWeb**: compatible, but without support for MathJax due to platform limitations.

Compatibility with **AnkiMobile** has not been tested yet. Feedback from AnkiMobile users is welcome!

If you are using a version of Anki prior to 2.1.55, I recommend the [ClozeAdv](https://github.com/ruin1990/AnkiTemplate/tree/main/ClozeAdv) script by ruin1990, which offers similar functionalities.

## License

This project is licensed under the GNU General Public License v3.0.

## Acknowledgements

### Inspiration

This script was inspired by the work of [ruin1990](https://github.com/ruin1990) and [kleinerpirat](https://github.com/kleinerpirat). For more details on their contributions, you can visit this [AnkiWeb forum discussion](https://forums.ankiweb.net/t/cloze-one-by-one-uncovering/12584). I also want to acknowledge [thiswillbeyourgithub](https://github.com/thiswillbeyourgithub) for creating the [Clozolkor](https://github.com/thiswillbeyourgithub/Clozolkor) script, which I used before developing this script.

### Functionality Reference

Thanks to [git9527](https://github.com/git9527) for the 'flip to back' functionality reference.
