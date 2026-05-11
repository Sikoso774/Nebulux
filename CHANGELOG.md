# Changelog

All notable changes to this project will be documented in this file.

## [1.1.0] - 2026-05-11

### ✨ Added
- 🌌 **Neon Graph View**: Implemented a global WebGL canvas `drop-shadow` hack to create an immersive, glowing "neon" effect on all nodes and links in the Graph View, while remaining 100% compatible with complex plugins like Excalidraw.

### 🛠️ Changed
- **Codebase Refactoring (Massive `!important` Reduction)**: Completely rewrote the CSS specificity architecture. Drastically reduced the usage of `!important` tags. The theme now relies heavily on proper DOM hierarchy (`body`, `.theme-dark`), making it vastly more compatible with user snippets and Obsidian's core engine, while preserving full Style Settings compatibility where necessary.

---

## [1.0.0] - 2026-05-07

### ✨ Added
- 🎉 Initial release of **Nebulux** (formerly Galaxy Master HUD).
- Sci-Fi Cockpit interface with darkened backgrounds and neon highlights.
- Dynamic Gradient Headers (H1-H6).
- Glassmorphism effects on active tabs and floating menus.
- "Rainbow Folders" dynamic file explorer.
- Custom Callout System (Nav, Status, Projects) with Tactical Mode icons.
