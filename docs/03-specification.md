# 03 Specification

*Settled · V2 Vibrant. Tokens and scale. Raw values live here; every other section names tokens.*

## Colour

*Version 2 · Vibrant.* Eight colours, used loud. ISMOS should feel like a celebration the moment a page opens: big flat blocks of Mauveine, Madder and Weld, stacked edge to edge, with Paper (light) or Ink (Hacker mode) as the breathing space between them. Hex values are exact and unchanged from V1; what changed is how much of each a page carries.

The six **Colour** cards in Components draw this section: palette, shares and rules, Hacker mode colours, ramps, contrast, and colour, motion and mobile. The **ColourCap** card shows the five cap colours of the default course card; the **HomePage** card shows the band layout.

### The minimums · both modes

These hold in light mode and in Hacker mode, on every page of the website and the app.

| Colour | Minimum share | Target share |
|---|---|---|
| Mauveine `#4D01E0` | **28%** | 32% light · 28% Hacker mode |
| Logwood 800 `#544281` | **10%** | 10% |
| Accent: Madder `#FF7700` + Weld `#FFD23F` | **11%** | 18%: Madder 10, Weld 8 |

Madder is an **Accent** in both modes (in V1 it sat under *Secondary* in Hacker mode). A page that falls below a minimum is not finished.

### Alerts · Cochineal

Alerts have their own colour, so Madder can be pure energy. **Cochineal** is a deep crimson, named, like the rest of the palette, after a natural dye.

| Token | Name | Hex | Use | Contrast |
|---|---|---|---|---|
| `cochineal` | Cochineal | `A8001E` | Alert text, error borders, the Alert icon, the ERROR and WRONG tags, on Paper | 7.82:1 on Paper (AAA); white on Cochineal 7.82:1 |
| `cochineal-300` | Cochineal 300 | `FF8A99` | The same, in Hacker mode and on Ink | 9.35:1 on Ink, 7.11:1 on Logwood (AAA) |

- **Alerts only.** Never a band, a card fill, a chart series, a bar or decoration. It stays rare so it stays alarming; it is not part of the shares.
- **Three cues, always:** Cochineal, the Alert icon, the word in capitals.
- **Never on Madder or Weld blocks** (Cochineal on Madder is 2.94:1): forms, errors and status messages sit on Paper, Ink or a Logwood panel.
- Cochineal is much darker than Madder, so the two stay apart for red-green colour-blind readers; the icon and the word carry the meaning anyway.

### 1 · The palette at a glance

Eight colours in four roles: Main, Neutral, Accent and Support. Percentages are each colour's share of a screen surface; circle size follows the share.

| Role | Light | Hacker mode | Colours | What it does |
|---|---|---|---|---|
| Main | 38% | 36% | `#4D01E0` · `#2A2550` | The brand: hero blocks, bands, filled cards, buttons, links. White type on top. |
| Accent | 18% | 18% | `#FF7700` · `#FFD23F` | Energy: bands, filled cards, highlights, the bar on dark blocks. Ink type on top. |
| Support | 10% | 10% | `#544281` | Bands, filled cards, section labels, captions. White type on top. |
| Neutral | 34% | 36% | `#FFFFFF` · `#251D3A` · `#000000` | The breathing space between blocks, and the type. |

| Group | Token | Name | Hex | Light | Hacker mode |
|---|---|---|---|---|---|
| Main | `mauveine` | Mauveine | `4D01E0` | 32% | 28% |
| | `indigo` | Indigo | `2A2550` | 6% | 8% |
| Accent | `madder` | Madder | `FF7700` | 10% | 10% |
| | `weld` | Weld | `FFD23F` | 8% | 8% |
| Support | `logwood-800` | Logwood 800 | `544281` | 10% | 10% |
| Neutral | `paper` | Paper | `FFFFFF` | 26% | 2% |
| | `logwood` | Logwood | `251D3A` | 4% | 8% |
| | `ink` | Ink | `000000` | 4% | 26% |

### 2 · Share of a screen and the colour rules

#### Share of a screen surface · Light

Paper `26%` · Mauveine `32%` · Logwood 800 `10%` · Madder `10%` · Weld `8%` · Indigo `6%` · Logwood `4%` · Ink `4%`

#### Colour-block layouts

A page is a stack of full-bleed bands, hard-edged, no gaps, no gradients.

