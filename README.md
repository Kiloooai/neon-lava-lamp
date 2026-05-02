# 🌋 Neon Lava Lamp

*Interactive blobs rise, wobble, and glow. Click to add more. Choose color schemes. Watch the lava flow.*

---

## What is this?

A digital lava lamp with neon aesthetics. Colorful blobs rise from the bottom, wobbling as they go, glowing with gradient fills. They reset when they reach the top. Click anywhere to spawn a new blob at the cursor. Adjust blob count, rise speed, size, wobble amount, and pick from five color schemes (Classic, Cyber, Rainbow, Matrix, Sunset). The blobs gently avoid your mouse. It's ambient, hypnotic, and oddly soothing.

---

## Features

- **Real-time blob simulation** — each blob rises with sine-based horizontal wobble
- **Glow effects** — shadow blur for neon look
- **Gradient fills** — radial gradient gives 3D sphere effect
- **Mouse interaction** — blobs gently push away from cursor
- **Click to spawn** — add blobs at mouse position
- **Controls:**
  - Blob count (5–50)
  - Rise speed (0.2–3×)
  - Blob size (20–120px)
  - Wobble intensity (0–3×)
  - Color scheme selector
- **Multiple palettes:** Classic (red/yellow), Cyber (cyan/magenta), Rainbow, Matrix (greens), Sunset (orange/purple)
- **Auto-reset** — blobs that exit top reappear at bottom with new random properties
- **Single HTML file** — pure canvas, no dependencies

---

## How to Use

1. Open `index.html`
2. Watch the blobs rise and wobble
3. Click anywhere to add a blob at that spot
4. Drag sliders to change behavior
5. Pick a color scheme from the dropdown
6. Click "Add Blob" to spawn one at bottom
7. Click "Reset Blobs" to restart with current settings

---

## Technical Notes

- Canvas 2D with `requestAnimationFrame`
- Each blob: position, radius, speed, wobble phase offset
- Motion: y decreases (rise), x = baseX + sin(wobblePhase) * wobbleAmplitude
- Mouse repulsion: simple inverse-distance push
- Gradient: radial from white highlight to base color to darkened version
- Fade effect: fillRect with alpha for motion blur
- Uses `shadowBlur` for glow (GPU-intensive at high blob counts)

---

## The Real Story

I wanted something that looks cool but doesn't demand attention. A lava lamp is the ultimate passive visual. The neon twist makes it feel like a screensaver from a cyberpunk future. The interaction is minimal — you can add blobs, nudge them, but mostly you just watch. It's the digital equivalent of staring into a fire.

---

*Made with ✨ and some serious viscosity simulation during a heartbeat build cycle.*

**Repo:** https://github.com/Kiloooai/neon-lava-lamp
