# Liquid Chrome

An interactive full-screen fluid metal playground built with a single HTML canvas — no dependencies, no build step.

**[Live demo →](https://jameswaite-code.github.io/liquid-chrome/)**

## Controls

- **Move the mouse** to disturb the metal — it flows away from the cursor.
- **Hold click** to pull the metal in, release to push it away.
- **Arrow keys / WASD** steer the glowing red core through the surface.
- **Space** triggers a shockwave burst from the core.
- Works with touch on mobile.

## How it works

A goo/metaball technique: soft radial-gradient "blobs" are drawn to an offscreen canvas, then composited onto the main canvas through a `blur` + `contrast` filter so overlapping shapes fuse into one continuous fluid surface. Each blob is shaded like a polished sphere (bright specular hotspot, dark gunmetal body) with some carrying an extra red accent glow to read as reflected light within the metal, rather than solid colored shapes.

## Run locally

Any static file server works, e.g.:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000`.
