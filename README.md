# Leave the Lamp Alone

> A minimalist, atmospheric physics simulation and interactive sound toy built in a single self-contained HTML file.

**Live Demo**: [https://itsmesyaam.github.io/buld-breaking/](https://itsmesyaam.github.io/buld-breaking/)

---

## Overview

A warm vintage porch lamp hangs in the quiet dark. A wall switch rests nearby, and a wooden slingshot sits on the floor with a supply of smooth pebbles. Everything responds in real time with canvas rendering and procedural Web Audio synthesis.

### Features

- **Interactive Hanging Lamp**: Grab and swing the lampshade with realistic pendulum physics and rotational inertia.
- **Glass Bulb Destruction & Repair**: Strike the bulb with pebbles to trigger dynamic fracture physics with glass shards scattering across the floor. Broken bulbs automatically screw back in and flicker to life.
- **Slingshot Physics**: Drag backwards on the rubber band to load and aim with real-time parabolic trajectory guides.
- **Wall Switch**: Click or shoot pebbles directly at the wall switch to toggle the light on and off.
- **Atmospheric Lighting**: Procedural radial illumination, dust motes floating through the beam, ground reflections, and warm room glow.
- **Pure Procedural Audio**: Synthesized with the Web Audio API — metallic clangs, glass fractures, switch clicks, elastic twangs, and floor thuds with zero external asset dependencies.
- **Mobile Responsive Design**:
  - Full touch support with safe-area insets (`env(safe-area-inset-*)`).
  - Dynamic viewport handling (`100dvh`) preventing browser toolbar clipping.
  - Generous touch hit targets calibrated for touchscreen finger precision.
  - Responsive layout geometry for portrait phones, landscape tablets, and high-DPI desktop screens.
  - Zero pinch/scroll conflicts (`touch-action: none`, `overscroll-behavior: none`).

---

## Controls

| Device | Action | Interaction |
| :--- | :--- | :--- |
| **Mouse / Touch** | **Aim & Shoot** | Drag backwards on the slingshot pebble and release |
| **Mouse / Touch** | **Swing Lamp** | Drag the lamp shade or bulb directly |
| **Mouse / Touch** | **Wall Switch** | Click/tap the switch or hit it with a pebble |
| **Keyboard** | **Toggle Light** | Press `Spacebar` |
| **Audio** | **Sound Toggle** | Click/tap the `sound: on/off` pill in the top-right |

---

## Tech Stack

- **HTML5 & CSS3**: Pure modern CSS with CSS variables, fluid clamps, and safe-area adaptation.
- **Canvas 2D API**: Smooth 60 FPS procedural rendering with composite blend modes.
- **Web Audio API**: Real-time noise generators, oscillators, and envelope shaping.
- **Zero Dependencies**: Self-contained single file with no build steps, bundlers, or external images/audio files.

---

## License

MIT
