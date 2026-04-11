# Install — Claude Code

## Quick install

```bash
# 1. Copy cognitive protocol to Claude's config
cp cognitive-protocol.md ~/.claude/interactive-cognition.md

# 2. Add reference in CLAUDE.md
echo '@~/.claude/interactive-cognition.md' >> ~/.claude/CLAUDE.md
```

## What gets loaded where

| File | Destination | Purpose |
|---|---|---|
| `cognitive-protocol.md` | `~/.claude/interactive-cognition.md` | Always-on core rules (~30 lines) |
| `SKILL.md` | `~/.claude/skills/interactive-cognition/SKILL.md` | Full reference (loaded on demand) |
| `anti-patterns.md` | `~/.claude/skills/interactive-cognition/anti-patterns.md` | Detailed anti-pattern guide |
| `examples.md` | `~/.claude/skills/interactive-cognition/examples.md` | Before/after reference |

## Full install (with skill files)

```bash
# 1. Core rules
cp cognitive-protocol.md ~/.claude/interactive-cognition.md

# 2. Skill files
mkdir -p ~/.claude/skills/interactive-cognition
cp SKILL.md ~/.claude/skills/interactive-cognition/
cp anti-patterns.md ~/.claude/skills/interactive-cognition/
cp examples.md ~/.claude/skills/interactive-cognition/

# 3. Register in CLAUDE.md
echo '@~/.claude/interactive-cognition.md' >> ~/.claude/CLAUDE.md
```

## Verify

Ask Claude Code: "What are the interactive cognition rules you're following?" It should list the five sections from `cognitive-protocol.md`: model the other party, manage information flow, assess bilateral state, adapt to opponent's state, output self-check.

## Stacking with other cognitive bases

Interactive Cognition operates on a unique axis — inter-personal cognition. It stacks with First Principles (reasoning input), Systems Thinking (structural analysis), and any other cognitive base without conflicts. No special loading order required.

## Uninstall

```bash
rm ~/.claude/interactive-cognition.md
rm -rf ~/.claude/skills/interactive-cognition
# Remove the @~/.claude/interactive-cognition.md line from ~/.claude/CLAUDE.md
```
