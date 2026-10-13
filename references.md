# Loop Engineering — references

Sources behind the talk *Loop Engineering: The Architecture Patterns Behind Autonomous AI Agents* (first given at Shift.Forward(), 27 Oct 2026), grouped by type; all links checked on 12–13 Oct 2026, and product docs are live pages read on those dates (exact versions at the end).

---

## Engineering blogs

### The hook

- Peter Steinberger — post on X (7 Jun 2026). https://x.com/steipete/status/2063697162748260627 — the opening quote
- Skye Jacobs, TechSpot — Meet "loop engineering": The next evolution in AI coding isn't a better prompt, it's a system that prompts itself (29 Jun 2026). https://www.techspot.com/news/112923-ai-developers-moving-beyond-prompts-loops-take-over.html — full wording of the opening quote
- Noelle Festa, WorkOS — Key takeaways from Boris Cherny on building Claude Code (2 Jun 2026). https://workos.com/blog/boris-cherny-claude-code-acquired-interview-takeaways — Cherny's "he writes loops" point, paraphrased
- WorkOS — Boris Cherny: Claude Code & the Future of Engineering, Acquired Unplugged presented by WorkOS (video, 2026). https://www.youtube.com/watch?v=RkQQ7WEor7w — the interview behind that recap

### Loops and harnesses

- Addy Osmani — Loop Engineering (7 Jun 2026). https://addyosmani.com/blog/loop-engineering/ — the loop's parts, the heartbeat, "split the verifier from the maker"
- Addy Osmani — Agent Harness Engineering (19 Apr 2026). https://addyosmani.com/blog/agent-harness-engineering/ — the ratchet; the figure the closing pillars are adapted from
- Addy Osmani — Long-running Agents (28 Apr 2026). https://addyosmani.com/blog/long-running-agents/ — the seven-step Ralph loop write-up, the three walls
- Vivek Trivedy, LangChain — The Anatomy of an Agent Harness (10 Mar 2026). https://www.langchain.com/blog/the-anatomy-of-an-agent-harness — "Agent = Model + Harness"
- Vivek Trivedy — The Claude Code SDK and the Birth of HaaS (Harness as a Service) (23 Sep 2025). https://www.vtrivedy.com/posts/claude-code-sdk-haas-harness-as-a-service — the levers you customise in a harness
- Mitchell Hashimoto — My AI Adoption Journey (5 Feb 2026). https://mitchellh.com/writing/my-ai-adoption-journey — the "harness engineering" idea: engineer a fix so a mistake never repeats
- Birgitta Böckeler, martinfowler.com — Harness engineering for coding agent users (2 Apr 2026). https://martinfowler.com/articles/harness-engineering.html — guides and sensors, computational vs inferential
- Birgitta Böckeler, martinfowler.com — Harness Engineering - first thoughts (17 Feb 2026). https://martinfowler.com/articles/exploring-gen-ai/harness-engineering-memo.html — early history of the term
- Kyle, HumanLayer — Skill Issue: Harness Engineering for Coding Agents (12 Mar 2026). https://www.humanlayer.dev/blog/skill-issue-harness-engineering-for-coding-agents — "success is silent", too many tools, sub-agents as a context firewall
- Dex Horthy, HumanLayer — Context-Efficient Backpressure for Coding Agents (9 Dec 2025). https://www.humanlayer.dev/blog/context-efficient-backpressure — hide passing output, show only failures
- Dex Horthy, HumanLayer — Advanced Context Engineering for Coding Agents (29 Aug 2025). https://www.humanlayer.dev/blog/advanced-context-engineering — keeping the window 40–60% full
- Dex Horthy, HumanLayer — 12-Factor Agents: Principles for building reliable LLM applications (2025–, living repo). https://github.com/humanlayer/12-factor-agents — "good agents are mostly just software"
- Geoffrey Huntley — Ralph Wiggum as a "software engineer" (14 Jul 2025). https://ghuntley.com/ralph/ — the original Ralph loop
- Ryan Carson — snarktank/ralph (GitHub repo). https://github.com/snarktank/ralph — a widely used Ralph implementation
- Simon Willison — Designing agentic loops (30 Sep 2025). https://simonwillison.net/2025/Sep/30/designing-agentic-loops/ — clear success criteria and tests make loops work
- Simon Willison — We're going to need default hard budget caps on pretty much everything (3 Oct 2026). https://simonwillison.net/2026/Oct/3/default-hard-budget-caps/ — hard caps as the default stop
- Wilson Lin, Cursor — Scaling long-running autonomous coding (14 Jan 2026). https://cursor.com/blog/scaling-agents — planners, workers and a judge at scale
- Ryan Lopopolo, OpenAI — Harness engineering: leveraging Codex in an agent-first world (11 Feb 2026). https://openai.com/index/harness-engineering/ — a short AGENTS.md as a map, lints as the gate

### Anthropic Engineering

- Erik S. and Barry Zhang, Anthropic — Building effective agents (19 Dec 2024). https://www.anthropic.com/engineering/building-effective-agents — the evaluator-optimizer workflow, compounding errors
- Anthropic Applied AI team — Effective context engineering for AI agents (29 Sep 2025). https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents — the "attention budget"
- Justin Young, Anthropic — Effective harnesses for long-running agents (26 Nov 2025). https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents — state on disk: feature list, progress file, git
- Prithvi Rajasekaran, Anthropic — Harness design for long-running application development (24 Mar 2026). https://www.anthropic.com/engineering/harness-design-long-running-apps — planner, generator and evaluator with an agreed contract
- Lance Martin, Gabe Cemaj and Michael Cohen, Anthropic — Scaling Managed Agents: Decoupling the brain from the hands (8 Apr 2026). https://www.anthropic.com/engineering/managed-agents — brain, hands and session log
- Siddharth Mishra-Sharma, Anthropic — Long-running Claude for scientific computing (23 Mar 2026). https://www.anthropic.com/research/long-running-Claude — a stop condition and a test gate in practice

### Patterns and naming

- Shubham Saboo, Google — Developer's guide to multi-agent patterns in ADK (16 Dec 2025). https://developers.googleblog.com/developers-guide-to-multi-agent-patterns-in-adk/ — "generator and critic"; monoliths don't scale
- OpenAI — A practical guide to building agents (PDF, undated). https://cdn.openai.com/business-guides-and-resources/a-practical-guide-to-building-agents.pdf — the agent runs in a loop until an exit condition
- Leela Kumili, InfoQ — news report on Anthropic's three-agent harness (4 Apr 2026). https://www.infoq.com/news/2026/04/anthropic-three-agent-harness-ai/ — secondary summary of the generator/evaluator post

---

## Research

### Long context

- Nelson F. Liu et al. — Lost in the Middle: How Language Models Use Long Contexts (TACL 2023). https://arxiv.org/abs/2307.03172 — the 2023 finding (2023 models)
- Kelly Hong, Anton Troynikov and Jeff Huber, Chroma — Context Rot: How Increasing Input Tokens Impacts LLM Performance (14 Jul 2025). https://www.trychroma.com/research/context-rot — 18 models get less reliable as input grows
- Ali Modarressi et al. — NoLiMa: Long-Context Evaluation Beyond Literal Matching (ICML 2025). https://arxiv.org/abs/2502.05167 — 13 long-context models degrade without literal matches
- Adobe Research — NoLiMa results table (GitHub README, updated Jun 2025). https://github.com/adobe-research/NoLiMa — advertised vs effective context length
- Cheng-Ping Hsieh et al., NVIDIA — RULER: What's the Real Context Size of Your Long-Context Language Models? (2024). https://arxiv.org/abs/2404.06654 — only half of 17 models hold up at 32K
- Kiran Vodrahalli et al., Google DeepMind — Michelangelo: Long Context Evaluations Beyond Haystacks via Latent Structure Queries (2024). https://arxiv.org/abs/2409.12640 — early sharp drop, then flat or linear decline
- Yufeng Du et al. — Context Length Alone Hurts LLM Performance Despite Perfect Retrieval (Oct 2025, preprint). https://arxiv.org/abs/2510.05381 — length hurts even with perfect retrieval (5 models)
- Blerta Veseli, Julian Chibane, Mariya Toneva and Alexander Koller — Positional Biases Shift as Inputs Approach Context Window Limits (Aug 2025, preprint). https://arxiv.org/abs/2508.07479 — the middle effect depends on how full the window is
- Nikolaus Salvatore, Hao Wang and Qiong Zhang — Lost in the Middle: An Emergent Property from Information Retrieval Demands in LLMs (Oct 2025, preprint). https://arxiv.org/abs/2510.10276 — why the U-shape appears
- Sam Martin and Fabien Roger — Classifier Context Rot: Monitor Performance Degrades with Context Length (May 2026, preprint). https://arxiv.org/abs/2605.12366 — 2026 frontier models miss more after 800K tokens
- Deli Huang et al. — ATLAS: All-round Testing of Long-context Abilities across Scales (May 2026, preprint). https://arxiv.org/abs/2605.28079 — 26 models from 8K to 1M tokens
- Thibaud Gloaguen et al., ETH Zurich and LogicStar.ai — Evaluating AGENTS.md: Are Repository-Level Context Files Helpful for Coding Agents? (v3, 29 Sep 2026). https://arxiv.org/abs/2602.11988 — context files raise cost more than success

### Errors that compound

- Muru Zhang et al. — How Language Model Hallucinations Can Snowball (2023). https://arxiv.org/abs/2305.13534 — early mistakes lead to more mistakes
- Samy Bengio et al. — Scheduled Sampling for Sequence Prediction with Recurrent Neural Networks (NeurIPS 2015). https://arxiv.org/abs/1506.03099 — models feed on their own output
- Mikhail L. Arbuzov et al. — Beyond Exponential Decay: Rethinking Error Accumulation in Large Language Models (v2, May 2026, not peer-reviewed). https://arxiv.org/abs/2505.24187 — the counter-argument to "exponential decay"

### Long tasks

- METR — Measuring AI Ability to Complete Long Tasks (19 Mar 2025, partly out of date). https://metr.org/blog/2025-03-19-measuring-ai-ability-to-complete-long-tasks/ — long chains of actions are harder than single steps
- METR — Time Horizon 1.1 (29 Jan 2026). https://metr.org/blog/2026-1-29-time-horizon-1-1/ — the updated trend
- METR — Time horizons (FAQ page, last updated 8 Sep 2026). https://metr.org/time-horizons/ — what a "time horizon" does and does not measure

### Vendor-reported evidence

- OpenAI — Introducing GPT-4.1 in the API (14 Apr 2025). https://openai.com/index/gpt-4-1/ — single-needle retrieval to 1M tokens; harder tasks still drop
- OpenAI Cookbook — GPT-4.1 Prompting Guide (14 Apr 2025). https://cookbook.openai.com/examples/gpt4-1_prompting_guide — long-context advice on instruction placement
- Google — Long context (Gemini API docs, updated 22 Jun 2026). https://ai.google.dev/gemini-api/docs/long-context — multiple needles are harder; avoid tokens you don't need
- Anthropic — Context windows (Claude docs, live). https://platform.claude.com/docs/en/build-with-claude/context-windows — "more context isn't automatically better"
- Anthropic — Long context prompting tips (Claude docs, now part of the prompting best practices). https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/long-context-tips — documents first, question last
- Anthropic — Introducing Claude Opus 4.6 (5 Feb 2026). https://www.anthropic.com/news/claude-opus-4-6 — context rot as "a common complaint"

---

## Product docs

### OpenClaw

