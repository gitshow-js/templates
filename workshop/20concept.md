# What We're Building

A tiny `wordcount` clone: pass it a file, get back lines, words, and bytes — just like the classic `wc`.

<div class="terminal"><span class="pr">$</span> <span class="cm">wordcount notes.txt</span>
<span class="hl">  12   84  511</span> <span class="dim">notes.txt</span></div>

The shape of every CLI is the same three moves:

<div class="step"><strong>Read the arguments.</strong> Grab the file path the user typed after the program name.<span class="step-note">cargo gives us <code>std::env::args()</code> for free — no dependencies yet.</span></div>

<div class="step"><strong>Do the work.</strong> Open the file, count what we care about, handle the "file not found" case gracefully.<span class="step-note">Errors are values in Rust — we will use <code>Result</code> and the <code>?</code> operator.</span></div>

<div class="step"><strong>Print the result.</strong> Format the three numbers and the filename to standard output.</div>

<div class="callout">
We start with the standard library only. In the exercise you will swap hand-rolled parsing for the <code>clap</code> crate.
</div>

Note:
Resist the urge to reach for crates immediately. Showing the std-lib version
first makes it obvious *why* clap is worth adding later. Keep the three-step
mental model visible — we return to it on the recap slide.

=--

# The Mental Model

<div class="col">

## Input
<span class="tag">argv</span>
<span class="tag">stdin</span>
<span class="tag">files</span>

Everything a CLI consumes arrives as text or bytes.

</div>
<div class="col">

## Output
<span class="tag plus">stdout</span>
<span class="tag">stderr</span>
<span class="tag">exit code</span>

Data goes to **stdout**, diagnostics go to **stderr**. Keep them separate so pipes stay clean.

</div>

<div style="clear: both"></div>

<div class="warning">
A tool that prints errors to <em>stdout</em> will corrupt the next command in a pipeline. This bites everyone once.
</div>

Note:
This vertical sub-slide (press DOWN) is the "why two output streams" aside.
Good place for the `wordcount big.txt | sort` anecdote.
