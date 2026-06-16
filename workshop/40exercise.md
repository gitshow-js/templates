# Your Turn

<div class="exercise">
<strong>Add a <code>--lines</code> flag.</strong> When the user passes <code>--lines</code> before the path, print <em>only</em> the line count. Otherwise keep the full three-number output.

<p class="small" style="margin-bottom:0">Hints: collect <code>env::args()</code> into a <code>Vec&lt;String&gt;</code>, check for the flag, then pick the path from the remaining argument. Don't reach for a crate yet — std lib is enough.</p>
</div>

## Expected behaviour

<div class="terminal"><span class="pr">$</span> <span class="cm">cargo run -- --lines notes.txt</span>
<span class="hl">12</span>
<span class="pr">$</span> <span class="cm">cargo run -- notes.txt</span>
<span class="hl">  12   84  511</span> <span class="dim">notes.txt</span></div>

<div class="callout small">
<strong>Stretch goal:</strong> handle the flag appearing <em>after</em> the path too, and print a friendly usage line to <strong>stderr</strong> when no path is given.
</div>

Work in pairs — **8 minutes**. We'll compare solutions, then refactor to `clap` together.

Note:
Set a visible timer. Circulate and look for two common bugs: (1) forgetting that
`args()` element 0 is the program name, and (2) printing the usage message to
stdout instead of stderr. Ask a pair to share their approach before you reveal
the model solution.
