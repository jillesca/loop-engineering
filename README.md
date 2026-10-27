# Loop Engineering

**The architecture patterns behind autonomous AI agents.**

Stop prompting agents; design the loops that prompt them. This repo holds the material for my talk on loop engineering: how agent harnesses such as OpenClaw, Hermes Agent and Pi run an agent until a task is truly done, built on three ideas:

1. **The loop**: triggers, a task list, an agent call, a check and a write to disk, repeated, with deterministic stop conditions.
2. **Context engineering**: treat context as a budget; load skills on demand and keep state on disk, outside the window.
3. **Checking**: a generator is not its own evaluator; separate the agent that does the work from the one that checks it.

Most of this is good software engineering applied to a component that guesses: one job per step, control loops, CI gates and event logs.

## Sessions

| Date        | Event                         | Material                                                    |
| ----------- | ----------------------------- | ----------------------------------------------------------- |
| 27 Oct 2026 | Shift.Forward() · Build track | [talks/2026-10-shift-forward](talks/2026-10-shift-forward/) |

## What's here

- [`references.md`](references.md): every source behind the talk, grouped by type, plus a claim index and the product versions inspected.
- [`talks/`](talks/): one folder per session, with its abstract and slides.

Each session is also tagged at delivery (for example `shift-forward-2026`) so the exact version presented stays available.

## License

[MIT](LICENSE). Quotes and product facts belong to their authors; see `references.md` for sources.
