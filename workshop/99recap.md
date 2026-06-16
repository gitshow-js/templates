# Recap & Resources

You built a real CLI from three moves — **read args**, **do the work**, **print the result** — using nothing but the standard library.

<div class="col">

## What you can do now
- Read positional **and** flag arguments
- Open files and handle errors with `?`
- Keep **stdout** and **stderr** separate
- Run and ship with `cargo run` / `cargo build --release`

</div>
<div class="col">

## Where to go next
- <span class="tag accent">clap</span> derive-based argument parsing
- <span class="tag">anyhow</span> ergonomic error handling
- <span class="tag">assert_cmd</span> end-to-end CLI tests
- Publish to <span class="tag">crates.io</span>

</div>

<div style="clear: both"></div>

<div class="success">
Solutions, slides, and the finished repo: <a href="https://workshops.codeforge.dev/rust-cli">workshops.codeforge.dev/rust-cli</a> &nbsp;·&nbsp; questions to <a href="mailto:mira@codeforge.dev">mira@codeforge.dev</a>
</div>

Note:
Leave this slide up during Q&A so the repo link stays visible. Remind folks the
exercise solution (with the clap refactor) lives on the `clap` branch of the repo.

=--

<!-- .slide: class="quote" -->

> A good CLI does one thing, reads from stdin, and writes to stdout — so it composes with everything else.

<p class="attrib">— the Unix philosophy, still undefeated</p>

Note:
Optional closing beat — land the "build small tools that compose" idea before
wrapping up. Pause here, then go to Q&A.
