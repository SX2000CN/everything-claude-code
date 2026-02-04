# /finish - End Session & Archive

Manually trigger "Session End" logic. Useful when automatic hooks might not fire (e.g., closing VSCode directly).

## Actions

Runs the following scripts to ensure memory and skills are saved.

### 1. Save Memory
Updates `memory.md` with the current session summary.

```bash
node ~/.claude/scripts/hooks/session-end.js
```

### 2. Extract Patterns
Analyzes session history to extract new skills.

```bash
node ~/.claude/scripts/hooks/evaluate-session.js
```

---

## Post-Run
Notify the user: "✅ Session archived. Memory updated and new skills extracted (if any). You may now safely close the window."
