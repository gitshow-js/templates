<!-- .slide: class="section" -->

<header>
    <p class="eyebrow">Module 02</p>
    <h1>Let's Write It Together</h1>
    <p>Open src/main.rs. We build the whole tool in two passes — watch the code grow.</p>
</header>

Note:
This indigo divider announces the live-coding module and resets attention.
Use section slides sparingly — one per major part of the workshop.

---

<!-- .slide: data-auto-animate -->
# Pass 1 — Read & Open

First, grab the path argument and open the file. Nothing fancy yet:

```rust [1-13|3-4|6-9|11-12]
use std::env;
use std::fs;

fn main() {
    let path = env::args().nth(1).expect("usage: wordcount <file>");

    let text = match fs::read_to_string(&path) {
        Ok(contents) => contents,
        Err(e) => {
            eprintln!("wordcount: {path}: {e}");
            std::process::exit(1);
        }
    };

    println!("read {} bytes", text.len());
}
```
<!-- .element: data-id="src" -->

We read the whole file into a `String` and bail out cleanly on errors — note `eprintln!` writes to **stderr**.

---

<!-- .slide: data-auto-animate -->
# Pass 2 — Count & Print

Now replace the placeholder print with the real counting logic:

```rust [1-21|11-13|15-20]
use std::env;
use std::fs;

fn main() {
    let path = env::args().nth(1).expect("usage: wordcount <file>");

    let text = match fs::read_to_string(&path) {
        Ok(contents) => contents,
        Err(e) => {
            eprintln!("wordcount: {path}: {e}");
            std::process::exit(1);
        }
    };

    let lines = text.lines().count();
    let words = text.split_whitespace().count();
    let bytes = text.len();

    println!("{lines:>4} {words:>4} {bytes:>4} {path}");
}
```
<!-- .element: data-id="src" -->

<div class="success">
Auto-Animate keeps the shared <code>data-id="src"</code> block in place and morphs it — the audience sees exactly which lines changed.
</div>

Note:
This is the one auto-animated beat in the deck. Both code blocks share
`data-id="src"`, so reveal.js morphs pass 1 into pass 2 instead of cutting.
The `[…]` after the fence steps through line highlights — press SPACE to advance
them while you narrate each region.
