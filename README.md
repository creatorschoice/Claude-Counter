# Claude Counter — Browser Extension

**A lightweight browser extension for tracking token usage, conversation cache time, and Claude AI usage limits.**

Developed and maintained in the `creatorschoice` GitHub workspace.

## 🚀 Overview

Claude Counter enhances your experience on [Claude.ai](https://claude.ai/) by displaying useful conversation statistics and usage information directly in the browser.

The extension helps users understand conversation context usage, monitor cache time, and track session and weekly usage limits.

## ✨ Features

- **Token Counter** — Estimates the token count of the current conversation and displays progress against a 200K context limit.
- **Cache Timer** — Displays a countdown for the conversation cache window.
- **Session Usage Tracker** — Monitors session usage over a 5-hour period.
- **Weekly Usage Tracker** — Displays usage over a 7-day period.
- **Usage Progress Bars** — Visual indicators for session and weekly utilization.
- **Reset Countdown** — Shows when usage limits are expected to reset, based on available usage data.
- **Lightweight Design** — Integrates directly into the Claude.ai interface.
- **Local Processing** — Designed to operate without external tracking servers.

## 🛠️ Technology Stack

- JavaScript
- Chrome Extension Manifest V3
- Browser Content Scripts
- DOM Integration
- Server-Sent Events (SSE) data handling
- Tokenizer integration

## 📦 Installation

### Install on Chrome, Edge, or Chromium-based browsers

1. Download or clone this repository.
2. Extract the project files if downloaded as a ZIP archive.
3. Open `chrome://extensions/` in your browser.
4. Enable **Developer mode**.
5. Click **Load unpacked**.
6. Select the extracted project folder containing `manifest.json`.
7. Open or refresh [Claude.ai](https://claude.ai/) to use the extension.

### Install on Firefox

The extension manifest includes Firefox-specific configuration. Compatibility depends on the Firefox version and packaging method. For local testing, open `about:debugging`, select **This Firefox**, and use **Load Temporary Add-on** to load the extension's `manifest.json`.

## ⚙️ How It Works

1. Integrates with the Claude.ai page using browser content scripts.
2. Estimates conversation token usage using the bundled tokenizer.
3. Reads available Claude usage information to display session and weekly utilization.
4. Uses available conversation and usage events to update the interface.
5. Observes page changes to keep the displayed information updated.

**Note:** Token counts are estimates. Usage indicators depend on the information exposed by Claude.ai and may change if its internal APIs or interface change.

## 🔒 Privacy

- No external analytics or tracking server is configured in the project documentation.
- The extension communicates with Claude.ai to retrieve relevant usage information.
- Conversation token counting is performed locally using the bundled tokenizer.
- Review the source code and permissions before installing or distributing the extension.

## 📁 Project Structure

```text
claude-counter/
├── manifest.json
├── README.md
├── LICENSE
├── THIRD_PARTY_NOTICES.md
├── icons/
└── src/
    ├── content/
    │   ├── bridge-client.js
    │   ├── constants.js
    │   ├── main.js
    │   ├── tokens.js
    │   └── ui.js
    ├── injected/
    │   └── bridge.js
    ├── vendor/
    │   └── o200k_base.js
    └── styles.css
```

## 🤝 Contributing

Contributions, bug reports, and improvement suggestions are welcome.

1. Fork the repository.
2. Create a feature branch.
3. Make and test your changes.
4. Submit a pull request with a clear description.

## 📄 License

This project includes an MIT license. Review `LICENSE` and `THIRD_PARTY_NOTICES.md` for applicable terms and third-party attribution.

## 👨‍💻 Development

Maintained in the **Creators Choice** development workspace, with a focus on browser extensions, automation tools, SaaS platforms, and practical software solutions.

**Repository:** `creatorschoice/my-free-projects`

---

*Claude Counter is an independent community project and is not affiliated with, endorsed by, or officially supported by Anthropic. Claude and Claude.ai are trademarks of their respective owners.*
