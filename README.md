<div align="center">
  <img src="assets/logo.svg" alt="OctoBit Studio" width="120" />

  <h1>OctoBit Studio</h1>
  <p><strong>A professional pixel art editor — built from scratch, runs in the browser.</strong></p>

  <a href="https://octobit.studio">
    <img src="https://img.shields.io/badge/▶%20Open%20App-octobit.studio-AE86EB?style=for-the-badge&labelColor=22223B" alt="Open App" />
  </a>

  <br/><br/>

  <img src="https://img.shields.io/badge/version-1.4.α-AE86EB?style=flat-square&labelColor=22223B" alt="version" />
  <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black&labelColor=22223B" alt="React" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white&labelColor=22223B" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Canvas_2D-API-orange?style=flat-square&labelColor=22223B" alt="Canvas 2D" />
</div>

---

![Drawing demo](assets/drawing.gif)

---

## Features

### Drawing Tools
| Tool | Shortcut | Description |
|------|----------|-------------|
| ✏️ Pencil | `Ctrl+B` | Bresenham, smooth stroke between points |
| 🧽 Eraser | `Ctrl+E` | Pixel-perfect erasing |
| 🪣 Bucket Fill | `Ctrl+G` | Iterative scanline flood fill — no stack overflow |
| 💧 Eyedropper | `Ctrl+I` / `Alt` | Samples from composite of all layers |
| 📏 Line | `Ctrl+L` | Bresenham, live preview while dragging |
| ⬜ Rectangle | `Ctrl+R` | Outline, live preview |
| ⭕ Ellipse | `Ctrl+O` | Zingl midpoint algorithm, live preview |

All tools support adjustable **brush size** — from 1px up to the canvas max dimension.

### Shape Tools in Action

![Shapes demo](assets/shapes.gif)

---

## Screenshots

<table>
  <tr>
    <td align="center">
      <img src="assets/screenshot-overview.png" alt="Full editor" />
      <br/><sub>Full editor</sub>
    </td>
    <td align="center">
      <img src="assets/screenshot-color.png" alt="Color panel" />
      <br/><sub>Color panel</sub>
    </td>
  </tr>
  <tr>
    <td align="center">
      <img src="assets/screenshot-layers.png" alt="Layers panel" />
      <br/><sub>Layers panel</sub>
    </td>
    <td align="center">
      <img src="assets/screenshot-tools.png" alt="Tool palette" />
      <br/><sub>Tool palette</sub>
    </td>
  </tr>
</table>

---

## Layers & Groups

- Full layer tree with **nested groups** (Pass-Through blend mode)
- Hide, lock, reorder — drag & drop (before / inside / after)
- Smart thumbnails cropped to the painted area
- Multi-select: `Ctrl+click`, `Shift+click` range

## Color System

- Two picker modes: **RGB/HSV** square and **HSL Triangle** (hue wheel + SV triangle)
- Primary / secondary color widget with animated highlight
- Palette system: document, system, app — persisted in localStorage
- **Color harmonies**: complementary, analogous, triadic
- Recent color history (last 10 used)

---

## Zoom & Navigation

![Zoom demo](assets/zoom.gif)

Mouse wheel zooms toward the cursor. `Space + drag` to pan. Pixel grid appears at zoom ≥ 4×.

---

## Built From Scratch

No graphics libraries. No canvas frameworks. Every pixel is hand-crafted:

- **DocumentEngine** — layer compositor with Canvas Pool, eliminates GC pressure at 60 FPS
- **Bresenham & Zingl algorithms** — pixel-perfect lines and ellipses
- **Command Pattern undo/redo** — 50 steps, three command types (`LayerPixels`, `LayerStructure`, `LayerRename`)
- **Snapshot-preview** — shape tools clone `ImageData` on every move for flicker-free live preview

---

## Themes

4 built-in themes: **OctoOne** (dark), **Kyoonotay**, **Dracula**, **Light** — pure CSS variables, zero hardcoded colors in component code.

---

## Roadmap

- [ ] Fill variants for Rectangle & Ellipse
- [ ] Rectangular selection, lasso, magic wand
- [ ] Custom `.octo` file format (lossless + embedded palettes)
- [ ] Animation timeline — keyframes, onion skinning
- [ ] Native desktop app (Tauri)
- [ ] Multiplayer collaboration

---

<div align="center">
  <sub>Source code: private &nbsp;·&nbsp; <a href="https://octobit.studio">octobit.studio</a></sub>
</div>
