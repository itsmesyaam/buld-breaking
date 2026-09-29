# Leave the Lamp Alone

> A single-page interactive physics simulation and motion piece. Delivered in one self-contained, dependency-free `index.html` file using Canvas 2D physics and procedural Web Audio synthesis. Responsive across desktop and mobile.

**Live Site**: [https://itsmesyaam.github.io/buld-breaking/](https://itsmesyaam.github.io/buld-breaking/)

---

## Features

- **Hanging Lamp Physics**: Physical pendulum simulation with damped oscillation, dynamic shadow projection, and interactive dragging.
- **Wooden Slingshot**: Draggable trajectory arc, authentic slingshot band tension, and realistic projectile motion with gravity and restitution.
- **Destructible Lightbulb**: Glass bulb shatters into 30+ physical shards upon impact, casting dynamic glints, bounces, and dark room ambience. Automatic replacement after 2.4 seconds.
- **Interactive Wall Switch**: Clickable or targetable wall toggle with glowing indicator in the dark.
- **Volumetric Lighting**: Dual-layer light cone, floor spotlight reflection, and illuminated floating dust motes.
- **Procedural Web Audio**: 100% synthesized sound effects (switch clicks, metallic shade clangs, glass shatter, slingshot twangs, floor thuds, and shard tinks).
- **Mobile Responsive Design**: Dynamic layout scaling for portrait and landscape orientations, viewport safe-area insets, and enlarged touch hitboxes for thumb ergonomics.

---

## Controls

| Action | Desktop (Mouse / Keyboard) | Mobile (Touch) |
| :--- | :--- | :--- |
| **Shoot Slingshot** | Click & drag pebble, release | Touch & drag pebble, release |
| **Flip Wall Switch** | Click switch or press `Spacebar` | Tap the wall switch |
| **Swing Lamp** | Click & drag shade or bulb | Touch & drag shade or bulb |
| **Toggle Sound** | Click `sound: on/off` | Tap `sound: on/off` |

---

## Technical Details

- Single self-contained HTML file (HTML5 + CSS + vanilla JavaScript).
- Zero external dependencies (no image or audio files).
- Canvas 2D with high-DPI scaling (`devicePixelRatio`).
- Web Audio API procedural sound synthesis.
- Touch action handling with `pointer-events`, `setPointerCapture`, and `touch-action: none`.

---

## License

MIT © 2026
