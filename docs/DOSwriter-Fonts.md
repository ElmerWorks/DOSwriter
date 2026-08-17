# DOSwriter Font System Summary

DOSwriter features a sophisticated typographic engine designed for ergonomic writing and precise text density control, specifically optimized for E-ink and distraction-free mobile editing.

## Font Types and Families

DOSwriter supports a wide range of internal and external font families:

### 1. Internal Standard Fonts
- **Monospace (Default)**, **Courier New**, **Consolas**, **Lucida Console**, **Roboto Mono**
- **Serif**, **Times New Roman**, **Georgia**
- **Sans-serif**, **Arial**, **Helvetica**, **Verdana**, **Trebuchet**, **Noto Sans**

### 2. High-Precision Noto Families
The app includes full weights for professional legibility:
- **Noto Sans Mono**: Light, Regular, Medium, Bold, Black
- **Noto Sans**: Light, Regular, Medium, Bold, Black
- **Noto Serif**: Light, Regular, Medium, Bold, Black

### 3. External/Custom Fonts
Users can link a dedicated folder on their device storage (`ALT + S > Font > Link Custom Font Folder`) to load any `.ttf` or `.otf` files. These appear in the selection menu under the **"--- EXTERNAL FONTS ---"** separator.

---

## Core Font Functions

### 1. Dynamic Typographic Presets (CPL Engine)
Instead of fixed point sizes, DOSwriter uses a **Characters Per Line (CPL)** system. When a preset is selected, the app performs a **binary search** to find the exact font size that fits the target character count within your current margins and device orientation.

- **Pocket**: ~45 Characters Per Line (Ideal for phones)
- **Compact**: ~60 Characters Per Line
- **Standard**: ~75 Characters Per Line (The classic "Manuscript" feel)
- **Comfortable**: ~90 Characters Per Line
- **Manuscript**: ~100 Characters Per Line

### 2. Hardware Density Profiles
Font rendering is automatically adjusted based on the active **Hardware Profile**:
- **Phone**: 1.0x baseline density.
- **Tablet**: 1.2x modifier (Compensates for typical viewing distance).
- **Custom / E-Ink**: 1.1x modifier (Optimized for high-contrast e-paper displays).

### 3. Line Spacing (Leading)
Four precise vertical spacing options are available to reduce eye strain:
- **Tight (1.0)**
- **Standard (1.2)**
- **Comfortable (1.5)**
- **Double (2.0)**

---

## Menus and Shortcuts

### Font Menus (`ALT + S > Font`)
- **Font Selection**: Visual picker showing all available internal and external typefaces.
- **Line Height**: Quick selection for leading/spacing.
- **Font Presets**: List of the 5 CPL-based density targets.
- **Bold Toggle**: Switch the entire buffer to a high-visibility bold weight.
- **Apply Fonts Globally**: Sync current font settings across all 16 buffers.

### Keyboard Shortcuts
- **Cycle Fonts**: `CTRL + ALT + B` cycles forward through all available typefaces with a status bar notification.
- **Font Presets**: `CTRL + ALT + =` (Equals) cycles through the CPL presets.
- **Adjust Size**: `CTRL +` (Plus) to increase size / `CTRL -` (Minus) to decrease size.
- **Bold Toggle**: `CTRL + B`
- **Cycle Line Height**: `CTRL + L`
- **Show Active Font**: `CTRL + SHIFT + F` forces a status message displaying the current typeface name.

---

## Technical Performance
Typographic metrics are calculated using `TextPaint` measurements. For Monospace fonts, DOSwriter uses an optimized single-character width; for proportional fonts, it utilizes a weighted average of the Latin alphabet to ensure CPL targets are met with high accuracy across all font families.
