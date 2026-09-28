# **DOSwriter**


<img align="right" src="images/DOSwriter-Logo.png" width="400">

**A distraction-free, retro-inspired text editor optimized for mobile and E-ink devices.**

**DOSwriter is a minimalist Android writing environment inspired by dedicated writing devices and keyboard-centric workflows such as the Alphasmart Neo and DOS/Unix text editing tools. It is designed [...]

**DOSwriter has good screen control for emulating e-ink displays on backlit devices and has easy ergonomic color settings. It also works on B&W and color Android e-ink displays such as the Boox and th[...]

**Other useful features are bookmarks, text collapse, file visualization tools, Markdown editing, an outline manager for project organization, a remote PC file sync tool, Vietnamese TELEX mode, and a [...]

**Use DOSwriter to capture and organize your thoughts on your Android device for later computer formatting with publishing software.**

<br>

## **Download Android DOSwriter installation APK :**

**DOSwriter is currently distributed as a free APK while the project is under active development.**

[**Download the latest DOSwriter APK**](https://github.com/ElmerWorks/DOSwriter/releases/download/Update092726/DWTEv0.9-092726-app.apk)
<br>
<br>


<p align="center">
  <img src="images/Boox-1200-800-hero.png" alt="Boox-Hero-Shot">
  <br>
  <b>The photo isn't the best. It's difficult to get useful photos of light-emitting devices like the Boox 7.</b>
</p>

<br>
<br>

<p align="center">
  <img src="images/boox7-scrshots-1.png" alt="Boox-ScrShots">
  <br>
  <b>Screenshots of DOSwriter on Boox 7 Color. Text example is from Frankenstein by Mary Shelley.</b>
</p>

<br>
<br>

<p align="center">
  <img src="images/Moto-scrshots4.png" alt="Moto-G-ScrShots">
  <br>
  <b>Screenshots from Moto G Power (circa 2023). DOSwriter looks good on this device.</b>
</p>

<br>
<br>

# Contents

- [Motivation](#motivation)
- [Core Concepts](#core-concepts)
- [Key Features](#key-features)
- [Getting Started](#getting-started)
- [Documentation](#documentation)

## Motivation
DOSwriter is designed for writers who want the simplicity of old-school word processors combined with the power of small Android devices. It features a unique multi-buffer system, keyboard-first navig[...]

There is a wide selection of compact, lightweight Bluetooth keyboards, and even heavier mechanical or ergonomic keyboards. Android devices are cheap and ubiquitous. This is an easy combination for a w[...]

Desktop and laptop tools are great for formatting and publishing, but that limits your mobility. Writing is more enjoyable away from the machines.

So I wrote DOSwriter. The irony is I spent 3 months hunched over my computer to create it so I would not be hunched over the computer. 

And I could have worked with some of the many fine editors and writing tools available for Android. I tried several out but they just didn't click with me, through no fault of the software. Thus 3 mon[...]

I think many editor developers wind up on the same path. They try out editors and nothing works so they write their own editor.

DOSwriter is a capture of my writing mental model. I wrote professionally for many years so have some background for attempting such an audacious project. Before writing your own editor (and that is v[...]

But if you are a fool and insist on developing your own tools, text processing and human interfacing is a fascinating topic of study and you will be richly rewarded for the effort. Nobody will care ab[...]

If this discussion interests you, I describe the DOSwriter design inspiration and use case on the [DOSwriter website.](https://doswriter.com/usecase/DOSwriterUseCase "DOSwriter Design Inspiration")

## Core Concepts
DOSwriter is built around simple ideas : A small screen shouldn't force you to think about your writing in a small way, and the device human interface should not pull you out of the mental writing mod[...]

The editor is designed around the way writers actually work: capture text, move between sections, organize a growing manuscript, review the larger structure, work with reference materials, and eventua[...]

Rather than adding conventional desktop-style controls to a small Android screen, DOSwriter uses a keyboard-first workflow built around Text Buffers, Workspaces, and Navigation/Document Visualization [...]

- [1. Visual Aesthetics and Ergonomic Writing Setup](#1-visual-aesthetics-and-ergonomic-writing-setup)
- [2. Buffers and The Working Text View](#2-buffers-and-the-working-text-view)
- [3. Workspaces and The Multi-Buffer Layout View](#3-workspaces-and-the-multi-buffer-layout-view)
- [4. The Writing Environment Stay in the Flow](#4-the-writing-environment-stay-in-the-flow)
- [5. Navigating Large Files on Small Screens Bookmarks and Text Collapse](#5-navigating-large-files-on-small-screens-bookmarks-and-text-collapse)
- [6. Visualizing Document Structure Filmstrip and Layout Views](#6-visualizing-document-structure-filmstrip-and-layout-views)
- [7. Split-Screen Editing and Image Slideshow](#7-split-screen-editing-and-image-slideshow)
- [8. Using Images and Reference Materials](#8-using-images-and-reference-materials)
- [9. Managing Writing Projects](#9-managing-writing-projects)
- [10. Markdown Editing with Live Preview](#10-markdown-editing-with-live-preview)
- [11. Review and Publication](#11-review-and-publication)
- [12. Desktop File Syncing and Cloud Sharing](#12-desktop-file-syncing-and-cloud-sharing)
- [13. Built-In Hipster PDA](#13-built-in-hipster-pda)
- [14. Intuitive Commands and Integrated Help](#14-intuitive-commands-and-integrated-help)
- [15. Virtual Keyboard](#15-virtual-keyboard)
- [16. Buffer and File Autosave](#16-buffer-and-file-autosave)



### 1. Visual Aesthetics and Ergonomic Writing Setup

DOSwriter creates a focused writing environment blending retro aesthetics with modern ergonomic controls. The typographic system replaces traditional point sizes with "Characters Per Line" (CPL) prese[...]

This setup is housed within a high-contrast, theme-aware viewport where users can fine-tune side margins and vertical offsets to create a perfectly balanced writing stage. An ergonomic feature is the [...]

DOSwriter provides instant typographic control through dedicated hardware hotkeys, allowing writers to increase or decrease font size on the fly without breaking their creative flow. The engine suppor[...]

Designed for use in any environment, DOSwriter features a robust theme engine optimized for ambient lighting comfort. Users can transition between high-contrast light modes for outdoor use and muted, [...]

<br>

[![Fonts Demo](https://img.youtube.com/vi/qcl8oykMreY/hqdefault.jpg)](https://youtu.be/5mE69HamK3I)

<p align="left">
  <b>Click for Fonts Demo Youtube video </b>
</p>

<br>

[![Color Themes Demo](https://img.youtube.com/vi/qcl8oykMreY/hqdefault.jpg)](https://youtu.be/EG3Rp9HvyRI)

<p align="left">
  <b>Click for Color Themes Demo Youtube video </b>
</p>

<br>

[![Viewport Margins Demo](https://img.youtube.com/vi/qcl8oykMreY/hqdefault.jpg)](https://youtu.be/xRQzJGRLHaM)

<p align="left">
  <b>Click for Viewport Margins Demo Youtube video </b>
</p>





### 2. Buffers and The Working Text View
At the heart of the application is the keyboard-oriented Working Buffer—a single-instance text view designed for speed and stability. DOSwriter buffers are built to handle large text files without l[...]

Buffers are intuitive for working with text. There are 8 buffers corresponding to keyboard F1-F8 keys. Think of the them as a stack of notepads. The 8 DOSwriter buffers map conveniently to keyboard F [...]

The F1-F8 key paradigm adapts well to modern Bluetooth keyboards. Not all keyboards have F keys available so DOSwriter also uses ALT+1-9 keys to swap buffers. 

![FKey-Buffers](images/keyboardF-buffers.png)


### 3. Workspaces and The Multi-Buffer Layout View

The 8 buffer concept works well for file visualization on small devices. DOSwriter has fast buffer layout and preview commands.

The buffer list can be viewed with ALT-B.  Use arrow keys, buffer number, or F keys to select.

 I borrowed an idea from MS Word where you can zoom out and see all your pages in a layout. In DOSwriter all 8 buffers can be viewed at once and selected in Buffer Layout View by pressing `[Esc]` key [...]

Workspaces keep related buffers together. Use one for a writing project, another for notes, and another for your ToDo list.
A Workspace contains eight active writing buffers that can be viewed together as a visual layout.

Press `[Esc]` while editing to step back from the text and see the entire Workspace. Each buffer can display text, an image, a file preview, or an image with a text overlay. Buffers can be selected wi[...]

Think of it as a digital corkboard for your writing. Instead of hunting through folders or tabs, your active work is always visible and one keystroke away. This makes the Workspace more than a collect[...]

<p align="center">
  <img src="images/tab-buffer-layout-1.png" alt="Lenovo-Tab">
  <br>
  <b>Screenshots from Lenovo Tab One showing default Buffer Layout images, text Preview, and Text Overlay.</b>
</p>

<p align="center">
  <img src="images/tab-buffer-layout-2.png" alt="Lenovo-Tab">
  <br>
  <b>The Layout View thumbnails can be changed with any image. 512x512 px is optimal.</b>
</p>



<br>

[![Buffer Layout View Demo](https://img.youtube.com/vi/qcl8oykMreY/hqdefault.jpg)](https://youtu.be/o8U3ulJxO6g)

<p align="left">
  <b>Click for Buffer Layout View Youtube video </b>
</p>

### 4. The Writing Environment Stay in the Flow

DOSwriter tries to keep routine computer operations from becoming interruptions to writing which helps manage work without leaving the writing environment.

The integrated File Browser provides keyboard-driven access to files and folders without sending the writer into Android's gesture-oriented file picker. You link the root working directory for the File [...]

The File Browser also has a minimalist design, presenting only the information you need without screen clutter. As you navigate the files, a preview window displays the image or first page of text, PD[...]

Arrow keys and Enter navigate the file system, while DOSwriter remembers the working directory for each Workspace. Text and image files can also be previewed within the application.

<br>

[![File Manager Video](https://img.youtube.com/vi/qcl8oykMreY/hqdefault.jpg)](https://youtu.be/D0zveg0oLVA)

<p align="left">
  <b>Click for DOSwriter File Manager Youtube video </b>
</p>

### 5. Navigating Large Files on Small Screens Bookmarks and Text Collapse

Small screens create a particular writing problem: you can concentrate on the current sentence or paragraph, but it is difficult to maintain awareness of a large document. DOSwriter provides tools to [...]

#### 6. Bookmarks
Bookmarks let you mark important locations in a document and return to them instantly. A high-contrast `[BK]` marker and dimmed contextual preview remain visible in the margin, while the Bookmark Menu[...]
<br>

[![Bookmarks Video](https://img.youtube.com/vi/qcl8oykMreY/hqdefault.jpg)](https://youtu.be/fKfPv9h6nj4)

<p align="left">
  <b>Click for DOSwriter Bookmarks Youtube video </b>
</p>


#### 7. Text Collapse
Collapse lets you temporarily hide material that you don't need to see while working—research notes, older drafts, completed sections, or other non-essential material. Blocks can be collapsed manual[...]

Focus on the paragraph you're writing without losing the structure around it.
<br>

[![Text Collapse Video](https://img.youtube.com/vi/qcl8oykMreY/hqdefault.jpg)](https://youtu.be/DM0lRnmyOHo)

<p align="left">
  <b>Click for DOSwriter Text Collapse Youtube video </b>
</p>

### 6. Visualizing Document Structure Filmstrip and Layout Views
Scrolling through thousands of words on a small device gives you only a tiny window into the document. DOSwriter's Layout and Filmstrip Viewer provide a different way to navigate: reduce the document [...]

The idea came from the same visual principle used by a filmstrip or photographic proof sheet: you can recognize the structure of a large work without reading every word. The DOSwriter analog uses an a[...]


#### Layout View
Displays the document as a grid of miniature pages. Scan the grid, select a page, and return directly to that location in the text.

#### Filmstrip View
This displays the document as a sequence of paragraph-sized views. Configure the amount of text shown and scan rapidly through a long manuscript. Select a section and return directly to that location [...]

Filmstrip View is a magnifier for the structure of a document. Both views can also be compiled to PDF, turning the same navigation tools into a way to create condensed reference or proof documents.

<br>

[![Manuscript Viewer Video](https://img.youtube.com/vi/qcl8oykMreY/hqdefault.jpg)](https://youtu.be/lOnAiGzctzE)

<p align="left">
  <b>Click for DOSwriter Manuscript Viewer Youtube video </b>
</p>




### 7. Split-Screen Editing and Image Slideshow 

Split-Screen Mode allows you to view and edit two buffers simultaneously. This is useful for comparing different chapters of a manuscript, taking notes from a PDF reference, or live-previewing Markdow[...]

<br>

[![Splitscreen Mode Video](https://img.youtube.com/vi/qcl8oykMreY/hqdefault.jpg)](https://youtu.be/l2l2WoLNTok)

<p align="left">
  <b>Click for DOSwriter Split-Screen Mode Youtube video </b>
</p>



### 8. Using Images and Reference Materials

Research, photographs, illustrations, diagrams, and other visual references can be part of the writing process. DOSwriter includes an integrated Image Viewer that can display images full-screen, move [...]

Markdown images can participate in the same workflow, and DOSwriter can use Markdown presentation mode to turn content into a sequence of rendered slides.

PDF documents can be navigated directly from the keyboard, with page navigation, and zoom. Favorites (bookmarks) can be added to the PDF view and exported to a text file.

Reference material can remain part of the Workspace instead of becoming another application to manage. When linked in the Outline Manager they become part of an organized project strcuture.


### 9. Managing Writing Projects
The Outline Manager acts as a hierarchical project hub, enabling you to organize cmanuscripts into custom containers, chapters, and nested folders. By linking individual external files into a cohesive[...]

### 10. Markdown Editing with Live Preview
DOSwriter supports Markdown editing, Useful for structured formatting without leaving the app. The editor highlights syntax in real-time, while the Live Preview mode (`ALT+R`) renders headers, tables,[...]

### 11. Review & Publication
DOSwriter has basic PDF publishing for buffers and manuscript views. This allows a writer to move between: Write → Navigate → Review → Revise → Publish without abandoning the keyboard-centered[...]

### 12. Desktop File Syncing and Cloud Sharing
#### Desktop Sync
DOSwriter connects mobile drafting and desktop finishing through a streamlined, local-network sync server. You can wirelessly transmit  active buffers to companion desktop applications such as Notepad[...]

I implemented the desktop sync server in the Go language, which works on Linux and Windows, and possibly Apple (did not try it). I have not used the sync tool much but when I have I am surprised how w[...]

#### Android App Sharing
The app integrates with the Android system provider, allowing for the direct opening and saving of documents to cloud services like Google Drive, OneDrive, or Dropbox without manual file transfers. I [...]

### 13. Built-In Hipster PDA
DOSwriter has a secondary 8-buffer Workspace that can be used for personal task management as described in this [DOSwriter link.](https://doswriter.com/instructions/DOSwriterPDA "DOSwriter PDA")

### 14. Intuitive Commands and Integrated Help
Reflecting its keyboard-centric philosophy, DOSwriter minimizes menu-diving through a comprehensive system of intuitive `CTRL` and `ALT` command chords. For users needing a quick reference, the Integr[...]

### 15. Virtual Keyboard
For devices without physical hardware, the DOSwriter Virtual Keyboard offers a tailored input experience optimized for retro writing. Beyond standard alpha-numeric keys, it includes specialized layout[...]

<p align="center">
  <img src="images/VirtualKeyboard.png" alt="Virtua-Keyboard">
  <br>
  <b>When a keyboard is not connected, DOSwriter has a dedicated 3-screen Virtual Keyboard. Key functions are described in ALT-H>Virtual Keyboard Map</b>
</p>

<br>
<br>

### 16. Buffer and File Autosave
DOSwriter employs a tiered data protection strategy to ensure that your writing is never lost, ranging from automatic session persistence to manual file exports and remote synchronization.

**1. Internal Session Persistence (Auto-Save)**
- **How it works**: Every time you switch buffers, minimize the app, or even when the device screen turns off, DOSwriter instantly saves the exact state of all 17 buffers (8 Main, 8 To-Do, 1 Scratchpa[...]
- **Recovery**: If the app crashes or your battery dies, your text will be exactly where you left it when you restart the app. You do **not** need to manually save to a file to preserve your work betw[...]
- **Visual Indicator**: An asterisk (`*`) appears next to the filename in the status bar if the current buffer has unsaved changes (relative to the last exported file).

**2. Accidental Deletion Recovery (Undo & Confirmation)**
If you accidentally clear a buffer or delete a large block of text:
- **Shortcut**: `CTRL + Z` (Undo) supports up to **100 steps** of history.
- **Unsaved Changes Confirmation**: If you attempt to close a buffer (`CTRL + W`) that contains unsaved changes, DOSwriter will now display a confirmation prompt asking if you want to **Save & Close**[...]
- **Accidental Close**: When you confirm a wipe, the entire content is pushed onto the Undo stack. If you still realize you made a mistake, pressing `CTRL + Z` will instantly restore your work.

--- 



## Key Features
- **Distraction-Free Editing**: The default visual mode is fullscreen with no icon clutter or Android distractions. 
- **Text-Only**: DOSwriter uses Unicode text fonts which are portable between all writing applications and operating systems.
- **Multi-Buffer Workspace**: Instant hotkey access to 8 active documents. 
- **Instant Workspace Viewing**   Use `Esc` to view a visual layout of all buffers with persistent thumbnails.
- **Scratchpad**: A dedicated 9th buffer for quick notes with auto-flushing to a permanent log file.
- **Visual Aesthetics**: Hotkey adjustable ergonomic color themes, fonts, margins, screen brightness.
- **Splitscreen Mode**: Splitscreen view and editing of multiple buffers or images.
- **Text Processing**: Macros, Bookmarks, and Text Collapse
- **Writing Visualization**: Tools for working with large text files on small devices.
- **Typewriter Mode**: Typewriter editing and scrolling with demo mode.
- **File Manager**: Keyboard-centric File Browser and file operations centered on your working folders.
- **Outline Manager**: Link work files in project trees with preview selection.
- **Markdown & PDF Support**: Full Markdown rendering (including tables) and PDF compilation.
- **Desktop Sync**: Real-time synchronization with a desktop host via network socket for seamless "mobile-to-PC" workflows.
- **E-Ink Optimized**: High-contrast UI elements, custom `[+]` Fold and `[BK]` Bookmark icons, and integrated hardware drivers for Onyx/Boox and Supernote.
- **Scripting Engine**: Automate repetitive tasks or create custom presentation modes with a built-in command script language.

# Getting Started
1. **Installation**: Deploy the APK to your Android device (Min SDK 23).
2. **Permissions**: Grant storage permissions to enable file opening and saving.
3. **Linking Folders**: Go to `ALT-S (SETTINGS) > File Manager` to link your primary writing folder.
4. **Learn the Keys**: DOSwriter is built for hardware keyboards but includes a powerful virtual layout. Press `ALT-H` anytime for the help system.

## App Operation

### App Integration & Workflow
- **Direct Entry**: Launches immediately into a keyboard-focused file editor. No splash screen delays (Help popups can be turned off in Settings).
- **Hotkeys**: Standardized shortcuts for all operations. Use `CTRL-ALT-X` to exit or `ALT-X` to quickly minimize the app.
- **Sharing**: Integrated Android sharing system allows you to send buffer content to other apps instantly.

### The Multi-Buffer Paradigm
- **Leverages Keyboard Layouts**: Uses `F1-F8` or `Alt1-Alt8` like a stack of notepads for instant access.
- **8+1 System**: Work on 8 standard documents plus a dedicated 9th **Scratchpad** `F9`.
- **Buffer Layout (`Esc`)**: A bird's-eye view of your entire workspace with persistent thumbnails and live file info. Supports finger-tap selection.
- **Split-Screen**: View two buffers at once (Vertical or Horizontal) or compare two sections of the same file.
- **Buffer Status**: `CTRL-H` hides or shows current buffer filename and details .

### Text Navigation
- **Keyboard Centric**: Designed for hardware keyboards with standard and power-user shortcuts.
- **Precision Movement**: 
  - **Arrows**: Character and visual line movement.
  - **CTRL + Arrows**: Word and paragraph jumps for rapid traversal.
  - **ALT + Arrows**: Sentence jumps or jumping to visual line start/end.
- **Selection**: Hold `SHIFT` with any navigation key to select text blocks. Supports system-wide and internal clipboard management.

### Multiple Workspaces
- **Default Mode**: Your primary environment for creative writing.
- **To-Do Mode**: Switch to a dedicated 8-buffer workspace via `ALT-W` designed for task tracking and project management.

### Viewport & Typography Control
- **Precision Font Control**: Adjust font size with `CTRL-` and `CTRL+`, and line height with `CTRL-L`
- **Margins**: Set custom side and top/bottom margins to create the perfect writing focus area.
- **Vertical Offset**: Shift the entire text block vertically to center your work on your device's unique screen or case.

### Visual Themes & Brightness
- **E-Ink Specific Color Themes**: High-contrast modes like "Classic", "E-Ink", and "CRT" designed for maximum legibility.
- **Day/Night Mode**: Automatic theme switching based on your local time.
- **Brightness Control**: Adjust system brightness directly from the app using `ALT-` and `ALT-+`.
- **Cycle Themes**: Cycle forward and back through available Themes with `CTRL-T` and `CTRL-ALT-T`
- **Display Themes**: Displays current Theme name `CTRL-SHIFT-T`
- **Custom Themes**: Define custom color themes using RGB values in Settings>Theme


### Editing Modes
- **Plain Text**: Efficient editing for standard `.txt` files with full support for power tools like folds and bookmarks.
- **Typewriter Mode**: Keep your focus point centered. Features include "Stationary Cursor" (platen moves) or "Moving Cursor" modes.
- **Markdown Support**: Dedicated rendering engine for `.md` files. Toggle live preview with `ALT-R`.
- **Split-Screen Rendering**: A unique side-by-side workflow. Edit Markdown source in one buffer while the second buffer displays the live rendered output (automatic for `.md` files).

### Publishing
- **PDF Compilation**: Export your work in Standard A4, Manuscript WYSWYG, or a unique 8-in-1 Landscape "Mini-Book" format.
- **Markdown Rendering**: Full live preview of Markdown files including tables and images.

### Text Viewing & Manuscript Management
- **Filmstrip Viewer**: View your document as a series of individual pages for easy proofreading.
- **Layout Grid**: A 4 or 8-page "light table" view to see the flow and structure of your manuscript.

### Cursor & Typewriter Control
- **Custom Styles**: Choose between Block, Thin/Thick Caret, Underline, and Retro styles.
- **Locator**: A special high-speed blink to help you find your cursor in large documents.

### File Management & Supported Types
- **Supported Files**: Seamlessly handles `.txt`, `.md` (Markdown), `.pdf`, `.jpg`, `.png`, and `.gif` files.
- **Dual Browsers**: Toggle between the standard **Android System Browser** and the custom, keyboard-optimized **DOSwriter File Browser**.
- **Images**: Link local folders for background reference images or use the built-in **Slideshow Viewer**.

### Virtual Keyboard
- **Custom Layouts**: Optimized Alpha, Punctuation, and Numeric layers.
- **CTRL Lock**: A virtual "Sticky Key" (`⎈L`) that allows you to perform complex chords and navigation with single taps.
- **Telex Support**: Integrated Vietnamese TELEX input mode.

### Power Tools
- **Outline Manager**: Organize large projects (`CTRL-ALT-O`). Link multiple local or remote files into folder hierarchies with preview.
- **Macros**: Use `CTRL-ALT-M` for the macro console or `CTRL-ALT->>` to define quick snippets.
- **Text Collapse**: Collapse paragraphs with `CTRL-J` to focus on specific sections. Features a high-contrast `[+]` marker with text preview.
- **Scripting Engine**: Automate repetitive tasks or create custom presentation modes with a built-in command script language.

# Documentation
- [Function & Keyboard Map](./docs/DOSwriter-Function-Keyboard-Map.md)
- [Menus & Settings](./docs/DOSwriter-Menus-Settings.md)
- [DOSwriter File Manager](./docs/DOSwriter-File-Manager.md)
- [DOSwriter Buffer&File Autosave](./docs/DOSwriter-Buffer-File-Operations.md)
- [Fonts](./docs/DOSwriter-Fonts.md)
- [Image, Markdown, & PDF](./docs/DOSwriter-ImageMdPDF-Commands.md)
- [Text Tools](./docs/DOSwriter-Text-Tools.md)
- [Text Macros](./docs/DOSwriter-Text-Macros.md)
- [Remote Desktop Sync](./docs/DOSwriter-Remote-Sync.md)
- [Virtual Keyboard](./docs/DOSwriter-Virtual-Keyboard )
- [Vietnamese TELEX](./docs/Vietnamese_TELEX_Test_Guide.md)

---


## License
Copyright © 2026. All rights reserved.

---
[Back to Top](#doswriter)
