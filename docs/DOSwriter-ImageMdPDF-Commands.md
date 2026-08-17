# DOSwriter: Non-Text File Commands

DOSwriter supports high-performance viewing and navigation for Images (including Animated GIFs), PDFs, and Markdown files.

## 🖼️ Image Viewer & Slideshow
Manage visual references and aesthetic backgrounds.

### General Commands
| Shortcut | Action |
| :--- | :--- |
| `ALT + SHIFT + I` | Open Image Viewer (Full Screen). |
| `ALT + I` | Image Settings (Interval, Link/Unlink folders). |
| `Arrows` (Left/Right) | Move to the Next or Previous image in folder. |
| `S` | Toggle Slideshow (Auto-playback). |
| `CTRL + (+) / (-)` | Zoom In / Out (Current Buffer Image). |
| `Arrow Keys` | Pan image within the viewport. |
| `CTRL + ALT + Arrows` | Large Pan (Jump image in larger increments). |
| `ESC` | Close the Image Viewer layer. |

### Scripting & Automation Directives
Automate imagery during presentations or demos.
| Directive | Action |
| :--- | :--- |
| `[IMAGE] target` | Loads an image. Supports filenames (linked folder), absolute paths (`/storage/...`), or URIs (`file://`). |
| `[IMAGE>BUF] 6, target` | Loads image into specific buffer (1-8). Supports filenames, paths, and URIs. |
| `![alt](target)` | Markdown syntax for images. Standalone line creates full-screen image slide in `[PRESENTATION]`. |
| `[CLOSE-IMAGE] 6` | Removes image from buffer 6 (defaults to current if num omitted). |

### Advanced Features
- **Animated GIFs**: Full support for frame-by-frame animation in standard and split-view modes.
- **Multi-Tasking**: In split-screen, you can run a slideshow in one panel while writing in the other. Use `ALT + N` to swap focus.
- **Link Management**: Use `ALT + I > Manage Linked Folders`. Highlight a folder and press `Delete` to unlink it.

---

## 📄 PDF Navigation
Professional document viewing with precise pagination.

### Page Navigation
| Shortcut | Action |
| :--- | :--- |
| `N` / `P` | Next Page / Previous Page. |
| `Arrows` (Left/Right) | Next Page / Previous Page. |
| `ALT + Arrows` (Up/Down) | Jump to the First Page / Last Page. |
| `CTRL + G` | Open "Go to Page" numeric input. |

### Manuscript Viewer
| Shortcut | Action |
| :--- | :--- |
| `CTRL + ALT + Q` | Open Manuscript **Filmstrip View** (Single page). |
| `CTRL + SHIFT + Q` | Open Manuscript **Layout View** (Grid overview). |
| `ALT + Q` | Manuscript Viewer Settings Menu. |

### View Controls
| Shortcut | Action |
| :--- | :--- |
| `CTRL + (+) / (-)` | PDF Zoom In / Out. |
| `CTRL + R` | Reset PDF View (Fit to screen). |
| `CTRL + V` | Open PDF Favorites list. |

### Favorites & Export
- **Add Favorite**: `CTRL + ALT + K` (Saves current page with a custom label).
- **Export List**: `CTRL + ALT + P` (Exports your favorite pages to a `.txt` file).

---

## 📝 Markdown Rendering
Write in plain text and view as a formatted document.

| Shortcut | Action |
| :--- | :--- |
| `ALT + R` | Toggle Markdown Render mode. |
| `CTRL + S` | Save the underlying Markdown source code. |

### Scripting Presentation Mode
| Directive | Action |
| :--- | :--- |
| `[PRESENTATION]` | Enters Presentation Mode: Renders Markdown slides. |
| `[CR]` / `[BR]` | Inserts a blank line (New Line) between text blocks. |
| `---` | Clears slide and enters `[STEP]` mode for the next transition. |

### Split-View Sync
- **Bottom-Snapping**: When viewing Markdown in split-screen, the renderer uses intelligent "Bottom-Snapping" logic. This ensures that as you type in the text panel, the Markdown preview panel automatically stays aligned to the bottom, keeping your most recent changes visible.
