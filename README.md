# Hand Ninja — Webcam Fruit Slicing Game with Real-Time Hand Tracking

**Hand Ninja** is a browser-based, Fruit-Ninja-style slicing game controlled entirely by your **index fingers** — no mouse, no keyboard, no controller. It runs your webcam through [Google MediaPipe](https://developers.google.com/mediapipe)'s `HandLandmarker` model to track your hands in real time and turns your fingertips into blades.

*Courtesy of [QubitsORG](#).* (my tech organisation)

Built as a **single self-contained `index.html` file** — no build step, no dependencies to install, no backend. Open it and play.

**[https://handninja.netlify.app/ ](#)** 

---

## ✋ How to Play

1. Allow camera access when prompted.
2. Press **Start**.
3. Swipe your **index finger** through falling fruit to slice it.
4. Avoid the **💣 bombs**.
5. Grab **🍌 special bananas** for power-ups, and rack up **combos** for bonus score.

Works with **both hands** at once — two blades, double the chaos.

---

## 🎮 Features

- **Real-time hand tracking** via MediaPipe `HandLandmarker` (runs entirely client-side, no server, no data leaves your browser)
- **Physics-based fruit** — realistic arcs, gravity, spin, and a subtle "alive" pulse/wobble on every fruit
- **Satisfying slice mechanics** — fruit splits into two independently-tumbling halves along your exact swipe angle, with a burst of dissolving binary digits (`0`/`1`) along the cut seam
- **Special power-up bananas**:
  - 🍌 **Frenzy** — a swarm of extra fruit, with bomb risk sharply reduced
  - 🍌 **Freeze** — fruit slows to a crawl while your swipe speed stays full-speed, making chains trivially easy
  - 🍌 **Double Score** — every slice bonus is doubled for a few seconds
- **Golden multi-hit fruit** — takes 3 hits to fully slice, each hit scores on its own
- **Combo scoring** — chain slices within a short window for escalating bonus points
- **Procedural sound effects** — synthesized live with the Web Audio API (no audio files, no music, just crisp slice/bomb SFX)
- **Techy blade trail** — layered glow + sharp core + digital tick marks, with an impact "slash flash" on every successful cut
- **Start / Pause support** — camera stays live while paused, so it's easy to hand off to someone else to try
- **Zero install** — one HTML file, works on any static host

---

## 🛠️ Tech Stack

| Layer | Tech |
|---|---|
| Hand tracking | [MediaPipe Tasks Vision](https://developers.google.com/mediapipe/solutions/vision/hand_landmarker) (`HandLandmarker`, loaded from CDN) |
| Rendering | HTML5 Canvas 2D |
| Camera | `navigator.mediaDevices.getUserMedia` |
| Audio | Web Audio API (procedural, no assets) |
| Everything else | Vanilla JavaScript — no frameworks, no build tools |

---


---

## 📁 Project Structure

```
.
└── index.html   ← everything: markup, styles, and game logic in one file
```

---

## 🙌 Credits

Built by [**QubitsORG**](#).

https://qubitsorg.netlify.app/ 

Hand tracking powered by [Google MediaPipe](https://developers.google.com/mediapipe).

---

## 📜 License

do whatever you want with it, just don't blame us if you slice a bomb.

---

### Keywords
hand tracking game, webcam game, gesture control game, MediaPipe hand landmarker, fruit ninja clone, browser game no install, JavaScript hand gesture recognition, computer vision game, HTML5 canvas game, real-time hand detection, AI webcam game, slice fruit with hands, gesture-based gameplay, index finger tracking game
