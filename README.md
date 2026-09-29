# Leave the Lamp Alone — The Electrician's Fix 💡🔧⚡

> An atmospheric, physics-driven interactive canvas story & simulation. A man steps out of his house onto a dark porch, tries the light switch to no avail, and calls his neighbor—Bob the electrician. With a swift throw of his heavy wrench across the yard—**CLANG!**—percussive maintenance strikes and the porch blazes to life!

[![Live Demo](https://img.shields.io/badge/Live%20Demo-Play%20Online-success?style=for-the-badge&logo=githubpages&logoColor=white)](https://itsmesyaam.github.io/buld-breaking/)

[![HTML5 Canvas](https://img.shields.io/badge/HTML5-Canvas-orange?logo=html5)](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)
[![Web Audio API](https://img.shields.io/badge/Web%20Audio-Procedural%20Synth-blue?logo=webrtc)](https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API)
[![Theme Animation](https://img.shields.io/badge/Theme-Narrative%20Animation-brightgreen)](#)
[![Zero Dependencies](https://img.shields.io/badge/Dependencies-Zero-success)](#)

👉 **Play the Live Demo:** [https://itsmesyaam.github.io/buld-breaking/](https://itsmesyaam.github.io/buld-breaking/)

---

## 🎬 The Story

1. **Act 1: The Dark Porch**: Arthur opens his front door and steps outside into the quiet night. The warm interior light closes behind him, leaving him in darkness.
2. **Act 2: The Realization**: Arthur reaches for the wall switch: *click... click*. Nothing happens. He scratches his head in confusion: *"Huh? The porch light won’t turn on..."*
3. **Act 3: Calling the Electrician**: Cupping his hands, Arthur calls over the fence to his neighbor: *"Hey Bob! Can you help me out? The light’s dead again!"*
4. **Act 4: Bob’s Entrance & Wind-Up**: The neighboring door swings open. Bob the electrician emerges in overalls and red cap, holding his trusty wrench: *"Hold tight neighbor! I got just the right tool for this!"*
5. **Act 5: The Throw & Impact**: Bob winds up his arm and hurls the wrench across the yard! The wrench spins through the air and slams the fixture with a resounding **CLANG** and an explosion of electrical sparks!
6. **Act 6: Let There Be Light!**: The lamp surges and flickers into full illumination, casting warm volumetric light and dancing dust motes across the porch. Arthur cheers with arms raised while Bob flashes a confident thumbs up: *"Works every time! Enjoy the light, neighbor!"*

---

## ✨ Features

- **🎭 Cinematic Narrative Animation**: Fully scripted state-machine animation with character sprites (Arthur & Bob), walking cycles, arm gestures, speech bubble subtitles, and comedic timing.
- **⚡ Physical Percussive Maintenance**: Bob's parabolic wrench throw transfers momentum to the lamp's damped pendulum, sparking real-time collision effects and triggering electrical surges.
- **🎮 Sandbox / Free Play Mode**: Switch to sandbox mode at any time! Choose between throwing **Wrenches 🔧**, **Hammers 🔨**, or **Pebbles 🪨** from the slingshot with real-time trajectory aiming dots.
- **💥 Shatter Mechanics & Self-Repair**: If a tool hits the glass bulb directly, it shatters into dozens of individual glass shards with realistic gravity, floor friction, and rotational bouncing. A new bulb automatically animates back in after 2.5 seconds.
- **🔊 Procedural Synthesized Audio (Web Audio API)**: Zero external audio files! All sounds are generated procedurally on-the-fly:
  - *Door creaks* and *footsteps*
  - *Switch clicks* and *whooshes*
  - *Harmonic metallic clangs* on fixture impact
  - *Electrical crackles & arcing sparks*
  - *Warm 60Hz power hum* & triumphant major-chord fanfare
  - *Glass shattering* and *shard tinks*
- **🏮 Volumetric Lighting & Dust Simulation**:
  - Rotating 2D light cone dynamically anchored to the pendulum angle.
  - Mathematical ray-plane projected floor spotlight.
  - Floating ambient dust particles that illuminate only when drifting through the beam.

---

## 🕹️ Controls

| Control | Input | Action |
| :--- | :--- | :--- |
| **Replay Story** | Click `Replay Story` button | Restarts the narrative cutscene from the beginning. |
| **Mode Switch** | Click `Free Play` / `Play Story` | Toggle between cinematic animation and interactive sandbox mode. |
| **Tool Launcher** | Click & drag slingshot band | Pull back to aim using trajectory dots, then release to fling wrenches, hammers, or pebbles. |
| **Pick Tool** | Click toolbar buttons | Select between `🔧 Wrench`, `🔨 Hammer`, or `🪨 Pebble`. |
| **Swing Shade** | Click & drag lamp shade | Directly grab the hanging shade and give it a wide pendulum swing. |
| **Manual Switch**| Click wall switch or press <kbd>Space</kbd> | Manually toggle the light ON or OFF (or hit the switch with a thrown tool!). |
| **Toggle Sound** | Click `Sound: On/Off` button | Enable or disable synthesized Web Audio effects. |

---

## 🚀 Getting Started

No build tools, Node modules, or package managers are required.

### Run in Browser
Simply open `index.html` in any modern web browser (Chrome, Edge, Safari, Firefox):
```bash
git clone https://github.com/itsmesyaam/buld-breaking.git
cd buld-breaking
start index.html   # On Windows
# or open index.html on macOS / xdg-open index.html on Linux
```

### Run Local Web Server
```bash
# Using Python
python -m http.server 8000

# Using Node.js
npx serve .
```
Visit `http://localhost:8000` in your browser.

---

## 📐 Architecture & Technology

- **Single-File Zero-Dependency**: Entire application packaged within clean, semantic HTML5, CSS3, and modern Vanilla ES6+ JavaScript.
- **Canvas Rendering**: High-DPI (`devicePixelRatio`) double-buffered 2D canvas with sub-pixel anti-aliasing and compositing modes (`lighter` for volumetric beams).
- **Physics Integration**: Euler numerical integration with frame-rate clamping (`dt` capped at 33ms) for consistent motion across 60Hz, 120Hz, and variable refresh rate screens.
- **Audio Synthesizer**: Uses native `AudioContext`, `OscillatorNode`, `BiquadFilterNode`, and `GainNode` with exponential attenuation and parameter range safeguards.

---

## 📄 License

This project is open-source under the [MIT License](LICENSE).
