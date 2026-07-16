# 🌀 Wiggle Rig

A browser-based bullet-time GIF maker for 3D Gaussian Splats. Load a splat, frame your shot, and export a looping wigglegram — all client-side, no install, no server.

**[→ Open the app](https://eyeohdice.github.io/Wigglegram-Rig/)**

![status](https://img.shields.io/badge/stack-three.js%20%2B%20vanilla%20JS-black) ![status](https://img.shields.io/badge/server-none%2C%20100%25%20client--side-ff4419)

![Wiggle Rig demo](assets/demo.gif)

---

## Get a splat first

This tool renders `.ply` 3D Gaussian Splats — it doesn't generate them. If you don't have one yet, make one for free here:

**[ml-sharp 3D Viewer (Hugging Face)](https://huggingface.co/spaces/notaneimu/ml-sharp-3d-viewer)**

Upload a photo, let it process, then download the `.ply` it produces. That's your input file for Wiggle Rig.

> Front view in Wiggle Rig is pre-tuned for these exports specifically — they use OpenCV-style axes (Y-down), and the app corrects for that automatically.

## What it does

1. **Load** your `.ply` — drag and drop, or use the panel.
2. **Frame the shot** — snap to a Quick View (Front/Right/Back/Left/Top/Bottom) on the compass dial, then fine-drag to taste. Scroll to zoom.
3. **Set a rotation center** *(optional)* — click any point on the splat to make it the pivot the camera arcs around, instead of the model's center.
4. **Crop** *(optional)* — turn on Crop, pick a ratio (1:1, 4:5, 9:16, 16:9, or freeform), drag the box.
5. **Shoot** — hit the shutter. It sweeps a small arc around your framing, captures every frame, and encodes a ping-pong bullet-time GIF right in your browser.

## Privacy

- **Everything runs locally** — your splat, your photo, your GIF never leave your machine.

## Stack

Single `index.html`. Three.js (r128, via CDN) for rendering, a hand-rolled anisotropic Gaussian splat shader, and an inlined GIF encoder ([omggif](https://github.com/deanm/omggif)). No build step, no dependencies to install — just open the file or visit the Pages link.

---

Wiggle responsibly.
 ____  _  _  ____     _____  _   _     ____  ____  ___  ____ 
( ___)( \/ )( ___)___(  _  )( )_( )___(  _ \(_  _)/ __)( ___)
 )__)  \  /  )__)(___))(_)(  ) _ ((___))(_) )_)(_( (__  )__) 
(____) (__) (____)   (_____)(_) (_)   (____/(____)\___)(____)

