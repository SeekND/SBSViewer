# SBS 3D Viewer

**A dead-simple web viewer for 3D images — works on XREAL glasses and without glasses.**

🌐 **Live:** [https://seeknd.github.io/SBSViewer/](https://seeknd.github.io/SBSViewer/)

---

## What it does

### SBS Image Mode
Load an existing side-by-side 3D image (from Owl3D, 3D cameras, etc.):
- **XREAL Glasses** — One tap fullscreen. Image fills the 3840×1080 display correctly. No zooming, no fiddling.
- **Wiggle 3D** — Alternates left/right to create depth perception (no glasses needed).
- **Anaglyph** — Red/cyan mode for classic 3D glasses.
- **Cross-eye** — Free-viewing for stereo pair fusing.

### Regular Photo Mode
Load any normal photo — AI estimates depth and converts it to 3D:
- **Parallax** — Move your mouse to look around the scene (like a 3D window).
- **Wiggle / Anaglyph** — Same glasses-free modes as SBS.
- **XREAL Glasses** — Generates an SBS pair from the depth map for fullscreen viewing.

## AI Depth Model

The "Regular Photo" mode uses **Depth Anything V2 Small** (~100MB) running directly in the browser via [transformers.js](https://github.com/huggingface/transformers.js). The model downloads from HuggingFace CDN on first use and is cached in the browser — subsequent uses load instantly. Nothing is stored on GitHub.


## Technical notes

- Single HTML file, zero dependencies, zero build step
- All processing happens client-side (images never leave your device)
- Works offline once the AI model is cached
- Depth estimation takes 2–5s on PC, 5–15s on phone
- SBS generation uses pixel-shifting with disocclusion hole filling
- Anaglyph uses optimized luminance-based red/cyan separation
