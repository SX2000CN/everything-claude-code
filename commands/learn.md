# /learn - Manual Pattern Extraction

Requests AI to analyze the current session and extract reusable patterns worth saving.
Unlike `/finish` (which runs scripts automatically), this is an interactive process allowing you to review and edit the generated skill.

## Trigger
Use when you've just solved a complex problem or discovered a "gotcha" you want to record.

## Steps

1.  **Review Session**: Analyze recent conversation history.
2.  **Identify Patterns**:
    *   Error Resolution
    *   Debugging Techniques
    *   Project Conventions
3.  **Draft Skill File**:
    *   Draft a markdown skill file in memory.
    *   Include: Problem, Solution, Code Example, When to Use.
4.  **Save**:
    *   Present the draft to the user.
    *   If approved, use `Write` tool to save to `~/.claude/skills/learned/[pattern-name].md`.

## Example Output

```markdown
# [Pattern Name]

**Extracted:** 2024-xx-xx
**Context:** [Brief description]

## Problem
...

## Solution
...
```
