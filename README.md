# claude.md

A `CLAUDE.md` template for AI coding agents — giving Claude (and other AI assistants) clear, opinionated instructions on how to work autonomously inside your codebase.

## What is `CLAUDE.md`?

`CLAUDE.md` is a special file that Anthropic's Claude reads at the start of every session. By adding one to your repository, you can define how Claude should behave: how it plans, how it manages tasks, and what core principles it should follow.

This repo provides a battle-tested template you can copy into any project.

## What's Inside

### Workflow Orchestration

| Principle | Description |
|---|---|
| **Plan Mode Default** | Enter plan mode for any non-trivial task (3+ steps or architectural decisions). Write detailed specs upfront to reduce ambiguity. |
| **Subagent Strategy** | Use subagents liberally to keep the main context window clean. Offload research, exploration, and parallel analysis. |
| **Self-Improvement Loop** | After any user correction, update `tasks/lessons.md` with the pattern so the same mistake isn't repeated. |
| **Verification Before Done** | Never mark a task complete without proving it works. Run tests, check logs, demonstrate correctness. |
| **Demand Elegance** | For non-trivial changes, pause and ask "is there a more elegant way?" Skip for simple, obvious fixes. |
| **Autonomous Bug Fixing** | When given a bug report, just fix it. Point at logs, errors, failing tests — then resolve them. |

### Task Management

1. **Plan First** — Write a plan to `tasks/todo.md` with checkable items
2. **Verify Plan** — Check in before starting implementation
3. **Track Progress** — Mark items complete as you go
4. **Explain Changes** — Provide a high-level summary at each step
5. **Document Results** — Add a review section to `tasks/todo.md`
6. **Capture Lessons** — Update `tasks/lessons.md` after corrections

### Core Principles

- **Simplicity First** — Make every change as simple as possible. Impact minimal code.
- **No Laziness** — Find root causes. No temporary fixes. Senior developer standards.
- **Minimal Impact** — Changes should only touch what's necessary. Avoid introducing bugs.

## Usage

Copy `CLAUDE.md` into the root of your repository:

```bash
curl -O https://raw.githubusercontent.com/gokulkrishh/claude.md/main/CLAUDE.md
```

Claude will automatically pick it up at the start of your next session.

## License

MIT © [Gokulakrishnan Kalaikovan](https://github.com/gokulkrishh)
