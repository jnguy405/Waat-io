# [Waat.io](https://jnguy405.github.io/Waatio/) | CMPM 121 D2 Project

## Waat.io

🎨 A fully interactive, feature-rich drawing application built with TypeScript, canvas rendering, and event-driven architecture to practice software fundamentals and user-centered design.

---

## 🚀 Project Progression

This project evolved from a simple drawing app into a modular, extensible system:

1. Started with core mouse event handling and canvas manipulation.
2. Introduced event dispatching and observation to decouple components.
3. Refactored into object-oriented stroke and command models.
4. Generalized tools using the command pattern and data-driven configuration.
5. Enhanced UX with real-time previews and fine-grained controls.

---

## 📦 Tech Stack

- **TypeScript**: Strong typing ensures runtime safety and maintainable code structure.
- **HTML5 Canvas**: Pixel-perfect rendering with scalable export.
- **Vanilla DOM**: UI constructed programmatically with `document.createElement`.
- **CSS3**: Styled entirely via JS-linked stylesheet (rounded canvas, drop shadows, responsive layout).
- **GitHub Actions**: Automated deployment to GitHub Pages.

---

## 🔧 Features & Technical Highlights

### ✅ Core Functionality

- **Canvas Drawing**: Mouse event observers enable smooth freehand drawing with stroke recording.
- **Clear Canvas**: One-click reset with visual feedback.
- **Export High-Res PNG**: Render drawing at 4× scale (1024×1024) for crisp, downloadable artwork.

### ⏪ State Management

- **Undo/Redo System**: Implemented command pattern with stack manipulation (`push`/`pop`) to allow multi-step history.
- **Event-Driven Redraws**: Dispatch `drawing-changed` events to synchronize UI updates with model state.

### 🛠️ Tool System

- **Dual Marker Tools**: Toggle between "thin" and "thick" stroke widths with visual selection feedback.
- **Sticker Placement**: Add emoji stickers (☕, 🍪, 🍩) via live preview and click-to-place interaction.
- **Custom Stickers**: Dynamically create new stickers using `prompt()` input — data-driven design allows seamless integration.
- **Tool Previews**: Cursor-following preview rendered in real time using `tool-moved` events.

### 🎨 User Customization

- **Color Control**: Hue slider adjusts marker color with live canvas preview.
- **Sticker Rotation**: Orientation slider enables precise sticker placement with real-time rotation feedback.
- **UI Synchronization**: Tool state (active tool, color, rotation) is maintained and reflected across controls.

### 💡 Refactorings & Architecture

- **Command Pattern**: All drawing actions (strokes, stickers) encapsulated as commands for consistent undo/redo behavior.
- **Data-Driven Design**: Stickers defined in a central array, enabling dynamic tool creation and easier extensibility.
- **Separation of Concerns**:
  - `display()` and `drag()` methods abstract rendering logic.
  - `renderStickerOnCanvas()` centralizes drawing logic for reuse.
- **Clean Code Practices**:
  - Functions grouped and commented in `main.ts`.
  - Reusable utilities like `deselectAll()` and `selectMarker()` reduce redundancy.
