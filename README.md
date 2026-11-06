# Mac Starter

Set up a new Mac with AI or terminal commands.

## 1. Open Terminal

Press `⌘ Space`, search for `Terminal`, and open it.

## 2. Install Codex (optional)

```sh
curl -fsSL https://chatgpt.com/codex/install.sh | sh
```

Complete the installer's PATH instructions, then reopen Terminal.

```sh
mkdir -p ~/mac-setup
cd ~/mac-setup
codex
```

Sign in and paste this prompt.

```text
Read https://github.com/cocojen/mac-starter and follow its README to set up my Mac.
Install Homebrew, Chrome, Rectangle, Obsidian, Notion, Slack, Telegram, Clipy,
Git, VS Code, GitHub CLI, Claude Code, Docker Desktop, AWS CLI, uv, and DBeaver.
Skip existing installations.
Explain each command briefly. Leave passwords, sign-ins, and permission
prompts to me. Stop on errors. Report what is installed and what remains.
```

If using Codex, continue to step 5 after installation. Otherwise, follow steps 3–4.

## 3. Install Homebrew

```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Run the installer's **Next steps** commands to add Homebrew to PATH.

```sh
brew --version
```

## 4. Install apps and developer tools

Omit apps you already have. Choose the developer tools you need.

### Everyday apps

```sh
brew install --cask google-chrome rectangle obsidian notion slack telegram clipy
```

Chrome: browser. Rectangle: window management. Obsidian: Markdown notes.
Notion: documents and collaborative workspaces. Slack: team communication.
Telegram: messaging. Clipy: clipboard history.

### Development

```sh
brew install git gh uv awscli
brew install --cask visual-studio-code dbeaver-community
brew install --cask claude-code
brew install --cask docker-desktop
```

- **Git / GitHub CLI:** version control and GitHub access.
- **VS Code:** code editor.
- **Claude Code:** terminal-based AI coding assistant. Update the Homebrew installation with `brew upgrade claude-code`.
- **uv:** Python package and environment management.
- **AWS CLI:** AWS commands.
- **DBeaver:** database client; requires a database to connect to.
- **Docker Desktop:** containers; requires initial app setup.

Docker installation may request an administrator password. Alternatively, use the [official Mac installer](https://docs.docker.com/desktop/setup/install/mac-install/).

## 5. Finish setup

- **Rectangle:** enable Accessibility permission when prompted.
- **Obsidian:** create or open a vault.
- **Notion:** open the app, sign in, and choose your workspace.
- **Slack:** open the app and sign in to your workspaces.
- **Telegram:** open the app and sign in to your account.
- **Clipy:** open the app and enable Accessibility permission when prompted for automatic pasting. Press `⌘⇧V` to open the clipboard menu.
- **GitHub CLI:** run `gh auth login`.
- **Claude Code:** run `claude` from your project directory and complete sign-in when prompted.
- **Docker:** open Docker Desktop, complete setup, then run `docker info`.
- **AWS CLI:** configure authentication for your AWS account.
- **DBeaver:** create a connection using your database credentials.

Verify developer tools:

```sh
git --version
gh --version
uv --version
aws --version
code --version
claude --version
```

Use `code .` to open a project in VS Code. Install uv once; keep Python dependencies in each project's virtual environment.

If `brew` or `codex` is not found, complete the installer's PATH instructions and reopen Terminal.

[Codex installation](https://learn.chatgpt.com/docs/codex/cli) · [Claude Code installation](https://code.claude.com/docs/en/setup) · [Notion installation](https://formulae.brew.sh/cask/notion) · [Homebrew](https://brew.sh/) · [uv](https://docs.astral.sh/uv/guides/projects/)
