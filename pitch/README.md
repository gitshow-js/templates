# pitch — Bold dark pitch-deck template

A high-energy, billboard aesthetic built for fundraising and product launches in
front of VCs and angels: a near-black canvas with a low coral/slate vignette
glow, oversized `Archivo Black` headlines that read like posters, ONE electric
coral accent used with confidence, a cool slate-blue secondary, and full-bleed
statement **section** slides. Body copy is `Sora`; labels, counters, and the
footer are `Martian Mono`.

## Slide classes

| Class | Use |
|---|---|
| `title` | Cover slide (logo bar, eyebrow, big headline, authors) |
| `normal` | Default content slide — auto-wrapped header / content / footer |
| `section` | Full-bleed billboard statement between acts |
| `section solid` | Coral full-bleed variant — for the money slide / big number |
| `quote` | Full-slide pull quote |

Modifiers: `centered`, `fullspace`. Content utilities include `col`, `metric` /
`metric-label`, `kpi` / `kpi-label`, `bar` / `bar-fill` (growth charts), `tag`,
`callout` / `warning` / `success` / `danger`, `cite`, and the colour helpers
(`accent`, `blue`, `plus`, `minus`, `amber`, …). See `template/template.json`
for the full list.

## Animations (used sparingly)

- **Fast slide transitions** carry the deck's momentum.
- **Auto-Animate** drives exactly ONE beat: the ARR traction bar and number
  growing across two adjacent slides in `30market.md` (matched by `data-id`).
  Keep motion this purposeful, never decorative.
- `||text||` wraps a fragment for step-by-step reveals when you need them.

## Demo deck

`presentation.json` builds a sample seed pitch — *Nimbus — Seed Round* — for a
fictional cloud-cost-intelligence startup, following the pitch arc: a title
slide, the Problem (full-bleed), the Solution, Market size + Traction (big
metrics and an auto-animated growth bar), the Ask (coral money slide + use of
funds + a thesis quote), and a closing/contact slide. Several slides carry
speaker `Note:` blocks (press **S** in reveal.js for the presenter view).

## Preview

```
~/git/gitshow/gitshow/gitshow.js serve
```

then open <http://localhost:8000/>.
