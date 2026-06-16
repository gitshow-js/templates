# academic — Scholarly template for research talks & lectures

A calm, citation-friendly light template for conference talks and lectures aimed
at researchers and graduate students. A warm paper canvas with a journal-style
hairline rule under every running head, serif `Spectral` titles over an `IBM
Plex Sans` body, a deep-teal primary accent and an oxblood secondary. Decoration
is restrained so figures, **MathJax equations**, and references carry the slide.
Muted slate **section** dividers give the talk rhythm.

## Slide classes

| Class | Use |
|---|---|
| `title` | Cover slide (logo masthead, eyebrow, authors + affiliations) |
| `normal` | Default content slide — auto-wrapped header / content / footer |
| `section` | Muted slate divider between major parts |
| `quote` | Full-slide pull quote |

Modifiers: `centered`, `fullspace`.

## Scholarly extras

- `result` — teal-tinted box for a key finding or theorem (auto-labelled "Result").
- `r-ref` — inline superscript-style citation marker, e.g. `<span class="r-ref">3</span>` → ³.
- `r-refs` — small reference-list container pinned along the bottom of a slide;
  wrap an `<ol>` of citations, use `<span class="authors">` for names.

Plus the usual utilities: `col`, `metric` / `metric-label`, `callout` /
`warning` / `success` / `danger`, `box`, `cite`, and the colour helpers
(`accent` = teal, `blue` = steel, `plus`, `minus`, …). See
`template/template.json` for the full list.

## Equations

MathJax (via the `mathjax2` plugin) renders inline `$…$` and display `$$…$$`
math. Display equations are boxed with a teal rule so theorems and key formulas
read prominently.

## Animations (used sparingly)

- **Auto-Animate** drives one beat only: the attention equation in `20method.md`
  morphs from plain softmax to the log-gated, sparse-support form across two
  adjacent slides that share the same title and displayed equation.
- `||text||` wraps a fragment for step-by-step reveals when you need them.

## Demo deck

`presentation.json` builds a sample talk — *Sparse Routing for Long-Context
Retrieval* — with a title slide (authors + fictional affiliations), motivation
and prior-work background, a method slide with a real-looking attention/softmax
equation, a results slide (baseline comparison table + `result` box), a
discussion slide using `r-ref` markers and an `r-refs` list, a quote, and a
closing slide with references. Several slides carry speaker `Note:` blocks
(press **S** in reveal.js for the presenter view).

All names, affiliations, emails, and URLs in the demo are fictional.

## Preview

```
~/git/gitshow/gitshow/gitshow.js serve
```

then open <http://localhost:8000/>.
