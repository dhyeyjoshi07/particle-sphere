# Particle Sphere — Hand Controlled

A webcam-driven particle playground built with [Three.js](https://threejs.org/) and [MediaPipe Hands](https://google.github.io/mediapipe/solutions/hands.html). A glowing sphere made of 3,000 particles responds to your hand in real time — move it, resize it, recolor it, and charge it up until it explodes.

A small vibe-coded side project, built for fun in spare time. No build step, no dependencies to install — just open it in a browser.

## ✨ Features

- **One hand** — move and rotate the sphere by moving your palm
- **Pinch & hold** — charge up the sphere (with a radial progress ring at your fingertips), then release to trigger an explosion
- **Two hands** — spread or bring your palms together to resize the sphere
- **Finger count** — hold up different numbers of fingers to shift the particle color palette
- Physically-inspired explode/reform animation with staggered timing, damping, and a subtle "breathing" idle state
- Optional live webcam background overlay
- Custom GLSL shader for particle glow, size pulsing while charging, and additive blending

## 🛠 Tech Stack

- **[Three.js r128](https://threejs.org/)** — WebGL rendering of the particle system (custom vertex/fragment shaders)
- **[MediaPipe Hands](https://google.github.io/mediapipe/solutions/hands.html)** — real-time hand landmark tracking from the webcam feed
- Vanilla HTML/CSS/JS — no frameworks, no build tools

All dependencies are loaded via CDN (`cdnjs.cloudflare.com` and `cdn.jsdelivr.net`), so there's nothing to `npm install`.

## 🚀 Getting Started

1. Download `index.html`.
2. Open it in a modern desktop browser (Chrome or Edge recommended for best MediaPipe/WebGL support).
3. Click **Start Camera** and allow webcam access when prompted.
4. Hold your hand up in frame and start playing with the sphere.

> **Note:** Because it requests camera access, some browsers may block it when opened directly from the filesystem (`file://`). If that happens, serve it locally instead, e.g.:
> ```bash
> python3 -m http.server 8000
> ```
> then open `http://localhost:8000` in your browser.

## 🎮 Controls

| Gesture | Effect |
|---|---|
| Move one hand | Moves and rotates the sphere |
| Pinch (thumb + index) and hold | Charges the sphere — release once fully charged to explode it |
| Two hands, move apart / together | Resizes the sphere |
| Hold up N fingers (0–10, either or both hands) | Changes the particle color palette |

There's also a **Show Webcam BG** button to toggle a faint live webcam feed behind the particles.

## ⚠️ Requirements

- A webcam
- A browser with WebGL and `getUserMedia` support
- Reasonable lighting for hand tracking to work well

## 📄 License

Released under the [MIT License](LICENSE) — do whatever you'd like with it.
