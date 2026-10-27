<img width="960" height="960" alt="ISMOS · White BG" src="https://github.com/user-attachments/assets/1a0348a4-6b0b-4adb-b30a-a67cc2e7d8d5" />
# ISMOS Design System · V2 · Vibrant

Brand and UI system for ISMOS: colour, type, components, rules, accessibility (WCAG 2.2) and research (human-centred design).

## Structure

| Folder | Contents |
|---|---|
| `docs/` | The system, section by section. Start with `00-overview.md`. |
| `tokens/` | `tokens.json` (source of truth), `tokens.css` (light + `[data-theme=hacker]`), `fonts.css`. |
| `components/` | `bundle.css` plus one folder per component: `README.md` and `preview.html`. |
| `fonts/` | Self-hosted WOFF2: Literata, IBM Plex Sans, IBM Plex Mono, Bricolage Grotesque. |
| `assets/logos/` | Mark and book motif, Ink and Paper. |
| `assets/icons/iconoir/` | 40 Iconoir icons. |
| `guides/` | Brand Guideline V2 (single HTML page). |

## Use

```html
<link rel="stylesheet" href="tokens/fonts.css">
<link rel="stylesheet" href="tokens/tokens.css">
<link rel="stylesheet" href="components/bundle.css">
<body class="ism-root">            <!-- light -->
<html data-theme="hacker">         <!-- Hacker mode -->
```

Open any `components/*/preview.html` in a browser to see the component.

## Colour minimums (per page)

Mauveine `#4D01E0` ≥ 28% · Logwood 800 `#544281` ≥ 10% · accents Madder `#FF7700` + Weld `#FFD23F` ≥ 11% · alerts Cochineal `#A8001E`.

## Source

Live source: ISMOS V2 · Vibrant design-system artifact on claude.ai. Owner: Dulce Villarreal.

## Licences

Fonts: SIL Open Font License 1.1. Iconoir: MIT. ISMOS logos and marks: all rights reserved.
