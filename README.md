# Portfolio

My personal portfolio: **[kartikkrishnan05.github.io](https://kartikkrishnan05.github.io/)**

The site is a 3D room you look around in. Scroll or use the arrow keys to turn toward a wall — about, projects, robotics, and contact. With the camera on, the view also follows your head: a small face-detection model ([face-api.js](https://github.com/justadudewhohacks/face-api.js), tiny face detector) runs entirely in the browser and shifts the perspective as you move, so the room feels like a window. Nothing from the camera leaves your device.

## Tech

React · TypeScript · Vite · CSS 3D transforms · face-api.js · GitHub Actions + GitHub Pages

## Run locally

```bash
npm install
npm run dev
```

Pushing to `main` builds the site and deploys it to GitHub Pages (`.github/workflows/deploy.yml`).

## Structure

| File | Purpose |
| --- | --- |
| `src/App.tsx` | Navigation between walls (scroll wheel, arrow keys) and camera toggle |
| `src/Box3D.tsx` | The 3D room and the content on each wall |
| `src/useHeadTracker.ts` | Webcam head tracking with face-api.js |
| `public/weights/` | Face-detector model weights |
