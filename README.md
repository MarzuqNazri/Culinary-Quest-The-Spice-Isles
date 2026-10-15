[README.md](https://github.com/user-attachments/files/33484480/README.md)
# Culinary Quest: The Spice Isles — Battle Fix

A small top-down culinary adventure RPG built with Phaser 3.80.1.

## What's fixed

- Battle actions use scene-level interactive controls instead of nested interactive container children, improving pointer/touch hit-testing.
- Battle actions are locked while an opponent is taking its turn, and keyboard input cannot accidentally stack quiz screens.
- Quiz answers are handled by one guarded function; the quiz is removed cleanly after an answer and the opponent then takes its turn.
- Spirit capture has explicit success/failure feedback, updates the party counter, and prevents multiple capture attempts during the capture animation.
- Battle HP labels update directly rather than searching through container children.
- Battle and quiz objects are cleaned up when the encounter ends, reducing stale controls after returning to exploration.

## Run locally

1. Extract the ZIP.
2. Open `index.html` in a browser with an internet connection. Phaser 3 is loaded from jsDelivr CDN.
3. For best results, publish the files to GitHub Pages.

## Controls

- Move: Arrow keys or WASD.
- Interact: E, Space, or Enter.
- Battle: click/tap the three action buttons, or press `1` for Spirit Move, `2` for Spice Seed, and `3` for Culinary Quiz.
- Mobile: use the on-screen direction pad and action button. Battle and quiz options are tappable.

## Gameplay notes

- Talk to Chef Mira to choose a starter before entering battles.
- Use Spirit Move to lower a wild spirit's HP; Spice Seeds have a higher chance of working when its HP is low.
- Culinary Quiz answers explain the culinary concept and award Guild Marks, up to three.
- Talk to Ranger Nasi to replenish Spice Seeds.

## Validation

`node --check main.js` and ZIP integrity checks passed. A full in-browser gameplay test could not be completed in this environment because the Phaser CDN could not be reached; please verify on a browser with internet access before using it with students.
