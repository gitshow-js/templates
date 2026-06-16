# At a Glance

The quarter in four numbers, quarter-over-quarter:

<div class="tile-grid cols-4">

<div class="tile ok">
<span class="metric-label">Events ingested / day</span>
<span class="metric">4.8<span class="unit">B</span></span>
<span class="delta plus">▲ 18%</span>
</div>

<div class="tile ok">
<span class="metric-label">Availability (SLO 99.9%)</span>
<span class="metric">99.96<span class="unit">%</span></span>
<span class="delta plus">▲ 0.07pp</span>
</div>

<div class="tile warn">
<span class="metric-label">p99 query latency</span>
<span class="metric">412<span class="unit">ms</span></span>
<span class="delta minus">▲ 9%</span>
</div>

<div class="tile ok">
<span class="metric-label">Cost / million events</span>
<span class="metric">$0.31</span>
<span class="delta plus">▼ 12%</span>
</div>

</div>

<div class="callout">
Volume is up <strong>18%</strong> while unit cost is <em>down</em> -- but p99 query latency is creeping toward its budget. That tension frames the rest of the review.
</div>

Note:
Don't dwell on every tile -- call out the story: we grew, we got cheaper, and
the one yellow tile (p99 latency) is the thing we'll spend time on later.
Latency delta is "up" which is bad here, hence the red minus chip.
