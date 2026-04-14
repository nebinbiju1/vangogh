# VanGogh

A browser-based finger painting app that uses your webcam to track hand movements in real time.

## How it works

Each fingertip acts as a brush with its own color. Raise or lower fingers to pick which brushes paint.

| Finger | Color |
|--------|-------|
| Thumb  | Red   |
| Index  | Orange |
| Middle | Green |
| Ring   | Blue  |
| Pinky  | Purple |

**Wave with all 5 fingers open** to erase the canvas. The canvas stays blank for 5 seconds before you can paint again.

## Run locally

```bash
cd vangogh
python3 -m http.server 8080
```

Then open [http://localhost:8080](http://localhost:8080) in Chrome or Edge and allow camera access.

## Tech

- [MediaPipe Hands](https://google.github.io/mediapipe/solutions/hands) — real-time hand landmark detection
- HTML5 Canvas — painting surface
- No frameworks, no build step — single `index.html` file
