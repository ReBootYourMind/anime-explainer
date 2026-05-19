# nanDECK HTMLTEXT Layout Guide

## Purpose
This guide documents the current SANA row text layout in this project, using only behaviors shown in nanDECK Tips & Tricks and nanDECK web changelog examples.

## Source-backed rules

1. Alignment split across directives (Tips & Tricks):
   - For HTMLTEXT, horizontal alignment is in HTMLFONT (6th parameter).
   - Vertical alignment is in HTMLMARGINS (6th parameter).

2. HTMLMARGINS can add spacing inside the HTMLTEXT rectangle (Tips & Tricks):
   - Use margins instead of shrinking the box when you want internal padding.
   - Keep vertical alignment as CENTER when you still want balanced text.

3. HTMLFONT can use shadow settings (Tips & Tricks examples):
   - Example lines show text shadow by setting shadow size and shadow color.
   - White shadow can be used instead of outline/border.

4. HTMLTEXT supports normal HTML and paragraph rendering options (Tips & Tricks + changelog):
   - This confirms we can structure text behavior without switching away from HTMLTEXT.

## Implemented pattern in this project

### 1) Lower-centered text with top padding
The row fonts use CENTER vertical alignment and non-zero margins so text sits slightly lower, leaving more air above the text.

```nandeck
HTMLMARGINS=word_font,3%,3%,0,0,CENTER
HTMLMARGINS=word_num_font,3%,3%,0,0,CENTER
```

### 2) Wrapped second line indentation
Instead of writing `1. [SANA1]` in one HTMLTEXT block, each row is split into two side-by-side HTMLTEXT blocks:

- Left narrow block: the row number (`1.` ... `6.`)
- Right wide block: the title text (`[SANA1]` ... `[SANA6]`)

Because the title is in its own right-hand block, wrapped lines naturally continue in the same indented column.

```nandeck
HTMLTEXT=,"1.",10%,{600/28}%,6%,{300/28}%,#FFFFFF,0,BE,100,word_num_font
HTMLTEXT=,"[SANA1]",16%,{600/28}%,79%,{300/28}%,#FFFFFF,0,BE,100,word_font
```

### 3) White shadow instead of border
The word fonts use white shadow parameters and no explicit outline width.

```nandeck
HTMLFONT=word_font,Arial,11.5,B,#000000,LEFT,0,0,0.12,#FFFFFF
HTMLFONT=word_num_font,Arial,11.5,B,#000000,RIGHT,0,0,0.12,#FFFFFF
```

## Why this is robust

- Works entirely with HTMLFONT, HTMLMARGINS, and HTMLTEXT behavior documented in tips/changelog.
- Keeps numbering stable and readable.
- Keeps wrapped titles visually aligned without manual line breaks.
- Avoids fragile per-title formatting logic.

## Notes for future edits

1. If text looks too low: reduce the first two margins from `3%` to `2%`.
2. If shadow looks too strong: reduce shadow size from `0.12` to `0.08`.
3. If number/title gap is too large/small: tune the number column width (`6%`) and title start (`16%`).

## Sources

- Tips & Tricks attachment in this repository (`tips_and_tricks.md`):
  - HTMLTEXT alignment split (HTMLFONT horizontal, HTMLMARGINS vertical)
  - HTMLMARGINS for internal spacing
  - HTMLFONT shadow/outline examples
- nanDECK changelog pages:
  - https://nandeck.com/archives/339 (HTMLMARGINS and HTMLFONT/HTMLTEXT related examples)
  - https://nandeck.com/archives/262 (extended HTMLMARGINS syntax)
