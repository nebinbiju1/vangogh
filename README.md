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

## Try it online

👉 **[nebinbiju1.github.io/vangogh](https://nebinbiju1.github.io/vangogh/)**

No install needed — just open the link in Chrome or Edge, allow camera access, and start painting.

## Run locally

1. Clone the repo
   ```bash
   git clone https://github.com/nebinbiju1/vangogh.git
   cd vangogh
   ```

2. Start a local server
   ```bash
   python3 -m http.server 8080
   ```

3. Open [http://localhost:8080](http://localhost:8080) in Chrome or Edge

4. Allow camera access when prompted — that's it, you're ready to paint

> **Note:** The app must be served over HTTP (not opened as a file) because the browser requires a server context to access the webcam.

## Tech

- [MediaPipe Hands](https://google.github.io/mediapipe/solutions/hands) — real-time hand landmark detection
- HTML5 Canvas — painting surface
- No frameworks, no build step — single `index.html` file
