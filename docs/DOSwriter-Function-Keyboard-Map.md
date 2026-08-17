# DOSwriter Function & Keyboard Map
**Updated:** August 2026

This document provides a comprehensive mapping of all keyboard commands and functions available in DOSwriter, including the advanced typographic and workspace features added in the latest version.

---

## 1. File Operations
Commands for managing files, exporting, and sharing content.

| Function | Keyboard Shortcut | Description |
| :--- | :--- | :--- |
| **File Menu** | `ALT + F` | Open the top-level File system menu. |
| **File Browser** | `CTRL + ALT + F` | Open the DOSwriter custom keyboard-centric file browser. |
| **Open File** | `CTRL + O` | Open a text, markdown, image, or PDF file. |
| **Open Recent** | `CTRL + SHIFT + O` | View and open from a list of recently accessed files. |
| **Save File** | `CTRL + S` | Save the current buffer to its linked file. |
| **Save As** | `CTRL + SHIFT + S` | Save the current buffer under a new filename. |
| **Desktop Sync** | `CTRL + D` | Open the Sync menu to manage real-time file synchronization. |
| **Instant PDF** | `CTRL + P` | Export the current buffer(s) to a paginated PDF. |
| **Close Buffer** | `CTRL + W` | Close the current file and clear the buffer. |
| **Close All** | `CTRL + ALT + W` | Close all open files across all 8 buffers. |
| **Share Buffer** | `CTRL + ALT + S` | Trigger the Android System Share for the current buffer. |
| **Copy to System** | `CTRL + ALT + C` | Copy the entire buffer content to the Android System Clipboard. |
| **Screenshot** | `CTRL + I` | Capture the screen and save to the device Pictures folder. |
| **Exit App** | `CTRL + ALT + X` | Protected prompt to exit the application. |

---

## 2. Editing & Selection
Standard and advanced text manipulation tools.

| Function | Keyboard Shortcut | Description |
| :--- | :--- | :--- |
| **Edit Menu** | `ALT + E` | Open the top-level Edit system menu. |
| **Undo** | `CTRL + Z` | Revert the last change (up to 100 levels). |
| **Redo** | `CTRL + ALT + Z` | Re-apply a previously undone change. |
| **Cut** | `CTRL + X` | Cut selected text to the clipboard. |
| **Copy** | `CTRL + C` | Copy selected text to the clipboard. |
| **Paste** | `CTRL + V` | Paste text from the clipboard at the cursor position. |
| **Select All** | `CTRL + A` | Select the entire contents of the buffer. |
| **Select Text** | `SHIFT + [Nav]` | Hold Shift while using any navigation command to select text. |
| **Find** | `CTRL + F` | Open the search overlay. Supports 8-slot query history (Up/Down). |
| **Replace** | `CTRL + R` | Open the replace overlay. Supports 8-slot replacement history. |
| **Unwrap Paragraphs** | `CTRL + ALT + U` | Strip extraneous newlines from imported "hard-wrapped" text. |
| **Bold On/Off** | `CTRL + B` | Toggle bold text mode for the current buffer. |

---

## 3. Typographic & Font Control
The hardware-profiled typographic system.

| Function | Keyboard Shortcut | Description |
| :--- | :--- | :--- |
| **Cycle Fonts** | `CTRL + ALT + B` | Rotate forward through all internal and custom fonts. |
| **Font Presets** | `CTRL + ALT + =` | Open the Characters Per Line (CPL) preset menu. |
| **Display Font** | `CTRL + SHIFT + F` | Display the name of the current font in a status toast. |
| **Increase Font** | `CTRL + =` (or `+`) | Fine-tune font size (switches to "Custom" preset). |
| **Decrease Font** | `CTRL + -` | Fine-tune font size (switches to "Custom" preset). |
| **Line Height Menu** | `ALT + L` | Open the menu to select line spacing (1.0, 1.2, 1.5, 2.0). |
| **Cycle Line Height** | `CTRL + L` | Rotate through available line spacing settings. |

---

## 4. Viewing & Atmospheric Comfort
Visual aesthetics and ergonomics, optimized for E-Ink and focus.

| Function | Keyboard Shortcut | Description |
| :--- | :--- | :--- |
| **View Menu** | `ALT + V` | Open the top-level View system menu. |
| **Cycle Themes** | `CTRL + T` | Rotate forward through color/E-Ink themes. |
| **Cycle Themes Back** | `CTRL + ALT + T` | Rotate backward through color/E-Ink themes. |
| **Display Theme** | `CTRL + SHIFT + T` | Display current theme name and Day/Night status. |
| **Toggle Status Bar** | `ALT + H` | Show or hide the word count and filename status line. |
| **Toggle Margins** | `CTRL + SHIFT + M` | Show or hide visual side margins. |
| **Adjust Vertical** | `CTRL + , / .` | Shift the text viewport up or down by 5px. |
| **Brightness** | `ALT + + / -` | Increase or decrease screen/frontlight brightness. |
| **Toggle Help** | `CTRL + H` | Show or hide the searchable Markdown Help system. |

