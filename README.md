# Cloze Interactive

This is a script for Anki that enhances the functionality of cloze cards, allowing individual revelation and hiding of clozes still on the front of the card. It supports touch gestures and keyboard shortcuts. It is compatible with AnkiDroid and supports MathJax rendering.

![Demonstration of Cloze Interactive](https://github.com/huandney/Anki-Cloze-Interactive/assets/19948348/5c64a125-97ef-4ae8-9855-327765ccc5c6)

## Installation

1. Download the script from this repository.
2. Open Anki and go to the card templates management section.
3. Add the script to the scripts section of your card template.

## Usage

- Tap or click on a cloze to reveal it.
- Use the configured keyboard shortcuts to reveal the next cloze or hide the last revealed cloze.

## Configuration

You can customize the script's behavior by modifying the user settings at the top of the script. Here are the available options:

- `invertGestures`: Inverts the touch gestures.
- `swipeThreshold`: Adjusts the swipe sensitivity.
- `scrollDuration`: Adjusts the smooth scroll duration.
- `revealNextKeys`: Sets the keys to reveal the next cloze.
- `hideLastKeys`: Sets the keys to hide the last cloze.

For AnkiDroid users, to ensure compatibility with this script, follow these steps:

1. Open AnkiDroid.
2. Go to **Settings**.
3. Navigate to **Advanced**.
4. Under the **Experimental** section, enable **Use the new backend**.

## Compatibility

This script is compatible with:

- Anki Desktop: version 2.1.55 or higher.
- AnkiDroid: version 2.16.2 or higher (requires experimental backend feature enabled).
- AnkiWeb: compatible, but without support for MathJax due to platform limitations.

Compatibility with AnkiMobile has not been tested yet. Feedback from AnkiMobile users is welcome!

## License

This project is licensed under the GNU General Public License v3.0.
