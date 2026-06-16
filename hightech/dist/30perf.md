<!-- .slide: class="section" -->

<header>
    <p class="eyebrow">Part 03</p>
    <h1>Measuring What Ships</h1>
    <p>Field data beats lab data. Every number here is p75, mobile, real users.</p>
</header>

Note:
This dark divider gives the deck a breath and resets attention.
Use section slides sparingly — one per major part is plenty.

---

# Core Web Vitals

<div class="col centered">
<span class="metric plus">0.18<span class="unit">s</span></span>
<span class="metric-label">Largest Contentful Paint</span>
</div>
<div class="col centered">
<span class="metric">0.02</span>
<span class="metric-label">Cumulative Layout Shift</span>
</div>

<div style="clear: both"></div>

| Metric | Before | After | Verdict |
|---|---|---|---|
| TTFB | 820 ms | 180 ms | <span class="plus">−78%</span> |
| LCP | 3.4 s | 1.1 s | <span class="plus">−68%</span> |
| Total JS | 540 kB | 92 kB | <span class="plus">−83%</span> |
| Hydration | 1.2 s | 0.3 s | <span class="plus">−75%</span> |

<div class="success">
Shipping HTML-first and hydrating islands cut blocking JavaScript by an order of magnitude.
</div>

---

<!-- .slide: data-auto-animate -->
# Time to First Byte

<div data-id="bar" style="background: var(--ht-negative); height: 90px; width: 82%; border-radius: 6px; display: flex; align-items: center; padding-left: 1rem; color: white; font-family: var(--ht-mono); font-weight: 700;">820 ms — origin SSR</div>

Rendering on a single origin means every user pays the round-trip to one region.

---

<!-- .slide: data-auto-animate -->
# Time to First Byte

<div data-id="bar" style="background: var(--ht-positive); height: 90px; width: 18%; border-radius: 6px; display: flex; align-items: center; padding-left: 1rem; color: white; font-family: var(--ht-mono); font-weight: 700; white-space: nowrap;">180 ms — edge</div>

The same render, executed at the nearest PoP. Auto-Animate morphs the bar between the two slides.

Note:
This is the one auto-animated beat in the deck. The bar shrinks and recolours
because both slides share `data-id="bar"`. Keep motion this purposeful — never decorative.
