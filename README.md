# AgentHarbor

**Your coding workspace, wherever you are.**

Keep your coding agent on your own computer. Follow its progress, add instructions, and continue conversations from a browser on your laptop or phone.

[Open AgentHarbor](https://agent-harbor.workautoman.com) · [Installation guide](https://agent-harbor.workautoman.com/install) · [Downloads](https://github.com/Victor-Sava/AgentHarbor/releases)

## How it works

- **Run on your own devices.** Keep your projects and model credentials in your existing development environment.
- **Continue in your browser.** Connect your computer to your workspace to view sessions and send follow-up instructions.
- **Keep conversations encrypted.** Your devices hold the keys used to decrypt synchronized session content.

AgentHarbor provides the connection between your devices and the web workspace. Bring your own model account; model usage is billed by your provider. Your computer must remain online with the agent running to execute tasks.

## Desktop for Windows

[Download AgentHarbor Desktop for Windows x64](https://github.com/Victor-Sava/AgentHarbor/releases/download/v2026.11.1-preview.3/AgentHarbor-Desktop-2026.11.1-preview.3-win-x64.exe) · [Release notes and checksums](https://github.com/Victor-Sava/AgentHarbor/releases/tag/v2026.11.1-preview.3)

Run the installer and open AgentHarbor. The desktop app connects to the Agent on your computer; if one is not installed yet, setup can download the recommended Agent. Use your own model account. This Windows installer is an unsigned preview. macOS and Linux desktop installers are not included in this release.

The command-line Agent installers below remain available separately.

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

## Disconnect or switch accounts

Agent version `2026.11.5-agentharbor.5` and later includes:

```text
agentharbor-agent logout
```

Review the prompt and enter `y` to confirm. This unlinks the computer and deletes the sessions it synced to your web account. Local project files, model credentials, the web account, and other computers' sessions are kept. To pause without removing remote history, use `agentharbor-agent stop` instead.

After a successful logout, back up your old account's Secret Key if needed, sign out in the web app, and create or restore the target account. Run `agentharbor-agent login` and approve the new authorization link in that account. Web logout alone does not unlink your computer or delete the account.

If the command is not recognized, update the Agent first. If removal cannot be confirmed, check connectivity and retry; do not delete your data directory.

## About these downloads

This repository contains the product overview, installation instructions, and prebuilt releases. Product source is maintained privately. Release archives include license notices and SHA-256 files.

These are preview builds. Windows binaries are not code-signed, and macOS binaries are not Apple-notarized. The installers do not disable operating-system security checks.