- **Every page** carries at least one Mauveine block, one accent block (Madder or Weld) and one Logwood 800 block. The home page opens on Mauveine.
- **Never two neighbouring bands in the same colour.** A Paper band (Ink in Hacker mode) may sit between two colour bands.
- **Course cards are colour cap cards:** a cap in Mauveine, Indigo, Logwood 800, Madder or Weld, with the type, bar and labels from the table below, the course on Paper (Ink in Hacker mode) beneath it, and a 2 px edge in the cap's colour round the card. Caps rotate by position in the grid, so no two neighbouring cards share one. Full-fill cards are for a featured row only. On course pages, teacher pages, partner pages and printed catalogues the **Editorial** card is used instead: Paper (Ink in Hacker mode) with a hairline, always inside a Mauveine or Weld band, so the band carries the colour. A fill never stands for a tag, a level, a format or a status.
- **Forms, errors and status messages** never sit on a Madder or Weld block. They sit on Paper (Ink in Hacker mode) or a Logwood panel, so an accent block never competes with an alert.
- **Flat colour only.** No gradient, tint, transparency, glow or pattern on a block.

#### What goes on each block

In code, a band is `.ism-block` plus `--main` (Mauveine), `--indigo`, `--support` (Logwood 800), `--accent` (Madder) or `--highlight` (Weld); a plain `.ism-block` is Paper (Ink in Hacker mode). Each modifier re-points the role tokens, so labels, bars, buttons, links and cards inside take the right colours. Titles `.ism-block__title` (Literata 400, 36–64 px), leads `.ism-block__lead` (19/30). The same five colours make the caps of the default course card (**ColourCap**, **CourseCard**).

| Block | Type | Bar and highlights | Button on it | Labels and tags |
|---|---|---|---|---|
| Mauveine `#4D01E0` | White, 8.76:1 | Weld, 6.07:1 | Weld fill, Ink type, 14.54:1 | White |
| Indigo `#2A2550` | White, 14.20:1 | Weld, 9.83:1 | Weld fill, Ink type | White |
| Logwood 800 `#544281` | White, 8.49:1 | Weld, 5.88:1 | Weld fill, Ink type | White |
| Madder `#FF7700` | Ink, 7.89:1 | Ink | Ink fill, white type, 21.00:1 | Ink |
| Weld `#FFD23F` | Ink, 14.54:1 | Mauveine, 6.07:1 | Mauveine fill, white type, 8.76:1 | Ink |
| Paper `#FFFFFF` | Ink, 21.00:1 | Mauveine, 8.76:1 | `action` (Mauveine), white type | Logwood 800 |
| Ink `#000000` (Hacker mode) | White, 21.00:1 | Mauveine 300, 7.84:1 | Mauveine fill, white type | Logwood 200 |

Weld as type on Mauveine, Indigo or Logwood 800 is for headings of 24 px and up, figures and the bar only (5.88–9.83:1, AA). Body text on every block is white or Ink, AAA.

#### Rules

- **Right and wrong answers, progress, streaks.** Never colour alone. Pair the colour with an icon and a word: Madder and Weld look alike to people with red-green colour blindness (about 1 in 12 men).
- **Type.** Ink on Weld and Madder. White on Mauveine, Logwood 800, Indigo and Logwood. Never white on Madder (2.66:1) or Weld (1.44:1).
- **Outlines.** A Weld or Madder element on Paper (a button, a chip, a small block under 48 px) takes a 1.5 px Ink border. Weld on Paper is 1.44:1, Madder 2.66:1.
- **Amounts.** Weld 8%, Madder 10%. Accents together never below 11%.
- **Madder as graphics on Paper.** Chart series and icons in Madder take an Ink outline. Madder is never an alert: alerts are Cochineal.
- **Meeting edges.** Mauveine against Madder is 3.29:1, Weld against Mauveine 6.07:1: blocks may meet edge to edge. Mauveine against Ink (2.40:1) and Logwood 800 against Ink (2.47:1) may meet as large areas, never as thin lines.

#### On screen · Light

- Paper is the breathing space, not the whole page. Ink for type, Mauveine for links and active states, always underlined or marked.
- The primary button is Mauveine with white type (8.76:1). On a Mauveine, Indigo or Logwood 800 block it turns Weld with Ink type.
- Card edges and table rules on Paper: Logwood 200 `#DFD8FB`. Panels and zebra rows: Logwood 50.

