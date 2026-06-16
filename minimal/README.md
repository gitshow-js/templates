# minimal — Brutally minimal template for focus-mode keynotes

A light, near-monochrome template for "one big idea" talks — the kind where the
speaker projects a few words and then talks. Enormous negative space, a single
typeface (`Familjen Grotesk`) across every weight, and exactly one colour event:
a small red dot / underline (`#ff3b30`) used like punctuation. Chrome is reduced
to a quiet slide number. Elegance through subtraction.

## Slide classes

| Class | Use |
|---|---|
| `title` | Cover slide (logo bar, eyebrow, one word, authors) |
| `normal` | Default content slide — auto-wrapped header / content / footer |
| `section` | Inverted near-black divider with white text and the red dot |
| `quote` | Full-slide centred pull quote |

Modifiers: `centered`, `fullspace` (combine both for a slide that is nothing but
a single centred statement). Content utilities include `lead` (the oversized
one-line statement that is the workhorse here), `kicker` (all-caps label),
`metric` / `metric-label`, `dot` (the standalone red mark), `rule` (a thin red
divider), plus the usual `callout` / `warning` / `success` / `danger` and colour
helpers. Note: the colour helpers (`blue`, `amber`, `gold`, …) are intentionally
collapsed onto greys + the one red, so the restraint never breaks. See
`template/template.json` for the full list.

## Animations (used once, on purpose)

- **Auto-Animate** drives a single beat: the statistic in `20metric.md` holds
  its position across two adjacent slides while a kicker fades in and the number
  recolours to red. Both slides share `data-id` on the figure and caption. In a
  minimal deck one moving element carries the whole weight — keep it that way.
- `||text||` wraps a fragment for step-by-step reveals when you need them.

## Demo deck

`presentation.json` builds a sample talk — *Subtract*, a design-philosophy talk
about doing less: a one-word title, a one-line provocation, a single big
statistic, an inverted three-word progression divider, a centred pull quote, and
a one-word close. Several slides carry speaker `Note:` blocks (press **S** in
reveal.js for the presenter view).

## Preview

```
~/git/gitshow/gitshow/gitshow.js serve
```

then open <http://localhost:8000/>.
