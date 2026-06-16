# workshop — Light, code-forward template for hands-on coding workshops

A bright, friendly, clearly-signposted aesthetic built for tutorials, coding
workshops, and developer-relations sessions where the audience codes along: a
clean white "notebook" canvas with a faint dotted grid, indigo signposting,
numbered **step** badges, green **"your turn"** exercise callouts, dark
**terminal** output blocks, split code/output columns, and a high-contrast
syntax theme tuned for live reading. Type pairing is `Lexend` (display & body)
+ `JetBrains Mono` (code, badges, footer). Indigo **section** slides announce
each module.

## Slide classes

| Class | Use |
|---|---|
| `title` | Cover slide (logo bar, eyebrow, authors) |
| `normal` | Default content slide — auto-wrapped header / content / footer |
| `section` | Indigo module divider between major parts |
| `quote` | Full-slide pull quote |

Modifiers: `centered`, `fullspace`.

## Workshop-specific content classes

- `step` — numbered step badge for "do this, then this" call-along layouts.
  The counter resets per slide; use one `<div class="step">` per step.
- `exercise` — green "▶ YOUR TURN" callout box for a task the audience completes.
- `terminal` — dark terminal-style block. Helper spans inside: `.pr` (prompt
  `$`), `.cm` (typed command), `.ok` / `.hl` (highlighted output), `.dim`.
- `tag` — mono pill for tools / versions; modifiers `.accent` (indigo) and
  `.plus` (green).

Plus the usual utilities: `col`, `callout` / `warning` / `success` / `danger`,
`metric` / `metric-label`, `box`, `shadow`, `cite`, and colour helpers
(`accent`, `blue`, `plus`, `minus`, `amber`, …). See `template/template.json`
for the full list.

## Animations (used sparingly)

- **Auto-Animate** drives one beat: the two-pass live-coding build-up in
  `30build.md`. Adjacent slides share `data-id="src"`, so reveal.js morphs the
  growing `src/main.rs` in place; `[…]` line-highlight steps narrate each region.
- `||text||` wraps a fragment for step-by-step reveals when you need them.

## Demo deck

`presentation.json` builds a sample workshop — *Build a CLI in Rust — Hands-On*
— covering a title slide, a setup/prerequisites slide (`tag`s + `terminal`
install check), a concept slide with numbered `step`s and a vertical sub-slide,
an indigo section divider, a guided auto-animated code build-up, a "your turn"
`exercise` with expected `terminal` output, and a recap + resources slide with a
closing quote. Several slides carry speaker `Note:` blocks (press **S** for the
presenter view).

## Preview

```
~/git/gitshow/gitshow/gitshow.js serve
```

then open <http://localhost:8000/>.
