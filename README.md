# Projects-style orchestration for Codex

A reusable workflow for coordinating project context, workers, handoffs, and verification.

## Install locally

Copy `skills/project-orchestration` to your Codex skills directory (`$CODEX_HOME/skills`, or `~/.codex/skills` when unset). Keep the directory name `project-orchestration`. The skill will be available on your next turn.

The selected public repository is `AndyZHENG0715/codex-project-orchestration`. Once published, install with:

```sh
npx skills add AndyZHENG0715/codex-project-orchestration --skill project-orchestration --agent codex --global
```

`npx` runs the Skills CLI without an npm global installation. Here `--global` makes the skill available across projects; it does not mean `npm install -g skills`.

## Use

Ask: `Use $project-orchestration to coordinate this project. Recover the current state, reuse existing workers, and continue toward the deliverable.`

For an existing coordinator, ask it to read the skill and incorporate relevant guidance without restarting completed work. See `examples/coordinator.md`.

## Environment

The workflow was developed in Codex desktop with project files, worker chats, and status/result tools. Available tools vary by host. Codex CLI can use the same guidance with available subagents and files; sidebar classification and persistent chat management require host support. The skill supplies instructions, not additional tools, shared cloud memory, or a scheduler.

Internal coordination prompts are in English. User-facing replies follow the user's language. Automatic skill selection is enabled by default; explicit invocation is also supported.

## Scope and positioning

This is an independent Projects-style workflow for Codex, inspired by project-oriented collaboration. It is not affiliated with OpenAI, Anthropic, or Cursor. It does not contain extracted proprietary prompts.

## Validation

Checked on October 20, 2026:

- The installable skill passed Codex skill-creator's `quick_validate.py` in both the release folder and a clean local Codex installation.
- The installed `SKILL.md` matched the release copy byte for byte (SHA-256: `3ea9a13ae98a5edcfce5165f49b7017b92820864be14d9636679aea3e7563ec1`).
- All four release files were reviewed: the generic skill, this README, a fictional coordinator example, and the MIT license.

Behavioral compatibility across hosts and installation from a public repository have not yet been tested.

## License and publication

MIT; see [LICENSE](LICENSE). The public package contains only generic guidance and fictional examples. Repository creation and public installation verification are being completed.
