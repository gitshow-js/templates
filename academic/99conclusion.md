# Conclusion

Sparse routing makes long-context retrieval **cheaper and more accurate** at once:

1. A differentiable log-gate selects blocks **inside** the softmax
2. End-to-end training &ndash; no external index, no straight-through estimator
3. **+6.4 EM** at **18%** of dense FLOPs on million-token contexts

<div class="success">
Code, checkpoints, and the RULER-1M routing splits are released at
<a href="https://orrery.research/sparse-routing">orrery.research/sparse-routing</a>.
</div>

<h2>Selected References</h2>

<div class="r-refs">
<ol>
<li><span class="authors">Anand, M., Følke, T., Nakamura-Reyes, P.</span> Sparse routing for long-context retrieval. <em>Proc. CLRW</em>, 2026.</li>
<li><span class="authors">Beltagy, I. et&nbsp;al.</span> Longformer: the long-document transformer. <em>Proc. NLP Systems</em>, 2020.</li>
<li><span class="authors">Borgeaud, S. et&nbsp;al.</span> Retrieval-augmented language modelling at scale. <em>JMLR</em>, 2022.</li>
<li><span class="authors">Nakamura-Reyes, P. et&nbsp;al.</span> Do sparse routers attend to evidence? <em>Findings of CLRW</em>, 2026.</li>
</ol>
</div>

Note:
Land on the three numbered takeaways, then point at the release link for Q&A.
Leave this slide up during questions so the references stay visible.
