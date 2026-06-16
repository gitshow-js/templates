# The Edge Stack

<div class="col">

## Runtime
<span class="tag accent">Workers</span>
<span class="tag">V8 isolates</span>
<span class="tag">WASM</span>

Cold starts measured in **single-digit milliseconds** — no container to spin up.

</div>
<div class="col">

## Framework
<span class="tag blue">Streaming SSR</span>
<span class="tag">Islands</span>
<span class="tag">RSC</span>

Ship HTML first, hydrate **only** the interactive islands.

</div>

<div style="clear: both"></div>

| Component | Choice | Status |
|---|---|---|
| Edge runtime | V8 isolates | <span class="status-ok">production</span> |
| Cache layer | Tiered KV + HTTP | <span class="status-ok">production</span> |
| Image pipeline | On-the-fly AVIF | <span class="status-warn">beta</span> |
| Edge database | Regional replicas | <span class="status-error">experimental</span> |

Note:
Don't read the table aloud — let it sit. Emphasise that "experimental" is honest:
edge databases solve read latency but consistency is still a hard problem.

=--

# Routing the Request

A request never travels further than the nearest PoP before it gets *some* HTML:

```js
export default {
  async fetch(request, env, ctx) {
    const url = new URL(request.url);
    const cached = await caches.default.match(request);
    if (cached) return cached;            // 1. edge cache hit → ~5 ms

    const stream = renderToReadableStream( // 2. stream HTML as it renders
      <App route={url.pathname} />,
      { signal: ctx.signal }
    );
    ctx.waitUntil(warmCache(request, stream.tee()));
    return new Response(stream, {
      headers: { "content-type": "text/html; charset=utf-8" },
    });
  },
};
```

The browser starts parsing **before** the server has finished rendering.
