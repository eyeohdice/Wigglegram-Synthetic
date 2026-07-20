# Synth Wiggle

Turn a single photo into an animated wigglegram. Runs entirely in the browser with no access or storage of your data.

![status](https://img.shields.io/badge/status-active-black) ![license](https://img.shields.io/badge/license-MIT-black)

## What it does

- **Image → depth → parallax.** Upload a photo, get an automatic depth estimate (Depth Anything V2, in-browser), and generate a looping GIF or video with orbit / parallax / warp motion.
- **Splat → 3D orbit.** Upload a `.ply` Gaussian splat instead, and Synth Wiggle drives a real 3D camera sweep around it; sharper, more convincing parallax than a 2D depth map can fake.
- **Click-to-set pivot.** Click anywhere on a loaded splat to re-center the orbit on that point.
- **Unlock rotate.** If needed, Free-drag around a splat to find your framing, then lock it back in for export.
- **Own depth map.** Supply a custom grayscale depth image instead of the automatic estimate.
- **Export GIF or MP4/WebM**, at whatever resolution you want.

## Using it

1. Download and Open `index.html` in a browser.
2. Upload a source image.
3. Either let it auto-estimate depth, upload your own depth map, or upload a `.ply` splat.
4. Tweak motion / depth / splat / output settings on the right.
5. Hit **Generate**, download the result.

## Where to make a splat

Synth Wiggle doesn't generate splats itself — bring your own `.ply`, made with [ml-sharp](https://github.com/apple/ml-sharp) (Apple's single-image → 3D Gaussian splat model). Two easy ways to make one without installing anything:

- **[sharp-onnx-webgpu.vercel.app](https://sharp-onnx-webgpu.vercel.app/)** — runs ml-sharp fully client-side via WebGPU. Upload a photo, download the `.ply`.
- **[huggingface.co/spaces/notaneimu/ml-sharp-3d-viewer](https://huggingface.co/spaces/notaneimu/ml-sharp-3d-viewer)** — hosted Space, same idea, also lets you preview the splat before exporting.


## Stack

Three.js, `@mkkellogg/gaussian-splats-3d`, Tweakpane, `gif.js`, and `@huggingface/transformers` (in-browser depth estimation) — no build step, no backend required.

WIGGLE RESPONSIBLY.
