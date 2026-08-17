# DOSwriter File Manager & Browser Guide
**Version:** 1.1 (August 2026)

## Overview
DOSwriter provides a dual-layered approach to file management, designed to balance modern Android "Scoped Storage" requirements with a keyboard-centric, retro workflow. Users can choose between the native **Android System Picker** and the integrated **DOSwriter Browser**.

---

## 1. The Dual-Browser System

### Android System Picker
- **Usage**: Default behavior for most devices.
- **Pros**: Access to cloud services (Google Drive, OneDrive, Dropbox) and a familiar interface.
- **Cons**: Requires touch navigation, heavy system resources, and can cause background "process death" on low-RAM hardware.

### DOSwriter Integrated Browser
- **Usage**: Enabled via `SETTINGS > Advanced Features > Use Workstation Browser`.
- **Pros**: 
  - **Keyboard Optimized**: Fully navigable with arrow keys and Enter.
  - **E-Ink Friendly**: Uses high-contrast UI and avoids heavy animations.
  - **Clutter-Free**: Screen space optimized for text writing and image management.
  - **Retro Simplicity**: No cognitive information beyond your files and folders.
  - **Low Overhead**: Remains within the DOSwriter process, preventing app-restarts.
  - **Persistence**: Remembers your last-used directory per buffer workspace.
  - **Writing Project Orientation**: Define your working folder and the File Browser works from there.
  - **File Preview**: Displays image or text file contents in side panel.
  
  

---

## 2. Integrated Browser Features
- **Sorting**: Toggle between **Name** and **Most Recent** via the settings menu.
- **Filtering**: Automatically hides non-relevant files when performing specific tasks (e.g., only shows images when linking thumbnails).
- **Directory Tree**: Provides a breadcrumb navigation bar and one-key access to "Go Up" a level.
- **Save As Protection**: Built-in overwrite confirmation prompts when saving new files to existing locations.

---

## 3. Device-Specific Issues: Moto G & Low-RAM Hardware

### The Problem
During development on certain devices (specifically the **Moto G** series), a critical Android lifecycle issue was identified. 
1. When a user chooses "Link Thumbnail Image," the device launches the **System File Picker**.
2. Because the System Picker is a separate, resource-intensive application, Android occasionally kills the background **DOSwriter** process to free up RAM.
3. Upon selecting an image, the user is returned to the Android Home Screen or a "restarting" app state, losing the context of the buffer they were trying to update.

### The DOSwriter Solution
To solve this, DOSwriter now implements **Foreground Context Protection**:
- **Internal Picking**: Functions like "Link Thumbnail Image" and "Set Global Image" now prioritize the **DOSwriter Browser** if enabled. By selecting the image inside the same app process, we prevent Android from flagging DOSwriter as an "idle" background task.
- **State Persistence**: The app now persistently saves the `pending_thumbnail_idx` during every transition. Even if the system forces a restart, the app will recover and complete the linking process.

---

## 4. File Actions & Workflows

### Save / Save As
- `CTRL+S`: Quick save to current linked file.
- `CTRL+SHIFT+S`: Open browser to save as a new filename.

### Syncing
- `CTRL+D`: Opens the Sync menu. Files linked via the browser can be synchronized to remote workstations using the built-in sync token system.

### Thumbnail Linking
- Accessible via `ALT+I > Buffer Thumbnails`. 
- Allows linking individual images to each of the 8 buffers.
- Supports **Global Image** mode to use a single "wallpaper" for the entire layout grid.

---

## 5. Best Practices
- **For E-Ink / Low-RAM Devices**: Always enable `Use Workstation Browser` for maximum stability and speed.
- **For Cloud Users**: Use the System Browser for the initial "Open" command to pull files from cloud providers, then switch to the Internal Browser for high-speed local writing and organization.
