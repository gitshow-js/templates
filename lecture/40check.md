<!-- .slide: class="section" -->

<header>
    <p class="eyebrow">Pause &amp; Think</p>
    <h1>Check Your Understanding</h1>
    <p>Try it before you peek. Talk to the person next to you for thirty seconds.</p>
</header>

Note:
This warm divider is a deliberate breather and a signal: time to stop taking
notes and start thinking. Actually run the thirty-second pair discussion —
do not rush it. Then advance to the question.

---

# Your Turn

Our table has **8** slots and the same hash function (add letter values, then mod 8).

**Question.** Into which slot does the key <span class="keyterm">"Bo"</span> go?

<div class="callout">
Hint: B = 2, o = 15. Add them, then take the remainder after dividing by 8.
</div>

Work it out, then reveal the answer:

||**2 + 15 = 17**, and **17 mod 8 = 1**, so "Bo" goes in **slot 1**. ✅||

<div class="success fragment">
If slot 1 were already taken, you would just add "Bo" to that slot's little list &ndash; chaining, exactly like before.
</div>

Note:
The answer is a reveal fragment — press SPACE/arrow to show it only after the
class has committed to a guess. Then reveal the second fragment to connect back
to chaining. Praise correct reasoning, not just the right number.
