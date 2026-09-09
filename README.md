<div align="center">

<img src="assets/icon.png" width="192" alt="Tactic Remote">

# Tactic Remote

### Control Claude Code, Codex, Amp, and Droid from your iPhone or iPad

[![iOS](https://img.shields.io/badge/iOS-16.4%2B-blue.svg?style=flat&logo=apple&logoColor=white)](https://apps.apple.com/us/app/tactic-remote-ai-coding/id6758008464)
[![macOS](https://img.shields.io/badge/macOS-14.6%2B-green.svg?style=flat&logo=apple&logoColor=white)](https://github.com/TacticSpaceTech/TacticRemote/releases)
[![npm](https://img.shields.io/badge/npx-tacticremote-cb3837.svg?style=flat&logo=npm&logoColor=white)](https://www.npmjs.com/package/tacticremote)
[![App Store](https://img.shields.io/badge/App%20Store-Available-purple.svg?style=flat&logo=apple&logoColor=white)](https://apps.apple.com/us/app/tactic-remote-ai-coding/id6758008464)

[Website](https://tacticremote.com) • [Documentation](https://tacticremote.com/docs) • [Support](https://github.com/TacticSpaceTech/TacticRemote/issues)

</div>

---

> **Tactic Remote 1.10** improves Windows sign-in, account linking, and Tactic Relay connections. Continue your AI coding tasks from iPhone and iPad with a project-based home screen and reusable prompt drafts.

---

## Overview

Tactic Remote brings AI coding agents to your iPhone or iPad. Run Claude Code, OpenAI Codex, Sourcegraph Amp, or Factory Droid on your computer, then monitor output, send prompts, approve blocking steps, review code changes, and keep long-running work moving from your mobile device.

It is built for developers who want to stay close to AI coding sessions without staying at their desk.

---

## What's New in 1.10

- **Windows account connections** — Sign in, bind your PC, and connect from an iPhone or iPad using the same Tactic account.
- **Tactic Relay on Windows** — Improved encrypted remote connections and reconnect behavior.
- **Project-based home screen** — Find a project, then return to its Agent conversations on iPhone and iPad.
- **Review before sending** — Commands and reusable prompts go into a draft, ready for your context.

This release updates iOS/iPadOS and the Windows Preview companion to 1.10.0. The existing macOS 1.9.0 download and Mac/Linux CLI remain available separately. The browser workspace is not part of this public launch.


---

## Features

<div align="center">

### **Chat Mode for Agent Output**
Read agent messages, tool calls, Thinking sections, and streaming updates in a mobile-friendly layout

### **Quick Prompts Library**
Save common review, test, debug, and summary prompts so repeat workflows are always close

### **Mobile Git Review**
View changed files, inspect diffs, and decide whether an agent's work should continue

### **Multi-Agent Sessions**
Choose Claude Code, OpenAI Codex, Sourcegraph Amp, or Factory Droid when creating a session

### **Git Worktree Workflow**
Group sibling worktrees and switch between parallel implementation branches

### **Smart Prompt Toolbar**
Auto-reveals shortcuts for blocking TUI prompts like confirmations and trust dialogs

### **Terminal Mode**
Full terminal with ANSI color support, real-time streaming, search, and keyboard submit

### **iPad-Optimized Layout**
Native split-view with hardware keyboard shortcuts

### **Cloud Speech-to-Text**
Dictate prompts in 25+ languages

### **File Uploads**
Send files from iOS to the remote server

### **Multi-Session Management**
Create, switch, and delete multiple tmux sessions

### **Remote File Browser**
Browse your computer's file system and select project directories from iOS

### **Local & Remote Access**
Connect on your local network, or use Tactic Relay with the Windows 1.10 companion for remote access. Advanced tunnel connections remain available.

### **Push Notifications**
Get notified when an agent completes tasks or sends hook events

### **Live Activity & Widgets**
Real-time agent status on Lock Screen, Dynamic Island, and Home Screen widgets

### **App Lock**
Protect sessions with Face ID or Touch ID

</div>

---

## How It Works

```text
┌──────────────────────────────────────────────────────────────────────────┐
│                                                                          │
│   ┌─────────────────┐            WebSocket            ┌─────────────────┐│
│   │   iOS Device    │                                 │ Mac/Linux/Win   ││
│   │                 │  ◄─────────────────────────►    │                 ││
│   │  Tactic Remote  │    ws://local or wss://         │  Server (Node)  ││
│   │      App        │                                 │                 ││
│   └─────────────────┘                                 └────────┬────────┘│
│                                                                │         │
│                                                                ▼         │
│                                                       ┌─────────────────┐│
│                                                       │ Coding Agent    ││
│                                                       │Claude/Codex/Amp/││
│                                                       │      Droid      ││
│                                                       └─────────────────┘│
│                                                                          │
└──────────────────────────────────────────────────────────────────────────┘
```

**Four ways to run the server:**

| Method | Platform | Command |
|--------|----------|---------|
| **npx** | Mac / Linux | `npx tacticremote` |
| **Homebrew** | Mac | `brew install TacticSpaceTech/tap/tacticremote` |
| **Mac App** | macOS 14.6+ | Menu bar GUI with one-click start and auto-update |
| **Windows App** (Preview) | Windows 10/11 x64 | Companion app — preview release, may have issues |

---

## Quick Start

The fastest way to get started on Mac or Linux is one command:

```bash
npx tacticremote
```

Scan the QR code with the Tactic Remote iOS app and you are connected.

### Options

```text
npx tacticremote [options]

  -p, --port <n>      Port to listen on          (default: 8765)
  --path <dir>        Allowed base directory      (default: $HOME)
  --api-key <key>     Require authentication key
  --tunnel            Enable Cloudflare Tunnel for remote access
  --no-qr             Do not show QR code
  -h, --help          Show this help
```

### Alternative: Mac Menu Bar App

If you prefer a graphical interface:

1. **Download** the DMG from [Releases](https://github.com/TacticSpaceTech/TacticRemote/releases/tag/v1.9.0)
2. **Install** by opening the DMG and dragging **Tactic Remote** to Applications
3. **Launch** from Applications; a menu bar icon will appear
4. **Start Server** from the menu bar app
5. **Connect** from Tactic Remote on your iPhone or iPad

The Mac app also provides:

- One-click Cloudflare Tunnel for remote access
- Live client count and session monitoring
- Copy server URL, tunnel address, and API key from the menu
- Server compatibility status
- Prevent Sleep while the server is running
- Language switcher for 8 languages
- Auto-start on login
- In-app update checks

### Alternative: Windows Companion App (Preview)

> 🟡 **Preview release.** The Windows companion is published as a preview. Most flows work, but expect rough edges compared to the Mac app and iOS app. We recommend macOS users continue using the Mac companion; we welcome bug reports from Windows users.

1. **Download** the installer from [Releases](https://github.com/TacticSpaceTech/TacticRemote/releases/tag/v1.9.0): `TacticRemote-Windows-Setup-1.10.0.exe`
2. **Install** by running the installer (Windows 10 or 11, x64)
3. **Launch** Tactic Remote from the Start menu
4. **Start Server** from the app window
5. **Connect** from Tactic Remote on your iPhone or iPad

Known limitations of the preview:

- The installer is not yet code-signed, so Windows SmartScreen may show a warning. Verify that it came from the official Tactic Remote release page before continuing.
- Some terminal scenarios (long ConPTY sessions, complex pairings) may need restart
- Auto-update is not yet enabled — new versions install manually
- Please report issues at [the issue tracker](https://github.com/TacticSpaceTech/TacticRemote/issues)

---

## Download

<table align="center">
<tr>
<td align="center" width="25%">
<b>iOS App</b><br>
<i>iPhone / iPad</i><br><br>
<a href="https://apps.apple.com/us/app/tactic-remote-ai-coding/id6758008464">
<img src="https://developer.apple.com/assets/elements/badges/download-on-the-app-store.svg" width="160" alt="Download on App Store">
</a>
</td>
<td align="center" width="25%">
<b>Mac App</b><br>
<i>macOS 14.6+</i><br><br>
<a href="https://github.com/TacticSpaceTech/TacticRemote/releases/tag/v1.9.0">
<img src="https://img.shields.io/badge/Download-DMG-success.svg?style=for-the-badge&logo=apple" width="160" alt="Download DMG">
</a>
</td>
<td align="center" width="25%">
<b>Windows App</b> 🟡<br>
<i>Windows 10/11 — Preview</i><br><br>
<a href="https://github.com/TacticSpaceTech/TacticRemote/releases/tag/v1.9.0">
<img src="https://img.shields.io/badge/Download-EXE%20(Preview)-orange.svg?style=for-the-badge&logo=windows" width="160" alt="Download Windows Installer (Preview)">
</a>
</td>
<td align="center" width="25%">
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
| **iOS** | 16.4 | iPhone or iPad |
| **macOS** | 14.6 Sonoma | For Mac app or CLI |
| **Windows** | 10 or 11 (x64) | For Windows companion app (Preview) |
| **Linux** | Any | For CLI (`npx tacticremote`) |
| **Node.js** | 16.0+ | Required for CLI; auto-installed by Mac app when needed |
| **tmux** | Latest | Required by Mac/Linux backends; auto-installed by the Mac app or Homebrew |
| **AI coding agent CLI** | Latest | Install and sign in to at least one: Claude Code, OpenAI Codex, Sourcegraph Amp, or Factory Droid |

---

## Connection Modes

### Local Network

Default mode for home or office use.

```text
ws://192.168.1.x:8765
```

Ensure your iOS device and computer are on the same Wi-Fi network.

### Public Access with Cloudflare Tunnel

Connect from anywhere using a secure tunnel, without opening ports on your machine:

```bash
npx tacticremote --tunnel
```

The server generates a `wss://` URL automatically. Use this URL in the iOS app.

---

## Security

### API Key Authentication

```bash
npx tacticremote --api-key "your-secure-key"
```

Then enter the same key in the iOS app.

### Path Restrictions

File operations are restricted to your home directory by default. Customize the allowed base path:

```bash
npx tacticremote --path "/Users/yourname/Projects"
```

### Cloudflare Tunnel

Public access uses Cloudflare's secure tunnel with TLS encryption, so you do not need to open inbound ports.

---

## Troubleshooting

### Cannot connect to server

- Verify your computer and iOS device are on the same network
- Check that the computer firewall allows connections on port 8765
- Confirm the server is running: `lsof -i :8765` on Mac/Linux or `Get-NetTCPConnection -LocalPort 8765` in Windows PowerShell

### Connection drops frequently

- Check Wi-Fi stability
- The app supports automatic fallback between LAN and tunnel connections
- iOS app auto-reconnects up to 5 times

### Agent not starting

- Ensure your selected agent CLI is installed and signed in: `claude --version`, `codex --version`, `amp --version`, or `droid --version`
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
