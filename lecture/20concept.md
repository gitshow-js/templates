# The Big Idea

A <span class="keyterm">hash function</span> takes any key &ndash; a word, a name, a number &ndash; and turns it into a position in a table.

<div class="flow">
  <span class="node coral">key<br>"Maya"</span>
  <span class="arrow">→</span>
  <span class="node">hash()<br><span class="small muted">add up letters,<br>then mod 8</span></span>
  <span class="arrow">→</span>
  <span class="node">slot<br><strong>3</strong></span>
</div>

The same key *always* lands in the same slot. So to find "Maya" later, we run the same function and look in **one** place.

<div class="success">
No searching. We <em>compute</em> the address. That is what makes lookups feel instant.
</div>

Note:
The keyterm "hash function" is highlighted on purpose — point at it. Use the
"Maya" example concretely: M=13, a=1, y=25, a=1 → 40, and 40 mod 8 = 0... but
keep the slide's number simple, students can do the arithmetic on the next slide.
Stress the one promise: same key, same slot, every time.

---

# The Table

A <span class="keyterm">hash table</span> is just an array of slots. The hash function tells us which slot to use.

<div class="flow">
  <span class="node bucket">0</span>
  <span class="node bucket">1</span>
  <span class="node bucket">2</span>
  <span class="node bucket" style="border-style: solid; border-color: var(--lec-coral);">3<br><span class="small">Maya</span></span>
  <span class="node bucket">4</span>
  <span class="node bucket">5</span>
  <span class="node bucket">6</span>
  <span class="node bucket">7</span>
</div>

But what if two different keys hash to the **same** slot? That is called a <span class="keyterm">collision</span> &ndash; and it is the next thing we will solve.
