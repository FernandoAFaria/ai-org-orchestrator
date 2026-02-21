# Nightshift AI

**Nightshift AI** is a standalone, local-first platform for managing an LLM-powered multi-agent team.

This repository distributes the compiled CLI (`nightshift`) so you can run the platform directly on your machine.

## 🚀 Installation

Install or update the CLI by running the following command in your terminal:

```bash
curl -fsSL https://raw.githubusercontent.com/FernandoAFaria/nightshift-ai/master/install.sh | bash
```

*This will download the latest release for your platform (macOS/Linux, x64/arm64) and place it in `~/.nightshift-ai`. After installation, restart your terminal or run `source ~/.bashrc` (or `~/.zshrc` on macOS) to use the `nightshift` command.*

## ⚙️ Configuration

The platform requires access to OpenRouter to power the AI agents. You will need to provide an API key.

1. The setup wizard will open automatically on first run at **http://localhost:8989/setup**
2. Enter your OpenRouter API key there

*Alternatively, you can edit the config file manually:*
```bash
nano ~/.nightshift-ai/.env
```

*(Note: The database `dev.db` is also stored locally in `~/.nightshift-ai/prisma/dev.db`.)*

## 💻 Usage

Once installed, you can manage the application using the `nightshift` CLI.

### Start the Platform
```bash
nightshift
```
Starts the Next.js frontend, backend API, and background heartbeat workers. The application will be accessible at:
**http://localhost:8989**

### Stop the Platform
```bash
nightshift stop
```
Safely stops all running Next.js and worker processes.

### View Logs
```bash
nightshift logs
```
Tails the real-time application and worker logs.

### Check Status
```bash
nightshift status
```
Checks if the Nightshift processes are currently running.

### Update the CLI
```bash
nightshift update
```
Pulls the latest release from GitHub and updates your local installation.

### Uninstall
```bash
nightshift uninstall
```
Removes Nightshift from your system.

---
*Powered by Bun, Next.js, and OpenRouter.*
