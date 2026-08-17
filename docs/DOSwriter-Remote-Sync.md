# DOSwriter Remote File Sync

DOSwriter features a powerful, low-latency remote file synchronization system called **ElmerSync**. This system allows you to edit files on your Android device while keeping them perfectly in sync with a desktop or laptop host running the `elmer-syncd` server.

## Access and Configuration

- **Keyboard Shortcut:** `CTRL + D` opens the Desktop Sync manager from anywhere in the editor.
- **Menu Path:** `FILE > Desktop Sync`

### Configuration Options
1. **Connect / Disconnect**: Manually establish or terminate the connection to the host server.
2. **Host IP**: Enter the local network IP address of your desktop/laptop.
3. **Port**: Set the communication port (default: `12345`).
4. **Token**: Enter your security API token for authorized access.
5. **Auto-Push**: Toggle background synchronization. When **ON**, DOSwriter automatically uploads changes to the linked remote file at regular intervals.
6. **Auto-Push Timeout**: Set the interval for background sync (1 to 30 minutes).

## Core Synchronization Functions

### 1. Remote File Browsing
Use **Sync with Remote File** to browse the file system of your host computer. You can open any text-based file (`.txt`, `.md`, `.html`, `.json`, etc.) directly into a DOSwriter buffer.

### 2. Remote Saving
- **Save Buffer to Remote Host**: Link a local buffer to a new path on the remote host.
- **Manual Push Update**: Use this to instantly send your local changes to the server without waiting for the Auto-Push timer.
- **Transfer Local File**: Upload an existing local device file to the remote host.

### 3. Bidirectional Notifications
DOSwriter listens for File System events from the server. If a file you are currently editing is modified on the host computer (e.g., by a desktop editor), DOSwriter will receive an immediate notification, ensuring you are always working on the most recent version of your text.

### 4. Remote Lock Model
To prevent data loss, the system supports a "Single Active Editor" model. If a file is locked by the host or another client, DOSwriter will reflect the lock status, protecting your work from accidental overwrites.

## Visual Indicators
- **[REMOTE] Prefix**: Remote files appear in the Buffer List and Status Bar with a `[REMOTE]` prefix.
- **[S] Indicator**: The Workspace Layout View (`Esc`) shows an `[S]` tag for any buffer that is successfully linked to a remote sync path.

## Technical Foundation
ElmerSync utilizes a hybrid **WebSocket and REST** protocol for maximum reliability. WebSockets provide real-time updates and locking, while REST handles efficient directory listings and initial file loading.
