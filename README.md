# The Smash & Save

> A fast-paced interactive branded mini-game (60–90s) built for the home-repair brand **FIXnGO**. Delivered in a single self-contained `index.html` file with HTML5 Canvas 2D physics, procedural Web Audio synthesis, and dynamic responsive layout for mobile and desktop.

**Live Site**: [https://itsmesyaam.github.io/buld-breaking/](https://itsmesyaam.github.io/buld-breaking/)

---

## The Concept

The game revolves around two contrasting visual worlds that communicate the core brand message:
- **World A ("Mischief")**: Grungy, dim, noisy, and rebellious. The player aims a slingshot at a solitary glowing desk lamp in a quiet bedroom and shatters the bulb in slow-motion.
- **World B ("FIXnGO")**: Clean, bright, high-tech, and reassuring. Mom's footsteps approach down the hallway, prompting an emergency call to FIXnGO. A technician somersaults through the window, tosses the Fix-Blaster, and the player rewinds the glass shards back into place before the door opens!

---

## 13-State Finite State Machine (FSM)

```
[INTRO] ──► [AIM] ──► [SMASH_SLOWMO] ──► [BLACKOUT] ──► [MOM_ALERT] ──► [PHONE_CALL]
                                                                               │
[CLIMAX] ◄── [MAGIC_REWIND] ◄── [FIX_MODE] ◄── [TECH_ENTRY] ◄── [VAN_ARRIVAL] ◄┘
   │
   ├──► [BRAND_REVEAL] (Success)
   └──► [FAIL] (Timeout)
```

1. **INTRO**: Grungy stencil title card with start button.
2. **AIM**: Slingshot physics with parabolic trajectory guide and unlimited tries.
3. **SMASH_SLOWMO**: Time dilates to 0.2x. Glass shatters into 60 polygon shards with floor/desk bounce physics and glints.
4. **BLACKOUT**: Lamp turns off. Moonlight faintly illuminates the scattered shards.
5. **MOM_ALERT**: Footsteps echo, light strip shines under door, 10s digital countdown begins with red vignette pulse and heartbeat SFX.
6. **PHONE_CALL**: Game pauses. Glowing neon smartphone slides up with massive pulsing "Call FIXnGO!" button.
7. **VAN_ARRIVAL**: Futuristic FIXnGO van with cyan neon strips screeches to a halt outside the window.
8. **TECH_ENTRY**: Technician bursts through the window with a somersault and tosses the spinning "Fix-Blaster".
9. **FIX_MODE**: UI morphs into clean white/cyan FIXnGO branding. Dragging the blaster charges shards with laser arcs and builds combo chains.
10. **MAGIC_REWIND**: Charged shards defy gravity and fly back along eased curved paths with golden sparks.
11. **CLIMAX**: Filament reconnects with an animated electrical arc, lamp bursts on brighter than ever, technician salutes and vanishes out the window, and Mom enters: *"Wow, this room looks great!"*
12. **BRAND_REVEAL**: FIXnGO logo drops down with light sweep, headline *"We fix your 'Oops' before anyone even notices"*, stats card (time taken, best combo, time to spare), and dual CTAs.
13. **FAIL**: If the countdown hits 0, Mom gasps: *"WHAT happened in here?!"* with retry and booking options.

---

## Controls

| Action | Mouse / Trackpad | Touchscreen | Keyboard |
| :--- | :--- | :--- | :--- |
| **Aim & Shoot Slingshot** | Click & drag pebble, release | Touch & drag pebble, release | Hold `Spacebar` to auto-fire |
| **Call FIXnGO** | Click "Call FIXnGO!" | Tap "Call FIXnGO!" | Press `Spacebar` or `Enter` |
| **Repair Shards** | Drag Fix-Blaster reticle over shards | Drag finger over shards | `Spacebar` to auto-target nearest shard |
| **Toggle Audio** | Click speaker icon in header | Tap speaker icon | Press `M` key |
| **Toggle Fullscreen** | Click fullscreen icon in header | Tap fullscreen icon | Press `F` key |

---

## Tech Stack & Architecture

- **Single File**: Self-contained HTML + CSS + vanilla JS with zero external dependencies (no image or audio files; Google Fonts allowed).
- **Canvas 2D Physics Engine**: Custom gravity, angular velocity, polygon rendering, and collision detection with restitution.
- **Web Audio API**: 14 distinct procedurally synthesized sound effects (rubber stretch, twang, glass shatter, heartbeat, footsteps, phone ring, tire screech, window burst, crystal pings, magical rewind, and bell chime).
- **Responsive Design**: Fixed 16:9 landscape aspect ratio on desktop and 9:16 portrait on mobile with dynamic touch targets and safe area insets.
- **Accessibility**: Screen reader live announcements (`aria-live="polite"`), full keyboard navigation, and `prefers-reduced-motion` compliance.

---

## License

MIT © 2026 FIXnGO Technologies Inc.
