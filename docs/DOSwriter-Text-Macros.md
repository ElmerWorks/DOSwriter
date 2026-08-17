# DOSwriter Text Macro System

DOSwriter includes a robust, context-aware Text Macro system designed to accelerate repetitive typing tasks and manage specialized snippets for different writing workflows (e.g., plain text, coding, or Markdown).

## Access and Management

The macro system is accessible via dedicated keyboard shortcuts and integrated into the **EDIT** menu.

### Core Shortcuts
- **Macro Console:** `CTRL + ALT + M` 
    - Opens the full management interface. 
    - Used to define new macros, delete existing ones, or switch/add new **Contexts**.
- **Fast Macro Paste:** `CTRL + M`
    - Opens a "sticky" picker list of the last 8 macros in the current context.
    - The menu remains open after pasting, allowing you to sequence multiple macros quickly.
    - Press **Enter** to paste, **Esc** to return to the editor.
- **Paste Last Macro:** `CTRL + SHIFT + M`
    - Instantly inserts the most recently used macro at the cursor without opening any menus.

## Macro Contexts

Macros are organized into **Contexts**, allowing you to maintain separate libraries for different tasks. DOSwriter includes three standard contexts:

1. **TEXT (Default)**: General-purpose strings and phrases.
2. **MARKDOWN**: Prepopulated with common formatting directives:
    - Headers (`# `, `## `, `### `)
    - Bold/Italic (`**BOLD**`, `*ITALIC*`)
    - Lists and Rules (`> `, `---`)
    - Links/Images (`![Alt](path)`)
    - *Auto-activates when editing `.md` files.*
3. **CODE**: Prepopulated with programming syntax:
    - Brackets and Braces (`{ }`, `( )`, `[ ]`)
    - Control structures (`if () { }`, `for () { }`)

### Custom Contexts
Users can create their own named contexts (e.g., "SCREENPLAY", "REPORTS") within the Macro Console (`CTRL + ALT + M`) to further organize their snippet libraries.

## Functionality and Limits

- **Storage**: Macros are persistent across app restarts and saved independently of individual buffers.
- **Capacity**: Each context stores up to **8 active macros** in a FIFO (First-In, First-Out) list.
- **Sequence Pasting**: In the `CTRL + M` picker, the selection bar remains at the top after a paste, making it easy to build complex structures (like nested Markdown) with minimal keystrokes.
- **Conflict Resolution**: If the user types in the console field, the typed text takes priority over the list selection for immediate insertion.

## UI Customization
The Macro Overlay respects the app's global theme settings. In **E-Ink Mode** (light background), the overlay uses high-contrast colors and outlines to ensure visibility. Menus can be navigated using standard arrow keys or by selecting the index number associated with each macro.
