# lecture — Warm, friendly template for classroom lectures & online courses

A calm, approachable light template built for teaching: a warm cream canvas with
a soft sunlit glow, generously sized type that reads from the back row, rounded
friendly headings, a gentle teal accent and a warm coral secondary. Deep-teal
**section** slides give a lecture its breathing points. Type pairing is
`Baloo 2` (display) + `Nunito Sans` (body) + `Spline Sans Mono` (code & labels).

## Slide classes

| Class | Use |
|---|---|
| `title` | Cover slide (logo bar, eyebrow, authors) |
| `normal` | Default content slide — auto-wrapped header / content / footer |
| `section` | Warm deep-teal divider / pause-and-think break |
| `quote` | Full-slide pull quote |

Modifiers: `centered`, `fullspace`.

### Teaching-specific utilities

- `objective` — a teal "Today you will…" learning-objective checklist box.
- `keyterm` — highlights a key vocabulary term with a soft coral underline.

Plus the usual content utilities: `col`, `box`, `callout` / `warning` /
`success` / `danger`, `metric` / `metric-label`, `cite`, `shadow`, and the
colour helpers (`accent`, `blue`, `plus`, `minus`, `muted`, …). Simple HTML
diagrams use `.flow`, `.node` (with `.coral` / `.bucket` variants) and `.arrow`
to draw boxes-and-arrows with no external images. See `template/template.json`
for the full class list.

## Animations (used sparingly)

- **Auto-Animate** drives one beat: in `30example.md` a hash-table slot box
  grows and gains a second name to show a collision being resolved by chaining.
  Adjacent slides share `data-id="slot"`. Keep motion gentle and purposeful.
- `||answer||` wraps a fragment — used on the check-your-understanding slide so
  the answer is revealed only after students commit to a guess.

## Demo deck

`presentation.json` builds a sample lecture — *How Hashing Works* (a fictional
CS 101 class) — with a title slide, a learning-objectives slide (with an
optional vertical review sub-slide), a core-concept slide using a `keyterm` and
a styled HTML diagram, a worked step-through with an auto-animated collision
beat, a "pause and think" section divider plus a check-your-understanding
question with a fragment answer, and a recap with next steps and a closing
quote. Several slides carry speaker `Note:` blocks (press **S** for the
presenter view).

## Preview

```
~/git/gitshow/gitshow/gitshow.js serve
```

then open <http://localhost:8000/>.
