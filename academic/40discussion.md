# Discussion & Limitations

<div class="col">

## What Holds Up
- Routing transfers across domains without re-training the gate<span class="r-ref">1</span>
- The selector is **interpretable**: gates align with human-annotated evidence spans<span class="r-ref">2</span>
- Stable training, with no auxiliary load-balancing loss

</div>
<div class="col">

## What Does Not
- Recall degrades when evidence is **diffuse** rather than clustered<span class="r-ref">3</span>
- Top-$k$ is fixed at inference; an adaptive $k$ is future work
- Evaluation is English-only; multilingual transfer untested

</div>

<div style="clear: both"></div>

<div class="warning">
The gate assumes relevant blocks are <em>locally coherent</em>. Where they are not,
fall back to a denser tier &ndash; we expose this as a tunable floor.
</div>

<p class="r-refs">
<ol>
<li><span class="authors">Anand &amp; Følke.</span> Cross-domain transfer of learned attention gates. <em>Workshop on Efficient Inference</em>, 2025.</li>
<li><span class="authors">Nakamura-Reyes et&nbsp;al.</span> Do sparse routers attend to evidence? <em>Findings of CLRW</em>, 2026.</li>
<li><span class="authors">Velthorn Orrery Lab.</span> Failure modes of block routing on diffuse contexts. Tech. report OR-26-04, 2026.</li>
</ol>
</p>

Note:
Be candid about the diffuse-evidence failure -- a research audience trusts a
talk more when limitations are stated plainly. The r-ref markers point at the
reference list pinned along the bottom.

---

<!-- .slide: class="quote" -->

> The art is not in attending to everything, but in knowing the little that is worth attending to.

<p class="attrib">— paraphrasing a reviewer of this very paper</p>

Note:
A short quote slide to land the section before the conclusion. Pause here.
