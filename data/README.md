# data — Instrument-panel template for analytics & status reports

A dark, dense, grid-based "instrument panel" aesthetic built for dashboards,
metrics reviews, and ops/data status reports: a deep navy canvas (`#0d1420`)
with faint dashboard gridlines, light slate text, a single cyan signal accent
(`#22d3ee`), and semantic green/amber/red status colours. Numbers are set in
`IBM Plex Mono` with tabular figures; body and headings use `IBM Plex Sans`.
Darker **section** panels with a cyan rule and glow give the deck rhythm.

## Slide classes

| Class | Use |
|---|---|
| `title` | Cover slide (logo bar, eyebrow, authors, cyan glow) |
| `normal` | Default content slide — auto-wrapped header / content / footer |
| `section` | Darker panel divider with a glowing cyan rule |
| `quote` | Full-slide pull quote |

Modifiers: `centered`, `fullspace`.

## Content utilities

- **KPI grid**: `tile-grid` (add `cols-2|3|4`) wrapping `tile` cards (variants
  `ok` / `warn` / `error` colour the left rail). Pair `metric` + `metric-label`
  + `delta` (`plus` / `minus`) inside a tile.
- **Status**: `status-ok` / `status-warn` / `status-error` render a glowing
  coloured dot + label; `tag` is a mono pill badge.
- **Charts**: `spark` (flex row of `<i>` bars sized by inline `height`) for
  sparklines, and `bar` for a single CSS track.
- **Callouts**: `callout` / `warning` / `success` / `danger`, plus `cite`,
  `box`, `shadow`.
- Colour helpers: `accent`, `blue` (both cyan), `plus`/`positive` (green),
  `minus`/`negative` (red), `amber`/`gold` (amber), `neutral`/`muted`/`grey`.
  Green/red track *direction*, not sign — a good "+18%" is green, a bad "+9%"
  p99 is red. See `template/template.json` for the full list.

## Animations (used sparingly)

- **Auto-Animate** drives one beat: the capacity-headroom bar in `40forecast.md`
  grows and recolours between two adjacent slides sharing `data-id="util"`.
- `||text||` wraps a fragment for step-by-step reveals when you need them.

## Demo deck

`presentation.json` builds a sample read-out — *Q2 Platform Health Review* for
the fictional SignalGrid analytics platform — covering a title slide, an
at-a-glance KPI tile grid, a dense core-metrics table, a reliability/incident
section with an SLO callout, a trend + forecast slide with a CSS sparkline and
the auto-animated capacity bar, and a closing next-actions slide. Several slides
carry speaker `Note:` blocks (press **S** in reveal.js for the presenter view).

## Preview

```
~/git/gitshow/gitshow/gitshow.js serve
```

then open <http://localhost:8000/>.
