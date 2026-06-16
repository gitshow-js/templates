# editorial — Magazine-style template for storytelling & brand keynotes

A light, print-magazine aesthetic built for narrative talks, brand stories and
design keynotes: a warm off-white paper canvas, near-black ink, and a single
crimson accent used with restraint. Strong typographic contrast pairs **DM
Serif Display** headlines with a tracked **Saira Condensed** for kickers,
labels and the footer, over a readable **Newsreader** body serif. Real CSS
drop-caps, oversized pull quotes, an asymmetric grid and full-bleed crimson
**section** dividers give the deck the rhythm of a printed feature.

## Slide classes

| Class | Use |
|---|---|
| `title` | Magazine-cover slide (masthead bar, kicker, byline rule) |
| `normal` | Default content slide — auto-wrapped header / content / footer |
| `section` | Full-bleed crimson divider; add `ink` for a near-black variant |
| `quote` | Full-slide pull quote on paper |

Modifiers: `centered`, `fullspace`.

## Editorial content utilities

- `dropcap` — large crimson drop-capital on a paragraph's first letter
- `kicker` — condensed uppercase eyebrow above a heading or block
- `pull` — oversized display-serif pull-quote text inside a normal slide
- `byline` — small condensed attribution / source line
- `frame` — full-bleed CSS "photo plate" placeholder (no image files); add a
  `<span class="cap">` for a printed caption
- `rule` — a hairline horizontal rule element
- `metric` / `metric-label` — big serif figures for the by-the-numbers sidebar

Plus the usual colour helpers (`accent` / `orange` = crimson, `blue` = slate,
`plus`/`minus`, `muted`, …) and `callout` / `warning` / `success` / `danger`
boxes. See `template/template.json` for the full list.

## Animations (used sparingly)

- **Auto-Animate** drives one beat only: the "9.4 minutes" figure scaling and
  recolouring across two adjacent slides in `30numbers.md` (shared
  `data-id="bignum"`). Keep motion this purposeful.
- `||text||` wraps a fragment for step-by-step reveals when needed.

## Demo deck

`presentation.json` builds a sample feature — *The Slow Web*, from the
fictional *GRAIN №04, The Craft Issue* — with a cover title slide, a crimson
feature-opening divider plus a drop-cap opening paragraph, a two-column
editorial spread, a by-the-numbers sidebar with the auto-animated figure, a
full-bleed pull quote, and an ink colophon. Several slides carry speaker
`Note:` blocks (press **S** in reveal.js for the presenter view).

## Preview

```
~/git/gitshow/gitshow/gitshow.js serve
```

then open <http://localhost:8000/>.
