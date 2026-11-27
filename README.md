# Stencil & Print Image Splitter – Offline Edition

An offline, browser-based tool for splitting large designs and stencils across multiple printable pages with interactive seam placement, overlap margins, alignment marks, and multi-page PDF export.

## Overview

`ImageSplitterForPrinting` is a self-contained single-file web application (`index.html`) designed for preparing large-format artwork, stencils, and garment/transfer prints on standard home or office printers. All image processing happens locally in the browser with no external servers or uploads.

## Features

- **Local Image Loading**: Supports PNG, JPG, WebP, and SVG files via click-to-browse or drag-and-drop.
- **Stencil Prep & Filters**:
  - Rotate 90° and automatic whitespace trimming.
  - Horizontal Mirror/Flip for face-down transfers.
  - Ink-Saver / Stencil modes: Original Colors, Grayscale (Ink-Saver), B&W High-Contrast Stencil, and Outline / Edge-Only Cut Lines with an adjustable B&W Threshold slider (15–240).
- **Physical Sizing & Paper Setup**:
  - Dimensions in inches (`in`) or centimeters (`cm`) with optional Aspect Ratio Lock.
  - Portrait and Landscape paper orientations.
  - Preset paper sizes: US Letter (8.5" × 11"), US Legal (8.5" × 14"), Tabloid / Ledger (11" × 17"), A4 (210 × 297 mm), and A3 (297 × 420 mm).
  - Configurable Printer Margin and Tape Overlap.
- **Interactive Split Lines & Page Control**:
  - Add, remove, or auto-distribute (`Auto-Even Splits`) vertical and horizontal cyan split lines.
  - Drag split lines on the canvas or nudge selected lines with the Arrow keys (`Shift` for 5× step) and on-screen nudge controls; `Delete` removes the selected split.
  - `Auto-Skip Blank Pages` and per-page include/skip checkboxes on the preview canvas.
- **Print & PDF Export Options**:
  - Thin Tile Border around each split tile.
  - Corner alignment crosshairs (`+`) and Grid IDs (`A1`, `B2`, etc.).
  - Overlap Tape Shading (`TAPE OVERLAP` hatch tabs).
  - Scale Calibration Bar (1" / 5 cm verification ruler on Page 1).
  - Optional Assembly Key Cover Page (miniature grid map as Page 0 of the PDF).
  - Optional PDF compression (150 DPI vs. 300 DPI print quality).
- **Interactive Workspace**:
  - Live preview with page count, max tile size, and effective DPI stats.
  - Garment Size Reference Overlays (Adult T-Shirt 20" × 28", Hoodie Back 22" × 27", Tote Bag 15" × 16").
  - Zoom/pan controls and automatic preference persistence via `localStorage`.

## Requirements / Dependencies

- **Runtime**: Any modern desktop or mobile web browser with HTML5 Canvas and JavaScript enabled (e.g., Chrome, Firefox, Edge, Safari).
- **Dependencies**: None. `index.html` is completely self-contained with zero external scripts, stylesheets, or build tools.

## Installation / Setup

1. Download or clone this repository from GitHub (`zadrian9/ImageSplitterForPrinting`).
2. Open `index.html` directly in your web browser (double-click the file or drag it into a browser tab). No web server, package manager, or internet connection is required.

### Install / Offline (PWA)

When opened over `https://` (such as GitHub Pages) or `http://localhost`, you can install the app from your browser's address bar / menu; it caches all shell assets on first load and continues working offline.

## Usage

1. **Load a Design**: Click or drop a PNG, JPG, WebP, or SVG image into **1. Design Image**.
2. **Prepare Stencil (Optional)**: Rotate, trim whitespace, mirror for transfers, or choose an ink-saver/stencil filter under **2. Stencil Prep & Filters**.
3. **Set Physical Size**: Enter the desired output width or height in inches or centimeters under **3. Physical Size**.
4. **Configure Paper & Overlap**: Select paper size, orientation, printer margin, and tape overlap under **4. Paper & Margins**.
5. **Adjust Split Lines**: Use **5. Split Lines** or drag/nudge the cyan split lines directly on the canvas so seams avoid fine details. Toggle individual pages on/off as needed.
6. **Configure Output & Export**: Choose your desired alignment marks, calibration bar, cover page, and compression settings under **6. Print & PDF Options**, then export or print your tiled PDF.

## License

This project is licensed under the [Mozilla Public License 2.0](LICENSE).
