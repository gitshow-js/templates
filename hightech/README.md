# hightech — High-tech template for technical & engineering talks

A light, "spec-sheet" aesthetic built for web-engineering and CS conference
talks: an airy blueprint-grid canvas, ink slide titles marked with a
signal-orange `//`, an azure secondary accent, and a `JetBrains Mono` + `Hanken
Grotesk` type pairing. Dark blueprint **section** slides give the deck rhythm.

## Slide classes

| Class | Use |
|---|---|
| `title` | Cover slide (logo bar, eyebrow, authors) |
| `normal` | Default content slide — auto-wrapped header / content / footer |
| `section` | Dark blueprint divider between major parts |
| `quote` | Full-slide pull quote |

Modifiers: `centered`, `fullspace`. Content utilities include `col`, `tag`,
`metric` / `metric-label`, `status-ok|warn|error`, `callout` / `warning` /
`success` / `danger`, and the usual colour helpers (`accent`, `blue`, `plus`,
`minus`, …). See `template/template.json` for the full list.

## Animations (used sparingly)

- **Auto-Animate** drives two beats only: the TTFB bar morph in `30perf.md`
  and the islands code build-up in `40code.md`. Adjacent slides share a
  `data-id`; keep motion purposeful, never decorative.
- `||text||` wraps a fragment for step-by-step reveals when you need them.

## Demo deck

`presentation.json` builds a sample talk — *Rendering at the Edge* — covering a
title slide, an agenda with a vertical sub-slide, a tech-stack/code slide, a
dark section divider plus Core Web Vitals metrics, an auto-animated code
walkthrough, and a closing slide. Several slides carry speaker `Note:` blocks
(press **S** in reveal.js for the presenter view).

## Preview

```
~/git/gitshow/gitshow/gitshow.js serve
```

then open <http://localhost:8000/>.
