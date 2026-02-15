# 🚀 Hold to New Tab🖱️✨

**Version:** 1.0.0
**Author:** AceBurgundy
**Homepage:** [sam-sabalo.vercel.app](https://sam-sabalo.vercel.app)

## 🎯 What is it?

**Hold-to-New-Tab** is a lightweight Firefox browser extension that lets you **open links in a new tab by holding down a click** — no more accidental clicks or unnecessary context menus!

* 🖱️ Long-press a link
* 🔄 Open it beside the current tab (or at the end)
* 🚀 Optionally switch to the new tab instantly

Perfect for **power users**, tab hoarders, and anyone who loves **smooth browsing**.

## ⚙️ Features

* **Long-press detection** ⏱️

  * Customizable delay before opening (default: 200ms)

* **Debounce protection** 🛑

  * Prevents rapid multiple tabs from opening accidentally

* **Flexible tab placement** 🗂️

  * Open beside the current tab or at the end
  * Switch to the new tab automatically if desired

* **Zero data collection** 🔒

  * The extension respects your privacy — no data is collected

* **MV3 ready & Firefox 140+** ✅

  * Fully compatible with modern Firefox (desktop ≥ 140, Android ≥ 142)

## 🖌️ How It Works

1. **Background script** (`background.js`)

   * Manages extension settings
   * Listens for `openTab` messages
   * Opens new tabs according to your preferences

2. **Content script** (`content.js`)

   * Detects long-press on links
   * Handles movement/cancellation
   * Sends messages to the background to open tabs
   * Prevents default click behavior when a hold triggers

3. **Manifest** (`manifest.json`)

   * Defines permissions (`tabs`, `storage`)
   * Registers content scripts and background
   * Declares no data collection

## 🛠️ Installation

1. Download the repository.
2. Open Firefox → **about:debugging** → "This Firefox" → "Load Temporary Add-on…"
3. Select `manifest.json`.
4. Enjoy **hold-to-open** tabs! 🥳

> For permanent installation, submit the extension to [AMO](https://addons.mozilla.org/).

## ⚡ Settings

Settings are stored in browser local storage:

| Setting            | Default | Description                         |
| ------------------ | ------- | ----------------------------------- |
| `extensionEnabled` | `true`  | Toggle the extension on/off         |
| `openBeside`       | `true`  | Open new tab next to current one    |
| `switchOnOpen`     | `true`  | Automatically switch to the new tab |
| `holdDelay`        | `200`   | Time in ms to trigger the hold      |

> ⚙️ Settings automatically persist across browser sessions.

## 🎨 Icons

* `icon-16.png` – Toolbar / menus
* `icon-32.png` – Extension list / popup
* `icon-48.png` – About pages / notifications
* `icon-128.png` – AMO listing

## 🔒 Privacy & Permissions

* Permissions: `tabs`, `storage`
* Host permissions: all `http` & `https` URLs
* **No personal data is collected** (`data_collection_permissions` = `none`)

## 💡 Tips

* Hold a link longer than the **holdDelay** to trigger a new tab.
* Small mouse movements (<6px) are ignored; large movement cancels the hold.
* Works on nearly all `<a>` elements except ones already targeting `_blank`.

## 📝 Contributing

Want to help? 🌟

* Fork the repo
* Add new features or improve UX
* Submit a pull request
* Star ⭐ the project

## 🛡️ License

MIT License — free to use, modify, and share.

## 💬 Contact

* **Author:** AceBurgundy
* **Website:** [https://sam-sabalo.vercel.app](https://sam-sabalo.vercel.app)
* **AMO ID:** `holdtonewtab@samsabalo.dev`

**Enjoy faster tab management!** 🖱️🔥
Happy browsing, and may your tabs always stay organized! 🗂️