- OpenClaw — openclaw/openclaw (GitHub repo). https://github.com/openclaw/openclaw — project home
- OpenClaw — Docs home. https://docs.openclaw.ai/ — the docs' own concept map
- OpenClaw — Why OpenClaw (vendor page). https://docs.openclaw.ai/start/why-openclaw — default security settings
- OpenClaw — Gateway architecture. https://docs.openclaw.ai/concepts/architecture — how the pieces connect
- OpenClaw — Agent loop. https://docs.openclaw.ai/concepts/agent-loop — how a turn runs and ends
- OpenClaw — Agent. https://docs.openclaw.ai/concepts/agent — the agent workspace and its files
- OpenClaw — Agent workspace. https://docs.openclaw.ai/concepts/agent-workspace — where workspace files live
- OpenClaw — Session. https://docs.openclaw.ai/concepts/session — resuming after a crash
- OpenClaw — System prompt. https://docs.openclaw.ai/concepts/system-prompt — what is always loaded
- OpenClaw — Memory. https://docs.openclaw.ai/concepts/memory — Markdown memory on disk
- OpenClaw — Compaction. https://docs.openclaw.ai/concepts/compaction — what happens when the window fills
- OpenClaw — Session pruning. https://docs.openclaw.ai/concepts/session-pruning — trimming old tool output
- OpenClaw — Multi-agent. https://docs.openclaw.ai/concepts/multi-agent — several agents, separate workspaces
- OpenClaw — Managed worktrees. https://docs.openclaw.ai/concepts/managed-worktrees — isolation for parallel work
- OpenClaw — Automation. https://docs.openclaw.ai/automation — what starts a run
- OpenClaw — Cron jobs: how it works. https://docs.openclaw.ai/automation/cron-jobs/how-it-works — scheduled runs
- OpenClaw — Standing orders. https://docs.openclaw.ai/automation/standing-orders — instructions that persist
- OpenClaw — Heartbeat. https://docs.openclaw.ai/gateway/heartbeat — the periodic wake-up
- OpenClaw — Sandboxing. https://docs.openclaw.ai/gateway/sandboxing — off by default
- OpenClaw — Config: extensions. https://docs.openclaw.ai/gateway/config-extensions — plugin configuration
- OpenClaw — Tools. https://docs.openclaw.ai/tools — tool policy
- OpenClaw — Goal. https://docs.openclaw.ai/tools/goal — goals and token budgets (opt-in)
- OpenClaw — Loop detection. https://docs.openclaw.ai/tools/loop-detection — stopping on repeated tool errors
- OpenClaw — Slash commands. https://docs.openclaw.ai/tools/slash-commands — starting work by command
- OpenClaw — Skills. https://docs.openclaw.ai/tools/skills — only the skill index is always loaded
- OpenClaw — Skill workshop. https://docs.openclaw.ai/tools/skill-workshop — writing skills
- OpenClaw — Plugins. https://docs.openclaw.ai/tools/plugin — how plugins extend the agent
- OpenClaw — MCP (tools). https://docs.openclaw.ai/tools/mcp — MCP servers as tools
- OpenClaw — MCP (CLI). https://docs.openclaw.ai/cli/mcp — managing MCP servers
- OpenClaw — Sub-agents. https://docs.openclaw.ai/tools/subagents — the parent reviews results
- OpenClaw — Sub-agents: tool reference. https://docs.openclaw.ai/tools/subagents/tool-reference — sub-agent options
- OpenClaw — Audit (CLI). https://docs.openclaw.ai/cli/audit — the audit ledger
- OpenClaw — Claws (CLI). https://docs.openclaw.ai/cli/claws — defining agents
- OpenClaw — A2A channel. https://docs.openclaw.ai/channels/a2a — agent-to-agent support

### Hermes Agent (Nous Research)

- Nous Research — NousResearch/hermes-agent (GitHub repo). https://github.com/NousResearch/hermes-agent — project home
- Hermes Agent — Docs home. https://hermes-agent.nousresearch.com/docs/ — project overview
- Hermes Agent — Features overview. https://hermes-agent.nousresearch.com/docs/user-guide/features/overview — Core, Automation, Media & Web, Integrations
- Hermes Agent — Integrations. https://hermes-agent.nousresearch.com/docs/integrations/ — integration list
- Hermes Agent — Architecture. https://hermes-agent.nousresearch.com/docs/developer-guide/architecture — how the parts fit
- Hermes Agent — Agent loop internals. https://hermes-agent.nousresearch.com/docs/developer-guide/agent-loop — how a turn runs
- Hermes Agent — Prompt assembly. https://hermes-agent.nousresearch.com/docs/developer-guide/prompt-assembly — what is always in the prompt
- Hermes Agent — Context compression and caching. https://hermes-agent.nousresearch.com/docs/developer-guide/context-compression-and-caching — compressing a full window
- Hermes Agent — Persistent goals. https://hermes-agent.nousresearch.com/docs/user-guide/features/goals — gates, then a judge, with a turn budget
- Hermes Agent — Cron. https://hermes-agent.nousresearch.com/docs/user-guide/features/cron — scheduled runs
- Hermes Agent — Heartbeat. https://hermes-agent.nousresearch.com/docs/user-guide/features/heartbeat — the periodic wake-up
- Hermes Agent — Hooks. https://hermes-agent.nousresearch.com/docs/user-guide/features/hooks — code at lifecycle points
- Hermes Agent — Memory. https://hermes-agent.nousresearch.com/docs/user-guide/features/memory — frozen memory snapshot
- Hermes Agent — Context files. https://hermes-agent.nousresearch.com/docs/user-guide/features/context-files — AGENTS.md and friends
- Hermes Agent — Skills. https://hermes-agent.nousresearch.com/docs/user-guide/features/skills — skills on demand
- Hermes Agent — Curator. https://hermes-agent.nousresearch.com/docs/user-guide/features/curator — maintaining skills
- Hermes Agent — Tools. https://hermes-agent.nousresearch.com/docs/user-guide/features/tools — built-in toolsets
- Hermes Agent — Tool search. https://hermes-agent.nousresearch.com/docs/user-guide/features/tool-search — loading tools on demand
- Hermes Agent — Code execution. https://hermes-agent.nousresearch.com/docs/user-guide/features/code-execution — running code as a tool
- Hermes Agent — MCP. https://hermes-agent.nousresearch.com/docs/user-guide/features/mcp — MCP servers
- Hermes Agent — Delegation. https://hermes-agent.nousresearch.com/docs/user-guide/features/delegation — child agents
- Hermes Agent — Delegation patterns. https://hermes-agent.nousresearch.com/docs/guides/delegation-patterns — verifier patterns
- Hermes Agent — Kanban. https://hermes-agent.nousresearch.com/docs/user-guide/features/kanban — "verify before complete" as guidance
- Hermes Agent — LSP. https://hermes-agent.nousresearch.com/docs/user-guide/features/lsp — the one checker on by default (git repos)
- Hermes Agent — Checkpoints and rollback. https://hermes-agent.nousresearch.com/docs/user-guide/checkpoints-and-rollback — opt-in checkpoints
- Hermes Agent — Profiles. https://hermes-agent.nousresearch.com/docs/user-guide/profiles — separate agent setups
- Hermes Agent — Personality. https://hermes-agent.nousresearch.com/docs/user-guide/features/personality — persona files
- Hermes Agent — Voice mode. https://hermes-agent.nousresearch.com/docs/user-guide/features/voice-mode — Media & Web feature
- Hermes Agent — Web dashboard. https://hermes-agent.nousresearch.com/docs/user-guide/features/web-dashboard — watching runs
- Hermes Agent — A2A. https://hermes-agent.nousresearch.com/docs/user-guide/messaging/a2a — agent-to-agent support

### Pi (Earendil)

- Earendil — earendil-works/pi (GitHub repo). https://github.com/earendil-works/pi — project home
- Pi — Docs. https://pi.dev/docs/latest — docs home
- Pi — How Pi works. https://pi.dev/docs/latest/how-pi-works — the loop: the model decides when it's done
- Pi — Quickstart. https://pi.dev/docs/latest/quickstart — first run
- Pi — Extensions. https://pi.dev/docs/latest/extensions — your own stop hooks and checks
- Pi — Configuration. https://pi.dev/docs/latest/configuration — AGENTS.md and settings
- Pi — Skills. https://pi.dev/docs/latest/skills — skill descriptions always loaded, bodies on demand
- Pi — Compaction. https://pi.dev/docs/latest/compaction — summary, history kept
- Pi — MCP. https://pi.dev/docs/latest/mcp — MCP tools
- Pi — JSON mode. https://pi.dev/docs/latest/json — the session event stream
- Pi — SDK. https://pi.dev/docs/latest/sdk — driving Pi from code
- Pi — Security. https://pi.dev/docs/latest/security — no approval step by default
- Pi — Packages. https://pi.dev/packages — bundling and sharing extensions
- Pi — pi-a2a (community package). https://pi.dev/packages/@bacnh85/pi-a2a — A2A via a package
- Pi — agent package README. https://github.com/earendil-works/pi/blob/main/packages/agent/README.md — how code can end a run
- Pi — telemetry package README. https://github.com/earendil-works/pi/blob/main/packages/telemetry/README.md — observability hooks
- Pi — sub-agent extension example. https://github.com/earendil-works/pi/blob/main/packages/coding-agent/examples/extensions/subagent/README.md — a reviewer sub-agent you add yourself
- Earendil — earendil-works/pi-chat (GitHub repo). https://github.com/earendil-works/pi-chat — chat-driven workers
- Earendil — Pi 1.0 (1 Oct 2026). https://earendil.com/posts/pi-1-0/ — the 1.0 release
- Earendil — Pi Durable (1 Oct 2026, experimental). https://earendil.com/posts/pi-durable/ — surviving crashes
- Earendil — What is a harness? (20 Aug 2026). https://earendil.com/posts/what-is-a-harness/ — Pi's own definition
- Earendil — You said no MCP (29 Sep 2026). https://earendil.com/posts/you-said-no-mcp/ — MCP support arrives in core
- Mario Zechner — What I learned building an opinionated and minimal coding agent (30 Nov 2025). https://mariozechner.at/posts/2025-11-30-pi-coding-agent/ — Pi's minimal design
- Mario Zechner — I've sold out (8 Apr 2026). https://mariozechner.at/posts/2026-04-08-ive-sold-out/ — Pi moves to Earendil

### Claude Code (Anthropic)

- Anthropic — How Claude Code works. https://code.claude.com/docs/en/how-claude-code-works — the agentic loop
- Anthropic — Glossary. https://code.claude.com/docs/en/glossary — Claude Code's own terms
- Anthropic — Features overview. https://code.claude.com/docs/en/features-overview — what loads every session vs on demand
- Anthropic — Best practices. https://code.claude.com/docs/en/best-practices — give Claude a way to verify its work
- Anthropic — Hooks reference. https://code.claude.com/docs/en/hooks — the Stop hook
- Anthropic — Hooks guide. https://code.claude.com/docs/en/hooks-guide — blocking a stop until a check passes
- Anthropic — /goal. https://code.claude.com/docs/en/goal — a fresh model judges "done" (opt-in)
- Anthropic — Agent SDK: the agent loop. https://code.claude.com/docs/en/agent-sdk/agent-loop — turns and budgets in the SDK
- Anthropic — Scheduled tasks. https://code.claude.com/docs/en/scheduled-tasks — runs on a schedule
- Anthropic — Routines (research preview). https://code.claude.com/docs/en/routines — saved, triggered workflows
- Anthropic — Headless mode. https://code.claude.com/docs/en/headless — running without a person at the keyboard
- Anthropic — Subagents. https://code.claude.com/docs/en/sub-agents — custom agents in files
- Anthropic — Plugins overview. https://code.claude.com/docs/en/plugins/overview — plugins bundle skills, subagents, hooks and MCP
- Anthropic — What's new, 2026 week 20. https://code.claude.com/docs/en/whats-new/2026-w20 — when /goal arrived
- Anthropic — Changelog (docs). https://code.claude.com/docs/en/changelog — release history
- Anthropic — Claude Code v2.1.277 release notes (18 Sep 2026). https://github.com/anthropics/claude-code/releases/tag/v2.1.277 — AGENTS.md is read when there is no CLAUDE.md
- Anthropic — ralph-wiggum plugin README. https://github.com/anthropics/claude-code/blob/main/plugins/ralph-wiggum/README.md — a Ralph loop as a plugin
- Delba de Oliveira and Michael Segner, Anthropic — Getting started with loops (30 Jun 2026). https://claude.com/blog/getting-started-with-loops — loops in Claude Code
- Thariq Shihipar, Anthropic — Building agents with the Claude Agent SDK (29 Sep 2025). https://claude.com/resources/articles/building-agents-with-the-claude-agent-sdk — verifying work, including a model as judge

