# Ingestion Trend &amp; Q3 Forecast

Daily peak events, last six weeks (billions), with the cyan bar marking the current week:

<div class="spark" style="max-width: 70%; margin: 0.6em 0 1.2em 0;">
<i style="height: 52%"></i>
<i style="height: 58%"></i>
<i style="height: 55%"></i>
<i style="height: 67%"></i>
<i style="height: 74%"></i>
<i style="height: 88%"></i>
</div>

<div class="col">

## Trajectory
- 6-week growth rate holding near **+3%/wk**
- Q3 close projected at **5.6 B/day** at current pace
- Headroom on the fleet: **~38%** before the next scale-out

</div>
<div class="col">

## Capacity Plan
- Re-shard <code>events_wide</code> -- recovers p99 budget
- Add 2 ingest cells in <span class="tag">eu-west</span>
- Trim legacy CSV export path

</div>

<div style="clear: both"></div>

<div class="callout small">
Forecast assumes no major customer onboarding; the pending <em>Meridian</em> contract would add ~0.4 B/day and pull the scale-out forward two weeks.
</div>

---

<!-- .slide: data-auto-animate -->
# Capacity Headroom

<p class="metric-label">Fleet utilization at quarter end</p>

<div data-id="util" style="height: 96px; width: 62%; border-radius: 6px; display: flex; align-items: center; padding-left: 1.1rem; color: #0a0f18; font-family: var(--dx-mono); font-weight: 700; font-size: 1.1em; background: linear-gradient(90deg, var(--dx-positive), #6ee7b7);">62% used</div>

Today the fleet runs comfortably -- a third of capacity is in reserve.

---

<!-- .slide: data-auto-animate -->
# Capacity Headroom

<p class="metric-label">Projected with the Meridian contract</p>

<div data-id="util" style="height: 96px; width: 87%; border-radius: 6px; display: flex; align-items: center; padding-left: 1.1rem; color: #0a0f18; font-family: var(--dx-mono); font-weight: 700; font-size: 1.1em; white-space: nowrap; background: linear-gradient(90deg, var(--dx-warning), #fcd34d);">87% used</div>

Onboarding Meridian pushes utilization into the watch zone -- the scale-out must land first. Auto-Animate morphs the bar between the two slides.

Note:
This is the one auto-animated beat in the deck. The utilization bar grows and
recolours green-to-amber because both slides share `data-id="util"`. Keep motion
this purposeful -- it shows the audience exactly what the new contract costs us.
