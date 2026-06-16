# retro — Retro-futuristic synthwave template

A dark, maximalist **80s synthwave / retro-computing** aesthetic for playful
tech talks — community meetups, hackathons, and demoscene / creative-coding
sessions. Deep purple-black canvas (`#0a0118`) with a sunset gradient and a
neon perspective grid-horizon, dual neon accents (**magenta** + **electric
cyan**), a hot-yellow highlight, CRT scanline texture, and glowing chrome/neon
titles. Type pairing: `Chakra Petch` (display) + `Share Tech Mono` (body, code,
labels, tags). Snappy `slide` transition with a zoom background transition.

## Slide classes

| Class | Use |
|---|---|
| `title` | Cover slide (logo bar, eyebrow, authors, grid-horizon) |
| `normal` | Default content slide — auto-wrapped header / content / footer |
| `section` | Full synthwave sunset + grid-horizon divider with glowing title |
| `quote` | Full-slide pull quote |

Modifiers: `centered`, `fullspace`. Content utilities include `col`, `tag`
(neon pill), `metric` / `metric-label`, `callout` / `warning` / `success` /
`danger`, the colour helpers (`accent` / `orange` = magenta, `blue` = cyan,
`amber` / `gold` = hot yellow, `plus` = neon green, `minus` = neon red), and the
synthwave-specific extras `neon` (glowing accent text) and `glow` (adds a neon
box-shadow to any element). See `template/template.json` for the full list.

## Animations (used sparingly)

- **Auto-Animate** drives one beat: the grid-renderer code build-up in
  `30code.md`, where two adjacent slides share `data-id="grid"` and the new
  lines fade in over the matched block. Keep motion purposeful, never decorative.
- `||text||` wraps a fragment for step-by-step reveals when you need them.

## Demo deck

`presentation.json` builds a sample talk — *RETROWAVE.JS — Demos in the
Browser* — covering a title slide, a playful "why retro" intro with a vertical
sub-slide, a neon tech-stack/shader slide, a full synthwave section divider plus
an auto-animated canvas-code walkthrough, a stat/metric slide, a quote, and a
closing/contact slide. Several slides carry speaker `Note:` blocks (press **S**
in reveal.js for the presenter view).

## Preview

```
~/git/gitshow/gitshow/gitshow.js serve
```

then open <http://localhost:8000/>.