### Codex (OpenAI)

- Michael Bolin, OpenAI — Unrolling the Codex agent loop (23 Jan 2026). https://openai.com/index/unrolling-the-codex-agent-loop/ — how the Codex harness loops
- OpenAI — Codex glossary. https://learn.chatgpt.com/docs/glossary — Codex's own terms
- OpenAI — AGENTS.md (Codex). https://learn.chatgpt.com/docs/agent-configuration/agents-md — the AGENTS.md chain
- OpenAI — Subagents (Codex). https://learn.chatgpt.com/docs/agent-configuration/subagents — custom agents in files
- OpenAI — Build skills. https://learn.chatgpt.com/docs/build-skills — skills in Codex
- OpenAI — Memories. https://learn.chatgpt.com/docs/customization/memories — what persists between sessions
- OpenAI — Developer commands. https://learn.chatgpt.com/docs/developer-commands — slash commands
- OpenAI — MCP (Codex). https://learn.chatgpt.com/docs/extend/mcp — MCP servers
- OpenAI — Sandboxing. https://learn.chatgpt.com/docs/sandboxing — sandbox and approval modes
- OpenAI — Auto-review. https://learn.chatgpt.com/docs/sandboxing/auto-review — reviewing approval requests at the sandbox boundary
- OpenAI — Long-running work. https://learn.chatgpt.com/docs/long-running-work — goals and budgets
- OpenAI — Hooks (Codex). https://learn.chatgpt.com/docs/hooks — code at lifecycle points
- OpenAI — Code review. https://learn.chatgpt.com/docs/code-review — a reviewer agent, opt-in
- OpenAI — GitHub integration. https://learn.chatgpt.com/docs/third-party/github — review on pull requests
- OpenAI — Non-interactive mode. https://learn.chatgpt.com/docs/non-interactive-mode — running Codex from scripts
- OpenAI — Codex SDK. https://learn.chatgpt.com/docs/codex-sdk — driving Codex from code
- OpenAI — Cloud environments. https://learn.chatgpt.com/docs/environments/cloud-environments — where cloud tasks run
- OpenAI — Prompting (Codex). https://learn.chatgpt.com/docs/prompting — prompting advice
- OpenAI — Automations (Codex). https://learn.chatgpt.com/docs/automations — scheduled work
- OpenAI — Codex rust-v0.128.0 release (30 Apr 2026). https://github.com/openai/codex/releases/tag/rust-v0.128.0 — when /goal arrived
- OpenAI — Codex pull request 18075. https://github.com/openai/codex/pull/18075 — how /goal marks a goal done
- OpenAI — Codex pull request 18076. https://github.com/openai/codex/pull/18076 — the budget soft stop

### Other tools and frameworks

- Microsoft — Custom agents in VS Code (docs, 7 Oct 2026). https://code.visualstudio.com/docs/agent-customization/custom-agents — custom agents in files
- Chad Kittel and Clayton Siemens, Microsoft — AI agent orchestration patterns (Azure Architecture Center, 12 Feb 2026). https://learn.microsoft.com/en-us/azure/architecture/ai-ml/guide/ai-agent-design-patterns — "maker-checker" and its synonyms
- LangChain — Workflows and agents (LangGraph docs). https://docs.langchain.com/oss/python/langgraph/workflows-agents — the evaluator-optimizer pattern
- OpenAI — Orchestrating multiple agents (Agents SDK docs). https://openai.github.io/openai-agents-python/multi_agent/ — a task agent plus an evaluator agent
- Google Cloud — Memory Bank (docs, updated 7 Oct 2026). https://docs.cloud.google.com/gemini-enterprise-agent-platform/scale/memory-bank — memory that persists across sessions

---

## Standards

- Suresh Krishnan and Frank Brockners, Cisco — BRKNWT-2622 Agentic AI Standards: An Overview (session slides; no public link). — the standards landscape this talk builds on
- Linux Foundation — Linux Foundation Announces the Formation of the Agentic AI Foundation (9 Dec 2025). https://www.linuxfoundation.org/press/linux-foundation-announces-the-formation-of-the-agentic-ai-foundation — the AAIF and its first projects
- Agentic AI Foundation — aaif.io. https://aaif.io/ — current project list
- Agentic AI Foundation — A2A joins AAIF (17 Aug 2026). https://aaif.io/blog/a2a-joins-aaif — A2A moves under the AAIF
- A2A project — A new chapter for A2A: joining the Agentic AI Foundation (27 Aug 2026). https://a2a-protocol.org/latest/blog/2026/08/27/a-new-chapter-for-a2a-joining-the-agentic-ai-foundation/ — the same move, from A2A's side
- Harald Kirschner, AAIF blog — From skills and tools to portable agent plugins (6 Aug 2026). https://aaif.io/blog/from-skills-and-tools-to-portable-agent-plugins — Agent Plugins 1.0, which leaves agents out
- Agent Plugins — agent-plugins.org. https://agent-plugins.org/ — the plugin spec and its steering committee
- Agent2Agent (A2A) — Protocol docs. https://a2a-protocol.org/latest/ — agents talking to agents
- Agent2Agent (A2A) — Specification. https://a2a-protocol.org/latest/specification/ — collaborate without sharing internals
- Model Context Protocol — Introduction. https://modelcontextprotocol.io/docs/getting-started/intro — tools for agents
- Model Context Protocol — Specification. https://modelcontextprotocol.io/specification/latest — the protocol itself
- AGENTS.md — agents.md. https://agents.md/ — plain-Markdown project instructions
- Agent Skills — agentskills.io. https://agentskills.io/home — the open skills format
- Agent Skills — Specification. https://agentskills.io/specification — the structure of a skill
- Agent Skills — agentskills/agentskills (GitHub repo). https://github.com/agentskills/agentskills — spec source
- Linux Foundation — Linux Foundation Welcomes the AGNTCY Project to Standardize Open Multi-Agent System Infrastructure and Break Down AI Agent Silos (29 Jul 2025). https://www.linuxfoundation.org/press/linux-foundation-welcomes-the-agntcy-project-to-standardize-open-multi-agent-system-infrastructure-and-break-down-ai-agent-silos — AGNTCY under the LF
- AGNTCY — agntcy.org. https://agntcy.org/ — the project
- AGNTCY — SLIM (GitHub repo). https://github.com/agntcy/slim — secure agent messaging
- AGNTCY — Open Agentic Schema Framework (OASF). https://docs.agntcy.org/oasf/open-agentic-schema-framework/ — agent discovery metadata
- IETF — Workload Identity in Multi System Environments (WIMSE) working group. https://datatracker.ietf.org/wg/wimse/about/ — identity for workloads and agents
- IETF — draft-schemacommons-aaif-00 (individual draft, last updated 25 Jun 2026). https://datatracker.ietf.org/doc/draft-schemacommons-aaif/ — no formal standing; unrelated to the Agentic AI Foundation

---

## Analogies & fundamentals

- Kubernetes — Controllers (docs). https://kubernetes.io/docs/concepts/architecture/controller/ — the reconcile loop: observe, compare, act
- Robert C. Martin — The Single Responsibility Principle (The Clean Code Blog, 8 May 2014). https://blog.cleancoder.com/uncle-bob/2014/05/08/SingleReponsibilityPrinciple.html — one reason to change
- Edsger W. Dijkstra — On the role of scientific thought (EWD447, 30 Aug 1974). https://www.cs.utexas.edu/~EWD/transcriptions/EWD04xx/EWD447.html — separation of concerns
- Wikipedia — Divide-and-conquer algorithm. https://en.wikipedia.org/wiki/Divide-and-conquer_algorithm — split a problem into smaller ones
- Martin Fowler — Event Sourcing (2005). https://martinfowler.com/eaaDev/EventSourcing.html — the log as the source of truth and the audit trail
- Martin Fowler — Continuous Integration (revised 18 Jan 2024). https://martinfowler.com/articles/continuousIntegration.html — only a green build counts as done

---

## Further reading

If you read six things in full, read these:

1. Addy Osmani — Loop Engineering. https://addyosmani.com/blog/loop-engineering/
2. Kyle, HumanLayer — Skill Issue: Harness Engineering for Coding Agents. https://www.humanlayer.dev/blog/skill-issue-harness-engineering-for-coding-agents
3. Prithvi Rajasekaran, Anthropic — Harness design for long-running application development. https://www.anthropic.com/engineering/harness-design-long-running-apps
4. Anthropic Applied AI team — Effective context engineering for AI agents. https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents
5. Birgitta Böckeler — Harness engineering for coding agent users. https://martinfowler.com/articles/harness-engineering.html
6. Ryan Lopopolo, OpenAI — Harness engineering: leveraging Codex in an agent-first world. https://openai.com/index/harness-engineering/

---

## Claim index

Some slides of the [Shift.Forward() session](talks/2026-10-shift-forward/) show small reference IDs (for example `R3-013`). Each one maps to the claim and source below. Claims were checked against their sources on 2026-10-12/13.

