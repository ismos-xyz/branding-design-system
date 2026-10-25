# CourseCardEditorial

The professional course card, for wherever ISMOS needs to look elegant: course pages, teacher pages, partner pages and printed catalogues. Paper (Ink in Hacker mode), one hairline, the book motif, a large Literata lesson count and a facts ledger. The colour lives in the band around it, not in the card.

```html
<section class="ism-block ism-block--main">   <!-- or ism-block--highlight (Weld) -->
  <a class="ism-card ism-card--editorial" href="…">
    <div class="ism-card__head"><img class="ism-card__book" src="(ismos-book-ink.svg, or -paper in Hacker mode)" alt="">
      <span class="ism-card__count">06<small>lessons</small></span></div>
    <span class="ism-label">AI · Privacy · Freedom Tech</span>
    <h3 class="ism-card__title">Local AI</h3><p class="ism-card__text">…</p>
    <div class="ism-card__teacher">…</div>
    <dl class="ism-card__ledger"><div><dt>Format</dt><dd>Live cohort</dd></div><div><dt>Length</dt><dd>9 h</dd></div><div><dt>Languages</dt><dd>EN · ES</dd></div></dl>
  </a>
</section>
```

- **Always inside a Mauveine or Weld band** (`.ism-block--main` or `.ism-block--highlight`), so the page keeps its minimums: Mauveine 28%, Logwood 800 10%, accents 11%. Never a page of Editorial cards on plain Paper.
- **Head:** the book motif (`assets/Logos/ismos-book-ink.svg`, `-paper` in Hacker mode), 20 px, top left; the lesson count right, Literata 44, two digits; a 2 px rule in the text colour below.
- **Body:** tags (`label`, Logwood 800; Logwood 200 in Hacker mode), title Literata 400 24/30, one sentence, the teacher.
- **Ledger:** three columns, Plex Mono labels over values: Format, Length, Languages. On a state (in progress, finished) the Length column shows it: *2 of 8 · continue*.
- `radius-4`, 1 px `card-editorial-edge` hairline, no shadow, no bar. Hover: the edge turns Ink (white in Hacker mode).
- Tokens `card-editorial`, `on-card-editorial`, `card-editorial-muted`, `card-editorial-edge` keep the card Paper or Ink inside a colour band.
- **In print** (catalogues): the teacher's name without a photo, as 04 Rules requires.
- **Use the CourseCard (colour cap)** for course grids on the home page, tag pages, search and *My courses*.
