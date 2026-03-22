# ✊ Rock & Roll

A sleek, minimal Rock Paper Scissors game with dark/light theme support — built with vanilla HTML, CSS, and JavaScript. No dependencies. No build step. Just open and play.
---

## Features

- **Dark & Light themes** — toggle with the button or press `Enter` anywhere on the page
- **Persistent score** — wins, ties, and losses are saved to `localStorage` so your score survives a page refresh
- **Persistent theme** — your theme preference is also saved to `localStorage`
- **Responsive** — works on mobile and desktop
- **Animated results** — pop + glow animation on every play

---

## How to Play

1. Open `index.html` in any modern browser
2. Click ✊, ✋, or ✌️ to make your move
3. The CPU picks randomly — result and score update instantly
4. Hit **Reset Score** to start fresh

---

## Project Structure

```
rock-and-roll/
├── index.html   # Everything — markup, styles, and logic in one file
└── README.md
```

This is intentionally a single-file project. There are no frameworks, bundlers, or external dependencies beyond two Google Fonts.

---

## Game Logic

```
rock     beats  scissor
paper    beats  rock
scissor  beats  paper
```

The CPU choice is `CHOICES[Math.floor(Math.random() * 3)]` — uniform random, no weighting.

---

## Fonts Used

- [Bebas Neue](https://fonts.google.com/specimen/Bebas+Neue) — headings and score numbers
- [DM Mono](https://fonts.google.com/specimen/DM+Mono) — body and UI text

Both loaded from Google Fonts.

---

## Customization

All colors are CSS custom properties on `:root`, so theming is straightforward:

```css
:root {
  --bg: #0e0e10;
  --accent: #00f5c4;   /* change this to repaint the whole UI */
  --win: #00f5c4;
  --lose: #ff4d6d;
  --tie: #ffd166;
}
```

---

## Browser Support

Works in all modern browsers (Chrome, Firefox, Safari, Edge). Requires `localStorage` support (available everywhere).

---