#### Dark surfaces · Ink and Logwood

- Text on Ink is white, Paper `#FFFFFF`, 21.00:1, for body and headings alike. Never an off-white or ghost-white tint on a dark colour.
- Logwood cards on Ink take a 1 px Logwood 700 `#6B55A2` edge. Logwood against Ink alone is 1.32:1.
- Links and indicators on dark are Mauveine 200 `#BFC3FF`, underlined or with a dot: 12.47:1 on Ink, 9.48:1 on Logwood. Mauveine 300 `#9293FF` is for the progress bar only (7.84:1).
- Weld and Madder keep Ink type on dark surfaces as well.

#### In print · On Paper

Printed pieces carry the same blocks: a full-bleed Mauveine, Madder or Weld band across the top third, a Logwood 800 band at the foot, Paper between. Ink type on Paper, Madder and Weld; white on Mauveine, Indigo and Logwood 800. Alert text prints in Cochineal `#A8001E`. The one-colour version still has to work: the photocopy test in 07 stands.

**Status is never carried by hue alone.** Every alert, in print and on screen, takes three cues: the colour, the icon, and the word in capitals, set as a boxed tag: **ALERT** (Cochineal, alert triangle) · **STREAK** (Ink, star). See the StatusTag component.

### 3 · Hacker mode colours

The same blocks, on Ink. Ink is the ground between bands, white is the text, Weld is the cursor. Mauveine, Logwood 800 and the accents keep their minimums.

| Group | Name | Hex | Share |
|---|---|---|---|
| Main · 36% | Mauveine · Indigo | `4D01E0` · `2A2550` | 28% · 8% |
| Neutral · 36% | Ink · Logwood · Paper | `000000` · `251D3A` · `FFFFFF` | 26% · 8% · 2% |
| Accent · 18% | Madder · Weld | `FF7700` · `FFD23F` | 10% · 8% |
| Support · 10% | Logwood 800 | `544281` | 10% |

Mauveine `28%` · Ink `26%` · Logwood 800 `10%` · Madder `10%` · Weld `8%` · Indigo `8%` · Logwood `8%` · Paper `2%`

- **Text.** Body text, code and headings in white `#FFFFFF` (21.00:1). Comments and secondary text in Logwood 200 (15.35:1 on Ink, 11.67:1 on Logwood).
- **Blocks.** Mauveine, Logwood 800, Madder and Weld bands run full bleed between Ink bands, with the type from the table above.
- **Links.** Mauveine 200 `#BFC3FF`, underlined (12.47:1 on Ink). Mauveine 300 only for the progress bar.
- **Terminal.** Ink ground, 1 px Logwood 700 edge, Weld prompt and cursor, Cochineal 300 alert with icon and word.

Every role token, elevation and component rule: **03.2 Hacker mode**.

### 4 · Ramps · Logwood neutrals and interface steps

The neutrals are the Logwood ramp, `black-velvet` in code. Eleven steps tinted toward the dye, so grays sit with the palette. 950 is Logwood itself. Each step lists its contrast on Paper.

| Step | Token | Hex | On Paper |
|---|---|---|---|
| 50 | `logwood-50` | `#F8F6FE` | 1.07:1 |
| 100 | `logwood-100` | `#EFECFD` | 1.16:1 |
| 200 | `logwood-200` | `#DFD8FB` | 1.37:1 |
| 300 | `logwood-300` | `#CABDF7` | 1.73:1 |
| 400 | `logwood-400` | `#AF9BEC` | 2.41:1 |
| 500 | `logwood-500` | `#9F87E1` | 2.99:1 |
| 600 | `logwood-600` | `#8369C4` | 4.39:1 |
| 700 | `logwood-700` | `#6B55A2` | 6.09:1 |
| 800 | `logwood-800` | `#544281` | 8.49:1 |
| 900 | `logwood-900` | `#453867` | 10.42:1 |
| 950 | `logwood-950` = `logwood` | `#251D3A` | 15.96:1 |

#### On Paper · Screen and print

- **950** · long-form body below Ink headings
- **800** · captions, notes, section labels
- **700** · rules, graphics, small text allowed (6.09:1)
- **600** · icons and large text only (4.39:1)
- **200** · hairlines and table rules, never text
- **50** · quiet panels and table zebra

