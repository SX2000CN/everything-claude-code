# 📂 Path Mapping & Manual Installation Guide

This branch (`beta`) is a pure configuration collection for Claude Code.
Please follow the mapping below to copy files to your local Claude configuration directory.

## Core Configuration Mapping

| 📁 Project Folder | ➡️ Target Path (macOS/Linux) | ➡️ Target Path (Windows) | 📝 Purpose |
| :--- | :--- | :--- | :--- |
| `agents/` | `~/.claude/agents/` | `%USERPROFILE%\.claude\agents\` | **Agents**: Specialized AI roles for specific tasks |
| `rules/` | `~/.claude/rules/` | `%USERPROFILE%\.claude\rules\` | **Rules**: Mandatory guidelines (Security/Style) |
| `skills/` | `~/.claude/skills/` | `%USERPROFILE%\.claude\skills\` | **Skills**: Pre-defined workflows and knowledge |
| `commands/` | `~/.claude/commands/` | `%USERPROFILE%\.claude\commands\` | **Commands**: Custom slash commands (e.g., `/plan`) |
| `contexts/` | `~/.claude/contexts/` | `%USERPROFILE%\.claude\contexts\` | **Contexts**: System prompts injected at launch |
| `scripts/` | `~/.claude/scripts/` | `%USERPROFILE%\.claude\scripts\` | **Scripts**: Automation scripts for Hooks |

---

## 🛠️ Advanced Configuration

### 1. Hooks & Scripts

1.  Open your Claude global settings:
    *   Mac/Linux: `~/.claude/settings.json`
    *   Windows: `%USERPROFILE%\.claude\settings.json`

2.  Copy the `hooks` field from `hooks/hooks.json` in this repo to your settings.
3.  **Critical Step**: Ensure command paths in `hooks.json` point to your global scripts directory.

    *   **Recommendation**: Use absolute paths.
    *   **Example (Mac/Linux)**: `"command": "node ~/.claude/scripts/hooks/session-start.js"`
    *   **Example (Windows)**: `"command": "node %USERPROFILE%\\.claude\\scripts\\hooks\\session-start.js"`

### 2. MCP Tools (Model Context Protocol)

1.  Open MCP config file:
    *   Mac/Linux: `~/.claude.json`
    *   Windows: `%USERPROFILE%\.claude.json`

2.  Copy desired server configs from `mcp-configs/mcp-servers.json` to your config file.
3.  **Note**: Replace `YOUR_API_KEY_HERE` with actual keys.
