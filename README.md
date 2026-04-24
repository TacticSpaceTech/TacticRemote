<div align="center">

<img src="assets/icon.png" width="192" alt="Tactic Remote">

# Tactic Remote

### Control Claude Code, Codex, and Amp from your iPhone or iPad

[![iOS](https://img.shields.io/badge/iOS-17.0%2B-blue.svg?style=flat&logo=apple&logoColor=white)](https://apps.apple.com/us/app/tactic-remote-ai-coding/id6758008464)
[![macOS](https://img.shields.io/badge/macOS-14.0%2B-green.svg?style=flat&logo=apple&logoColor=white)](https://github.com/TacticSpaceTech/TacticRemote/releases)
[![npm](https://img.shields.io/badge/npx-tacticremote-cb3837.svg?style=flat&logo=npm&logoColor=white)](https://www.npmjs.com/package/tacticremote)
[![App Store](https://img.shields.io/badge/App%20Store-Available-purple.svg?style=flat&logo=apple&logoColor=white)](https://apps.apple.com/us/app/tactic-remote-ai-coding/id6758008464)

[Website](https://tacticremote.com) • [Documentation](https://tacticremote.com/docs) • [Support](https://github.com/TacticSpaceTech/TacticRemote/issues)

</div>

---

> **Tactic Remote v1.7.0 is now available.** Choose Claude Code, OpenAI Codex, or Sourcegraph Amp for each new session, organize parallel work with Git worktrees, and keep the same mobile control surface across your AI coding workflow.

---

## Overview

Tactic Remote brings AI coding agents to your iPhone or iPad. Run Claude Code, OpenAI Codex, or Sourcegraph Amp on your computer, then monitor output, send prompts, approve blocking steps, and compare worktree-based explorations from your mobile device.

Perfect for reviewing code, monitoring long-running tasks, or quick iterations without being tied to your Mac.

---

## Features

<div align="center">

### **Multi-Agent Sessions**
Choose Claude Code, OpenAI Codex, or Sourcegraph Amp when creating a session

### **Git Worktree Workflow**
Group sibling worktrees and switch between parallel implementation branches

### **Smart Prompt Toolbar**
Auto-reveals shortcuts for blocking TUI prompts like confirmations and trust dialogs

### **iOS Terminal Interface**
Full terminal with ANSI color support, real-time streaming, search, and keyboard submit

### **Git Workspace Panel**
Live git status, file tree browsing, and branch info

### **iPad-Optimized Layout**
Native split-view with hardware keyboard shortcuts

### **Cloud Speech-to-Text**
Dictate prompts in 25+ languages

### **File Uploads**
Send files from iOS to the remote server

### **Multi-Session Management**
Create, switch, and delete multiple tmux sessions simultaneously

### **Remote File Browser**
Browse your Mac's file system and select project directories from iOS

### **Local & Remote Access**
Connect via WiFi or Cloudflare tunnel — with automatic fallback switching

### **Push Notifications**
Get notified when an agent completes tasks or sends hook events

### **Live Activity & Widgets**
Real-time agent status on Lock Screen, Dynamic Island, and Home Screen widgets

### **App Lock**
Protect sessions with Face ID or Touch ID

### **Pro Subscriptions**
Free trial included — unlock all features with monthly or yearly plans

</div>

---

## How It Works

```
┌──────────────────────────────────────────────────────────────────────────┐
│                                                                          │
│   ┌─────────────────┐            WebSocket            ┌─────────────────┐│
│   │   iOS Device    │                                 │   Mac / Linux   ││
│   │                 │  ◄─────────────────────────►    │                 ││
│   │  Tactic Remote  │    ws://local or wss://         │  Server (Node)  ││
│   │      App        │                                 │                 ││
│   └─────────────────┘                                 └────────┬────────┘│
│                                                                │         │
│                                                                ▼         │
│                                                       ┌─────────────────┐│
│                                                       │ Coding Agent    ││
│                                                       │ Claude/Codex/Amp││
│                                                       └─────────────────┘│
│                                                                          │
└──────────────────────────────────────────────────────────────────────────┘
```

**Three ways to run the server:**

| Method | Platform | Command |
|--------|----------|---------|
| **npx** | Mac / Linux | `npx tacticremote` |
| **Homebrew** | Mac | `brew install TacticSpaceTech/tap/tacticremote` |
| **Mac App** | macOS 14+ | Menu bar GUI with one-click start and auto-update |

---

## Quick Start

The fastest way to get started — one command, no install:

```bash
npx tacticremote
```

Scan the QR code with the Tactic Remote iOS app and you're connected.

### Options

```
npx tacticremote [options]

  -p, --port <n>      Port to listen on          (default: 8765)
  --path <dir>        Allowed base directory      (default: $HOME)
  --api-key <key>     Require authentication key
  --tunnel            Enable Cloudflare tunnel for remote access
  --no-qr             Don't show QR code
  -h, --help          Show this help
```

### Alternative: Mac Menu Bar App

If you prefer a graphical interface:

1. **Download** the DMG from [Releases](https://github.com/TacticSpaceTech/TacticRemote/releases/tag/v1.7.0)
2. **Install** — open the DMG and drag **Tactic Remote** to Applications
3. **Launch** — open from Applications, a menu bar icon will appear
4. **Setup** — the app will auto-install dependencies (Homebrew, Node.js, tmux) if needed
5. **Start Server** — click the menu bar icon → **Start Server**
6. **Connect** — open Tactic Remote on your iPhone, scan the QR code or enter the IP shown in the menu bar

The Mac app also provides:
- One-click Cloudflare tunnel for remote access
- Live client count and session monitoring
- Copy server URL / tunnel address / API key from the menu
- Language switcher (8 languages)
- Auto-start on login

---

## Download

<table align="center">
<tr>
<td align="center" width="33%">
<b>iOS App</b><br>
<i>iPhone / iPad</i><br><br>
<a href="https://apps.apple.com/us/app/tactic-remote-ai-coding/id6758008464">
<img src="https://developer.apple.com/assets/elements/badges/download-on-the-app-store.svg" width="160" alt="Download on App Store">
</a>
</td>
<td align="center" width="33%">
<b>Mac App</b><br>
<i>macOS 14+</i><br><br>
<a href="https://github.com/TacticSpaceTech/TacticRemote/releases/tag/v1.7.0">
<img src="https://img.shields.io/badge/Download-DMG-success.svg?style=for-the-badge&logo=apple" width="160" alt="Download DMG">
</a>
</td>
<td align="center" width="33%">
<b>CLI</b><br>
<i>Mac / Linux</i><br><br>
<code>npx tacticremote</code>
</td>
</tr>
</table>

---

## Requirements

| Platform | Minimum Version | Notes |
|----------|----------------|-------|
| **iOS** | 17.0 | iPhone or iPad |
| **macOS** | 14.0 Sonoma | For Mac app or CLI |
| **Node.js** | 16.0+ | Required for CLI; auto-installed by Mac app |
| **tmux** | Latest | Auto-installed by Mac app or Homebrew |
| **AI coding agent CLI** | Latest | Install and sign in to at least one: Claude Code, OpenAI Codex, or Sourcegraph Amp |

---

## Connection Modes

### Local Network (WiFi)

Default mode for home/office use.

```
ws://192.168.1.x:8765
```

Ensure your iOS device and Mac are on the same WiFi network.

### Public Access (Cloudflare Tunnel)

Connect from anywhere using a secure tunnel — no open ports, no configuration:

```bash
npx tacticremote --tunnel
```

The server generates a `wss://` URL automatically. Use this URL in the iOS app.

---

## Security

### API Key Authentication (Optional)

```bash
npx tacticremote --api-key "your-secure-key"
```

Then enter the same key in iOS app settings.

### Path Restrictions

File operations are restricted to your home directory by default. Customize:

```bash
npx tacticremote --path "/Users/yourname/Projects"
```

### Cloudflare Tunnel

Public access uses Cloudflare's secure tunnel with TLS encryption — no open ports on your machine.

---

## Troubleshooting

### Cannot connect to server

- Verify Mac and iOS are on the same network
- Check Mac firewall allows connections on port 8765
- Confirm server is running: `lsof -i :8765`

### Connection drops frequently

- Check WiFi stability
- The app supports automatic fallback between LAN and tunnel connections
- iOS app auto-reconnects up to 5 times

### Agent not starting

- Ensure your selected agent CLI is installed and signed in: `claude --version`, `codex --version`, or `amp --version`
- Check tmux is installed: `tmux -V`
- Verify the working directory exists

---

## Documentation

Visit [tacticremote.com](https://tacticremote.com) for:
- Visual setup guides
- Advanced configuration
- Troubleshooting tips
- Release notes

---

## License

This software is proprietary. See [LICENSE](LICENSE) for details.

---

## Support

- [Report Issues](https://github.com/TacticSpaceTech/TacticRemote/issues)
- [Discussions](https://github.com/TacticSpaceTech/TacticRemote/discussions)
- [Website](https://tacticremote.com)

---

<div align="center">

Copyright 2025-2026 [TacticSpace Tech](https://tacticspacetech.com/). All rights reserved.

</div>
