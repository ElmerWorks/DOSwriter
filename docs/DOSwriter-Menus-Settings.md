# DOSwriter Menus & Settings

This document describes the structure and options available in the DOSwriter menu system.

---

## 1. Top-Level App Menus
Accessible via `ALT + [Letter]` or `F10`. Use `Arrow Keys` to navigate between adjacent menus.

| Menu | Shortcut | Key Options |
| :--- | :--- | :--- |
| **FILE** | `ALT + F` | File Browser, Save, Save As, Open, Recent, Close, Close All, Exit. |
| **EDIT** | `ALT + E` | Undo, Redo, Cut/Copy/Paste, Find/Replace, Bookmarks, Macros, Unwrap. |
| **VIEW** | `ALT + V` | Buffers, Workspace Layout, Manuscript Viewer, Scratchpad, Image Viewer, Margins, Render, Status Bar, Split Screen. |
| **WORKSPACE**| `ALT + W` | ToDo List (Toggle Mode). |
| **TOOLS** | `ALT + T` | Simple Collapse, Pattern Manager, Recollapse, Typewriter Mode, Outline Manager, Desktop Sync. |
| **PUBLISH** | `ALT + P` | Standard PDF Compile, Manuscript Format PDF, 8-in-1 Minibook, Manuscript Settings. |
| **SETTINGS** | `ALT + S` | Cursor, Font, Margins, Theme, File Manager, Advanced Features, Global Settings Toggle. |
| **HELP** | `ALT + H` | Shortcuts Reference, Tutorial, Detailed Topics, Keyboard Map, Typewriter Demo, About. |

---

## 2. Settings Sub-Menus
Detailed configuration options found under the **SETTINGS (ALT + S)** menu.

### Cursor Settings
| Option | Description |
| :--- | :--- |
| **Style** | Choose cursor shape: Thin/Thick Caret, Block, Underline, Inverted, Retro, Dim. |
| **Typewriter Mode** | Access settings for Typewriter scrolling and cursor anchoring. |
| **Blink on Shortcut** | Toggle rapid blink feedback when using locator shortcuts. |
| **Cursor Blink Always** | Toggle continuous cursor blinking. |
| **Blink Interval** | Set the standard blinking speed (in milliseconds). |
| **Locator Duration** | Set how long the cursor "pings" after a find/center command. |
| **Virtual Input** | Toggle specialized input logic (e.g., for Supernote devices). |
| **Auto Typewriter** | Automatically enable typewriter scrolling for large files. |
| **Apply Globally** | Push current cursor settings to all 8 buffers. |

#### Typewriter Mode (Sub-Menu)
Settings for the typewriter-style scrolling engine, demonstrated in **ALT + D (Typewriter Demo)**.

| Option | Description |
| :--- | :--- |
| **Typewriter Active** | Toggle the typewriter engine. When ON, text scrolls while the cursor attempts to maintain a relative vertical position. |
| **Stationary Cursor** | Lock the cursor to a fixed screen coordinate. Text moves horizontally and vertically while the cursor stays centered or anchored. |
| **Position** | Choose the vertical anchor: **CENTER** (eye-level writing) or **BOTTOM** (terminal-style bottom-fill). |
| **Type Guide Graphic** | Toggle visual crosshair/guide lines. Visible only when **Stationary Cursor** is ON and **Terminal Mode** is OFF. |
| **Terminal Mode** | When ON, text fills from the top naturally until hitting the anchor point, then transitions to typewriter scrolling. |
| **Char/CRLF Delay** | Adjust simulation timing for the Typewriter Demo (ALT + D). |

### Font Settings
| Option | Description |
| :--- | :--- |
| **Font Selection** | Pick from Monospace, Courier, Noto Sans/Serif, and built-in professional weights. |
| **Line Height** | Set vertical spacing: Tight (1.0), Standard (1.2), Comfortable (1.5), Double (2.0). |
| **Font Bold** | Toggle bold weight for all text in the buffer. |
| **Link Custom Folder** | Select a folder on device storage to scan for `.ttf` or `.otf` files. |
| **Apply Globally** | Push current font and spacing settings to all 8 buffers. |

### Margin Settings
| Option | Description |
| :--- | :--- |
| **Side Margin** | Set horizontal padding (0px to 150px or Custom). |
| **Top/Bottom Margin** | Set vertical padding to clear system bars or physical bezels. |
| **Apply Globally** | Push current margin dimensions to all 8 buffers. |

### Theme Settings
| Option | Description |
| :--- | :--- |
| **Theme Selection** | Choose from 20+ schemes (Classic, CRT, E-Ink, Solarized, etc.). |
| **KB Background** | Toggle whether the virtual keyboard uses the theme background or font color. |
| **Day/Night Mode** | Set automated schedules for theme switching. |
| **App Menu Theme** | Toggle between Light and Dark interface for menus and overlays. |
| **Apply Globally** | Sync the visual theme across all active buffers. |

---

## 3. Advanced Features
Deep configuration for power users and device-specific hardware.

| Section | Key Options |
| :--- | :--- |
| **Manuscript View** | Page Size (8.5x11, 6x9, etc.), Orientation, Ref Font Size, Physical Margins, Paragraph Collapse logic. |
| **Text Display** | CRLF Symbol visibility, Tab Size (2, 4, 8), Page Jump Length, PDF Favorites limit, File Browser toggle (Custom vs System). |
| **Virtual Keyboard** | Toggle KB, Predictive Text, Numeric Row visibility, Keyboard Outlines, Save/Load Configs. |
| **Keyboard Mode** | Switch between Standard English and Vietnamese TELEX input. |
| **Scratchpad Buffer** | Set character limit and log filename for the F9 buffer. |
| **Hardware** | Display Type (LCD vs E-Ink), Vendor SDK selection (BOOX, Bigme, Supernote), System Clipboard suppression. |
| **Dev** | Keyboard overlays, Debug modes, Image transitions, External font scanning, Pattern collapse performance limits. |

---

## 4. Special Menus

### Desktop Sync (CTRL + D)
*   **Connect/Disconnect**: Toggle LAN connection to the Elmer-syncd host.
*   **Host/Port/Token**: Connection credentials.
*   **Auto-Push**: Toggle background saving and set the inactivity timeout.
*   **Manual Operations**: Fetch remote list, Push update, or Transfer local files.

### Outline Manager (ALT + O)
*   **Select Project**: Open existing `.json` outline files.
*   **Setup (CTRL-ALT-O)**: Create Folders, Add File Containers, Link Local/Remote files, Rename, and Delete.
*   **Live Preview**: Scroll through the outline to see instant content snippets.

### Manuscript Viewer (CTRL + Q)
*   **Layout View**: 4 or 8-page grid overview of the document structure.
*   **Filmstrip View**: Single-page continuous scrolling "print preview."
*   **WYSWYG Sync**: Press Enter on any page to jump the editor to that exact paragraph.
