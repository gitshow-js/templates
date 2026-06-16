<!-- .slide: class="section" -->

<header>
    <p class="eyebrow">Part 03</p>
    <h1>Drawing the Grid</h1>
    <p>From an empty canvas to an infinite neon road — in twelve lines.</p>
</header>

Note:
This full synthwave divider gives the deck a breath and resets the room.
Use section slides sparingly — one per major beat is plenty. Then start the
live-coding bit on the next slide.

---

<!-- .slide: data-auto-animate -->
# Grid Horizon

Start with the bare loop — clear, set the neon stroke, nothing on screen yet:

```js
function frame(t) {
  ctx.fillStyle = "#0a0118";
  ctx.fillRect(0, 0, W, H);
  ctx.strokeStyle = "#ff2e97";
  ctx.lineWidth = 2;
  requestAnimationFrame(frame);
}
```
<!-- .element: data-id="grid" -->

=--

<!-- .slide: data-auto-animate -->
# Grid Horizon

Now scroll a perspective grid toward the vanishing point &ndash; instant retro road:

```js
function frame(t) {
  ctx.fillStyle = "#0a0118";
  ctx.fillRect(0, 0, W, H);
  ctx.strokeStyle = "#ff2e97";
  ctx.lineWidth = 2;
  const horizon = H * 0.55, scroll = (t * 0.06) % 40;
  for (let z = scroll; z < 600; z += 40) {       // receding rows
    const y = horizon + (H - horizon) * (40 / z);
    line(0, y, W, y);
  }
  for (let x = -20; x <= 20; x++) {               // radiating columns
    line(W / 2, horizon, W / 2 + x * 90, H);
  }
  requestAnimationFrame(frame);
}
```
<!-- .element: data-id="grid" -->

<div class="callout small">
Auto-Animate keeps the matched code block in place and fades the new lines in &ndash; the audience sees exactly what changed. Two adjacent slides, same <code>data-id="grid"</code>.
</div>

Note:
This is the one auto-animated beat in the deck — the code block grows from the
bare loop into the full grid renderer because both slides share `data-id="grid"`.
Keep motion this purposeful, never decorative.
