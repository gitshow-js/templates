<!-- .slide: data-auto-animate -->
# Islands, Step by Step

Start with a plain server-rendered component — **zero** client JavaScript:

```jsx
export function PriceChart({ data }) {
  return (
    <figure class="chart">
      {renderSVG(data)}
    </figure>
  );
}
```
<!-- .element: data-id="island" -->

=--

<!-- .slide: data-auto-animate -->
# Islands, Step by Step

Mark it as an island — now *only this subtree* hydrates on the client:

```jsx
export function PriceChart({ data }) {
  return (
    <figure class="chart" client:visible>
      {renderSVG(data)}
      <Tooltip />
      <ZoomControls />
    </figure>
  );
}
```
<!-- .element: data-id="island" -->

<div class="callout small">
<code>client:visible</code> defers hydration until the element scrolls into view — the rest of the page stays static HTML.
</div>

Note:
Auto-Animate keeps the matched code block in place and fades the new lines in,
so the audience sees exactly what changed. Two adjacent slides, same `data-id="island"`.

---

<!-- .slide: class="quote" -->

> The fastest JavaScript is the JavaScript you never ship.

<p class="attrib">— a principle worth tattooing on every bundle</p>

Note:
A quote slide to land the section. Pause here before moving to the wrap-up.
