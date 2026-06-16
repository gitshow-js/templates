# studio — Dark art-directed gallery template

A dark, curatorial "gallery after dark" aesthetic built for creative portfolios
and design case-study showcases. A near-black canvas (`#0e0e10`) with subtle
film-grain and vignette, oversized **Syne** display titles that let the work
breathe, a catalogue-style **Space Mono** index, and ONE vivid accent — acid
lime `#c6ff3a` — used as a spotlight. **Manrope** carries the body copy. Section
slides are bold geometric lime colour-blocks that reset attention between
projects.

## Slide classes

| Class | Use |
|---|---|
| `title` | Cover slide (logo bar, eyebrow, studio + author block) |
| `normal` | Default content slide — auto-wrapped header / content / footer |
| `section` | Bold lime geometric colour-block divider between projects |
| `quote` | Full-slide pull quote |

Modifiers: `centered`, `fullspace`.

## Studio content utilities

- `frame` — geometric image/work placeholder frame (CSS gradients + crop marks,
  no external image files). Add `blue` for the cool-secondary variant.
- `index` — mono catalogue project number, e.g. `01 / 06` (wrap the total in
  `<span class="total">`).
- `caption` — small uppercase mono project caption beneath a frame.
- `tag` — discipline pill; add `accent` or `blue` to tint.

Plus the shared set: `col`, `box`, `note`, `metric` / `metric-label`,
`callout` / `warning` / `success` / `danger`, `cite`, `shadow`, and the colour
helpers (`accent`, `blue`, `plus`, `minus`, `muted`, …). See
`template/template.json` for the full list.

## Animations (used sparingly)

- **Auto-Animate** drives one purposeful beat: in `20case-halden.md` the
  `frame` carrying `data-id="hero"` and the project title morph from a
  full-width cover into a detail layout across two adjacent slides.
- `||text||` wraps a fragment for step-by-step reveals when you need them.

## Demo deck

`presentation.json` builds a sample portfolio — *Selected Works 2026* by the
fictional **Studio FORMWORK** — with a title slide, a catalogue index, two
in-depth project case studies (one brand, one digital), a services/capabilities
slide with a closing principle quote, and a contact divider. Several slides
carry speaker `Note:` blocks (press **S** in reveal.js for the presenter view).

## Preview

```
~/git/gitshow/gitshow/gitshow.js serve
```

then open <http://localhost:8000/>.
