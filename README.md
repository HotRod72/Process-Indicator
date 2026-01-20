# Process Indicators

A lightweight Stream Deck plugin that displays a live ON/OFF indicator showing whether a chosen Windows or macOS process is currently running.

---

## ✨ Features

- Shows a live ON / OFF state for any process
- Updates automatically every 2 seconds
- Supports any executable name (e.g. `notepad.exe`, `obs64.exe`, `chrome.exe`)
- Indicator-only button (pressing the key does nothing)
- Uses custom icons for running and not running states
- Designed for Windows and macOS (Windows fully tested)

---

## 🧰 Installation

### Option 1 — Install from .streamDeckPlugin file

1. Download `Process-Indicators.streamDeckPlugin`
2. Double-click the file
3. Stream Deck will install the plugin automatically

---

## 🎮 How to Use

1. Open the Stream Deck application
2. Find **Process Indicators** in the Actions list
3. Drag **Process Indicator** onto a key
4. In the Property Inspector, enter the process name

Examples:

```
notepad.exe
obs64.exe
chrome.exe
vlc.exe
```

The key will automatically switch:

- OFF → when the process is not running
- ON → when the process is running

---

## ⚠️ Notes About Process Names

- On Windows, the process name must match the executable filename
  - Example: `obs64.exe`, `notepad.exe`
- On macOS, use the process name as shown in Activity Monitor
  - Example: `Safari`, `Google Chrome`

---

## 🛠 Technical Notes (SDK Limitation)

This plugin runs with Node debug mode enabled due to a known limitation in the Elgato Stream Deck SDK v3.

When debug mode is disabled, plugins that use `child_process` and background polling may lose IPC messages, causing state updates to stop reaching the Stream Deck UI.

Keeping debug mode enabled ensures stable and correct plugin behavior and does not affect performance, security, or user experience.

---

## 🧩 Compatibility

- Stream Deck Software: 6.9 or later
- Windows: 10 or later
- macOS: 12 or later

---

## 🧑‍💻 Author

HotRods Garage

---

## 📄 License

© 2026 HotRods Garage. All rights reserved.



## 🚀 Version History

### 1.0.0

- Initial public release
- Live process indicator
- Custom ON / OFF icons
- Property Inspector configuration

