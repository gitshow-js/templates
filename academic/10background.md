# Motivation

Retrieval over long contexts is bottlenecked by **dense attention**, which scales
quadratically with sequence length:

- A 1M-token context costs ~$10^{12}$ pairwise scores per layer
- Most of that work is wasted &ndash; relevant evidence is **sparse and clustered**
- Truncation and chunking discard exactly the cross-document links we need

<div class="callout">
Our question: can a model <em>learn where to look</em> before it pays to look there?
</div>

Note:
The audience here is researchers, so don't belabour the quadratic-attention point.
Spend the time on the "sparse and clustered" observation -- that is the premise
the whole method rests on.

=--

# Prior Work

Three families, each trading recall for cost differently:

| Family | Mechanism | Weakness |
|---|---|---|
| Fixed sparse | Sliding / dilated windows | Misses long-range links |
| Retrieval-augmented | External index, top-k chunks | Index drifts from the model |
| Learned routing | Token-level gating | Unstable, costly to train |

<p class="r-refs">
<ol>
<li><span class="authors">Beltagy et&nbsp;al.</span> Longformer: the long-document transformer. <em>Proc. NLP Systems</em>, 2020.</li>
<li><span class="authors">Borgeaud et&nbsp;al.</span> Retrieval-augmented language modelling at scale. <em>JMLR</em>, 2022.</li>
</ol>
</p>

Note:
Frame our work as taking the strengths of learned routing while fixing its
instability -- that is the bridge to the method slide.
