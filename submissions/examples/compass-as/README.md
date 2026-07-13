# Compass

### What does this do?

It shows a brass compass. The needle hunts back and forth as it settles on north, the case tilts gently as if held in a hand, and hovering or focusing the compass sends the needle spinning as though a magnet passed by. Under reduced motion the needle rests.

### How is it used?

```html
<div class="comp" tabindex="0">
  <span class="ticks"></span>
  <span class="mark mn">N</span>
  <div class="needle">
    <span class="pointn"></span>
  </div>
</div>
```

The whole tick ring is one element: a `repeating-conic-gradient` cuts a mark every 15 degrees and a radial `mask-image` punches out the middle so only the outer band survives. The cardinal letters use `rotate(var(--ma)) translateY(-88px) rotate(calc(var(--ma) * -1))`: the first rotation aims each letter around the dial, the translate pushes it to the rim, and the counter rotation cancels the spin so the text still reads upright. The needle is two `border` triangles sharing a pivot at the pin.

### Why is it useful?

Navigation, travel, and exploration themes use a compass. This builds one with pure CSS gradients and animation, no images and no JavaScript, with a reduced motion fallback.
