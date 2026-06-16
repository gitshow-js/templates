# Core Metrics — Q1 → Q2

Full read-out across the ingestion and query tiers. Deltas are quarter-over-quarter.

| Metric | Q1 FY26 | Q2 FY26 | Delta | Status |
|---|---|---|---|---|
| Events / day (peak) | 4.07 B | 4.81 B | <span class="plus">+18.2%</span> | <span class="status-ok">healthy</span> |
| Ingest success rate | 99.91% | 99.97% | <span class="plus">+0.06pp</span> | <span class="status-ok">healthy</span> |
| Query p50 | 88 ms | 79 ms | <span class="plus">−10.2%</span> | <span class="status-ok">healthy</span> |
| Query p99 | 378 ms | 412 ms | <span class="minus">+9.0%</span> | <span class="status-warn">watch</span> |
| Pipeline lag (p95) | 14 s | 11 s | <span class="plus">−21.4%</span> | <span class="status-ok">healthy</span> |
| Cost / M events | $0.35 | $0.31 | <span class="plus">−11.4%</span> | <span class="status-ok">healthy</span> |
| Failed exports | 38 | 61 | <span class="minus">+60.5%</span> | <span class="status-error">action</span> |

<div class="col">
<div class="warning">
<strong>p99 latency</strong> rose with volume -- the hot shard for the <code>events_wide</code> table is the suspected cause. Re-sharding is scheduled for early Q3.
</div>
</div>
<div class="col">
<div class="danger">
<strong>Failed exports</strong> jumped 60%, concentrated on the legacy CSV connector. Migration to the streaming export API closes this gap.
</div>
</div>

<div style="clear: both"></div>

Note:
This is the dense table the data team came for. Tabular figures keep the
numeric columns aligned. Green = good direction, red = bad direction, regardless
of sign -- that's why a "+18%" on volume is green but "+9%" on p99 is red.
