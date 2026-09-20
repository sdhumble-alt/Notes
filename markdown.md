# A Humble Note Builder
**Version:** 1.1.0 — 2026-09-20[cite: 5]
**Author:** Steven Humble
**Suite:** "A Humble..." Educational Web Applications

> **IMPORTANT NOTE:** Do not update the application version number until explicitly directed to do so by the user.

## Overview
**A Humble Note Builder** is a client-side, single-page web application designed specifically for educators. It solves the formatting frustrations of standard word processors by providing a free-form, mathematically scaled canvas optimized for creating guided notes, graphic organizers, and Interactive Student Notebook (ISN) inserts. 

The application ensures that what is designed on the screen scales perfectly to physical paper, offering specialized tools like automated Cornell Notes layouts, smart alignment guides, and rich-text editing with built-in scientific symbols.

---

## Core Features

### 1. Precision Canvas & Layout Engine
* **Custom Dimensions:** Built-in presets for Standard Letter (8.5" x 11") and Composition Notebooks (6.25" x 8.5" & 7" x 9"), plus custom inch-based inputs.
* **Orientation:** One-click toggling between Portrait and Landscape, remembered locally.
* **Intelligent Scaling:** Custom 3-way confirmation modal (*Yes, scale*, *No, do not scale*, *Cancel*) when changing paper dimensions with existing content.
* **Smart Snapping:** Elements automatically snap to a customizable pixel grid or to the edges/centers of other elements via magenta Smart Guides (active on both drag and resize).

### 2. Element Library
* **Blank Boxes:** Resizable containers that support independent, locally-saved line/grid spacing sizes and inline Header Labels with Left, Center, or Right justification.
* **Text Blocks:** Borderless floating text zones.
* **Data Tables:** Highly customizable grids where rows and columns can be scaled, and individual cells can be formatted independently or globally.
* **Images:** Local file uploads that scale proportionally.
* **Page Numbers:** Auto-calculates the bottom-right corner of the safe zone to drop a 9pt centered page number block.

### 3. Pedagogical Templates
* **Cornell Notes:** Instantly generates a mathematically scaled, 4-part layout (Topic, Cues, Notes, Summary).
* **Frayer Model:** Auto-generates a 5-part vocabulary matrix with right-justified headers on the right-hand boxes to prevent overlap with the center box.

### 4. Advanced Text & Formatting
* **Global Typography:** Select a master font (saved locally) that applies to the entire document.
* **Rich Text Toolbar:** Organized into a clean 3-tier layout featuring Bold, Italic, Underline, Strikethrough, and Horizontal/Vertical alignment controls.
* **List Engine:** Auto-incrementing Bullet, Numbered, Outline, and Checkbox (`☐`) lists featuring automatic word-processor style line continuation and hanging indents.
* **Scientific Notation:** Dedicated insertion panels for Greek letters and Math symbols, plus single-click Subscript and Superscript conversion.

### 5. Project Management & Export
* **.humblenote Files:** Save and open ongoing projects as lightweight local JSON files.
* **History Stack:** Full Undo/Redo tracking for all canvas actions.
* **Local Storage:** Remembers paper size, orientation, custom dimensions, font family, and line/grid spacing preferences.
* **High-Fidelity PDF Export:** Utilizes `jsPDF` to generate resolution-perfect PDF files with cutting guide tick-marks for non-standard paper sizes.

---

## Technical Architecture

* **Frontend Structure:** HTML5 & CSS3, utilizing CSS Grid and Flexbox.
* **Rendering Engine:** HTML5 `<canvas>` API (`CanvasRenderingContext2D`) for drawing, text wrapping, and bounding boxes.
* **Dependencies:** Tabler Icons, jsPDF.

---

## Keyboard Shortcuts

| Shortcut | Action | Scope |
| :--- | :--- | :--- |
| `Backspace` / `Delete` | Delete Element | Canvas (when element selected, not typing) |
| `Ctrl + C` / `Cmd + C` | Copy Element | Canvas |
| `Ctrl + X` / `Cmd + X` | Cut Element | Canvas |
| `Ctrl + V` / `Cmd + V` | Paste Element | Canvas (Pastes with a 20px offset) |
| `Ctrl + Scroll Wheel` | Zoom Canvas | Viewport |
| `Enter` | Next List Item | Textarea (auto-increments list markers) |
