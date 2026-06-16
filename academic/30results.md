<!-- .slide: class="section" -->

<header>
    <p class="eyebrow">Part 03</p>
    <h1>Does It Read Less, and Read Right?</h1>
    <p>Evaluated on RULER-1M and a held-out multi-hop QA suite. All numbers are mean over five seeds.</p>
</header>

Note:
This muted divider lets the talk breathe before the numbers. Use section
slides sparingly -- one per major part is plenty. Tell the audience the next
slide is the headline result.

---

# Results

<div class="col centered">
<span class="metric plus">+6.4</span>
<span class="metric-label">Multi-hop QA · exact match</span>
</div>
<div class="col centered">
<span class="metric accent">11<span class="unit">%</span></span>
<span class="metric-label">Blocks attended per query</span>
</div>

<div style="clear: both"></div>

| Model | Context | EM | Recall@10 | FLOPs (rel.) |
|---|---|---|---|---|
| Dense attention | 128K | 61.2 | 88.1 | 1.00 |
| Fixed sparse (window) | 1M | 58.7 | 79.4 | <span class="plus">0.21</span> |
| Retrieval-augmented | 1M | 63.0 | 85.2 | <span class="plus">0.30</span> |
| **Sparse Routing (ours)** | 1M | **67.6** | **91.3** | <span class="plus">0.18</span> |

<div class="result">
At <strong>18%</strong> of dense FLOPs, sparse routing recovers <strong>+6.4 EM</strong>
over the dense baseline while reading only the relevant 11% of blocks.
</div>

Note:
Don't read the table aloud -- let the bold row carry it. The headline is that we
beat dense accuracy at a fraction of the cost; the result box restates it for
people skimming from the back.
