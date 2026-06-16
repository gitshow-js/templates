# Agenda

What we will cover in the next 25 minutes:

1. The **rendering spectrum** — CSR, SSR, SSG, and everything between
2. A modern **edge stack** and how the pieces fit together
3. **Core Web Vitals** — what we measured, and what moved the needle
4. A **streaming SSR** walkthrough, line by line

<div class="callout">
Slides, code, and the benchmark harness are open source — link on the final slide.
</div>

Note:
Set expectations: this is hands-on and code-heavy toward the end.
Tell the audience the vertical arrow (down) drills into detail on some slides.

=--

# Why It Matters

- Every **100&nbsp;ms** of latency measurably moves conversion
- The median page now ships **&gt;&nbsp;2&nbsp;MB** of JavaScript
- Users are on mobile networks far more hostile than our dev laptops

<div class="warning">
We optimise for the device we <em>have</em>, not the device our users <em>hold</em>.
</div>

Note:
This vertical sub-slide is reached by pressing the DOWN arrow.
Good place to drop the "test on a real mid-range phone" anecdote.
