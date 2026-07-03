<div align="center">
  <img src="assets/logo.svg" alt="OctoBit Studio" width="120" />

  <h1>OctoBit Studio</h1>
  <p>A pixel art editor that actually feels good to use.</p>

  <a href="https://octobit.studio">
    <img src="https://img.shields.io/badge/▶%20Open%20App-octobit.studio-AE86EB?style=for-the-badge&labelColor=22223B" alt="Open App" />
  </a>

  <br/><br/>

  <img src="https://img.shields.io/badge/version-1.5.α-AE86EB?style=flat-square&labelColor=22223B" alt="version" />
  <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black&labelColor=22223B" alt="React" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white&labelColor=22223B" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Canvas_2D-API-orange?style=flat-square&labelColor=22223B" alt="Canvas 2D" />
</div>

---

<div align="center">
  <img src="assets/hero.gif" alt="Tropical island scene speed-painted in OctoBit Studio" width="900" />
  <br/><sub>A 64×64 tropical island — painted start to finish with OctoBit tools: flood fill, shapes, pencil and line.</sub>
</div>

No install. No account. No friction. Open the browser and start drawing.

---

## Draw with precision

<div align="center">
  <img src="assets/shapes.gif" alt="Shapes and fill tools" width="900" />
</div>

| | Tool | Shortcut |
|--|------|----------|
| ✏️ | Pencil | `Ctrl+B` |
| 🧽 | Eraser | `Ctrl+E` |
| 🪣 | Bucket Fill | `Ctrl+G` |
| 💧 | Eyedropper | `Ctrl+I` |
| 📏 | Line | `Ctrl+L` |
| ⬜ | Rectangle | `Ctrl+R` |
| ⬛ | Fill Rectangle | `Ctrl+R` (toggle) |
| ⭕ | Ellipse | `Ctrl+O` |
| 🔵 | Fill Ellipse | `Ctrl+O` (toggle) |

All tools support adjustable brush size. Rectangle and Ellipse toggle between outline and fill mode via a flyout.

---

## Layers

<div align="center">
  <img src="assets/layers.gif" alt="Layer workflow" width="900" />
</div>

Full layer tree with nested groups — hide, lock, drag & drop reorder, thumbnails auto-cropped to painted area. Flip H/V and merge layers directly from the context menu.

---

## Your projects, your files

<div align="center">
  <img src="assets/screenshot-file-menu.png" alt="File menu" />
</div>

OctoBit uses its own binary format — **`.octo`** — storing layer pixel data as raw PNG blobs with gzip-compressed metadata. No dependencies, no base64 overhead.

- **File → Save As...** opens your OS native file picker (Chrome, Edge, Brave)
- **File → Open...** loads a `.octo` file back with all layers intact
- The `●` indicator in the project tab shows unsaved changes
- Auto-save to browser storage keeps your work between sessions

---

## Zoom & Navigation

<div align="center">
  <img src="assets/zoom.gif" alt="Zoom demo" width="900" />
</div>

Mouse wheel zooms toward cursor. `Space + drag` to pan. Pixel grid appears at ≥ 4×. Zoom controls in the toolbar: `−` / `100%` / `+` / **Center**.

---

## Color

<div align="center">
  <img src="assets/screenshot-color.png" alt="Color panel" width="360" />
</div>

Two picker modes: HSV square and HSL triangle. Primary/secondary color widget. Palette system with document palettes, harmonies (complementary, analogous, triadic), and last 10 used colors.

---

## Screenshots

<table>
  <tr>
    <td align="center">
      <img src="assets/screenshot-overview.png" alt="Full editor" />
      <br/><sub>Full editor</sub>
    </td>
    <td align="center">
      <img src="assets/screenshot-layers.png" alt="Layers panel" />
      <br/><sub>Layers panel</sub>
    </td>
  </tr>
  <tr>
    <td align="center">
      <img src="assets/screenshot-color.png" alt="Color panel" />
      <br/><sub>Color panel</sub>
    </td>
    <td align="center">
      <img src="assets/screenshot-tools.png" alt="Tool palette" />
      <br/><sub>Tool palette</sub>
    </td>
  </tr>
</table>

---

## Under the hood

Built from scratch — no canvas libraries:

- **DocumentEngine** — layer compositor with Canvas Pool (60 FPS, no GC pressure)
- **Bresenham & Zingl** — pixel-perfect lines and ellipses
- **Command pattern** — undo/redo, 50 steps
- **Snapshot-preview** — live shape preview without flicker
- **OctoFormat** — binary `.octo` container, gzip metadata, raw PNG blobs, no dependencies

4 themes: **Octoone** (dark), **Kyoonotay**, **Dracula**, **Light**.

---

## What's next

- [ ] Selection tools (rect, lasso, magic wand)
- [ ] Animation timeline + onion skinning
- [ ] Desktop app (Tauri)

---

<div align="center">
  <sub>Source code: private &nbsp;·&nbsp; <a href="https://octobit.studio">octobit.studio</a></sub>
</div>
