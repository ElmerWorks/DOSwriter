# DOSwriter Command Scripting Syntax

DOSwriter scripts are written in plain text (Markdown files) and executed via `CTRL + F8`. The script engine drives the editor by simulating keyboard commands and automated text entry.

## Script Instructions

| Instruction | Argument | Description |
| :--- | :--- | :--- |
| `[LINE-DELAY]` | `milliseconds` | Sets the pause duration between subsequent lines (Default: 500). |
| `[CHAR_DELAY]` | `milliseconds` | Sets the delay between characters for the `[TYPE]` command (Default: 50). |
| `[PAUSETIME]` | `seconds` | Sets the default duration for `[PAUSE]` (1-60). |
| `[CR]` / `[BR]` | (none) | Inserts a blank line (New Line) into the buffer. |
| `[PAUSE]` | `seconds` (opt) | Pauses execution. Uses `[PAUSETIME]` if no argument is provided. |
| `[CMD]` | `Identifier` | Executes a command or shortcut. Supports **Keyboard Combinations**. |
| `[TYPE]` | `String` | Automatically types text. Supports `{CLIPBOARD}`. **Auto-appends \n**. |
| `[TYPE_CLIPBOARD]` | (none) | Instantly types the contents of the internal clipboard. |
| `[PASTE]` | `String` | Instantly inserts text (no typing simulation). Supports `{CLIPBOARD}`. |
| `[PRESENTATION]` | (none) | Enters Presentation Mode: Enables Markdown and treats plain text as slide content. |
| `[IMAGE]` | `Target` | Loads an image. Supports **filenames** (linked folder), **absolute paths** (`/storage/...`), or **URIs** (`file://`). |
| `[IMAGE>BUF]` | `Buf, Target` | Loads an image into a specific buffer (1-8). Supports filenames, paths, and URIs. |
| `[CLOSE-IMAGE]` | `Num` (opt) | Removes the image from the specified buffer (or current if omitted). |
| `[CLEAR]` | `1-8` | Clears the specified buffer instantly (Suppressing watermark). |
| `[BEEP]` | (none) | Plays a short notification tone to prompt user action. |
| `[NOTIFY]` | `Message` | Displays a message in the Script HUD. |
| `[STEP]` | (none) | Pauses script execution. Press `F8` to advance to the next line. |
| `[GOTO_BUFFER]` | `1-8` | Quickly switches focus to the specified buffer. |
| `[HIDE-CURSOR]` | (none) | Hides the text cursor from the viewport. |
| `[SHOW-CURSOR]` | (none) | Restores visibility of the text cursor. |
| `[HIDE-EMPTYBUFFER-MSG]` | (none) | Hides the "DOSwriter Menu..." watermark. |
| `[SHOW-EMPTYBUFFER-MSG]` | (none) | Restores the "DOSwriter Menu..." watermark. |
| `---` | (none) | In `[PRESENTATION]` mode: Clears buffer and enters `[STEP]` mode. |
| `[MACRO] NAME` | (none) | Defines a macro. Ends with `[ENDMACRO]`. Call by using `NAME`. |
| `[VAR] : VAL` | (none) | Defines a global variable for `[VAR]` substitution. |
| `[INCLUDE] File` | `Name` | Includes script content/macros from another file (Assets or Local). |
| `[BYPASS]` | (none) | Starts a block of code that the engine will ignore. |
| `[END-BYPASS]` | (none) | Ends a bypass block and resumes normal script processing. |
| `#` | `Content` | In `[PRESENTATION]` mode, this is a **Markdown Header**. |
| `//` | `Comment` | Any line starting with `//` is ignored. |

---

## Markdown Formatting (Presentation Mode)

When using `[PRESENTATION]` mode, DOSwriter renders your text using professional Markdown formatting.

### Supported Options:

1. **Headers**: Use `#` followed by a space.
   - `# Level 1 Header` (Large, Bold)
   - `## Level 2 Header` (Medium, Bold)

2. **Emphasis**:
   - `**Bold Text**` or `__Bold Text__`
   - `*Italic Text*` or `_Italic Text_`
   - `***Bold and Italic***`

3. **Lists**:
   - `- Bullet points`
   - `1. Numbered lists`

4. **Blockquotes**:
   - `> This is a blockquote (renders in Italics)`

5. **Tables**: Standard Markdown table syntax.
   ```
   | Feature | Status |
   | :--- | :--- |
   | High Perf | OK |
   | Scripting | OK |
   ```

6. **Images**: `![alt](filename/path/uri)`
   - Note: Supports simple filenames (linked folder), absolute paths (`/storage/emulated/0/...`), or `file:///` URIs. In `[PRESENTATION]` mode, an image on a standalone line acts as a full-screen visual slide.

7. **Horizontal Rules**: `---`
   - *Note: In scripting, `---` also triggers a slide break.*

---

## Advanced Variable & Markup Features

### NULL Content Skipping
If a variable is assigned the value **`NULL`** (case-insensitive), DOSwriter will automatically skip any Markdown lines that would result in empty markup or just the "NULL" keyword.

- **Assignment**: `[SUBTITLE]: NULL`
- **Effect**: A script line containing `##[SUBTITLE]` will be ignored entirely instead of displaying `##` or `NULL` in the buffer.
- **Empty Markers**: Any line containing only Markdown markers (`#`, `##`, `>`) with no content will also be skipped.

---

## Supported [CMD] Identifiers

The `[CMD]` instruction supports standardized keyboard naming.

### Common Shortcuts
- `CTRL-S`, `CTRL-SHIFT-S`, `CTRL-O`, `CTRL-SHIFT-O`
- `CTRL-Z`, `CTRL-ALT-Z` (Undo/Redo)
- `CTRL-C`, `CTRL-X`, `CTRL-V` (Clipboard)
- `CTRL-A` (Select All)
- `CTRL-F`, `CTRL-R` (Find/Replace)
- `CTRL-P` (Instant PDF), `ALT-P` (Publish Menu)
- `CTRL-Q` (Manuscript Menu), `CTRL+ALT+Q` (Filmstrip), `CTRL+SHIFT+Q` (Layout)
- `CTRL-Y` (Toggle Typewriter), `ALT-Y` (Typewriter Settings)
- `ALT-K` (Bookmarks), `CTRL-K` (Add Bookmark)
- `ALT-J` (Pattern Manager), `CTRL-J` (Simple Collapse), `CTRL-SHIFT-J` (Recollapse)
- `ENTER`, `TAB`, `ESC`

### Navigation & Combinations
- `UP`, `DOWN`, `LEFT`, `RIGHT`, `HOME`, `END`
- `CTRL-BACKSLASH` (Home), `CTRL-APOSTROPHE` (End)
- `SHIFT-UP/DOWN/LEFT/RIGHT` (Selection)
- `CTRL-COMMA` / `CTRL-PERIOD` (Vertical Margin)

---

## Example Presentation Script

```markdown
[PRESENTATION]
[PAUSETIME] 3
[SPLIT-SCREEN-V] 2
[FOCUS-RIGHT] [IMAGE] title.png
[FOCUS-LEFT]

# Project Vision
*A focus-first workstation.*

[PAUSE]
---
[FOCUS-RIGHT] [IMAGE] features.jpg
[FOCUS-LEFT]

## Core Features
- Real-time Markdown
- Advanced Scripting
- Split-Screen Visuals
```
