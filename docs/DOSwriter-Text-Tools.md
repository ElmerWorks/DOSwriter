# DOSwriter Text Tools: Bookmarks & Text Collapse
**Version:** 1.0 (August 2026)

## Overview
DOSwriter includes advanced text organization tools designed to help writers navigate long documents and maintain focus by hiding non-essential content. These tools follow the app's high-contrast, theme-aware, and keyboard-centric design.

---

## 1. Bookmarks (`[BK]`)

Bookmarks allow you to tag specific lines in your document for instant navigation.

### Visual Style
- **Marker**: A high-contrast `[BK]` icon appears in the left margin.
- **Context Preview**: To the right of the marker, a dimmed snippet of the bookmarked line is displayed, providing immediate context without cluttering the primary text flow.
- **Theme Awareness**: The `[BK]` marker and preview text automatically adjust their colors based on your active Day or Night theme.

### Controls & Navigation
- **`CTRL+K`**: Toggle a bookmark on the current line.
- **`CTRL+SHIFT+K`**: Jump immediately to the last created bookmark.
- **`ALT+K`**: Open the **Bookmark Menu**. This displays a numbered list of all active bookmarks with their text previews. You can use arrow keys or numeric keys (1-8) to jump to a specific location.

---

## 2. Text Collapse & Folding (`[+]`)

Text Collapse (also known as Folding) allows you to hide large blocks of text—such as research notes, older drafts, or completed chapters—behind a single icon.

### Visual Style
- **Marker**: A high-contrast `[+]` icon represents a collapsed block of text.
- **Content Preview**: Similar to bookmarks, a dimmed preview of the first line of the hidden text is shown next to the `[+]` icon.
- **Expansion**: Simply move the cursor onto the `[+]` icon or the preview text to automatically expand the block.

### Controls & Methods
There are three ways to collapse text in DOSwriter:

#### A. Selection Collapse
- **`CTRL+J`**: Collapses the currently selected block of text. 

#### B. Pattern Collapse (Automated)
- **`CTRL+ALT+J`**: Define a custom "Pattern" (e.g., `//NOTES` or `(DRAFT)`). Every instance of this text and the remainder of its paragraph will be automatically collapsed.
- **`ALT+J`**: Open the **Pattern Picker**. This menu allows you to manage and toggle your global collapse patterns.

#### C. Smart Recollapse
- **`CTRL+SHIFT+J`**: If you have expanded a fold to check a detail and want to hide it again, this command "re-folds" the last expanded block instantly.

---

## 3. Typographic Integration
Both Bookmarks and Folds are integrated into the line-counting and rendering engine. 
- **Margin Consistency**: Markers are designed to fit within the standard side margins, ensuring that your text layout remains stable even as you add tools.
- **E-Ink Optimization**: Markers use thick, solid strokes to ensure they remain crisp on e-ink displays with slower refresh rates.
- **Performance**: Folds and Bookmarks are calculated during the layout pass and do not cause lag during active typing, even in very large files (>100KB).