#### On Ink · Dark surfaces

- **200** · secondary text on Logwood (11.67:1). Body text on Ink and Logwood is white
- **400** · borders and dividers on Logwood (6.63:1)
- **700** · card edges, hairlines and table rules on Ink
- **950** · cards and panels, always with a 700 edge

### 5 · Colour accessibility and contrast

WCAG 2.2 AA on every screen and printed piece, AAA (7:1) as the aim for text. Four principles: Perceivable, Operable, Understandable, Robust.

- **4.5:1** standard text · **3:1** large text (24 px, or 18.66 px bold) · **3:1** graphics and UI components.
- **On Ink:** white 21.00:1 for body, code and headings; Logwood 200 15.35:1 for muted text; Mauveine 200 12.47:1 for links.
- **Banned:** Madder text on Paper (2.66:1), Weld on Paper (1.44:1), Mauveine on Ink (2.40:1), Paper on Madder (2.66:1).

The full contrast table, with every pair and its PASS or FAIL: **06 Accessibility**. Rendered with Aa samples in the **Colour contrast** card.

### 6 · Colour, motion and mobile

- **Never colour alone.** An invalid field takes a 2 px Cochineal border, the Alert icon and a message that names the fix. A border alone is wrong.
- **Motion.** Respect Reduce Motion; nothing flashes more than three times a second; motion over 5 s gets a pause control.
- **Mobile.** 44 × 44 pt (iOS) and 48 × 48 dp (Android) targets; text scales to 200%; screens rotate freely; dark mode is Hacker mode.

Details in **06 Accessibility** and the **Colour, motion and mobile** card.

### Focus

`:focus-visible` takes a 2 px `focus` outline at 2 px offset: Mauveine on light, Weld on Hacker mode.

### How the palette applies across this system

- **Tags, not colours.** Tags are words (01.1). A tag never has its own colour: it is a `label` in `logwood-800` on Paper, white on Mauveine, Indigo and Logwood 800, Ink on Madder and Weld. A card's fill never stands for its tags.
- **The 6 px bar** that opens a section or tops a card is `bar`: Mauveine on Paper, Mauveine 300 on Ink, Weld on Mauveine, Indigo and Logwood 800, Ink on Madder, Mauveine on Weld.
- **Links.** `link` (Mauveine; Mauveine 200 in Hacker mode), hover `link-hover` (Logwood 800; white in Hacker mode), always underlined.
- **Buttons.** The primary button is `action`: Mauveine with white type in both modes. On Mauveine, Indigo and Logwood 800 blocks it is `action-on-color`: Weld with Ink type. On a Madder block: Ink with white type. On a Weld block: Mauveine with white type.
- **Status colours** (accepted October 2026). Each status differs by colour, container and icon + word:

| Status | Light | Hacker mode | Container | Icon · word |
|---|---|---|---|---|
| Info | `status-info` Logwood 800 on Logwood 50, 7.93:1 | Logwood 200 on Logwood, 11.67:1 | Filled panel, no border | Square-i · NOTE |
| Success | `status-success` Indigo on Paper, 14.20:1 | Mauveine 200 on Ink, 12.47:1 | 1.5 px border | Check · DONE |
| Warning | `status-warning` Ink on Weld, 14.54:1 | Ink on Weld, 14.54:1 | Weld fill, 1.5 px Ink border | Triangle · CHECK THIS |
| Error | `status-error` Cochineal on Paper, 7.82:1 | Cochineal 300 on Ink, 9.35:1 | 2 px border | Triangle · ERROR |

Never a green tick. All four meet AAA (7:1) on their own grounds.

- **Charts.** Series in Mauveine, Madder (with an Ink outline on Paper), Weld (with an Ink outline) and Logwood 800, each labelled directly.
- **Progress.** A 6 px `bar` on a `track`, with the count as a figure.
- **No gradients.** No gradient between two palette colours. No rainbow rules, arcs or ribbons. No colour-coded difficulty.

## Typography

### Three typefaces, and the wordmark

Three faces do the work, and a fourth sets the wordmark alone. All four ship as files in `fonts/` (Latin subsets). Other scripts use companion faces, listed under All languages at parity.

