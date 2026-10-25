# CourseCard

The most repeated component on the platform. In V2 it is a **colour cap** card: a flat colour cap on top, the course on Paper (Ink in Hacker mode) below, and a 2 px edge in the cap's own colour around the whole card. The only image a card may carry is the teacher's photo.

**Cap** `.ism-card__cap`: the 6 px bar, the tags, and the lesson count (`.ism-card__count`, Literata 48). **Body** `.ism-card__body`: title, sentence, teacher, facts.

```html
<a class="ism-card ism-card--cap ism-cap--accent" href="…">
  <div class="ism-card__cap"><span class="ism-bar"></span><span class="ism-label">Critical Thinking · AI</span>
    <span class="ism-card__count">5<small>lessons</small></span></div>
  <div class="ism-card__body"><h3 class="ism-card__title">…</h3><p class="ism-card__text">…</p>
    <div class="ism-card__teacher">…</div><div class="ism-card__facts">…</div></div>
</a>
```

1. `.ism-bar`: 6 px `bar`, 32 px wide
2. Tags: up to three, `.ism-label`, separated by a middle dot (*AI · PRIVACY · FREEDOM TECH*)
3. Title: `.ism-card__title`, Literata, two lines maximum, never truncated
4. One sentence: `.ism-card__text`, what the student will be able to do
5. Teacher (optional): `.ism-card__teacher`, a 32 px circle photo (`.ism-avatar`) and the teacher's name, `body-small` 15/24 at 500. Up to two teachers. Self-paced courses show the teacher who wrote it.
6. Facts: `.ism-card__facts`, Plex Mono behind a hairline (lessons, hours, languages), or the state (*2 of 5 · continue*, *Finished · record available*, *Saved for offline · 4 MB*)

- **Teacher photo:** circle, full colour, head and shoulders on a plain background, 1 px `hairline` ring, no filter, frame or badge. Shared with the teacher's written consent. Alt is empty because the name sits beside it. No photo, or data saver on: initials in Plex Mono 500 on a Logwood 100 circle (`.ism-avatar--initials`).
- **Cap colours:** `.ism-cap--main` (Mauveine), `--indigo`, `--support` (Logwood 800), `--accent` (Madder), `--highlight` (Weld). White type and a Weld bar on Mauveine, Indigo and Logwood 800; Ink type and an Ink bar on Madder; Ink type and a Mauveine bar on Weld.
- **Edge:** 2 px, the cap's own colour, all the way round: an orange cap has an orange edge. Weld on Paper (1.44:1) and Indigo on Ink are faint as edges; the cap itself marks the card, so the edge is a finish, not the boundary a student relies on.
- Rotate caps by position so no two neighbours match. A cap never stands for a tag, level, format or status.
- `radius-4`, no shadow. Hover: the edge turns `text` (Ink, white in Hacker mode); nothing moves.
- **Where:** the colour cap card is the **default grid card** for courses: home page, tag pages, search, *My courses*.
- **Editorial** (`.ism-card--editorial`, see CourseCardEditorial) for course pages, teacher pages, partners and printed catalogues, always inside a Mauveine or Weld band.
- **Full fill** (`.ism-card--main` and the other fills, the whole card in one colour) is for a featured row only.
- The whole card is the link; height free.
- **Don't:** any image other than the teacher photo, a student photo, ratings, enrolment counts, *new* or *popular* flags, tag chips.
