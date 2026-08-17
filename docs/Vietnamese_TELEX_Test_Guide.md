# Vietnamese TELEX Testing Guide

This guide provides a list of keyboard sequences and expected results to verify the implementation of Stages 1, 2, and 3 of the Vietnamese TELEX engine.

**Prerequisite:** Go to `Settings > Keyboard Mode` and select **Vietnamese TELEX**.

---

## 1. Stage 1: Base Character Conversions
These sequences convert double letters or "w" combinations into modified Vietnamese characters.

| Type | Sequence | Result | Description |
| :--- | :--- | :--- | :--- |
| **aa** | `aa` | **â** | a + a |
| **aw** | `aw` | **ă** | a + w |
| **ee** | `ee` | **ê** | e + e |
| **oo** | `oo` | **ô** | o + o |
| **ow** | `ow` | **ơ** | o + w |
| **uw** | `uw` | **ư** | u + w |
| **dd** | `dd` | **đ** | d + d |
| **Caps** | `AA` | **Â** | Uppercase support |
| **Title** | `Aw` | **Ă** | Title case support |

---

## 2. Stage 2: Basic Tone Marks
Tone keys are usually typed at the end of a syllable.

| Tone | Key | Example Sequence | Result |
| :--- | :--- | :--- | :--- |
| **Acute** | `s` | `as` | **á** |
| **Grave** | `f` | `af` | **à** |
| **Hook** | `r` | `ar` | **ả** |
| **Tilde** | `x` | `ax` | **ã** |
| **Dot Below** | `j` | `aj` | **ạ** |

---

## 3. Stage 3: Complex Syllable Processing (Primary Vowel Detection)
This stage ensures the tone mark is placed on the *linguistically correct* vowel in a cluster.

| Test Word | Sequence | Result | Note |
| :--- | :--- | :--- | :--- |
| **School** | `truowngf` | **trường** | Tone on `ơ` |
| **Language** | `tieengs` | **tiếng** | Tone on `ê` |
| **Name** | `nguyeenx` | **Nguyễn** | Tone on `ê` |
| **Water** | `tuowis` | **tưới** | Tone on `ơ` |
| **Peace** | `hoaf` | **hòa** | Tone on `o` (Modern style) |
| **Right** | `duwngs` | **đứng** | Combined d+d and tone |

---

## 4. Editing & Navigation Verification
*   **Arrow Keys**: If you type `truow` (trươ) and press the **Left Arrow**, then press `f`, it should insert a literal `f` (not a tone), because moving the cursor resets the TELEX state.
*   **Undo**: Pressing **Ctrl+Z** after typing `aa` (â) should ideally restore the original `aa`. 
*   **Backspace**: Pressing backspace after `aa` -> `â` should delete the entire `â` character.

---

## 5. Sample Paragraph for Verification
Try typing this sentence exactly as shown:
`DOSwriter laf trinhf soạn thảo văn bản tuyệt vời.`

**Expected Result:**
`DOSwriter là trình soạn thảo văn bản tuyệt vời.`