- **Bricolage Grotesque** · `--font-wordmark` · the wordmark, and nothing else. Less formal than the faces below, which is the point: the name should read as a place to learn rather than an institution. Never for a heading, a title, a label, or a word of copy.
- **Literata** · `--font-serif` · titles and quotations. Regular 400 · Medium 500 · Italic. No Light weight: thin strokes break up on low-quality screens. Built for long reading at screen sizes: large x-height, open counters, a low-contrast stroke that survives a bad display. Titles, section headings, pull quotes and a student's own words. Not for interface labels, buttons, tables or figures.
- **IBM Plex Sans** · `--font-sans` · everything a student reads or presses. Regular 400 · Medium 500 · SemiBold 600 · Italic. Body copy, lesson text, interface, buttons, form labels, navigation. No Light and no Bold.
- **IBM Plex Mono** · `--font-mono` · labels, figures, code. Regular 400 · Medium 500. Every countable thing, every code sample, every lesson number, the address line, and the small uppercase labels above a block. Tabular figures on. Never body copy or a heading. Weight follows the ground: Medium on Paper, SemiBold on a colour block.

**Licence and fallbacks.** All four are under the SIL Open Font License: they may be embedded, self-hosted and shipped inside offline course packages. Fallbacks: `Literata, Georgia, serif` and `"IBM Plex Sans", system-ui, sans-serif`.

**Never** Spectral on an ISMOS surface (it belongs to the Foundation). Never a fifth face, including for a single poster. Never Bricolage Grotesque except in the wordmark. Never Literata and Plex Sans in the same paragraph. Never a system serif standing in for Literata in a printed piece.

### The type scale · Screen, 16 px base

| Role | Style | Face | Size / line | Specimen |
|---|---|---|---|---|
| Display | `display` | Literata 400 | 48 / 52 | Freedom Tech |
| H1 | `h1` | Literata 400 | 36 / 42 | Run your own node |
| H2 | `h2` | Literata 400 | 28 / 34 | What you'll build |
| H3 | `h3` | Literata 500 | 21 / 28 | Lesson 4 · Keys and backups |
| Lead | `lead` | Plex Sans 400 | 19 / 30 | Twelve weeks, in your own language. |
| Body | `body` | Plex Sans 400 | 17 / 28 | You'll finish with a wallet you set up yourself. |
| Body small | `body-small` | Plex Sans 500 | 15 / 24 | Metadata, table body, card copy. |
| Caption | `caption` | Plex Sans 500 | 13 / 20 | Handwoven cotton, detail. Not a place. |
| Label | `label` | Plex Mono 400–500 | 11 / 16 | CODING & CRYPTOGRAPHY |
| Figure | `figure` | Plex Mono 500 | Contextual | 1 240 · 87 % · 12 |

- **Print:** title 24 pt · H1 18 pt · H2 14 pt · body 10.5/16 pt · caption 8.5 pt · label 7.5 pt. Nothing below 8 pt, including a footer.
- **Slides · 1920 × 1080:** nothing below 24 px, ever. Titles 72–96 px, body 32–40 px.
- **Mobile:** body stays 17 px. Display drops to 32 px, H1 to 27 px. Every tap target at least 44 px tall.

### Guide document scale · Letter, print-first

The scale used by the ISMOS Brand Style Guide pages and by the printable Guideline. Seven roles plus the lede, no interpolation.

| Role | Style | Face | Size / line |
|---|---|---|---|
| Display | `doc-display` | Literata 400 | 29 / 38 (cover title) |
| Title | `doc-title` | Literata 400 | 21 / 26 (page header) |
| Head | `doc-head` | Literata 400 | 16 / 20 |
| Sub | `doc-sub` | Plex Sans 600 | 13.5 / 19 |
| Lede | `doc-lede` | Plex Sans 400 | 14 / 24 |
| Body | `doc-body` | Plex Sans 400 | 12.5 / 20 · notes 11.5 / 18 |
| Label | `doc-label` | Plex Mono 500, caps, 0.14 em | 9 / 12 · footer 8.5 |
| Data | `doc-data` | Plex Mono 500 | 10.5 / 16 |

A heading uses Literata or a Plex Mono label, never both. Plex Mono never in running text. Ragged right. Measure 60–75 characters.

### Type rules

**Setting**

