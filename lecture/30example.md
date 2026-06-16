# Worked Example: Storing "Maya"

Let's do it together, step by step. Our table has **8** slots, and our hash function is simply: *add the letter positions, then take the remainder after dividing by 8.*

| Step | What we do | Result |
|---|---|---|
| 1 | Letter values: M=13, a=1, y=25, a=1 | sum = **40** |
| 2 | Take the remainder: 40 mod 8 | slot = **0** |
| 3 | Store "Maya" in slot 0 | done! |

<div class="callout small">
<code>mod</code> just means "the remainder after dividing." 40 &divide; 8 = 5 remainder <strong>0</strong>.
</div>

Note:
Walk the table row by row — do not reveal the answer before the class computes it.
Ask a student for each step. The point is that every step is mechanical: no
judgement, no searching, just arithmetic. Then move to the collision animation.

---

<!-- .slide: data-auto-animate -->
# Now Store "Liam"

"Liam" also hashes to slot **0**. A <span class="keyterm">collision</span>!

<div data-id="slot" class="node bucket" style="margin: 0.6em 0; border-color: var(--lec-coral); border-style: solid; width: 7em;">
slot 0<br><strong>Maya</strong>
</div>

We cannot just overwrite Maya. We need a plan.

---

<!-- .slide: data-auto-animate -->
# Chaining: Make a Little List

The fix is gentle: each slot holds a small *list*. Both names live in slot 0, side by side.

<div data-id="slot" class="node bucket" style="margin: 0.6em 0; border-color: var(--lec-coral); border-style: solid; width: 16em; text-align: left; padding: 0.8em 1em;">
slot 0<br><strong>Maya</strong> → <strong>Liam</strong>
</div>

To find "Liam" we still jump straight to slot 0 &ndash; then scan a list of *two*, not a million.

<div class="success">
Collisions are normal and totally fine. A good hash function just keeps the little lists <em>short</em>.
</div>

Note:
This is the deck's one auto-animated beat: the slot box grows and gains a second
name because both slides share `data-id="slot"`. Let the morph play, then
reassure the class — collisions sound scary but the handling is simple. Keep
motion this purposeful.
