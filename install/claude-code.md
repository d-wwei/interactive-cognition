# Install — Claude Code

## Quick install

```bash
# 1. Inject core rules into CLAUDE.md (direct content injection — works on all versions)
cat cognitive-protocol.md >> ~/.claude/CLAUDE.md
```

## What gets loaded where

| File | Destination | Purpose |
|---|---|---|
| `cognitive-protocol.md` | `~/.claude/CLAUDE.md` (appended) | Always-on core rules (~30 lines) |
| `SKILL.md` | `~/.claude/skills/interactive-cognition/SKILL.md` | Full reference (loaded on demand) |
| `anti-patterns.md` | `~/.claude/skills/interactive-cognition/anti-patterns.md` | Detailed anti-pattern guide |
| `examples.md` | `~/.claude/skills/interactive-cognition/examples.md` | Before/after reference |

## Full install (with skill files)

```bash
# 1. Core rules (inject directly into CLAUDE.md)
cat cognitive-protocol.md >> ~/.claude/CLAUDE.md

# 2. Skill files
mkdir -p ~/.claude/skills/interactive-cognition
cp SKILL.md ~/.claude/skills/interactive-cognition/
cp anti-patterns.md ~/.claude/skills/interactive-cognition/
cp examples.md ~/.claude/skills/interactive-cognition/

# 3. (Core rules already injected in step 1)
```

## Verify

Ask Claude Code: "What are the interactive cognition rules you're following?" It should list the five sections from `cognitive-protocol.md`: model the other party, manage information flow, assess bilateral state, adapt to opponent's state, output self-check.

## Stacking with other cognitive bases

Interactive Cognition operates on a unique axis — inter-personal cognition. It stacks with First Principles (reasoning input), Systems Thinking (structural analysis), and any other cognitive base without conflicts. No special loading order required.

## Uninstall

```bash
# Remove the Interactive Cognition section from ~/.claude/CLAUDE.md (search for "# Interactive Cognition — Cognitive Protocol" header)
rm -rf ~/.claude/skills/interactive-cognition
```