| ID | Claim | Source |
|---|---|---|
| R1-001 | LLM accuracy is highest when the relevant info is at the beginning or end of the input, and drops significantly when it's in the middle, even for long-context m… | https://arxiv.org/abs/2307.03172 |
| R1-002 | "In 2023 models, the position effect formed a U-shape (primacy and recency bias). Newer studies find position effects depend on the model and on how full the wi… | https://arxiv.org/html/2307.03172v3 |
| R1-004 | Extended-context model variants are not necessarily better at using their context. | https://arxiv.org/html/2307.03172v3 |
| R1-005 | Adding more context is a trade-off: more information, but more to reason over, which can lower accuracy. | https://arxiv.org/html/2307.03172v3 |
| R1-006 | Across 18 LLMs (incl. GPT-4.1, Claude 4, Gemini 2.5, Qwen3), performance becomes increasingly unreliable as input length grows. | https://research.trychroma.com/context-rot |
| R1-010 | Same question, same answer present: every model did significantly better on a focused ~300-token prompt than on the full ~113k-token prompt. | https://research.trychroma.com/context-rot |
| R1-011 | In autoregressive models, the model's output becomes part of its input; each token is conditioned on everything generated so far. | https://research.trychroma.com/context-rot |
| R1-015 | LLMs have an "attention budget"; every new token depletes it. | https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents |
| R1-016 | Why: every token attends to every other token (n² pairs), so with longer context attention is stretched thin; models also train mostly on shorter sequences. | https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents |
| R1-017 | The degradation is a gradient, not a hard cliff. | https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents |
| R1-018 | Design principle: use the smallest possible set of high-signal tokens. | https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents |
| R1-019 | Bigger windows won't fix it: all window sizes will face context pollution for the foreseeable future. | https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents |
| R1-020 | HumanLayer: too many MCP tools fill the context with tool descriptions and push the agent into the "dumb zone" faster. | https://www.humanlayer.dev/blog/skill-issue-harness-engineering-for-coding-agents |
| R1-021 | HumanLayer: delegating discrete tasks to sub-agents keeps the main thread in the "smart zone". | https://www.humanlayer.dev/blog/skill-issue-harness-engineering-for-coding-agents |
| R1-025 | ETH Zurich: context files (AGENTS.md etc.) don't generally improve coding-agent task success, but raise inference cost by >20% on average. | https://arxiv.org/abs/2602.11988 |
| R1-027 | v3 numbers: developer-written files +2.4% on average (p=21%); LLM-generated files −0.5% / −2% (no significant effect); steps and cost up in every setting. | https://arxiv.org/html/2602.11988v3 |
| R1-034 | "Hallucination snowballing": LMs over-commit to early mistakes and make more mistakes; ChatGPT and GPT-4 could separately identify 67% / 87% of their own mistak… | https://arxiv.org/abs/2305.13534 |
| R1-035 | Caveat: the "independent per-token error → exponential decay" argument (LeCun 2023) is contested; errors may concentrate at a few key tokens. | https://arxiv.org/html/2505.24187v2 |
| R1-036 | Anthropic: agent autonomy brings higher costs and the potential for compounding errors. | https://www.anthropic.com/research/building-effective-agents |
| R2-001 | Addy defines loop engineering as replacing yourself as the prompter; it sits one floor above the harness. | https://addyosmani.com/blog/loop-engineering/ |
| R2-002 | A loop needs five pieces plus memory: automations, worktrees, skills, plugins/connectors, sub-agents, then memory. | https://addyosmani.com/blog/loop-engineering/ |
| R2-003 | Loop memory must live on disk, outside the conversation. | https://addyosmani.com/blog/loop-engineering/ |
| R2-004 | Automations are the heartbeat that turns one run into a loop. | https://addyosmani.com/blog/loop-engineering/ |
| R2-006 | Maker/checker split: the authoring model grades its own work too generously. | https://addyosmani.com/blog/loop-engineering/ |
| R2-007 | Worktrees isolate parallel agents so their edits can't collide. | https://addyosmani.com/blog/loop-engineering/ |
| R2-008 | Skills write down project knowledge so the agent doesn't restart cold every session. | https://addyosmani.com/blog/loop-engineering/ |
| R2-009 | Even with a verifier, a loop's "done" is a claim, not a proof. | https://addyosmani.com/blog/loop-engineering/ |
| R2-010 | "A decent model with a great harness beats a great model with a bad harness" is Addy Osmani's own sentence. | https://addyosmani.com/blog/agent-harness-engineering/ |
| R2-011 | "Agent = Model + Harness. If you're not the model, you're the harness." (Vivek Trivedy). | https://blog.langchain.com/the-anatomy-of-an-agent-harness/ |
| R2-012 | A harness is everything that isn't the model; a raw model only becomes an agent once a harness is added. | https://blog.langchain.com/the-anatomy-of-an-agent-harness/ |
| R2-013 | Simon Willison: an agent runs tools in a loop to achieve a goal; the skill is designing tools and loop. | https://simonwillison.net/2025/Sep/30/designing-agentic-loops/ |
| R2-014 | Hashimoto calls it "harness engineering": each time an agent makes a mistake, engineer a fix so it never repeats. "Ratchet" is Addy Osmani's word. | https://mitchellh.com/writing/my-ai-adoption-journey#step-5-engineer-the-harness |
| R2-015 | Hashimoto: each line in an example Ghostty AGENTS.md file is based on a bad agent behavior, and it almost completely resolved them all. | https://mitchellh.com/writing/my-ai-adoption-journey#step-5-engineer-the-harness |
| R2-016 | Addy names the habit "the ratchet: every mistake becomes a rule". | https://addyosmani.com/blog/agent-harness-engineering/ |
| R2-017 | The ratchet runs both ways: add a rule only after a real failure, and remove it once the model no longer needs it. | https://addyosmani.com/blog/agent-harness-engineering/ |
| R2-020 | Huntley's earlier version of the ratchet: tune Ralph after each bad action, like putting up a sign. | https://ghuntley.com/ralph/ |
| R2-021 | Böckeler's "steering loop": when an issue happens repeatedly, improve the guides and sensors. | https://martinfowler.com/articles/harness-engineering.html |
| R2-022 | Guides (feedforward) steer before the agent acts; sensors (feedback) observe afterwards and help it self-correct. | https://martinfowler.com/articles/harness-engineering.html |
| R2-023 | You need both: feedback-only repeats the same mistakes, and feedforward-only never learns whether its rules worked. | https://martinfowler.com/articles/harness-engineering.html |
| R2-024 | Computational controls are deterministic and fast; inferential ones are semantic, slower and non-deterministic. | https://martinfowler.com/articles/harness-engineering.html |
| R2-027 | HumanLayer's wording: "success is silent, and only failures produce verbose output". | https://www.humanlayer.dev/blog/skill-issue-harness-engineering-for-coding-agents |
| R2-029 | Addy's punchier phrasing, credited to HumanLayer. | https://addyosmani.com/blog/agent-harness-engineering/ |
| R2-030 | A Stop hook stays silent on success; on failure it exits with code 2 and re-engages the agent. This is a deterministic "not done yet" gate. | https://www.humanlayer.dev/blog/skill-issue-harness-engineering-for-coding-agents |
| R2-031 | The three walls of long-running agents: finite context, no persistent state, no self-verification. | https://addyosmani.com/blog/long-running-agents/ |
| R2-033 | Addy's 7-step Ralph loop. | https://addyosmani.com/blog/long-running-agents/ |
| R2-034 | The original Ralph (Geoffrey Huntley) is a bash while-loop that feeds a prompt file to the agent. | https://ghuntley.com/ralph/ |
| R2-035 | Huntley's rule is one item per loop, because more context use means worse outcomes. | https://ghuntley.com/ralph/ |
| R2-036 | Ryan Carson's snarktank/ralph loops until every PRD story passes, with a completion-promise exit and max iterations. | https://github.com/snarktank/ralph |
| R2-037 | The Claude Code ralph-wiggum plugin uses a Stop hook with `--max-iterations` and an exact-match `--completion-promise`. | https://github.com/anthropics/claude-code/blob/main/plugins/ralph-wiggum/README.md |
| R2-038 | Anthropic: Ralph counters "agentic laziness" by kicking the agent back when it claims completion. | https://www.anthropic.com/research/long-running-Claude |
| R2-041 | Because the log lives outside the harness, a crashed harness reboots with `wake(sessionId)` and resumes from the last event. | https://www.anthropic.com/engineering/managed-agents |
| R2-042 | The session is a durable context store outside the context window; the brain queries it with `getEvents()`. | https://www.anthropic.com/engineering/managed-agents |
| R2-043 | Addy: the session-as-event-log is what makes a long-running agent recoverable. | https://addyosmani.com/blog/long-running-agents/ |
| R2-044 | Initializer agent + coding agent leaving clear artifacts (init.sh, claude-progress.txt, initial git commit). | https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents |
| R2-045 | The feature list is JSON with every item starting as failing. Agents may only flip `passes`, and removing tests is forbidden. | https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents |
| R2-046 | Compaction alone isn't enough for long-running work. | https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents |
| R2-047 | Each session starts the same way: pwd → read git log and progress → pick the top unfinished feature. | https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents |
| R2-048 | Failure mode: a later agent sees partial progress and declares the job done. | https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents |
| R2-049 | Three context-rot techniques: compaction, tool-call offloading, skills with progressive disclosure. | https://blog.langchain.com/the-anatomy-of-an-agent-harness/ |
| R2-050 | Too many MCP tools push the agent into the "dumb zone"; skills disclose instructions only when needed. | https://www.humanlayer.dev/blog/skill-issue-harness-engineering-for-coding-agents |
| R2-051 | Sub-agents work as a "context firewall". | https://www.humanlayer.dev/blog/skill-issue-harness-engineering-for-coding-agents |
| R2-052 | Self-evaluation bias: agents confidently praise mediocre work. | https://www.anthropic.com/engineering/harness-design-long-running-apps |
| R2-053 | A standalone skeptical evaluator is more tractable than a self-critical generator. | https://www.anthropic.com/engineering/harness-design-long-running-apps |
| R2-054 | Out of the box, Claude is a poor QA agent: it finds issues, then approves the work anyway. | https://www.anthropic.com/engineering/harness-design-long-running-apps |
| R2-055 | Planner / generator / evaluator: hard per-criterion thresholds fail a sprint, and a sprint contract agrees "done" before coding starts. | https://www.anthropic.com/engineering/harness-design-long-running-apps |
| R2-056 | Every harness component encodes an assumption about what the model can't do on its own. | https://www.anthropic.com/engineering/harness-design-long-running-apps |
| R2-057 | Context resets (fresh agent + structured handoff) differ from compaction. | https://www.anthropic.com/engineering/harness-design-long-running-apps |
| R2-064 | Addy: write down the done-condition before the agent starts, as an external file of testable criteria. | https://addyosmani.com/blog/long-running-agents/ |
| R2-065 | Addy: long runs need budgets, circuit breakers and a hard cap on tool spend. | https://addyosmani.com/blog/long-running-agents/ |
| R2-070 | Attribution conflict: Addy says Viv Trivedy coined "harness engineering", but Hashimoto used the term on 5 Feb 2026, before Viv's anatomy post (10 Mar 2026). | https://addyosmani.com/blog/agent-harness-engineering/ |
| R2-073 | Progress files should log failed approaches, or later sessions repeat the same dead ends. | https://www.anthropic.com/research/long-running-Claude |
| R2-074 | State lives outside the agent: the agent is amnesiac, but the filesystem isn't. | https://addyosmani.com/blog/long-running-agents/ |
| R2-075 | Hooks turn instructions into enforcement. | https://addyosmani.com/blog/agent-harness-engineering/ |
| R2-076 | Keep AGENTS.md short and earn each line: "Pilot's checklist, not style guide." | https://addyosmani.com/blog/agent-harness-engineering/ |
| R2-077 | Tools such as browsers, logs and test runners let agents build self-verification loops. | https://blog.langchain.com/the-anatomy-of-an-agent-harness/ |
| R2-078 | Hashimoto: given a way to verify its work, an agent usually fixes its own mistakes. | https://mitchellh.com/writing/my-ai-adoption-journey |
| R3-001 | The Gateway is OpenClaw's local control plane for sessions, tools, events and channels. | https://github.com/openclaw/openclaw |
| R3-003 | The agent loop is a serialized, per-session run: intake → context → inference → tools → streaming → persistence. | https://docs.openclaw.ai/concepts/agent-loop |
| R3-004 | Heartbeat runs a periodic main-session turn, every 30 minutes by default. | https://docs.openclaw.ai/automation |
| R3-007 | Automations are the built-in scheduler for all recurring and one-shot work, including heartbeat. | https://docs.openclaw.ai/automation |
| R3-010 | A goal is one durable objective per session that survives process restarts. | https://docs.openclaw.ai/tools/goal |
| R3-011 | Docs instruct that `update_goal` should mark a goal `complete` only when it is verified against the full objective. This is model guidance, not a runtime-enforc… | https://docs.openclaw.ai/tools/goal |
| R3-013 | An optional token budget stops goal pursuit by moving the goal to `budget_limited`. | https://docs.openclaw.ai/tools/goal |
| R3-015 | After a Gateway restart interrupts a turn, OpenClaw auto-continues the session, with a budget of 3 failed attempts. | https://docs.openclaw.ai/concepts/session |
| R3-016 | Replaying an interrupted turn reuses its recorded tool calls/results and the original user message (event-log-style recovery). | https://docs.openclaw.ai/concepts/session |
| R3-020 | Workspace bootstrap auto-injects AGENTS.md, SOUL.md, IDENTITY.md, USER.md, BOOTSTRAP.md and MEMORY.md. | https://docs.openclaw.ai/automation/standing-orders |
| R3-023 | Skills use progressive disclosure: a compact XML index in the prompt, with search and full reads on demand. | https://docs.openclaw.ai/tools/skills |
| R3-025 | Skill Workshop: the agent saves and fixes its own learned skills, reviews in the background after 10 iterations, and archives unused skills after 30 days. | https://docs.openclaw.ai/tools/skill-workshop |
| R3-026 | Cross-session memory is plain Markdown in the workspace, with no hidden state. | https://docs.openclaw.ai/concepts/memory |
| R3-029 | Compaction summarizes older turns near the context limit; the full history stays on disk. | https://docs.openclaw.ai/concepts/compaction |
| R3-030 | Before compacting, OpenClaw prompts the agent to save important notes to memory (memory flush). | https://docs.openclaw.ai/concepts/compaction |
| R3-036 | Sub-agents are background runs in their own session that announce their result to the requester for review. | https://docs.openclaw.ai/tools/subagents |
| R3-037 | Native sub-agents start with isolated (clean) context unless fork is explicitly requested. | https://docs.openclaw.ai/tools/subagents/tool-reference |
| R3-042 | Delegation mode is prompt guidance only; it does not enforce delegation. | https://docs.openclaw.ai/tools/subagents/tool-reference |
| R3-043 | With `completionTarget: "parent"`, the parent reviews the child's result and continues unfinished work. | https://docs.openclaw.ai/tools/subagents/tool-reference |
| R4-001 | Hermes' core agent loop executes tool calls and loops until the model returns a text response, then persists the session. | https://hermes-agent.nousresearch.com/docs/developer-guide/agent-loop |
| R4-003 | `/goal` keeps a standing objective across turns: a judge model checks after every turn and, if unmet, Hermes feeds a continuation prompt into the same session. … | https://hermes-agent.nousresearch.com/docs/user-guide/features/goals |
| R4-004 | Hermes describes `/goal` as its take on the Ralph loop, inspired by Codex CLI 0.128.0's `/goal`. | https://hermes-agent.nousresearch.com/docs/user-guide/features/goals |
| R4-005 | `/goal` has a default 20-turn continuation budget, after which it auto-pauses. | https://hermes-agent.nousresearch.com/docs/user-guide/features/goals |
| R4-006 | Quality gates are deterministic shell commands that must exit 0 before a goal can complete; a failing gate skips the judge and its output becomes the next promp… | https://hermes-agent.nousresearch.com/docs/user-guide/features/goals |
| R4-008 | The goal judge fails open: on judge error the verdict is "continue", and the turn budget is the backstop. | https://hermes-agent.nousresearch.com/docs/user-guide/features/goals |
| R4-009 | Goal state persists in the session DB, so a goal survives `/resume`. | https://hermes-agent.nousresearch.com/docs/user-guide/features/goals |
| R4-010 | Cron is run by the gateway daemon, which ticks every 60 s and runs due jobs in isolated, fresh agent sessions (no history). Jobs can also be fired by webhooks. | https://hermes-agent.nousresearch.com/docs/user-guide/features/cron |
| R4-011 | Cron keeps an execution ledger: attempts end in one immutable terminal state, abandoned "unknown" attempts are never automatically rerun, and a tick lock preven… | https://hermes-agent.nousresearch.com/docs/user-guide/features/cron |
| R4-014 | `/heartbeat` re-enters the current session with one recurring prompt when idle; missed ticks coalesce. | https://hermes-agent.nousresearch.com/docs/user-guide/features/heartbeat |
| R4-015 | On messaging platforms a chat is one continuous session that survives restarts, gateway crashes and reboots. | https://hermes-agent.nousresearch.com/docs/user-guide/features/memory |
| R4-016 | Skills are on-demand documents using progressive disclosure (Level 0 index → Level 1 full skill → Level 2 reference file) and are compatible with the agentskill… | https://hermes-agent.nousresearch.com/docs/user-guide/features/skills |
| R4-017 | The agent creates and updates its own skills via `skill_manage` ("procedural memory"), including when the user corrects its approach. | https://hermes-agent.nousresearch.com/docs/user-guide/features/skills |
| R4-020 | Built-in memory is two small files (MEMORY.md 2,200 chars, USER.md 1,375 chars), injected as a frozen snapshot at session start. Mid-session writes are invisibl… | https://hermes-agent.nousresearch.com/docs/user-guide/features/memory |
| R4-023 | Compression triggers at 50% of the context window (85% in the gateway), flushes memory first, summarises middle turns, protects the last N messages and starts a… | https://hermes-agent.nousresearch.com/docs/developer-guide/agent-loop |
| R4-024 | Phase 1 of compaction is a cheap, no-LLM pass that replaces old tool outputs with a placeholder (tool-output offloading). | https://hermes-agent.nousresearch.com/docs/developer-guide/context-compression-and-caching |
| R4-025 | Hermes loads one project context type per session (first match: .hermes.md → AGENTS.override.md → AGENTS.md → CLAUDE.md → .cursorrules), merges AGENTS.md from g… | https://hermes-agent.nousresearch.com/docs/user-guide/features/context-files |
| R4-027 | MCP ships with the standard install, supports stdio and HTTP servers, and has per-server tool filtering. | https://hermes-agent.nousresearch.com/docs/user-guide/features/mcp |
| R4-029 | Tool Search replaces MCP/plugin tool schemas with three bridge tools and loads schemas on demand (progressive disclosure for tools). | https://hermes-agent.nousresearch.com/docs/user-guide/features/tool-search |
| R4-032 | `delegate_task` spawns children with isolated context and their own terminal sessions; only the child's final summary enters the parent's context. | https://hermes-agent.nousresearch.com/docs/user-guide/features/delegation |
| R4-037 | Subagents share the parent's working directory by default; opt-in `worktree_isolation` gives each child its own git worktree and branch. | https://hermes-agent.nousresearch.com/docs/user-guide/features/delegation |
| R4-039 | hermes kanban swarm builds a root card, parallel worker cards, a verifier card gated on all workers and a synthesizer gated on the verifier. Workers are told to… | https://hermes-agent.nousresearch.com/docs/user-guide/features/kanban |
| R4-040 | The delegation guide suggests a fresh-context subagent for code review and tells the parent to verify subagent claims by running the tests or reading the diff; … | https://hermes-agent.nousresearch.com/docs/guides/delegation-patterns |
| R4-041 | Inside a git workspace with an available (and, where required, trusted) language server, each write_file/patch surfaces only the diagnostics that the edit intro… | https://hermes-agent.nousresearch.com/docs/user-guide/features/lsp |
| R5-001 | Pi describes itself as a minimal, extensible agent harness. | https://github.com/earendil-works/pi |
| R5-002 | Pi was created by Mario Zechner; the repo moved from badlogic/pi-mono to earendil-works/pi and Pi is owned by Earendil, with Zechner in charge of decisions alon… | https://mariozechner.at/posts/2026-04-08-ive-sold-out/ |
| R5-006 | One turn = model response + executed tool calls; Pi starts another turn only if tool results or queued messages require it, otherwise the run ends (model-driven… | https://pi.dev/docs/latest/how-pi-works |
| R5-008 | pi-agent-core exposes programmatic stop hooks: finishTurn can return { action: "end" } to end the run after turn_end; tools or afterToolCall can return terminat… | https://github.com/earendil-works/pi/blob/main/packages/agent/README.md |
| R5-011 | Automation of Pi is external: print mode for scripted tasks, JSON event stream, RPC to control a separate process, SDK to embed. (No built-in scheduler/cron doc… | https://pi.dev/docs/latest |
| R5-012 | Pi the coding agent has no automatic crash recovery: a human inspects and tells it to continue. | https://earendil.com/posts/pi-durable/ |
| R5-014 | Pi Durable checkpoints every step as a task and resumes unfinished tasks from the last checkpoint after a crash; app state lives in documents committed with the… | https://earendil.com/posts/pi-durable/ |
| R5-015 | Pi Durable is experimental and its API may change. | https://earendil.com/posts/pi-durable/ |
| R5-017 | Pi loads AGENTS.md / CLAUDE.md context files from the agent dir, working dir and parent dirs. | https://pi.dev/docs/latest/configuration |
| R5-019 | Pi implements the Agent Skills spec (SKILL.md) with progressive disclosure: only name/description/path go into the system prompt at startup. | https://pi.dev/docs/latest/skills |
| R5-020 | Auto-compaction triggers when context exceeds window minus a reserve (default 16,384 tokens) and writes a structured summary (Goal, Progress, Next Steps…). | https://pi.dev/docs/latest/compaction |
| R5-021 | Compaction is non-destructive: original entries stay in the session tree. | https://pi.dev/docs/latest/how-pi-works |
| R5-025 | MCP tools default to `codemode` exposure (not declared to the model); `deferred` loads via tool_search; only `direct` is declared like a built-in, which limits … | https://pi.dev/docs/latest/mcp |
| R5-028 | Pi deliberately ships without sub-agents and plan mode; users build or install them. | https://github.com/earendil-works/pi |
| R5-029 | The repo's example subagent extension runs each subagent in a separate `pi` process (isolated context) and includes a worker → reviewer → worker workflow. | https://github.com/earendil-works/pi/blob/main/packages/coding-agent/examples/extensions/subagent/README.md |
| R5-031 | Pi has no built-in permission system; isolation is via containerization (Gondolin micro-VM extension, Docker, OpenShell). | https://github.com/earendil-works/pi |
| R5-032 | Pi Durable has no built-in subagents but makes them a few lines of code; a reviewer conversation can use a cheaper model, read-only tools, and its own checkout. | https://earendil.com/posts/pi-durable/ |
| R5-035 | OpenClaw is built on Pi. | https://mariozechner.at/posts/2026-04-08-ive-sold-out/ |
| R6-001 | BRKNWT-2622 "Agentic AI Standards: An Overview" is by Suresh Krishnan (Distinguished Engineer, Cisco) and Frank Brockners (Distinguished Engineer, Outshift by C… | BRKNWT-2622 deck (Cisco), page=1 |
| R6-004 | The Linux Foundation formed AAIF on 2025-12-09 with founding contributions MCP (Anthropic), goose (Block) and AGENTS.md (OpenAI). | https://www.linuxfoundation.org/press/linux-foundation-announces-the-formation-of-the-agentic-ai-foundation |
| R6-006 | On 2026-10-12, aaif.io lists AGENTS.md, goose, MCP, agentgateway, A2A and Agent Router as projects. Agent Skills and AGNTCY are not listed. | https://aaif.io/ |
| R6-007 | A2A joined AAIF as a hosted project, announced 2026-08-17. | https://aaif.io/blog/a2a-joins-aaif |
| R6-008 | The A2A project says it was accepted as a Growth Stage project at AAIF. | https://a2a-protocol.org/latest/blog/2026/08/27/a-new-chapter-for-a2a-joining-the-agentic-ai-foundation/ |
| R6-011 | A2A is for agent-to-agent communication and MCP is for agent-to-tool. A2A is not a sub-agent or tool-call protocol. | https://a2a-protocol.org/latest/ |
| R6-012 | MCP is an open-source standard for connecting AI applications to external systems. | https://modelcontextprotocol.io/docs/getting-started/intro |
| R6-015 | AGENTS.md is a simple, open format for guiding coding agents, described as a "README for agents". | https://agents.md/ |
| R6-016 | The Agentic AI Foundation, under the Linux Foundation, stewards AGENTS.md. | https://agents.md/ |
| R6-018 | Agent Skills is an open format: a skill is a folder with a SKILL.md file (name and description metadata plus instructions). | https://agentskills.io/home |
| R6-019 | Agent Skills loads progressively in three tiers: metadata (~100 tokens), instructions (<5000 tokens recommended), and resources as needed. | https://agentskills.io/specification |
| R6-020 | Anthropic originally developed the Agent Skills format and released it as an open standard. The site names no foundation as its home. | https://agentskills.io/home ; https://github.com/agentskills/agentskills |
| R6-022 | The LF welcomed AGNTCY on 2025-07-29, with Cisco, Dell Technologies, Google Cloud, Oracle and Red Hat as formative members. | https://www.linuxfoundation.org/press/linux-foundation-welcomes-the-agntcy-project-to-standardize-open-multi-agent-system-infrastructure-and-break-down-ai-agent-silos |
| R6-023 | Cisco open-sourced AGNTCY in March 2025, with LangChain and Galileo. | (same as R6-022) |
| R6-024 | AGNTCY's core features are discovery via OASF, verifiable identity, messaging via SLIM, and observability. | (same as R6-022) |
| R6-025 | agntcy.org lists a TSC of Cisco, Dell, Google, Oracle and Red Hat. AGNTCY is a Series of LF Projects, LLC. | https://agntcy.org/ |
| R6-028 | IETF WIMSE is an active working group in the ART area, chartered on workload identity, that builds on OAuth, JWT and SPIFFE. | https://datatracker.ietf.org/wg/wimse/about/ |
| R6-029 | The deck says identity and authorization for distributed multi-agent systems are a "center of gravity". | BRKNWT-2622 deck (Cisco), page=86 |
| R6-031 | In June 2026 the deck labelled A2A an LF project, not an AAIF one (superseded by R6-007). | BRKNWT-2622 deck (Cisco), page=31 |
| R6-032 | OpenClaw supports MCP servers (stdio and remote) configured under `mcp.servers`. | https://docs.openclaw.ai/gateway/config-extensions.md |
| R6-034 | OpenClaw follows the AgentSkills spec (SKILL.md with YAML frontmatter). | https://docs.openclaw.ai/tools/skills.md |
| R6-038 | Hermes Agent treats AGENTS.md as its primary project context file. | https://hermes-agent.nousresearch.com/docs/user-guide/features/context-files |
| R6-040 | Pi connects to MCP servers over stdio or streamable HTTP (built in). | https://pi.dev/docs/latest/mcp |
| R6-041 | Pi implements the Agent Skills specification. | https://pi.dev/docs/latest/skills |
| R6-042 | Pi loads AGENTS.md (or CLAUDE.md) context files from the agent directory, the working directory and its parents. | https://pi.dev/docs/latest/configuration |
| R7-001 | Peter Steinberger on X, 7 Jun 2026: "Here's your monthly reminder that you shouldn't be prompting coding agents anymore. You should be designing loops that prom… | https://x.com/steipete/status/2063697162748260627 |
| R7-002 | Addy Osmani quotes Steinberger and links to that exact status | https://addyosmani.com/blog/loop-engineering/ |
| R7-003 | TechSpot (29 Jun 2026) reproduces the full wording, including "monthly reminder", and says he wrote it on X. | https://www.techspot.com/news/112923-ai-developers-moving-beyond-prompts-loops-take-over.html |
| R7-005 | Steinberger is described as an OpenAI engineer and creator of OpenClaw | https://www.techspot.com/news/112923-ai-developers-moving-beyond-prompts-loops-take-over.html |
| R7-006 | WorkOS's recap (2 Jun 2026) says Cherny described writing loops at Acquired Unplugged, presented by WorkOS. No first-party Cherny post containing the line was f… | https://workos.com/blog/boris-cherny-claude-code-acquired-interview-takeaways |
| R7-011 | Cherny's role: head of Claude Code at Anthropic | https://addyosmani.com/blog/loop-engineering/ |
| R7-016 | MDN advises keeping jobs short and splitting a long job into several | https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Execution_model |
| R7-020 | A control loop regulates a system toward desired state (thermostat example) | https://kubernetes.io/docs/concepts/architecture/controller/ |
| R7-021 | K8s controllers drive current state toward the desired state held in the object's spec | https://kubernetes.io/docs/concepts/architecture/controller/ |
| R7-022 | For a Job, the desired state is "completed", and the controller marks it Finished | https://kubernetes.io/docs/concepts/architecture/controller/ |
| R7-023 | Caveat: the controller loop itself never terminates, and a cluster may never be stable | https://kubernetes.io/docs/concepts/architecture/controller/ |
| R7-024 | K8s prefers many simple controllers over one monolithic loop | https://kubernetes.io/docs/concepts/architecture/controller/ |
| R7-026 | Mapping: "each task runs until actual = desired" ≈ a deterministic stop condition checked against observable state | n/a (speaker's analogy) |
| R7-035 | CS divide and conquer: split into sub-problems until each is simple, then combine | https://en.wikipedia.org/wiki/Divide-and-conquer_algorithm |
| R8-001 | Claude Code's docs name the core cycle the "agentic loop": gather context, take action, verify results; the model decides each next step. | https://code.claude.com/docs/en/how-claude-code-works |
| R8-002 | Claude Code defines itself as the "agentic harness": the layer around the model that provides tools and manages context. | https://code.claude.com/docs/en/how-claude-code-works |
| R8-007 | First-party confirmation of R2-030: a Stop hook exiting with code 2 prevents Claude from stopping and sends it back to work. | https://code.claude.com/docs/en/hooks |
| R8-008 | Safety valve: Claude Code overrides a Stop hook after eight consecutive blocks with no tool call in between. | https://code.claude.com/docs/en/hooks-guide |
| R8-009 | Prompt hooks let a model decide a Stop (reason fed back to Claude); agent hooks spawn a subagent with tools to verify; agent hooks are experimental. | https://code.claude.com/docs/en/hooks-guide |
| R8-011 | Default stop is model judgment: Claude stops when the work looks done; without a runnable check, you become the verification loop. | https://code.claude.com/docs/en/best-practices |
| R8-012 | Mechanically, the loop ends when Claude produces output with no tool calls. | https://code.claude.com/docs/en/agent-sdk/agent-loop |
| R8-014 | `/goal` is a session-scoped prompt-based Stop hook evaluated by the configured small fast model (confirms R2-005). | https://code.claude.com/docs/en/goal |
| R8-015 | With `/goal`, completion is decided by a fresh model, not the one doing the work. | https://code.claude.com/docs/en/goal |
| R8-016 | The `/goal` evaluator does not run commands, read files or call tools; it judges only what Claude surfaced in the conversation. | https://code.claude.com/docs/en/goal |
| R8-017 | A `/goal` turn or time cap is written into the condition text and judged by the evaluator from the conversation. | https://code.claude.com/docs/en/goal |
| R8-021 | `/goal` vs Stop hook: both fire after every turn; a Stop hook lives in settings and can run a script (deterministic) or a prompt (model-evaluated). | https://code.claude.com/docs/en/goal |
| R8-022 | `/loop` and cron tools re-run a prompt on an interval; scheduled tasks are session-scoped. | https://code.claude.com/docs/en/scheduled-tasks |
| R8-025 | Recurring `/loop` tasks expire after 7 days, bounding forgotten loops. | https://code.claude.com/docs/en/scheduled-tasks |
| R8-026 | Routines (research preview) are saved prompt + repos + connectors that run in the cloud on schedule, API or GitHub triggers, and keep working with the laptop cl… | https://code.claude.com/docs/en/routines |
| R8-033 | "Agent SDK caps: `maxTurns` limits tool-use turns and `maxBudgetUsd` stops the loop once estimated spend reaches the cap (it can overshoot by one response). Bot… | https://code.claude.com/docs/en/agent-sdk/agent-loop |
| R8-034 | Every message, tool use and result is written to a plaintext JSONL session file, enabling rewind, resume and fork. | https://code.claude.com/docs/en/how-claude-code-works |
| R8-039 | CLAUDE.md loads at the start of every session after the system prompt; scopes concatenate; project-root CLAUDE.md survives compaction. | https://code.claude.com/docs/en/glossary |
| R8-040 | AGENTS.md support added in v2.1.277: read when a project has no CLAUDE.md. | https://code.claude.com/docs/en/changelog |
| R8-041 | Auto memory: Claude-written notes per repo; first 200 lines / 25 KB of MEMORY.md load every session. | https://code.claude.com/docs/en/glossary |
| R8-043 | Context cost by feature: skills load descriptions at start and full content when used; hooks cost zero unless they return context. | https://code.claude.com/docs/en/features-overview |
| R8-045 | MCP tool definitions are deferred by default (tool search); only names and server instructions use context until used. | https://code.claude.com/docs/en/how-claude-code-works |
| R8-047 | Plugins bundle skills, agents, hooks and MCP servers as one unit; an enabled plugin's invocable descriptions are in context every turn. | https://code.claude.com/docs/en/plugins/overview |
| R8-048 | Docs: a rule in CLAUDE.md or a skill is a request; a blocking hook is enforcement. | https://code.claude.com/docs/en/features-overview |
| R8-049 | The docs' gating ladder: prompt → `/goal` → Stop hook (deterministic gate) → second-opinion subagent or workflow, so the worker isn't the grader. | https://code.claude.com/docs/en/best-practices |
| R8-050 | Adversarial review: a fresh-context reviewer subagent sees only the diff and criteria; bundled `/code-review` does this; reviewers over-report gaps. | https://code.claude.com/docs/en/best-practices |
| R8-064 | Agent teams (multiple coordinated sessions with a lead) are experimental and off by default. | https://code.claude.com/docs/en/glossary |
| R9-002 | Codex is OpenAI's coding agent; the glossary lists it across desktop app, CLI, IDE extension, web, cloud and SDK. | https://learn.chatgpt.com/docs/glossary.md |
| R9-003 | OpenAI calls the Codex harness the core agent loop and execution logic shared by all Codex experiences. | https://openai.com/index/unrolling-the-codex-agent-loop/ |
| R9-004 | The agent loop repeats tool calls until the model returns an assistant message, which ends the turn; the model decides when it is done. | https://openai.com/index/unrolling-the-codex-agent-loop/ |
| R9-009 | Codex reads AGENTS.md files before doing any work, building an instruction chain once per run. | https://learn.chatgpt.com/docs/agent-configuration/agents-md.md |
| R9-010 | The chain goes global → project root → cwd, at most one file per directory, concatenated so that closer files override earlier ones. | https://learn.chatgpt.com/docs/agent-configuration/agents-md.md |
| R9-011 | Codex stops adding AGENTS.md content at 32 KiB by default (project_doc_max_bytes). | https://learn.chatgpt.com/docs/agent-configuration/agents-md.md |
| R9-013 | Skills use progressive disclosure; the initial skills list uses at most 2% of the context window (or 8,000 characters). | https://learn.chatgpt.com/docs/build-skills.md |
| R9-015 | Local Codex memories are off by default and are a recall layer; required guidance belongs in AGENTS.md. | https://learn.chatgpt.com/docs/customization/memories.md |
| R9-019 | The sandbox is the boundary that lets the agent act autonomously, and it applies to spawned commands. | https://learn.chatgpt.com/docs/sandboxing.md |
| R9-020 | Sandbox and approvals are separate controls: the sandbox sets boundaries, the approval policy decides when to stop and ask. | https://learn.chatgpt.com/docs/sandboxing.md |
| R9-023 | The common approval policies are `on-request` and `never` (a granular policy also exists); `untrusted` is no longer selectable. | https://learn.chatgpt.com/docs/sandboxing.md |
| R9-024 | Auto-review replaces the human approver at the sandbox boundary with a separate reviewer agent, without granting permissions. | https://learn.chatgpt.com/docs/sandboxing/auto-review.md |
| R9-026 | OpenAI states auto-review is not a deterministic security guarantee. | https://learn.chatgpt.com/docs/sandboxing/auto-review.md |
| R9-027 | With `/goal`, the goal text is both the first prompt and the completion criteria. | https://learn.chatgpt.com/docs/long-running-work.md |
| R9-028 | The docs ask for goals that let the agent verify its own progress, with tests or measurements as verification. | https://learn.chatgpt.com/docs/long-running-work.md |
| R9-030 | In goal mode the model can only mark a goal complete; pause, resume, clear and budget-limited transitions belong to the user or runtime. | https://github.com/openai/codex/pull/18075 |
| R9-031 | The goal runtime starts continuation turns when idle, treats budget exhaustion as a soft stop, suppresses continuation after a turn with no tool calls, and reac… | https://github.com/openai/codex/pull/18076 |
| R9-034 | A `Stop` hook returning decision "block" makes Codex continue, with the reason as a new continuation prompt. | https://learn.chatgpt.com/docs/hooks.md |
| R9-038 | Custom agents are standalone TOML files in ~/.codex/agents/ or .codex/agents/ that must define name, description and developer_instructions; the format may evol… | https://learn.chatgpt.com/docs/agent-configuration/subagents.md |
| R9-040 | `/review` starts a dedicated reviewer that reads the diff and reports findings without changing the working tree; reviews can use a different model. | https://learn.chatgpt.com/docs/code-review.md |
| R9-041 | On GitHub, `@codex review` (or automatic review) posts a review that flags only P0 and P1 issues. | https://learn.chatgpt.com/docs/third-party/github.md |
| R9-043 | Sessions can be resumed (`codex resume`, `codex exec resume`) and forked (`codex fork`); session rollout files persist to disk unless `--ephemeral` is used, and… | https://learn.chatgpt.com/docs/non-interactive-mode.md |
| R9-052 | OpenAI's harness team keeps a ~100-line AGENTS.md as a table of contents into a structured docs/ system of record. | https://openai.com/index/harness-engineering/ |
| R9-054 | OpenAI's team has Codex request agent reviews and iterate until all agent reviewers are satisfied, a Ralph Wiggum Loop. | https://openai.com/index/harness-engineering/ |
| R9-055 | Architecture is enforced by custom linters and structural tests whose error messages inject remediation instructions into agent context. | https://openai.com/index/harness-engineering/ |
| R10-001 | NoLiMa: across 13 LLMs claiming ≥128K context, performance degrades significantly as context grows; at 32K, 11 fall below half their short-context baseline. | https://arxiv.org/abs/2502.05167 |
| R10-004 | On NoLiMa, GPT-4.1 (claimed 1M) has an effective length of 16K, i.e. the longest context where it keeps ≥85% of its base score. | https://github.com/adobe-research/NoLiMa |
| R10-005 | RULER (2024): almost all 17 long-context models drop sharply as length grows; only half hold up at 32K despite claiming ≥32K. | https://arxiv.org/abs/2404.06654 |
| R10-007 | Even with perfect retrieval, performance drops 13.9–85% as input grows, including when the filler is whitespace or masked, and when evidence sits right before t… | https://arxiv.org/abs/2510.05381 |
| R10-009 | Position effects are conditional: "lost in the middle" is strongest when input fills ≤50% of the window; beyond that it becomes a recency/distance bias (open mo… | https://arxiv.org/abs/2508.07479 |
| R10-011 | Contradicting (vendor): GPT-4.1 retrieves a single needle at all positions up to 1M tokens. | https://openai.com/index/gpt-4-1/ |
| R10-012 | OpenAI: GPT-4.1 long-context performance can degrade as more items must be retrieved or with reasoning over the whole context. | https://cookbook.openai.com/examples/gpt4-1_prompting_guide |
| R10-013 | OpenAI: in long context, place instructions at both the beginning and end; placement affects performance. | https://cookbook.openai.com/examples/gpt4-1_prompting_guide |
| R10-016 | Contradicting (vendor): Google says Gemini can extract information from a large context with up to 99% accuracy in many cases. | https://ai.google.dev/gemini-api/docs/long-context |
| R10-017 | Anthropic docs (current): more context isn't automatically better; accuracy and recall degrade as tokens grow ("context rot"), so curation matters. | https://platform.claude.com/docs/en/build-with-claude/context-windows |
| R10-018 | Anthropic: for 20k+ token inputs, put long documents at the top and the query at the end, which can improve quality by up to 30%. | https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/long-context-tips |
| R10-020 | 2026: as transcript monitors, Opus 4.6, GPT 5.4 and Gemini 3.1 miss dangerous actions 2× to 30× more often after 800K tokens of benign activity. | https://arxiv.org/abs/2605.12366 |
| R10-021 | Same study: prompting techniques such as periodic reminders only partly mitigate it (a harness fix). | https://arxiv.org/abs/2605.12366 |
| R10-022 | ATLAS (2026, 26 models, 8K–1M): most models degrade roughly linearly on a log-length axis to 128K; beyond 128K some decline gradually, others hit cliffs. | https://arxiv.org/html/2605.28079v1 |
| R10-023 | ATLAS: degradation is capability-specific; e.g. GPT-5.2's Retrieval decays 46.4% from 128K to 1M while its ICL stays strong. | https://arxiv.org/html/2605.28079v1 |
| R11-001 | VS Code custom agents bundle instructions, tools and an optional model into a reusable role, defined in `.agent.md` Markdown files. | https://code.visualstudio.com/docs/agent-customization/custom-agents |
| R11-005 | VS Code also reads Claude Code's sub-agent format from `.claude/agents` and maps Claude tool names to VS Code tools. | https://code.visualstudio.com/docs/agent-customization/custom-agents |
| R11-006 | Claude Code subagents are Markdown files with YAML frontmatter; the body becomes the subagent's system prompt. | https://code.claude.com/docs/en/sub-agents |
| R11-009 | Codex custom agents are standalone TOML files, one per file, in `~/.codex/agents/` (personal) or `.codex/agents/` (project). | https://developers.openai.com/codex/subagents.md |
| R11-010 | A Codex custom agent must define `name`, `description` and `developer_instructions`, and may set other config keys such as model, reasoning effort, sandbox mode… | https://developers.openai.com/codex/subagents.md |
| R11-011 | OpenAI says the Codex custom-agent file reuses session config, may feel heavier than a dedicated manifest, and may change. | https://developers.openai.com/codex/subagents.md |
| R11-015 | OpenClaw's Claw is an experimental, versioned package for one agent; its `CLAW.md` has YAML frontmatter and a Markdown body applied as `SOUL.md`. | https://docs.openclaw.ai/cli/claws.md |
| R11-017 | A Hermes profile is a separate Hermes home (config.yaml, .env, SOUL.md, memories, sessions, skills, cron) under `~/.hermes/profiles/`. | https://hermes-agent.nousresearch.com/docs/user-guide/profiles |
| R11-022 | Pi's subagent example extension defines agents as Markdown + YAML (name, description, tools, model) in `~/.pi/agent/agents/*.md` or `.pi/agents/*.md`. | https://github.com/earendil-works/pi/blob/main/packages/coding-agent/examples/extensions/subagent/README.md |
| R11-024 | AGENTS.md has no required fields. It is plain Markdown with no schema for declaring an agent's name, tools or model. | https://agents.md/ |
| R11-025 | Agent Plugins 1.0 standardises only Agent Skills and MCP servers; agents, commands, hooks and rules are explicitly excluded because clients don't share semantic… | https://aaif.io/blog/from-skills-and-tools-to-portable-agent-plugins |
| R11-026 | Agent Plugins is independently governed and not an AAIF project. | https://aaif.io/blog/from-skills-and-tools-to-portable-agent-plugins |
| R11-027 | Agent Plugins' steering committee includes Amazon, Cursor, Microsoft, OpenAI and Vercel; listed clients include VS Code, Cursor, GitHub Copilot, OpenAI Codex an… | https://agent-plugins.org/ ; https://aaif.io/blog/from-skills-and-tools-to-portable-agent-plugins |
| R11-028 | An A2A Agent Card is JSON metadata an A2A server publishes about itself (identity, capabilities, skills, endpoint, auth). A2A lets agents collaborate without ne… | https://a2a-protocol.org/latest/specification/ |
| R11-029 | OASF records represent metadata about agentic AI applications and can be annotated with skills and domains for announcement and discovery. (That OASF is not a r… | https://docs.agntcy.org/oasf/open-agentic-schema-framework/ |
| R11-030 | "Autonomous Agent Interchange Format (AAIF)" is an individual IETF Internet-Draft with no formal standing (not the Agentic AI Foundation). | https://datatracker.ietf.org/doc/draft-schemacommons-aaif/ |
| R12-001 | Anthropic's harness post names the roles "generator" and "evaluator", and its final design is planner / generator / evaluator. | https://www.anthropic.com/engineering/harness-design-long-running-apps |
| R12-004 | Microsoft's architecture guide calls the pattern "maker-checker": a maker proposes, a checker evaluates against criteria. | https://learn.microsoft.com/en-us/azure/architecture/ai-ml/guide/ai-agent-design-patterns |
| R12-005 | Microsoft lists the synonyms: maker-checker = evaluator-optimizer = generator-verifier = critic or reflection loops. | https://learn.microsoft.com/en-us/azure/architecture/ai-ml/guide/ai-agent-design-patterns |
| R12-008 | LangChain/LangGraph docs use "evaluator-optimizer", with generator and evaluator nodes. | https://docs.langchain.com/oss/python/langgraph/workflows-agents |
| R12-009 | OpenAI Agents SDK docs describe a task agent plus an "evaluator agent" in a while loop. | https://openai.github.io/openai-agents-python/multi_agent/ |
| R12-010 | Addy uses "planner / generator / evaluator" in his harness post (and "verifier/maker" in *Loop Engineering*, R2-009). | https://addyosmani.com/blog/agent-harness-engineering/ |
| R12-011 | The alt text of the harness-anatomy figure in Addy Osmani's *Agent Harness Engineering* (19 Apr 2026) reads: "The model sits in the middle; the harness surround… | https://addyosmani.com/blog/agent-harness-engineering/ |
| R12-012 | Addy's list of harness parts includes orchestration logic and observability. | https://addyosmani.com/blog/agent-harness-engineering/ |
| R12-013 | Viv Trivedy uses "context injection" as the only way to add knowledge without changing weights. | https://www.langchain.com/blog/the-anatomy-of-an-agent-harness |
| R12-018 | SRP (Robert C. Martin): each module should have one and only one reason to change. | https://blog.cleancoder.com/uncle-bob/2014/05/08/SingleReponsibilityPrinciple.html |
| R12-019 | Martin's alternative wording of SRP: gather what changes together, separate what changes for different reasons. | https://blog.cleancoder.com/uncle-bob/2014/05/08/SingleReponsibilityPrinciple.html |
| R12-020 | Martin named SRP in the late 1990s and credits Dijkstra (1974) with the term "separation of concerns". | https://blog.cleancoder.com/uncle-bob/2014/05/08/SingleReponsibilityPrinciple.html |
| R12-021 | Dijkstra (EWD447): separation of concerns is the only available technique for ordering one's thoughts. | https://www.cs.utexas.edu/~EWD/transcriptions/EWD04xx/EWD447.html |
| R12-022 | Dijkstra splits "making a thing" into stating its properties and making a thing guaranteed to have them (spec vs build). | https://www.cs.utexas.edu/~EWD/transcriptions/EWD04xx/EWD447.html |
| R12-024 | Fowler: an event-sourced system replays events after a crash, and the events make an audit log. | https://martinfowler.com/eaaDev/EventSourcing.html |
| R12-025 | Fowler (CI): integration is complete only when the integration build is green. | https://martinfowler.com/articles/continuousIntegration.html |
| R12-026 | Fowler (CI): any failing test fails the build; "99.9% green is still red". | https://martinfowler.com/articles/continuousIntegration.html |
| R12-030 | Dex Horthy (12-Factor Agents): good agents are "mostly just software". | https://raw.githubusercontent.com/humanlayer/12-factor-agents/main/README.md |
| R12-033 | Böckeler: as software engineers we distrust AI code because LLMs are non-deterministic. | https://martinfowler.com/articles/harness-engineering.html |
| R12-036 | The phrase is the title of Anthropic's Managed Agents engineering post. | https://www.anthropic.com/engineering/managed-agents |
| R12-037 | Section heading "Decouple the brain from the hands": brain = Claude + harness; hands = sandboxes and tools; session = event log. | https://www.anthropic.com/engineering/managed-agents |
| R12-038 | Once decoupled, brain, hands and session can each fail or be replaced independently. | https://www.anthropic.com/engineering/managed-agents |
| R12-039 | Thesis and mappings: loop engineering is good software engineering applied to a non-deterministic component (SRP ↔ one job per step, CI gate ↔ "done", event sou… | n/a (speaker's framing) |
| R12-040 | Wrapping the five pillars in a loop, with each pointing back to its slide, is the speaker's addition to Addy's anatomy (R12-011). | n/a (speaker's framing) |
| R13-001 | The docs' Capabilities tab groups OpenClaw's building blocks as Plugins, Skills, Automation, Tools and Agent coordination; its overview page is the entry point … | https://docs.openclaw.ai/tools.md ; https://docs.openclaw.ai/ (nav) |
| R13-002 | Tools are callable actions, skills teach how to work, plugins add runtime capabilities. | https://docs.openclaw.ai/tools.md |
| R13-005 | A plugin can add tools, skills, channels, providers, hooks and other runtime capabilities. | https://docs.openclaw.ai/tools.md |
| R13-006 | Tool policy is enforced before the model call; removed tools are not sent to the model. | https://docs.openclaw.ai/tools.md |
| R13-007 | Automation runs background work via runtimes, scheduled jobs, event hooks and standing instructions. | https://docs.openclaw.ai/automation.md |
| R13-010 | The docs' Agent coordination section contains Agent send, Goal, Steer and Sub-agents (plus Swarm and ACP agents). | https://docs.openclaw.ai/ (nav) |
| R13-011 | Sub-agents are designed to be isolated by default (session separation, optional sandboxing). | https://docs.openclaw.ai/tools/subagents.md |
| R13-012 | OpenClaw's system prompt tells the agent that a child's completion is not proof the delegated goal is complete. | https://docs.openclaw.ai/concepts/system-prompt.md |
| R13-013 | A goal is a shared target for long-running work, not a background task, reminder, cron job or standing order; it does not schedule work (though starting or resu… | https://docs.openclaw.ai/tools/goal.md |
| R13-016 | OpenClaw always stops a turn after three consecutive identical tool errors, regardless of loop-detection config. | https://docs.openclaw.ai/tools/loop-detection.md |
| R13-020 | Sub-agent sessions inject only AGENTS.md; other bootstrap files are filtered out. | https://docs.openclaw.ai/concepts/system-prompt.md |
| R13-021 | On ordinary turns, daily `memory/*.md` files are not bootstrapped; they are read on demand via `memory_search` / `memory_get` (a bare `/new` or `/reset` can pre… | https://docs.openclaw.ai/concepts/system-prompt.md |
| R13-022 | The agent loop builds the system prompt from base prompt, skills prompt, bootstrap context and per-run overrides. | https://docs.openclaw.ai/concepts/agent-loop.md |
| R13-023 | A plugin `before_tool_call` hook returning block is terminal. | https://docs.openclaw.ai/concepts/agent-loop.md |
| R13-025 | The Gateway projects lifecycle and tool events into a metadata-only audit ledger. | https://docs.openclaw.ai/concepts/agent-loop.md |
| R13-026 | Run and tool audit records are on by default and store metadata, never content. | https://docs.openclaw.ai/cli/audit.md |
| R13-028 | The README sums up OpenClaw's architecture as trusted gateway, untrusted execution, deterministic policy. | https://raw.githubusercontent.com/openclaw/openclaw/v2026.10.1/README.md |
| R13-029 | Harnesses and other features ship as plugins against a deliberately small core. | https://docs.openclaw.ai/start/why-openclaw.md |
| R13-033 | The Automations scheduler persists jobs, wakes the agent on time, and delivers output to a channel or webhook. | https://docs.openclaw.ai/automation.md |
| R13-035 | OpenClaw states that configured policy is enforced in code, not only by model compliance. | https://docs.openclaw.ai/start/why-openclaw.md |
| R13-036 | Sandboxing and exec approvals are off by default. | https://docs.openclaw.ai/start/why-openclaw.md |
| R14-002 | The Features Overview page groups features under Core, Automation, Media & Web, Integrations and Customization, which "work together". | https://hermes-agent.nousresearch.com/docs/user-guide/features/overview |
| R14-003 | Integrations is its own top-level docs section, covering inference providers, tool servers (MCP), IDE workflows and programmatic access. | https://hermes-agent.nousresearch.com/docs/integrations/ |
| R14-004 | Core: tools are grouped into toolsets that can be switched per platform. | https://hermes-agent.nousresearch.com/docs/user-guide/features/overview |
| R14-005 | Core: persistent memory is bounded and curated, stored in MEMORY.md and USER.md. | https://hermes-agent.nousresearch.com/docs/user-guide/features/overview |
| R14-006 | Core: Hermes auto-discovers and loads project context files. (Load rules: use R4-025 corrected wording.) | https://hermes-agent.nousresearch.com/docs/user-guide/features/overview |
| R14-007 | Core: `@` context references inject files, folders, git diffs and URLs into a message. | https://hermes-agent.nousresearch.com/docs/user-guide/features/overview |
| R14-008 | Checkpoints (shadow-git snapshots before write_file/patch and destructive commands, restored with /rollback) are opt-in and off by default. | https://hermes-agent.nousresearch.com/docs/user-guide/checkpoints-and-rollback |
| R14-011 | The Automation sidebar group contains Cron, Subagent Delegation, Kanban, Persistent Goals, Session Heartbeats, Recurring Loops, Code Execution, Event Hooks and … | https://hermes-agent.nousresearch.com/docs/user-guide/features/cron |
| R14-015 | The Media & Web sidebar group covers voice, wake word, web/X search, browser, computer use, vision, image generation and TTS. | https://hermes-agent.nousresearch.com/docs/user-guide/features/voice-mode |
| R14-016 | Media & Web: browser automation with multiple cloud and local backends navigates sites, fills forms and extracts information. | https://hermes-agent.nousresearch.com/docs/user-guide/features/overview |
| R14-018 | Integrations: fallback providers fail over automatically to backup LLMs, with separate fallback for auxiliary tasks. | https://hermes-agent.nousresearch.com/docs/user-guide/features/overview |
| R14-019 | Integrations: external memory backends plug in beyond the built-in memory system. | https://hermes-agent.nousresearch.com/docs/user-guide/features/overview |
| R14-022 | Plugins come in three types, one of which, context engines, replaces context management. | https://hermes-agent.nousresearch.com/docs/user-guide/features/overview |
| R14-023 | Management: the web dashboard configures settings and keys and monitors sessions. | https://hermes-agent.nousresearch.com/docs/user-guide/features/web-dashboard |
| R14-024 | Architecture: one AIAgent class serves every entry point (CLI, gateway, ACP, batch, API server); platform differences live in the entry point. | https://hermes-agent.nousresearch.com/docs/developer-guide/architecture |
| R14-025 | Design principle "Observable execution": every tool call is visible via callbacks, with progress in CLI and gateway. | https://hermes-agent.nousresearch.com/docs/developer-guide/architecture |
| R14-027 | The Agent Loop subsystem handles provider selection, prompt construction, tool execution, retries, fallback, callbacks, compression and persistence. | https://hermes-agent.nousresearch.com/docs/developer-guide/architecture |
| R14-030 | Session persistence is SQLite with FTS5, with parent/child lineage across compressions. | https://hermes-agent.nousresearch.com/docs/developer-guide/architecture |
| R14-031 | The cached system prompt is three ordered tiers: stable (SOUL.md identity, tool guidance), context (project context files) and volatile (skills index, MEMORY.md… | https://hermes-agent.nousresearch.com/docs/developer-guide/prompt-assembly |
| R14-032 | Discrepancy: the same page places the skills index in the volatile tier and also says skills are part of the stable tier. Say only "in the cached prompt". | https://hermes-agent.nousresearch.com/docs/developer-guide/prompt-assembly |
| R14-036 | When gates and a contract are both set, gates run first. Each gate retries 3 times by default (5-min timeout), then the goal auto-pauses. | https://hermes-agent.nousresearch.com/docs/user-guide/features/goals |
| R14-038 | In a Kanban swarm, workers run in parallel, the verifier wakes after all of them finish, and the synthesizer wakes only after the verifier marks the work clean. | https://hermes-agent.nousresearch.com/docs/user-guide/features/kanban |
| R14-041 | The docs home calls Hermes "the only agent with a built-in learning loop". This is a vendor marketing claim: quote it as theirs, never as fact. | https://hermes-agent.nousresearch.com/docs/ |
| R15-001 | Pi's own architecture overview names four responsibilities and defines a session as a record of messages, tool calls, results, model changes and compactions. Th… | https://pi.dev/docs/latest/how-pi-works |
| R15-002 | Every request carries the system prompt (base instructions + discovered context files), tool definitions and skill descriptions, i.e. what is always loaded. | https://pi.dev/docs/latest/how-pi-works |
| R15-003 | Full skill instructions load on demand, and extensions can add instructions or transform context. | https://pi.dev/docs/latest/how-pi-works |
| R15-004 | All Pi interfaces (interactive, print, JSON, RPC, SDK) share the same agent and session mechanisms; RPC uses JSONL over stdin/stdout. | https://pi.dev/docs/latest/how-pi-works |
| R15-005 | Extensions are TypeScript modules running inside the Pi process that register tools, commands, providers, event handlers and UI. | https://pi.dev/docs/latest/how-pi-works |
| R15-006 | Skills, prompt templates and themes are resources; Pi packages distribute them (and extensions) via npm or git as one unit. | https://pi.dev/docs/latest/how-pi-works |
| R15-007 | Pi's quickstart says "Start with the least powerful mechanism that meets your need" and maps needs to mechanisms: AGENTS.md (persistent folder instructions), pr… | https://pi.dev/docs/latest/quickstart |
| R15-008 | Extension handlers at `turn_end` and `agent_before_settle` can request one more model request, and an unguarded continuation can loop; `agent_settled` is notifi… | https://pi.dev/docs/latest/extensions |
| R15-009 | Extensions can gate tool calls: `tool_call` can block execution, a failing `tool_call` handler blocks the tool as a fail-safe, and a permission extension can us… | https://pi.dev/docs/latest/extensions |
| R15-010 | In pi-agent-core, `finishTurn` runs after the assistant message and all tool results, before `turn_end`; returning continue unconditionally creates an endless l… | https://github.com/earendil-works/pi/blob/main/packages/agent/README.md |
| R15-011 | JSON mode streams structured events for one run (agent, turn, message, tool, queue, compaction, retry); `agent_settled` signals no remaining automatic work. | https://pi.dev/docs/latest/json |
| R15-015 | Pi does not ask for approval before every tool call; watching the transcript, project trust and reviewing changes are not a security boundary. | https://pi.dev/docs/latest/security |
| R15-016 | Context files (AGENTS.override.md, AGENTS.md, CLAUDE.md) load regardless of project trust unless context loading is disabled. | https://pi.dev/docs/latest/security |
| R15-017 | In Pi Durable (experimental), everything the harness runs is a task, and each step stores a checkpoint. | https://earendil.com/posts/pi-durable/ |
| R15-019 | Pi Durable does not replace the coding agent; it is a framework for any agentic application, and any number of clients can attach to its committed state. | https://earendil.com/posts/pi-durable/ |
## Versions inspected

Checked on 13 Oct 2026. The slides show no versions; every product statement holds "as of" these versions and docs dates.

| Product / source | Version inspected | Docs date | Latest at check (13 Oct 2026) |
|---|---|---|---|
| Claude Code | 2.1.296 (9 Oct 2026), per `CHANGELOG.md` on `main`: https://raw.githubusercontent.com/anthropics/claude-code/main/CHANGELOG.md | code.claude.com docs, live, fetched 13 Oct 2026; the docs changelog also shows 2.1.296 | Same. Feature anchors: `/goal` since v2.1.139; AGENTS.md read since v2.1.277 |
| OpenAI Codex CLI | 0.162.1 (tag `rust-v0.162.1`, commit `092d3ac`, 9 Oct 2026): https://github.com/openai/codex/releases/tag/rust-v0.162.1 | learn.chatgpt.com docs, live (developers.openai.com/codex redirects there); no per-page dates; newest "What's new" entries 5–9 Oct 2026 | Same. `/goal` since 0.128.0 (30 Apr 2026) |
| OpenClaw | README at v2026.10.1 (commit `e178c39`, 10 Oct 2026): https://github.com/openclaw/openclaw/releases | docs.openclaw.ai, live and unversioned, fetched 13 Oct 2026; *Why OpenClaw* page snapshot `7b624e9de25` (27 Aug 2026) | **v2026.10.2** (commit `b8952d4`, 12 Oct 2026) was the latest stable release at check time, so the README inspected was one release behind. Newest pre-release: 2026.10.5-beta.3 (`1808b57`, 13 Oct 2026) |
| Hermes Agent (Nous Research) | v0.21.7 (commit `71d34ba`, released 11 Oct 2026): https://github.com/NousResearch/hermes-agent/releases/latest | Docusaurus "current" docs built from `main`, fetched 13 Oct 2026 | Same (v0.21.7 marked Latest) |
| Pi (earendil-works/pi) | v1.1.0 (commit `abe508e`, 7 Oct 2026): https://github.com/earendil-works/pi/releases | pi.dev/docs/latest (from `main`, after v1.1.0), fetched 13 Oct 2026 | Same |
| Pi Durable | `@earendil-works/pi-durable`, experimental | Earendil post, 1 Oct 2026 | "API might still change" |
| VS Code custom agents | — | page dated 7 Oct 2026 | live |
| Agent Plugins | 1.0.0 | AAIF blog, 6 Aug 2026 | — |
| A2A specification | 1.0.0 (latest released) | live | — |
| IETF "AAIF" draft | draft-schemacommons-aaif-00 (individual draft) | last updated 25 Jun 2026, expires 27 Dec 2026 | no formal standing |
| Microsoft orchestration patterns | page commit `ff159411…` | page dated 12 Feb 2026 | live |
| NoLiMa | arXiv v3 (9 Jul 2025), ICML 2025; README results updated 9 Jun 2025 | — | — |