- Measure 60–70 characters. Never a full-width line of body text.
- Ranged left, unjustified, everywhere. No hyphenation in headings.
- Headings balance; body wraps pretty. No manual line breaks in copy that will be translated.
- Sentence case for headings, buttons and labels, except the Plex Mono uppercase label, letterspaced 0.14 em.
- Type on a colour block goes up one weight: Literata titles to Medium, Plex Mono labels to SemiBold, both in Paper.
- One space after a full stop. Serial comma in English.
- Thin space as the thousands separator in Plex Mono figures: 1 240, not 1,240.

**Never**

- All caps for a heading, a title or a sentence. Uppercase belongs to the Plex Mono label only.
- Underline for emphasis. Underline means link.
- Italic for a whole paragraph. Italic is for a title, a foreign word, or a student's own voice.
- Faux bold or faux italic.
- Letterspacing on lowercase text, at any size.
- Exclamation marks in interface copy.

**A worked heading stack.** Five levels, in order, every time: the bar (`bar`, 6 px), the label (`label`, `text-muted`), the title (`h1`–`h3`), the lead (`lead`), the facts (`figure` behind a hairline). *Freedom Tech · Course 02 / Run your own node / Eight lessons on setting up, syncing and looking after a node you control. / 8 lessons · 6 h / week · ES · EN*

### All languages at parity

Ten languages, each an original: English, Mandarin Chinese, Hindi, Spanish, French, Modern Standard Arabic, Bengali, Russian, Portuguese, Japanese. Content rules are in 05.1; these are the layout and type rules.

| Script | Languages | Titles | Text and UI | Labels and figures |
|---|---|---|---|---|
| Latin, Cyrillic | en, es, fr, pt, ru | Literata | IBM Plex Sans | IBM Plex Mono |
| Simplified Chinese | zh-Hans | Noto Serif SC | IBM Plex Sans SC | IBM Plex Sans SC (no uppercase) |
| Japanese | ja | Noto Serif JP | IBM Plex Sans JP | IBM Plex Sans JP (no uppercase) |
| Devanagari | hi | Noto Serif Devanagari | IBM Plex Sans Devanagari | IBM Plex Mono for digits |
| Bengali | bn | Noto Serif Bengali | Noto Sans Bengali | IBM Plex Mono for digits |
| Arabic | ar | Noto Naskh Arabic | IBM Plex Sans Arabic | IBM Plex Sans Arabic |

- The token font stacks already list these faces, so the right one is picked per character. Load them from Google Fonts per language, not all at once.
- Size every button, tab, nav item and card title against the longest language (often French, Russian or Spanish, about 30% longer than English). No fixed-height cards, no single-line truncation on titles.
- CJK and Devanagari need more line height: body 17/30 instead of 17/28. Never letterspace them, and never set them in uppercase (the Plex Mono label style becomes plain weight 500).
- **Arabic reads right to left.** The whole layout mirrors: navigation, the lesson rail, icons with a direction (arrows, chevrons). The mark, media controls and numbers do not mirror. Build with logical CSS properties (`margin-inline-start`) and `dir="rtl"` so this costs no rebuild.
- Set `lang` (and `dir`) on every page and every passage in another language.
- Every language version exists before a surface ships in that language.

## Layout
### The grid

Twelve columns on the platform, because course lists divide by four, three and two. Eight columns in documents. Both use the same gutter and the same reading measure.

| Platform | |
|---|---|
| Max content width | 1 200 px (`content-max`) |
| Columns | 12 |
| Gutter | 24 px (`gutter`) |
| Page margin | 32 px · 16 px mobile (`page-margin`, `page-margin-mobile`) |
| Reading column | 7 of 12 · 680 px (`reading-column`) |
| Breakpoints | 640 · 1 024 · 1 280 |

| Documents · A4 and Letter | |
|---|---|
| Columns | 8 |
| Margin | 20 mm · 13 mm foot |
| Gutter | 5 mm |
| Section head | Number, title, 2 px rule, right kicker (SectionHead) |
| Footer | Hairline, then two Plex Mono lines |
| Both papers | Every page fits A4 and Letter unchanged |

**Full bleed is a decision.** Colour blocks and the motif field may break the grid and run to the edge. Type never does: a caption, a label, a footer and a lockup all sit on the text column's margin, including on top of an image.

### Spacing, rules and corners

