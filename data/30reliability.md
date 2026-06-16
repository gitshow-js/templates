<!-- .slide: class="section" -->

<header>
    <p class="eyebrow">Part 02</p>
    <h1>Reliability &amp; Incidents</h1>
    <p>Two incidents this quarter. Total user-facing downtime: 21 minutes against a 43-minute monthly error budget.</p>
</header>

Note:
This darker divider resets attention before the incident detail. Keep section
slides to one per major part. Mention the error budget framing up front -- it
sets up the SLO callout on the next slide.

---

# SLO &amp; Incident Log

<div class="col">

## Service Health
<span class="status-ok">Ingestion API -- nominal</span><br/>
<span class="status-ok">Query gateway -- nominal</span><br/>
<span class="status-warn">Export workers -- degraded</span><br/>
<span class="status-error">Legacy CSV connector -- failing</span>

## Tags
<span class="tag accent">SLO 99.9%</span>
<span class="tag">multi-region</span>
<span class="tag">auto-failover</span>

</div>
<div class="col">

| Date | Incident | Sev | MTTR |
|---|---|---|---|
| Apr 14 | Kafka rebalance storm | S2 | 12 m |
| May 30 | Export queue backlog | S3 | 9 m |

<div class="success">
Both incidents auto-detected by alerting before any customer ticket. MTTR down from a 19-minute trailing average.
</div>

</div>

<div style="clear: both"></div>

<div class="callout">
<strong>Error budget:</strong> 53% of the quarterly 99.9% budget remains. We are well inside SLO and can spend budget on the Q3 re-sharding rollout.
</div>

Note:
The SLO callout is the punchline of this slide: we have budget to spend, which
gives us room for the riskier re-sharding work next quarter. Note status-ok /
warn / error each render a glowing coloured dot.
