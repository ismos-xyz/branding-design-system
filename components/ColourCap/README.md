# ColourCap

The five cap colours of the default course card (CourseCard): a flat colour cap on top, the course on Paper (Ink in Hacker mode) below, and a 2 px edge in the cap's own colour around the whole card.

| Class | Cap | Type on the cap | Bar | Edge |
|---|---|---|---|---|
| `.ism-cap--main` | Mauveine `#4D01E0` | White, 8.76:1 | Weld, 6.07:1 | 2 px Mauveine |
| `.ism-cap--accent` | Madder `#FF7700` | Ink, 7.89:1 | Ink | 2 px Madder |
| `.ism-cap--support` | Logwood 800 `#544281` | White, 8.49:1 | Weld, 5.88:1 | 2 px Logwood 800 |
| `.ism-cap--highlight` | Weld `#FFD23F` | Ink, 14.54:1 | Mauveine, 6.07:1 | 2 px Weld |
| `.ism-cap--indigo` | Indigo `#2A2550` | White, 14.20:1 | Weld, 9.83:1 | 2 px Indigo |

- Use with `.ism-card.ism-card--cap`; the full anatomy (cap, count, body, teacher, facts) is in **CourseCard**.
- Caps rotate by position so no two neighbours match. A cap never stands for a tag, level, format or status.
- Weld on Paper (1.44:1) and Indigo on Ink are faint as edges; the cap itself marks the card.
- Full-bleed page bands use the same five colours: `.ism-block--main`, `--accent`, `--support`, `--highlight`, `--indigo` (03 Specification · What goes on each block).
