# Install — Generic (Any Agent/Framework)

## Universal principle

Interactive Cognition is a cognitive base — it changes how the agent reasons about multi-party scenarios, not what tools it uses. Installation means injecting `cognitive-protocol.md` into the agent's always-on instructions (system prompt, rules file, or configuration).

## Platform mapping

| Platform | Where to inject | File to use |
|---|---|---|
| Claude Code | `~/.claude/interactive-cognition.md` + ref in `CLAUDE.md` | `cognitive-protocol.md` |
| Codex | Prepend to `AGENTS.md` | `cognitive-protocol.md` |
| Gemini | `system_instruction` field | `cognitive-protocol.md` |
| Cursor | Prepend to `.cursorrules` | `cognitive-protocol.md` |
| ChatGPT | Custom Instructions -> system prompt | `cognitive-protocol.md` |
| LangChain | System message in chain | `cognitive-protocol.md` |
| AutoGPT / CrewAI | Agent system prompt | `cognitive-protocol.md` |
| Any other | Find the "always-on instructions" config and inject there | `cognitive-protocol.md` |

## Step by step

1. Locate your agent's system prompt or always-on rules file
2. Copy the contents of `cognitive-protocol.md` (~30 lines)
3. Paste it into the system prompt, AFTER any internal reasoning bases (First Principles, Systems Thinking, etc.)
4. Interactive Cognition is the inter-personal layer — it builds on internal reasoning, so it goes last among cognitive bases

## File selection guide

| Need | File | Size |
|---|---|---|
| Minimal install (core rules only) | `cognitive-protocol.md` | ~30 lines |
| Full reference framework | + `SKILL.md` | ~180 lines |
| Anti-pattern detection | + `anti-patterns.md` | ~120 lines |
| Teaching examples | + `examples.md` | ~160 lines |

For most agents, `cognitive-protocol.md` alone is sufficient. The additional files are reference material for when the agent needs deeper guidance.

## Troubleshooting

- **Agent ignores the rules**: Move `cognitive-protocol.md` content closer to the beginning of the system prompt. Most models weight earlier instructions more heavily.
- **Agent over-applies opponent modeling**: This is the "over-modeling" anti-pattern. Add the calibration section from `SKILL.md` (section 5) to teach the agent when NOT to model.
- **Agent slides into manipulation**: Add the "Manipulation slope" section from `anti-patterns.md` to reinforce the ethical boundary.
- **Context window pressure**: `cognitive-protocol.md` is ~30 lines. If that's too much, something else in your prompt needs trimming first.
