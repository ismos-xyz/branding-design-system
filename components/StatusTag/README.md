# StatusTag

Status is never carried by hue alone: every status takes three cues, the colour, the icon, and the word in capitals, set as a boxed tag.

- `.ism-tag`: `text` colour (Ink), 1.5 px border in the same colour. Used for CORRECT and STREAK.
- `.ism-tag--alert`: `alert` colour (Cochineal `#A8001E` on Paper, Cochineal 300 `#FF8A99` on Ink). Used for ALERT and WRONG. Never on a Madder or Weld block.
- **Provide:** an inline 24-grid line icon (alert triangle, check, cross, star) and the word.
- STREAK appears in the palette rules but streaks are forbidden on the platform (see 09 Release, open items).
