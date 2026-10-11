# Windows 12 Clone

**Date:** 11 October 2026 | **Time:** 19:42

A web simulation of a Windows 12-style operating system, built as a single self-contained HTML page. It runs in any modern browser with no installation, no server, and no external libraries.

## How it was made

Idea and request: **Saša Jovanović**
Built by: **Claude** (Anthropic), model Claude Opus 5.5

The whole project came from a single prompt, written in Serbian:

> ok sad kreiraj windows 12 klon i da ne pada i nema greske

*(English: "ok, now create a Windows 12 clone, and make it not crash and have no errors")*

From that, Claude designed the look, wrote all the code (about 1,600 lines of HTML, CSS, and JavaScript), tested it, and published it. There were no further instructions, sketches, or manual fixes. The interface was later translated to English at Saša's request.

## Running it

Open `windows12_en.html` in a browser (Chrome, Edge, Firefox, or Safari). That's all.

## Features

**Desktop**
- Floating taskbar in the center (or on the left, if you prefer), with indicators for running apps
- Top bar with weather and search
- Desktop icons and a right-click menu
- Screens for boot, lock, sleep, shut down, and restart

**Window management**
- Drag, resize from any edge, minimize, maximize
- Snap layouts: drag a window to the top edge for full screen, or to the left or right edge for half the screen
- Double-click the title bar to maximize
- On small screens, windows open full screen automatically

**Start menu**
- Pinned apps and recommended (recent) files
- Search across apps and files, tolerant of accented characters

**Apps**
- **File Explorer:** navigation, back/forward history, new folder and file, rename (F2), delete to Recycle Bin (Del), restore from the Recycle Bin, empty the Recycle Bin
- **Notepad:** open, save (Ctrl+S), Save as, word wrap, zoom, insert date and time (F5), warning about unsaved changes
- **Calculator:** basic operations, percent, square, square root, 1/x, keyboard input, safe division by zero
- **Paint:** pencil, eraser, line, rectangle, ellipse, fill bucket, 16 colors, brush size, undo, save image to the Pictures folder
- **Terminal:** `help`, `dir`, `cd`, `type`, `echo`, `mkdir`, `touch`, `del`, `open`, `start`, `cls`, `date`, `time`, `ver`, `whoami`, `neofetch`, `exit`, with command history on the arrow keys
- **Settings:** dark/light theme, 8 accent colors, 5 backgrounds, taskbar alignment, brightness, volume, night light, Wi-Fi, Bluetooth, airplane mode

**Quick settings and calendar**
- Toggles for Wi-Fi, Bluetooth, airplane mode, night light, dark mode, and battery saver
- Sliders for brightness and volume
- Notifications and a monthly calendar

## Technical notes

- One file, about 104 KB, with no external dependencies
- All icons are hand-written SVG, and the backgrounds are CSS gradients
- The file system lives only in memory, and settings are remembered in the browser (localStorage)
- Every app runs isolated: if one runs into a problem, the rest of the system keeps working
- Dialogs are custom-built and don't use the browser's `alert` or `prompt`

## Testing

Before publishing, the code was checked for syntax errors and then run in a simulated browser (jsdom). The test opened all six apps, ran commands in the terminal, checked the calculator's math (including division by zero, percent, and number formatting), changed the theme, background, and alignment, and used quick settings, the calendar, the right-click menu, File Explorer, and the power menu. Result: **0 errors**.

A simulated browser is not the same as testing in a real browser, so small differences in how things look are possible.

## Limitations

- Files you create disappear when you close or refresh the page
- There is no real internet access and no web browser inside the system
- The weather in the top bar is demo data, not a real forecast

## Legal notice

This is an independent, non-commercial project inspired by the look of Windows. It is not a Microsoft product and is not affiliated with Microsoft. "Windows" is a trademark of Microsoft Corporation.
