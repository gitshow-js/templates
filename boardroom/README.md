# boardroom — Corporate strategy template, annual-report elegance

A refined, conservative template for board meetings, quarterly business reviews,
and investor updates. The aesthetic is *annual report*: a warm off-white paper
canvas with a faint texture, deep ink text, a single brass accent, and deep
forest green reserved for positive figures. Generous whitespace, hairline rules,
and restrained fades — nothing flashy. Type pairs a high-contrast serif
(`Fraunces`) with `Asap` body and `Spline Sans Mono` for figures, labels, and the
footer. Section dividers use a deep forest-green background with a brass eyebrow.

## Slide classes

| Class | Use |
|---|---|
| `title` | Cover slide (logo bar, eyebrow, authors) |
| `normal` | Default content slide — auto-wrapped header / content / footer |
| `section` | Deep forest-green divider between major parts |
| `quote` | Full-slide pull quote |

Modifiers: `centered`, `fullspace`. Content utilities include `col`, `lede`,
`eyebrow` / `kicker`, `rule`, `metric` / `metric-label` (serif numerals with a
`.delta` for deltas and `.unit` for units), `callout` / `warning` / `success` /
`danger`, `cite`, `box`, `shadow`, and the colour helpers (`accent`/`amber`/`gold`
→ brass, `blue` → forest, `plus`/`positive` → forest, `minus`/`negative` →
oxblood, `muted`/`grey`, `neutral`). See `template/template.json` for the full
list.

## Animations (used sparingly)

- **Auto-Animate** drives a single beat: the recurring-revenue bar in
  `30metrics.md` grows and recolours to forest green across two adjacent slides
  sharing `data-id="arr-bar"`. Motion stays quiet and purposeful.
- `||text||` wraps a fragment for step-by-step reveals when needed.

## Demo deck

`presentation.json` builds a fictional review — *FY26 Strategic Review* for
*Meridian Group* — with a title slide, an agenda (plus a vertical reading-key
sub-slide), a forest-green section divider with a segment table, four KPI metric
tiles plus the auto-animated revenue bar, three strategic priorities using
callout/success/warning boxes, a closing pull quote, and a Q&A slide. Several
slides carry speaker `Note:` blocks (press **S** in reveal.js for presenter view).

## Preview

```
~/git/gitshow/gitshow/gitshow.js serve
```

then open <http://localhost:8000/>.
