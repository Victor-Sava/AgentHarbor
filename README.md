# AgentHarbor

**Your coding workspace, wherever you are.**

Keep your coding agent on your own computer. Follow its progress, add instructions, and continue conversations from a browser on your laptop or phone.

[Open AgentHarbor](https://agent-harbor.workautoman.com) · [Installation guide](https://agent-harbor.workautoman.com/install) · [Downloads](https://github.com/Victor-Sava/AgentHarbor/releases)

## How it works

- **Run on your own devices.** Keep your projects and model credentials in your existing development environment.
- **Continue in your browser.** Connect your computer to your workspace to view sessions and send follow-up instructions.
- **Keep conversations encrypted.** Your devices hold the keys used to decrypt synchronized session content.

AgentHarbor provides the connection between your devices and the web workspace. Bring your own model account; model usage is billed by your provider. Your computer must remain online with the agent running to execute tasks.

## Install the agent

### macOS and Linux

```bash
curl -fsSL https://agent-harbor.workautoman.com/install.sh | bash
```

Supports Apple silicon and Intel Macs, plus Linux x64 with glibc. Linux is tested on Ubuntu 24.04; Alpine/musl is not supported. Reopen your terminal after installation.

### Windows

Run in PowerShell on Windows x64:

```powershell
irm https://agent-harbor.workautoman.com/install.ps1 | iex
```

The installer downloads the matching package, verifies its SHA-256 checksum, and installs it for the current user. No local Node.js, Rust, or C++ build environment is needed. Existing configuration is preserved.

## Connect your workspace

1. Sign in to your model provider on the computer running the agent.
2. Follow the [installation guide](https://agent-harbor.workautoman.com/install) to configure your identity and enabled provider.
3. Run `agentharbor-agent login`, then paste the `agentharbor://terminal?...` authorization link into **Connect computer** in [AgentHarbor](https://agent-harbor.workautoman.com).

To upgrade, finish active tasks and run `agentharbor-agent stop`. Run the same installation command again, then `agentharbor-agent start`.

## About these downloads

This repository contains the product overview, installation instructions, and prebuilt releases. Product source is maintained privately. Release archives include license notices and SHA-256 files.

These are preview builds. Windows binaries are not code-signed, and macOS binaries are not Apple-notarized. The installers do not disable operating-system security checks.
