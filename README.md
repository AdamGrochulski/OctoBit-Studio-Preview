<div align="center">
  <img src="assets/logo.svg" alt="OctoBit Studio" width="120" />
  <h1>OctoBit Studio</h1>
  <p><strong>A professional pixel art editor — built from scratch, runs in the browser.</strong></p>

  <a href="https://octobit.studio">
    <img src="https://img.shields.io/badge/▶%20Open%20App-octobit.studio-4285F4?style=for-the-badge" alt="Open App" />
  </a>

  <br/><br/>

  ![Version](https://img.shields.io/badge/version-1.4.α-blue?style=flat-square)
  ![React](https://img.shields.io/badge/React-19-61DAFB?style=flat-square&logo=react&logoColor=black)
  ![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?style=flat-square&logo=typescript&logoColor=white)
  ![Canvas 2D](https://img.shields.io/badge/Canvas_2D-API-orange?style=flat-square)
  ![Source](https://img.shields.io/badge/source-private-lightgrey?style=flat-square)
</div>

---

![Drawing demo](assets/gif-drawing.gif)

---

## Features

### Drawing Tools
| Tool | Shortcut | Description |
|------|----------|-------------|
| ✏️ Pencil | `Ctrl+B` | Bresenham line algorithm, smooth stroke |
| 🧽 Eraser | `Ctrl+E` | Pixel-perfect erasing |
| 🪣 Bucket Fill | `Ctrl+G` | Iterative scanline flood fill — no stack overflow |
| 💧 Eyedropper | `Ctrl+I` / `Alt` | Samples from composite of all layers |
| 📏 Line | `Ctrl+L` | Bresenham, live preview while dragging |
| ⬜ Rectangle | `Ctrl+R` | Outline, live preview |
| ⭕ Ellipse | `Ctrl+O` | Zingl midpoint algorithm, live preview |

All drawing tools support adjustable **brush size** (1 to max canvas dimension).

### Shape Tools in Action

![Shapes demo](assets/gif-shapes.gif)

### Layers & Groups
- Full layer tree with **nested groups** (Pass-Through blend mode)
- Hide, lock, reorder — drag & drop with precision (before / inside / after)
- Smart thumbnails cropped to the painted area
- Multi-select: `Ctrl+click`, `Shift+click` range

### Color System
- Two picker modes: **RGB/HSV** square and **HSL Triangle** (hue wheel + SV triangle)
- Primary / secondary color widget with animated highlight
- Palette system: document (DOC), system (SYS), app (APP) — persisted in localStorage
- **Color harmonies**: complementary, analogous, triadic
- Recent color history (last 10 used)

---

## Screenshots

<table>
  <tr>
    <td align="center"><img src="assets/screenshot-overview.png" alt="Overview" /><br/><sub>Full editor</sub></td>
    <td align="center"><img src="assets/screenshot-color.png" alt="Color panel" /><br/><sub>Color panel</sub></td>
  </tr>
  <tr>
    <td align="center"><img src="assets/screenshot-layers.png" alt="Layers" /><br/><sub>Layers panel</sub></td>
    <td align="center"><img src="assets/screenshot-tools.png" alt="Toolbar" /><br/><sub>Tool palette</sub></td>
  </tr>
</table>

---

## Zoom & Navigation

![Zoom demo](assets/gif-zoom.gif)

Mouse wheel zooms toward the cursor. `Space + drag` to pan. Grid appears at zoom ≥ 4×.

---

## Built From Scratch

No graphics libraries. No canvas frameworks. Everything is custom:

- **DocumentEngine** — layer compositor with Canvas Pool, eliminates GC pressure at 60 FPS
- **Bresenham & Zingl algorithms** — pixel-perfect line and ellipse rendering
- **Command Pattern undo/redo** — up to 50 steps, three command types
- **Snapshot-preview** — shape tools clone ImageData on each move for flicker-free live preview

---

## Themes

4 built-in themes switchable from the menu bar: **OctoOne** (dark), **Kyoonotay**, **Dracula**, **Light** — all via CSS variables, zero hardcoded colors.

---

## Roadmap

- [ ] Rectangle & Ellipse fill variants
- [ ] Rectangular selection, lasso, magic wand
- [ ] Custom `.octo` file format (lossless, includes palettes)
- [ ] Animation timeline — keyframes, onion skinning
- [ ] Native desktop app (Tauri)
- [ ] Multiplayer collaboration

---

<div align="center">
  <sub>Source code: private &nbsp;·&nbsp; <a href="https://octobit.studio">octobit.studio</a></sub>
</div>
