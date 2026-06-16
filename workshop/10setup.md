# Before We Start

You will need these installed and on your `PATH`:

<span class="tag accent">rustc 1.78+</span>
<span class="tag">cargo</span>
<span class="tag">a terminal</span>
<span class="tag">any editor</span>

## Verify your toolchain

<div class="terminal"><span class="pr">$</span> <span class="cm">rustc --version && cargo --version</span>
<span class="ok">rustc 1.78.0 (9b00956e5 2026-04-29)</span>
<span class="ok">cargo 1.78.0 (54d8815d0 2026-04-21)</span></div>

<div class="success">
If both versions print, you are ready. If not, install via <code>rustup</code> from <a href="https://rustup.rs">rustup.rs</a> and re-open your terminal.
</div>

## Create the project

<div class="terminal"><span class="pr">$</span> <span class="cm">cargo new wordcount --bin</span>
<span class="dim">    Creating binary (application) `wordcount` package</span>
<span class="pr">$</span> <span class="cm">cd wordcount && cargo run</span>
<span class="hl">Hello, world!</span></div>

Note:
Walk the room while this runs. The most common failure is an outdated toolchain
on a corporate laptop — have them run `rustup update` if `rustc --version`
prints anything below 1.78. Everyone should see "Hello, world!" before moving on.
