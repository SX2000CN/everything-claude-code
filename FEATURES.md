# 🌟 Features Guide

This document details the core modules included in this repository.

## 1. 🤖 Agents
**Location**: `agents/`

Specialized AI roles for specific complex tasks. Delegated via `/plan` etc.

| Agent | File | Purpose |
| :--- | :--- | :--- |
| **Planner** | `planner.md` | Breaks down tasks, generates implementation plans |
| **Architect** | `architect.md` | System design decisions, diagrams |
| **Code Reviewer** | `code-reviewer.md` | Checks quality, style consistency |
| **Security Reviewer** | `security-reviewer.md` | Vulnerability analysis (OWASP Top 10) |
| **TDD Guide** | `tdd-guide.md` | Test-Driven Development guidance |
| **Refactor Cleaner** | `refactor-cleaner.md` | Removes dead code and unused variables |
| **Doc Updater** | `doc-updater.md` | Auto-updates docs after code changes |

---

## 2. 🧠 Skills
**Location**: `skills/`

Pre-defined workflows and domain knowledge. Claude retrieves these based on context.

| Category | Content | Purpose |
| :--- | :--- | :--- |
| **TDD Workflow** | `tdd-workflow/` | Red-Green-Refactor cycle |
| **Security Review** | `security-review/` | Security checklists |
| **Coding Standards** | `coding-standards/` | Immutability, functional patterns |
| **Continuous Learning** | `continuous-learning/` | **Auto-Learning**: Extracts patterns from sessions |
| **Strategic Compact** | `strategic-compact/` | Smart context compaction strategies |
| **Verification Loop** | `verification-loop/` | Ensures implementation actually works |

---

## 3. 🛡️ Rules
**Location**: `rules/`

Mandatory guidelines. Copy to `~/.claude/rules/`.

| File | Core Content |
| :--- | :--- |
| `security.md` | **Red Lines**: No hardcoded secrets, no unverified execution |
| `coding-style.md` | **Style**: File limits, naming conventions |
| `testing.md` | **Testing**: TDD requirement, coverage baseline |
| `git-workflow.md` | **Git**: Commit message format, PR process |

---

## 4. ⚡ Commands
**Location**: `commands/`

Shortcuts for complex operations.

| Command | File | Purpose |
| :--- | :--- | :--- |
| `/plan` | `plan.md` | Start planning (calls Planner Agent) |
| `/verify` | `verify.md` | Run verification loop |
| `/tdd` | `tdd.md` | Start TDD mode |
| `/checkpoint` | `checkpoint.md` | Save progress snapshot |
| `/learn` | `learn.md` | **Manual Learning**: Extract patterns interactively |
| `/finish` | `finish.md` | **End Session**: Run save/archive scripts manually |

---

## 5. 🔌 Hooks & Scripts
**Location**: `hooks/` & `scripts/`

Automations for lifecycle management.

*   **Session Start**: Loads `memory.md` context.
*   **Session End**: Saves summary to `memory.md`.
*   **Pre-Compact**: Saves state before context compaction.
*   **Tool Use**: Security checks (prevents dangerous commands).

---

## 6. 🎭 Contexts (Advanced)
**Location**: `contexts/`

System prompts injected via CLI arguments.

*   `dev.md`: **Dev Mode** (Efficient, terse)
*   `review.md`: **Review Mode** (Strict, skeptical)
*   `research.md`: **Research Mode** (Deep, explanatory)
