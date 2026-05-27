<div align="center">
  <img src="assets/logo.svg" alt="OctoBit Studio" width="120" />

  <h1>OctoBit Studio</h1>
  <p>A pixel art editor that actually feels good to use.</p>

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

Most pixel art tools either look intimidating or just feel clunky to use.
OctoBit Studio is my answer to that — a browser-based editor where
the experience comes first. No install. No friction. Just open and draw.

---

## Tools

| | Tool | Shortcut |
|--|------|----------|
| ✏️ | Pencil | `Ctrl+B` |
| 🧽 | Eraser | `Ctrl+E` |
| 🪣 | Bucket Fill | `Ctrl+G` |
| 💧 | Eyedropper | `Ctrl+I` / `Alt` |
| 📏 | Line | `Ctrl+L` |
| ⬜ | Rectangle | `Ctrl+R` |
| ⭕ | Ellipse | `Ctrl+O` |

All tools support adjustable brush size.

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

## Layers

Full layer tree with nested groups, hide/lock, drag & drop reorder,
and thumbnails that auto-crop to the painted area.

## Color

Two picker modes (RGB/HSV square + HSL triangle), primary/secondary
color widget, palette system with harmonies, last 10 used colors.

## Zoom & Navigation

![Zoom demo](assets/zoom.gif)

Wheel zooms toward cursor. `Space + drag` to pan. Pixel grid at ≥ 4×.

---

## Under the hood

Built from scratch — no canvas libraries:

- **DocumentEngine** — layer compositor with Canvas Pool (60 FPS, no GC pressure)
- **Bresenham & Zingl** — pixel-perfect lines and ellipses
- **Command pattern** — undo/redo, 50 steps
- **Snapshot-preview** — live shape preview without flicker

4 themes: **Octoone** (dark), **Kyoonotay**, **Dracula**, **Light**.

---

## What's next

- [ ] Fill mode for shapes
- [ ] Selection tools (rect, lasso, magic wand)
- [ ] `.octo` file format with embedded palettes
- [ ] Animation timeline + onion skinning
- [ ] Desktop app (Tauri)

---

<div align="center">
  <sub>Source code: private &nbsp;·&nbsp; <a href="https://octobit.studio">octobit.studio</a></sub>
</div>
