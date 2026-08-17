# DOSwriter: Text Collapse & Document Folding

DOSwriter provides professional-grade tools for structural outlining and managing long manuscripts through an intelligent "Text Collapse" system.

## 🛠️ Core Commands

| Shortcut | Function | Description |
| :--- | :--- | :--- |
| `CTRL + J` | **Simple Collapse** | Instantly collapse the currently selected text block. |
| `ALT + J` | **Pattern Manager** | View active collapse patterns or perform structural batch operations. |
| `CTRL + SHIFT + J` | **Recollapse** | "Zip up" the last section you expanded. Supports an 8-level undo stack. |
| `CTRL + ALT + J` | **Define Pattern** | Enter a custom string pattern (e.g., "CHAPTER") to trigger automatic folding. |

## 💡 Key Features

### 1. Pattern-Based Folding
Automatically organize your document by defining keyword "Headers". Any text following your pattern will be hidden until you explicitly expand it. Patterns are persistent and are applied **globally** to all 8 buffers by default.

### 2. Intelligent Expansion Stack
When you expand a folded section to edit it, DOSwriter remembers. Pressing `CTRL + SHIFT + J` will re-fold that exact section when you are done, allowing you to maintain focus without manual scrolling.

### 3. Structural Outlining & Fold List
The Pattern Collapse Manager (`ALT + J`) allows you to manage active patterns or perform a global structural collapse:
- **Collapse All Paragraphs**: Folds every paragraph in the text (not just patterns) to create a high-level outline.
- **Expand All Paragraphs**: Restores visibility to all collapsed paragraphs.
- **Fold List**: Opens a dedicated menu to see and jump to any currently collapsed section in the buffer.

### 4. Performance Safety
To ensure a lag-free experience on E-ink devices, the **Pattern Collapse Limit** (found in `Settings > Dev`) prevents automated folding on massive files (default 30KB). For files exceeding this limit, manual selection-based folding (`CTRL + J`) is recommended.
