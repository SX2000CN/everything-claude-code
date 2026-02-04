# Claude Bockup (Manual Install Edition)

> **Note**: This is the pure configuration branch (`beta`) of `claude-bockup`.
> All plugin packaging logic has been removed. This repo contains only the **source configuration files**, ideal for advanced users who prefer manual control.

![License](https://img.shields.io/badge/license-MIT-blue.svg)

A battle-tested collection of Claude Code configurations, including Agents, Skills, Hooks, and Rules, evolved over 10+ months of daily use.

## 📚 Documentation

*   **[👉 Manual Installation Guide (PATH_MAPPING.md)](./PATH_MAPPING.md)**
    *   **Must Read**: Detailed mapping of where to copy each folder.
    *   Includes setup instructions for Hooks and MCP.

*   **[✨ Features Guide (FEATURES.md)](./FEATURES.md)**
    *   Explains what each Agent, Skill, and Rule does.
    *   Lists all available commands (`/plan`, `/verify`, etc.).

## 📂 Structure

```text
claude-bockup/
├── agents/       # 🤖 Agents (copy to ~/.claude/agents/)
├── rules/        # 🛡️ Rules (copy to ~/.claude/rules/)
├── skills/       # 🧠 Skills (copy to ~/.claude/skills/)
├── commands/     # ⚡ Commands (copy to ~/.claude/commands/)
├── contexts/     # 🎭 Contexts (copy to ~/.claude/contexts/)
├── scripts/      # 📜 Scripts (copy to ~/.claude/scripts/)
├── hooks/        # 🔌 Hooks (config for settings.json)
└── mcp-configs/  # 🛠️ MCP configs (for mcp-servers.json)
```

## 🚀 Quick Start

1.  **Clone this repo**:
    ```bash
    git clone -b beta https://github.com/SX2000CN/claude-bockup.git ~/tools/claude-bockup
    ```
2.  Follow **[PATH_MAPPING.md](./PATH_MAPPING.md)** to copy files to your global Claude configuration directory.
3.  (Advanced) Update your `settings.json` to enable Hooks and Scripts.

---

**Star this repo if it helps. Build something great.**
