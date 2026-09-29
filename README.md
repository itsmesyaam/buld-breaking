# Leave the Lamp Alone 💡🪨

> A minimalist, physics-driven interactive canvas simulation where you can flip the switch, swing the pendant lamp, or launch pebbles with a slingshot to shatter the bulb.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-Play%20Online-success?style=for-the-badge&logo=githubpages&logoColor=white)](https://itsmesyaam.github.io/buld-breaking/)

[![HTML5 Canvas](https://img.shields.io/badge/HTML5-Canvas-orange?logo=html5)](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)
[![Web Audio API](https://img.shields.io/badge/Web%20Audio-Synthesizer-blue?logo=webrtc)](https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API)
[![Vanilla JS](https://img.shields.io/badge/JavaScript-ES6+-yellow?logo=javascript)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Zero Dependencies](https://img.shields.io/badge/Dependencies-Zero-brightgreen)](#)

👉 **Experience It Live on GitHub Pages:**  
### **[https://itsmesyaam.github.io/buld-breaking/](https://itsmesyaam.github.io/buld-breaking/)**

---

## 🎮 Overview

**"Leave the Lamp Alone"** is a single-file, zero-dependency browser experience created with vanilla HTML5 Canvas and the Web Audio API. 

In a dark, atmospheric room hangs a single pendant lamp cast over a wooden floor. On the wall sits a tactile toggle switch, and on the ground rests a classic wooden slingshot. You can respect the lamp's peaceful glow—or grab a pebble, pull back the slingshot band, and let it fly.

---

## ✨ Features

- **🎯 Slingshot Ballistics & Trajectory Preview**: Pull back the elastic band and see real-time trajectory dots calculated with simulated gravity and initial velocity.
- **🏮 Damped Physical Pendulum**: The lamp swings according to damped pendulum physics ($I \cdot \ddot{\theta} + c\dot{\theta} + g\sin\theta = 0$). Grab and swing the shade directly with your mouse/touch, or transfer momentum by pelting it with pebbles.
- **💥 Destructible Bulb & Shard Particle System**: Direct hits shatter the bulb into dozens of glass shards that scatter, bounce off the floor with realistic friction, and spin. If lit, breaking the bulb triggers a realistic pop flash.
- **🔄 Auto-Replacing Bulb**: After being broken, a replacement bulb animates back into place, screwing in and flickering back to life.
- **🔦 Volumetric Lighting & Dust Motes**:
  - Dynamic 2D light cone that rotates and projects based on the lamp's tilt angle.
  - Floor spotlight projected using ray-plane intersection mathematics.
  - Floating ambient dust particles that illuminate only when passing through the light beam.
  - Warm room ambient occlusion and wall switch glowing indicator in the dark.
- **🔊 100% Procedurally Synthesized Audio**: No external audio files or sound assets required! Uses the browser's native Web Audio API to synthesize:
  - *Click*: Mechanical switch toggle.
  - *Clang*: Resonant metallic reverberation when hitting the shade.
  - *Shatter*: Multi-oscillator glass pop and high-frequency breakage.
  - *Twang*: Elastic band slingshot release.
  - *Thud*: Pebbles landing on the wooden floor.
  - *Tink*: Delicate glass shards settling on the ground.
- **📱 Fully Responsive & Touch-Ready**: Automatically scales for mobile and desktop screens with pointer capture for smooth dragging.

---

## 🕹️ Controls

| Action | Input | Description |
| :--- | :--- | :--- |
| **Shoot Pebble** | `Click/Touch & Drag` the slingshot | Pull back against the sling to aim. Release to shoot towards the bulb, shade, or switch. |
| **Swing Shade** | `Click/Touch & Drag` the lampshade | Manually grab the pendant shade and drag it to create a wide pendulum swing. |
| **Flip Switch** | `Click` switch / Press <kbd>Space</kbd> | Toggle the light on or off. You can also toggle the switch by hitting it with a pebble from across the room! |
| **Sound Toggle** | `Click` the button in top-right | Mute or unmute the synthesized sound effects. |

---

## 🚀 Getting Started

No build tools, bundlers, or package managers are required.

### Option 1: Open Directly in Browser
Simply clone or download the repository, then double-click `index.html` to open it in your browser of choice (Chrome, Edge, Firefox, Safari):
```bash
git clone https://github.com/itsmesyaam/buld-breaking.git
cd buld-breaking
start index.html   # On Windows
# or open index.html on macOS / xdg-open index.html on Linux
```

### Option 2: Run a Local Static Server
If preferred, you can serve it via Python or Node:

**Using Python:**
```bash
python -m http.server 8000
```
Then visit [http://localhost:8000](http://localhost:8000).

**Using Node.js:**
```bash
npx serve .
```

---

## 📂 Project Structure

```text
buld-breaking/
├── .github/
│   └── workflows/
│       └── deploy.yml   # GitHub Pages automated deployment
├── index.html           # Complete application (Canvas + Simulation + Synthesizer + Styles)
├── README.md            # Documentation and guide
└── .gitignore
```

---

## 🔬 Technical Architecture

1. **Rendering**: Double-buffered HTML5 Canvas 2D Context scaled to device pixel ratio (`devicePixelRatio`) for sharp rendering on retina displays.
2. **Physics Loop**: Fixed time-step integration (`dt` capped at 33ms) for consistent motion independent of display refresh rates (60Hz, 120Hz, 144Hz+).
3. **Sound Synthesizer**: Uses `AudioContext`, custom `OscillatorNode` waveforms, and generated noise buffers passed through `BiquadFilterNode` filters with exponential gain envelopes.
4. **Collision Detection**: Ray and point-in-polygon bounding checks transformed between canvas world space and the lamp's local rotating reference frame.

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
