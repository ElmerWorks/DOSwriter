# DOSwriter Virtual Keyboard

DOSwriter features a built-in virtual keyboard optimized for high-speed writing and distraction-free editing on devices without a physical hardware keyboard.

## Access and Toggling

- **Keyboard Shortcut:** `ALT + K` toggles the on-screen keyboard visibility.
- **Automatic Detection:** The keyboard automatically activates when no hardware keyboard is detected and hides when one is connected.
- **Support for CTRL Lock (⎈L):** Allows for sustained control key actions even on a touch interface.

## Layered Design

The keyboard is organized into three specialized layers to maximize efficiency:
1. **Alpha Layer (ABC):** Standard alphanumeric layout for primary text entry.
2. **Punctuation Layer (Punc):** Contains special characters, symbols, and standard editing hotkeys.
3. **Numeric Layer (Num):** Features a dedicated numeric keypad along with advanced toggles like Predictive Text and ToDo Mode.

## Core Functions and Special Keys

- **Predictive Text:** Integrates with a dedicated predictive console to suggest words based on typing context.
- **One-Touch Navigation:** Dedicated keys for jumping by word, sentence, or paragraph.
- **App Integration:** Instant access keys for:
    - **Share:** Send buffer content to other Android applications.
    - **Macros:** Trigger the text macro system.
    - **Outline:** Open the project Outline Manager.
    - **Settings:** Quick jump to app configuration.
    - **ToDo Mode (TD):** Instant swap to the ToDo workspace.

## Configuration and Customization

Settings are managed via `ALT + S > Advanced Features > Virtual Keyboard`.

### Appearance and Layout
- **KB Background:** Choose between using the **Theme Background** or **Theme Font** color for the keyboard keys.
- **Keyboard Outline:** Toggle high-contrast outlines for keys, improving visibility on E-ink devices.
- **Show Numeric Row:** Toggle the optional number row above the Alpha layout.
- **Adjustable Height:** The keyboard height can be manually adjusted and saved to match device dimensions.

### Management
- **Save Keyboard Size:** Persist the current height setting for the active buffer.
- **Save/Load Config:** Save custom keyboard configurations (layout, size, and style) under named profiles (e.g., "Phone", "Tablet", "E-Ink").
- **Apply Settings Globally:** Instantly sync virtual keyboard preferences across all 16 buffers.

## Technical Optimization
The virtual keyboard uses a vector-based rendering engine that respects the active buffer's color theme, ensuring visual consistency. It is specifically designed to minimize screen "ghosting" on E-ink hardware by using high-contrast transitions.