**Spacing:** `space-4` `space-8` `space-12` `space-16` `space-24` `space-32` `space-48` `space-64` `space-96`. Nine values, no others. 4 and 8 inside a control; 12 and 16 between related lines; 24 between blocks; 32 and 48 between sections; 64 and 96 above a section opener. If a layout needs 20 px, it needs 16 or 24.

**Three rule weights:** `rule-1` (1 px `hairline`) separates rows and list items · `rule-2` (2 px `rule-strong`) closes a section heading · `rule-6` (6 px `bar`) opens a section, tops a card. No other weights. No dotted or double rules.

**Corners and depth**

- `radius-0` · colour blocks, images, bars, the motif field, tables, documents.
- `radius-4` · things a student presses or types into: buttons, inputs, course cards, tabs.
- `radius-8` · the maximum, for a modal or a sheet on mobile.
- `radius-circle` · avatars and teacher photos only. No pills, no round buttons, no circular badges.
- `shadow-float` · the only shadow, on a modal or a menu that floats over content. Cards use a hairline.

### Data and progress

A chart is about many people and belongs in a report. Progress is about one student and belongs in the interface.

**Charts · one accent, five greys**

- Six series at most: Mauveine plus five steps of the Logwood ramp, darkest at the centre of the group.
- The accent is the series the chart is about. Everything else is grey.
- No tints of an accent, and never opacity to distinguish series.
- Label lines directly; no legend. Figures in Plex Mono, tabular.
- One-colour print versions distinguish series by hatch, not by grey.

**Progress · a bar, and a sentence** (Progress component)

- 6 px `bar` on `track`. Same weight as the section bar.
- Always show the count as a figure: 5 of 8. Never a percentage alone.
- Zero progress is an empty bar and a plain sentence, never a warning colour, never a nudge.
- No badges, points, leaderboards or confetti. Nothing tells a student they are behind.

**Denominators, always.** 87% completed is not a fact; 87% of 240 enrolled is. Never invent, estimate or round up a number; leave a visible placeholder where a figure has not been supplied.

## Icons

The mark is solid; the icons are line. ISMOS uses **[Iconoir](https://iconoir.com)** (MIT licence, about 1 600 icons, `iconoir@7.11.0`), accepted October 2026. Files in `assets/Iconoir/`.

| Spec | |
|---|---|
| Grid | 24 × 24 |
| Stroke | 1.5 px, Iconoir's own; 2 px at 48 px and above |
| Caps and joins | Round, as Iconoir draws them. Never mix with another set. |
| Fill | None, ever: regular style only, never Iconoir's solid style |
| Colour | One per icon: Ink on light, white on dark |
| Sizes | 20, 24, 32, 48 px. Minimum 20 px; below that, use a word. |

| Meaning | Iconoir | Meaning | Iconoir |
|---|---|---|---|
| Courses | `book-stack` | Translation | `translate` |
| Lesson | `open-book` | Search | `search` |
| Assessment | `task-list` | Download | `download` |
| Record | `page-star` | Saved | `bookmark` |
| Progress | `percentage-circle` | External link | `open-new-window` |
| Cohort | `group` | Data | `stats-report` |
| Discussion | `chat-lines` | Contact | `mail` |
| Offline | `cloud-download` | Community | `community` |
| Device | `smartphone-device` | Open access | `open-in-browser` |
| Connectivity | `wifi` | Regions | `globe` |

**For learning content:** `brain` thinking it through · `light-bulb-on` tip · `puzzle` exercise · `sparks` built with AI · `code-brackets` code · `terminal` command line · `flask` lab · `compass` where to start · `bitcoin-circle` Bitcoin · `wallet` · `key` keys and backups · `shield-check` security · `cube` blocks · `network` peer to peer · `coins` money · `coffee-cup` short lesson · `headset` listen · `media-video` watch · `help-circle` ask the AI tutor · `map-pin` location.

- Label by default: the word carries the meaning. An icon alone only for search, close, download.
- One idea per icon. 8 px from the word. Interactive icons get a 44 px target.
- **Offline is a promise:** `cloud-download`, never a crossed-out cloud or an error state.
- **Progress is not Data:** never `stats-report` for a student's progress.
- **Never use:** `graduation-cap` (implies a credential), `trophy`, `medal`, `crown` (rank people), `star` (ratings, streaks), `rocket` (hype).
- **Never** inside a circle, badge, chip or tile; filled; below 20 px; emoji anywhere; the mark as an icon.
