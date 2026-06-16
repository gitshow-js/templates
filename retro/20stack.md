# The Retro Stack

<div class="col">

## Rendering
<span class="tag accent">Canvas 2D</span>
<span class="tag">WebGL</span>
<span class="tag">GLSL shaders</span>

Draw the grid-horizon with a single perspective matrix and a fragment shader for the **neon bloom**.

</div>
<div class="col">

## Sound
<span class="tag accent">Web Audio</span>
<span class="tag amber">chiptune</span>
<span class="tag">tracker mods</span>

Square waves, a noise channel, and an arpeggiator. That's a whole soundtrack.

</div>

<div style="clear: both"></div>

| Layer | Tool of choice | Status |
|---|---|---|
| Geometry | WebGL + custom matrices | <span class="plus">solid</span> |
| Post-FX bloom | GLSL fragment shader | <span class="plus">solid</span> |
| Synth engine | Web Audio API | <span class="amber">tweaking</span> |
| CRT scanlines | CSS overlay (free!) | <span class="plus">solid</span> |

Note:
Don't read the table aloud — let it sit. The CSS-only scanline row always
gets a laugh because this very slide is using it.

=--

# The Sunset, In Code

The whole horizon glow is one gradient and one perspective transform:

```glsl
// fragment shader — synthwave sun with scan-strips
precision highp float;
uniform vec2  uRes;
uniform float uTime;

void main() {
  vec2 uv = gl_FragCoord.xy / uRes;
  float sun = smoothstep(0.34, 0.30, distance(uv, vec2(0.5, 0.62)));
  float strips = step(0.5, fract(uv.y * 40.0 - uTime));  // scan-lines
  vec3 magenta = vec3(1.0, 0.18, 0.59);
  vec3 cyan    = vec3(0.0, 0.94, 1.0);
  vec3 col = mix(cyan, magenta, uv.y) * sun * strips;
  gl_FragColor = vec4(col + col * 0.6, 1.0);   // cheap bloom
}
```

Ship it, tweet the link, watch the GPU fans spin up.
