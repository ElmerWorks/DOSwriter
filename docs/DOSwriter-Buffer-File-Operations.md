# DOSwriter Buffer & File Operations

DOSwriter employs a tiered data protection strategy to ensure that your writing is never lost, ranging from automatic session persistence to manual file exports and remote synchronization.

## 1. Internal Session Persistence (Auto-Save)

The most important "auto-save" feature in DOSwriter is the **Session Persistence Engine**.

- **How it works**: Every time you switch buffers, minimize the app, or even when the device screen turns off, DOSwriter instantly saves the exact state of all 17 buffers (8 Main, 8 To-Do, 1 Scratchpad) to the app's private storage (`SharedPreferences`).
- **Recovery**: If the app crashes or your battery dies, your text will be exactly where you left it when you restart the app. You do **not** need to manually save to a file to preserve your work between sessions.
- **Visual Indicator**: An asterisk (`*`) appears next to the filename in the status bar if the current buffer has unsaved changes (relative to the last exported file).

## 2. Accidental Deletion Recovery (Undo & Confirmation)

If you accidentally clear a buffer or delete a large block of text:
- **Shortcut**: `CTRL + Z` (Undo) supports up to **100 steps** of history.
- **Unsaved Changes Confirmation**: If you attempt to close a buffer (`CTRL + W`) that contains unsaved changes, DOSwriter will now display a confirmation prompt asking if you want to **Save & Close**, **Close Anyway**, or **Cancel**. This prevents the accidental loss of work that hasn't been exported to a file yet.
- **Accidental Close**: When you confirm a wipe, the entire content is pushed onto the Undo stack. If you still realize you made a mistake, pressing `CTRL + Z` will instantly restore your work.

## 3. Remote Sync Auto-Push (ElmerSync)

For users utilizing the **Remote File Sync** feature (`CTRL + D`):
- **Auto-Push**: When enabled, the app will automatically upload your changes to the linked host computer at a defined interval (1 to 30 minutes).
- This provides an external backup of your work-in-progress without any manual intervention.

## 4. Manual File Operations (`ALT + F`)

While the app handles session data automatically, "Saving" in DOSwriter refers to exporting that data to the Android file system or a linked folder.

- **Save (`CTRL + S`)**: Updates the currently linked file.
- **Save As (`CTRL + SHIFT + S`)**: Creates a new file from the buffer content.
- **Close Buffer (`CTRL + W`)**: Wipes the active buffer and clears its link to any external file. *Note: Data is recoverable via Undo if performed immediately.*

---

## Recommended Test Strategy (User Perspective)

To gain confidence in the DOSwriter file system, we recommend the following tests:

1.  **The "Kill Test"**: Type several paragraphs of text, then force-close the app using the Android task switcher. Restart the app. Your text should remain in the buffer.
2.  **The "Undo Recovery"**: Press `CTRL + W` to clear a buffer containing text. Then press `CTRL + Z`. Verify that all text and cursor position are restored.
3.  **The "Linked Save"**: Link a working folder, create a new file via `CTRL + S`, make edits, and then check the file using a different app (like the system File Manager) to ensure the bytes were written correctly.
4.  **The "Mode Swap"**: Switch between Main and To-Do workspaces (`ALT + P`). Verify that both stacks maintain their independent content perfectly.

## Future Improvements for Recovery

To further enhance user safety, we are evaluating the following features:
1.  **Automated Local Backups**: Periodically saving a timestamped `.bak` copy of every buffer to the device's internal "Documents" folder.
2.  **Global Close Warning**: A "Save All?" prompt when exiting the application.
