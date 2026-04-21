# Contributing

Thanks for considering a contribution. This repo distributes Claude Code subagent definitions — small, focused markdown files with YAML frontmatter.

## Ground rules

1. **One agent per file.** The filename is the canonical agent name.
2. **Filename = frontmatter `name:`.** Both must be lowercase, hyphen-separated (e.g. `my-new-agent.md` → `name: my-new-agent`).
3. **Declare your `tools:` allowlist.** Start with `Read, Grep, Glob`. Only add `Bash`, `Write`, `Edit`, or MCP tools if the agent genuinely needs them; justify each addition in the PR description.
4. **Conform to the shared output schema** (status, severity-tagged issues with `path:line`, recommendations, next-agent suggestions). See [README.md](README.md#shared-output-schema).
5. **Cross-agent references are manual.** Every agent should carry the "Note on cross-agent references" reminder so users understand they must invoke chained agents explicitly.

## How to add a new agent

1. Copy [TEMPLATE.md](TEMPLATE.md) to `your-agent-name.md`.
2. Fill in `name`, `description`, `tools`, `color`, and the body.
3. Slot your agent into the chain diagram in [README.md](README.md) if it should participate in reviews.
4. Add a one-line entry to the "Agents at a glance" table and, if applicable, to the "Which agent do I need?" table.
5. Open a PR.

## Review criteria

PRs are evaluated on:

- **Scope.** Is the agent's role distinct from existing agents? If it overlaps heavily, why?
- **`tools:` minimalism.** Is the declared tool surface actually needed?
- **Testability.** Does the description make it clear when the agent should and should not be used?
- **Safety.** Does the agent encourage review rather than auto-execution? Does it avoid adversarial or inappropriate tone?
- **Documentation delta.** README and diagram updated accordingly.

## Changes to existing agents

Small tweaks (typos, clearer examples, schema alignment) are welcome. Larger behavioural changes should be discussed in an issue first.