---

## 5. Navigation & Bookmarks
Moving through large documents efficiently.

| Function | Keyboard Shortcut | Description |
| :--- | :--- | :--- |
| **Move Char/Line** | `Arrow Keys` | Standard character and terminal line movement. |
| **Jump Word** | `CTRL + Left / Right` | Move the cursor to the previous or next word boundary. |
| **Jump Line Bound** | `ALT + Left / Right` | Move the cursor to the beginning or end of the visual line. |
| **Jump Paragraph** | `CTRL + Up / Down` | Move the cursor to the previous or next paragraph break. |
| **Jump Sentence** | `ALT + Up / Down` | Move the cursor to the start of the previous or next sentence. |
| **Jump File Start** | `CTRL + \` | Move the cursor to the very start of the document. |
| **Jump File End** | `CTRL + '` | Move the cursor to the very end of the document. |
| **Add Bookmark** | `CTRL + K` | Set a bookmark (indicated by `[BK]` and text preview). |
| **Bookmark List** | `ALT + K` | Open the Bookmark Menu to jump between tagged locations. |
| **Jump Last Bookmark** | `CTRL + SHIFT + K` | Instantly jump to the most recently added bookmark. |
| **Center Cursor** | `ALT + C` | Recenter the text on the cursor and trigger a locator blink. |

---

## 6. Workspace & Buffers
Managing multiple drafts and focused environments.

| Function | Keyboard Shortcut | Description |
| :--- | :--- | :--- |
| **Workspace Menu** | `ALT + W` | Open the top-level Workspace system menu. |
| **Layout Overview** | `Esc` | View all 8 buffers in a grid for selection (Normal Mode). |
| **Switch Buffer** | `F1 - F8` | Instantly switch to buffers 1 through 8. |
| **Alt Switch Buffer** | `ALT + 1 - 8` | Alternative shortcuts for buffer switching. |
| **Toggle To-Do Mode** | `ALT + W` (Menu) | Swap between the Main stack and the To-Do task stack. |
| **Open Scratchpad** | `F9` or `ALT + 9` | Open the character-limited Scratchpad (Index 16). |
| **Flush Scratchpad** | `CTRL + F9` | Save Scratchpad content to the log file and clear it. |
| **Manuscript Layout** | `CTRL + SHIFT + Q` | Open the tiled physical pagination viewer. |
| **Manuscript Strip** | `CTRL + ALT + Q` | Open the scrollable "Filmstrip" pagination viewer. |
| **Split Screen** | `CTRL + ALT + Arrows` | Open a split-view to compare two buffers side-by-side. |
| **Exit View/Split** | `Esc` | Close Layout view, split-screen, or rendered previews. |

---

## 7. Special Tools & Scripting
Advanced automation and organization.

| Function | Keyboard Shortcut | Description |
| :--- | :--- | :--- |
| **Script Console** | `ALT + Z` | Open the single-line popup Scripting Console. |
| **Run Script** | `CTRL + F8` | Execute the current buffer as a Command Script. |
| **Simple Collapse** | `CTRL + J` | Collapse the currently selected text block into a `[+]` icon. |
| **Recollapse Last** | `CTRL + SHIFT + J` | Instantly refold the most recently expanded text section. |
| **Pattern manager** | `ALT + J` | Manage patterns for automated global text folding. |
| **Markdown Preview** | `ALT + R` | Render current Markdown file as a professional document. |
| **Outline Manager** | `ALT + O` (or `F12`) | Open the hierarchical project tree tool. |
| **Typewriter Mode** | `ALT + Y` (or `F11`) | Toggle typewriter scrolling with visual guide lines. |
| **Virtual Keyboard** | `ALT + K` | Toggle the on-screen keyboard (supports CTRL Lock ⎈L). |

---

## 8. Buffer Layout View Shortcuts
Context-specific commands when the Workspace Layout grid (`Esc`) is visible.

| Function | Keyboard Shortcut | Description |
| :--- | :--- | :--- |
| **Preview Mode** | `CTRL + P` | Show text snapshots for all buffer tiles. |
| **Image Mode** | `CTRL + T` | Prioritize linked images for all buffer tiles. |
| **Text Mode** | `ALT + T` | Prioritize custom text thumbnails for all buffer tiles. |
| **Direct Select** | `1 - 8` (or `F1-F8`) | Select and open the corresponding buffer. |
| **Navigation** | `Arrow Keys` | Move the focus highlight between tiles. |
| **Open Buffer** | `Enter` | Open the currently highlighted buffer. |
