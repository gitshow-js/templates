# Method: Sparse Routing <!-- .slide: data-auto-animate -->

A lightweight **router** scores each candidate block, then attention is computed
only over the top-$k$ selected blocks per query.

We begin from standard scaled dot-product attention:

`$$\mathrm{Attn}(Q,K,V) = \mathrm{softmax}\!\left(\frac{QK^{\top}}{\sqrt{d_k}}\right)V$$`

The router learns a gate $g_i \in [0,1]$ over blocks; the rest is masked out.

=--

# Method: Sparse Routing <!-- .slide: data-auto-animate -->

A lightweight **router** scores each candidate block, then attention is computed
only over the top-$k$ selected blocks per query.

We restrict the softmax to a learned, sparse support set $\mathcal{S}_k$:

`$$\mathrm{Attn}(Q,K,V) = \mathrm{softmax}\!\left(\frac{QK^{\top}}{\sqrt{d_k}} + \log g\right)V, \quad g_i = \mathbb{1}\!\left[i \in \mathcal{S}_k\right]$$`

<div class="result">
Adding the log-gate <em>inside</em> the softmax keeps routing differentiable, so
the selector trains end-to-end with the backbone &ndash; no separate index, no
straight-through estimator.
</div>

Note:
This is the one auto-animate beat. The shared equation morphs: the plain
softmax gains the +log g term and the support-set constraint. Both slides share
the title and the displayed equation, so MathJax containers animate in place.
Pause on the second slide -- the differentiability point is the contribution.
