# SBS 3D Viewer

**A dead-simple web viewer for side-by-side 3D images — works on XREAL glasses and without glasses.**


🌐 **Live:** [https://seeknd.github.io/SBSViewer](https://seeknd.github.io/SBSViewer)

---

## What it does

- **XREAL / AR Glasses mode** — One tap fullscreen SBS. Image fills the entire 3840×1080 display correctly. No zooming, no fiddling.
- **Wiggle 3D** — Rapidly alternates left/right eye views to create depth perception on any screen (no glasses needed).
- **Anaglyph** — Red/cyan 3D for classic 3D glasses.
- **Cross-eye** — Free-viewing mode for those who can cross their eyes to fuse stereo pairs.

## How to use

### On XREAL glasses

1. Open the page
2. Plug in XREAL glasses via USB-C
3. Put glasses in SBS mode (long-press brightness+ ~3 sec until chime)
4. Load your SBS image
5. Tap **"View on XREAL Glasses"** → fullscreen fills the display
6. Tap to exit

### On any screen (no glasses)

1. Open the page in any browser
2. Load your SBS image
3. Choose **Wiggle 3D** or **Anaglyph**
4. Adjust speed with the slider (wiggle mode)


## Technical notes

- Single HTML file, zero dependencies, zero build step
- All processing happens client-side (images never leave your device)
- Works offline once loaded
- Anaglyph uses optimized luminance-based red/cyan separation
- Wiggle speed is adjustable (50ms–500ms interval)

---
