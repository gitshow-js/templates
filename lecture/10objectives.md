# Today's Plan

We have one big question to answer: *how can a computer find a name in a list of a million without checking them all?*

<div class="objective">

- Explain what a **hash function** does, in your own words
- Trace how a key becomes a slot in a table
- Predict and handle a **collision**
- Use a hash table to look something up in roughly *one* step

</div>

By the end you should be able to sketch the whole idea on a napkin. That is the goal.

Note:
Read the objectives out loud — students remember what they hear and see together.
Promise them the napkin sketch; come back to this slide at the very end so they
can check off each point. Keep the tone light and encouraging here.

=--

# Where We Left Off

Last week we searched a list the slow way:

- To find one name among **1,000**, we sometimes checked all **1,000**
- Double the list, double the work &ndash; that does not scale

<div class="callout">
Today's trick: instead of <em>searching</em> for where something is, we will <em>calculate</em> where it should be.
</div>

Note:
This vertical sub-slide (press DOWN) is optional review. Skip it if the class
is confident with linear search. Good moment to ask: "who remembers how long
linear search took?" before revealing the callout.
