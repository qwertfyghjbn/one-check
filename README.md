# one-check

A personal experiment continues after one related check. The next edit does not wait for a unique baseline, a hash chain, a smoke matrix, or an acceptance matrix.

The skill is [Agent Skills](https://agentskills.io/specification) format: `skills/one-check/SKILL.md`. The same directory installs into Cursor, Claude Code, Codex, and the other agents supported by the [skills CLI](https://github.com/vercel-labs/skills).

## Install

From any project, or with `-g` for every project on this machine:

```bash
npx skills add qwertfyghjbn/one-check --skill one-check -g -y
```

Install to every detected agent:

```bash
npx skills add qwertfyghjbn/one-check --skill one-check --agent '*' -g -y
```

List the skill without installing:

```bash
npx skills add qwertfyghjbn/one-check --list
```

The CLI copies `skills/one-check/` into that agent's skills directory. It does not install the Cursor rule or the `AGENTS.md` snippet below.

## Install by hand

Copy the `skills/one-check/` directory to one of these paths. The folder name must stay `one-check`.

| Agent | This project | This machine |
| --- | --- | --- |
| Cursor | `.agents/skills/one-check/` or `.cursor/skills/one-check/` | `~/.cursor/skills/one-check/` |
| Claude Code | `.claude/skills/one-check/` | `~/.claude/skills/one-check/` |
| Codex, Gemini CLI, GitHub Copilot | `.agents/skills/one-check/` | `~/.agents/skills/one-check/` or the agent path in the skills CLI table |

Cursor also reads `.claude/skills/` and `.codex/skills/`. Start a new session after copying.

## When a skill is not enough

The skill loads when the task starts to look like ceremony. A repository that already orders a gate in `AGENTS.md` will still inject that order on every turn.

- Copy `templates/cursor-rule.mdc` to `.cursor/rules/one-check.mdc` in a Cursor project.
- Paste `templates/AGENTS.snippet.md` into `AGENTS.md`, replacing the section that requires the harness.

`examples/cairn.md` shows how one research repo kept its own names out of this skill.

This repository has no checker script. A script here would become the next gate.
