# A Humble Note Builder
**Version:** 1.3.0 — 2026-09-20
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
* **Auto-Fit Viewport:** The canvas automatically defaults to 100% zoom or "fit width" on load, whichever is smaller.

### 2. Element Library
* **Properties Panel:** Context-aware "Element Properties" panel intelligently docks at the top of the controls sidebar the moment an element is selected.
* **Blank Boxes:** Resizable containers that support independent, locally-saved line spacing (default 20px) and grid spacing (default 14px), and inline Header Labels with Left, Center, or Right justification.
* **Text Blocks:** Borderless floating text zones.
* **Data Tables:** Highly customizable grids where rows and columns can be scaled. Newly inserted tables default to Center and Middle alignment, with the first row automatically bolded.
* **Images:** Local file uploads that scale proportionally.
* **Page Numbers:** Auto-calculates the bottom-right corner of the safe zone to drop a 9pt centered page number block.

### 3. Pedagogical Templates
* **Cornell Notes:** Instantly generates a mathematically scaled, 4-part layout (Topic, Cues, Notes, Summary).
* **Frayer Model:** Auto-generates a 5-part vocabulary matrix with right-justified headers on the right-hand boxes to prevent overlap with the center box.
* **Science Lab Protocol:** Auto-generates a dynamically scaled, proportional layout featuring reading sections (Background, Safety, Materials, Procedure, Formulas, Clean Up, and Stamp) and open workspace boxes for data collection.

### 4. Advanced Text & Formatting
* **Global Typography:** Select a master font (saved locally) that applies to the entire document. The base font size for all new elements defaults to 12pt.
* **3-Tier Rich Text Toolbar:** Cleanly organized into three distinct rows for rapid formatting:
  * *Row 1:* Font Size, Bold, Italic, Underline, Strikethrough.
  * *Row 2:* Math/Greek symbol insertion, Subscript/Superscript (which toggle on and off for all selected text), and List toggles.
  * *Row 3:* Horizontal and Vertical alignment controls.
* **List Engine:** Auto-incrementing Bullet, Numbered, Outline, and Checkbox (`☐`) lists featuring automatic word-processor style line continuation and hanging indents.
* **Scientific Notation:** Dedicated insertion panels for Greek letters and Math symbols, plus multi-character Subscript and Superscript toggling.

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
