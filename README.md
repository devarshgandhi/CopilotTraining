# CopilotTraining

> Open training content for teams adopting GitHub Copilot, customizations, agent workflows, and AI-assisted software delivery.

## Start Here

The easiest way to use this repository is the live site:

- [Browse CopilotTraining on GitHub Pages](https://msbart2.github.io/CopilotTraining/)

That is the fastest way to find the right workshop module, tech talk, or executive talk without learning the repository structure first.

## Choose Your Path

| If you are trying to... | Start here | Why |
|-------------------------|------------|-----|
| Build hands-on skill with Copilot customizations and agent workflows | [Workshop](workshop/) | Best for structured learning, team training, and experiential practice |
| Understand a specific capability or technical pattern | [Tech Talks](tech-talks/) | Best for engineers, architects, and technical champions who need depth |
| Explain the organizational or economic implications to leadership | [Executive Talks](exec-talks/) | Best for leaders making adoption, investment, and operating-model decisions |
| Just browse the material quickly | [Live Site](https://msbart2.github.io/CopilotTraining/) | Best for first-time visitors who want the easiest navigation |

If you want the simplest recommendation: start on the live site, then choose a workshop, tech talk, or executive talk based on your audience.

## Why This Repo Exists

Most Copilot material explains features one at a time. This repository is organized around a more useful question:

**How do teams actually get better results from AI-assisted development?**

Copilot becomes much more valuable when people move beyond one-off prompting and start shaping context, workflows, guardrails, and operating models. This repository collects practical material for that shift in three forms:

- **Workshop modules** for hands-on practice
- **Tech talks** for practitioners who want a focused deep dive
- **Executive talks** for leaders deciding what AI changes in delivery and economics

## What You Will Find

This repository is designed to support three different kinds of conversations:

- how practitioners build better with GitHub Copilot
- how teams shape context and workflows so results improve consistently
- how leaders think about delivery, economics, and governance as AI takes on more work

### Workshop

The [workshop](workshop/) is the hands-on path through the material.

It uses a story-driven format, recurring personas, and a production-style application template so teams can see what changes when Copilot is given better context and stronger workflows. The goal is not just to explain customization, but to let people feel its compounding value over time.

Core modules include:

| Module | Why it matters |
|--------|----------------|
| [00 — Orientation](workshop/00-orientation/) | Frames the shift from syntax-first development to clarity-first development |
| [01 — Instructions](workshop/01-instructions/) | Shows how repository guidance changes Copilot behavior immediately |
| [02 — Agent Plan Mode](workshop/02-agent-plan-mode/) | Teaches more structured collaboration for non-trivial work |
| [03 — Custom Prompts](workshop/03-custom-prompts/) | Turns repeatable work into reusable prompt assets |
| [04 — Agent Skills](workshop/04-agent-skills/) | Encodes domain knowledge so Copilot can load it when needed |
| [05 — MCP Servers](workshop/05-mcp-servers/) | Connects agents to real tools, systems, and live data |
| [06 — Custom Agents](workshop/06-custom-agents/) | Pulls the pieces together into more autonomous workflows |

Start with the workshop if you want a guided path that builds from fundamentals to more autonomous agent workflows.

### Tech Talks

The [tech-talks](tech-talks/) directory is the practitioner library.

These talks are for engineers, architects, enablement leads, and technical champions who want a deep dive on one capability, one pattern, or one architectural shift. Each talk is meant to answer a concrete question and leave people with something they can apply right away.

Current themes include:

| Theme | Example talks | What they help explain |
|------|---------------|------------------------|
| Copilot surfaces | [Copilot Chat](tech-talks/copilot-chat/), [Copilot CLI](tech-talks/copilot-cli/), [Copilot Web](tech-talks/copilot-web/) | Where Copilot shows up and how each interface changes the workflow |
| Context and customization | [Copilot Primitives](tech-talks/copilot-primitives/), [Copilot Hooks](tech-talks/copilot-hooks/), [Copilot Memory](tech-talks/copilot-memory/) | How to shape agent behavior with instructions, prompts, hooks, and memory |
| Agent architecture | [Agent Teams](tech-talks/agent-teams/), [Multi-Step Tasks](tech-talks/multi-step-tasks/), [Parallel Execution](tech-talks/parallel-execution/) | How to break complex work into coordinated agent workflows |
| Agentic delivery | [Agentic Journey](tech-talks/agentic-journey/), [Agentic SDLC](tech-talks/agentic-sdlc/), [Enterprise Patterns](tech-talks/enterprise-patterns/) | What changes in repos, PRs, CI, and team design when AI does more of the labor |

If you are not sure which talk fits your audience, use the [tech talk decision guide](tech-talks/DECISION-GUIDE.md).

### Executive Talks

The [exec-talks](exec-talks/) directory translates the same ideas into leadership language.

These talks focus less on feature mechanics and more on organizational consequences: what changes in delivery models, where the economic leverage comes from, and what leaders need to instrument or govern as AI takes on more work.

Current executive talks include:

| Talk | Why a leadership audience would care |
|------|--------------------------------------|
| [Agentic Delivery](exec-talks/agentic-delivery/) | How delivery changes when agents operate with tools, context, and guardrails |
| [Agentic Economics](exec-talks/agentic-economics/) | How to think about ROI, throughput, and capacity in AI-assisted engineering |
| [Agentic Labor](exec-talks/agentic-labor/) | What kinds of work agents can take on beyond code generation |

Start here if your audience is making strategy, investment, governance, or operating-model decisions rather than implementation decisions.

## Live Site vs. Repository

Use the [live site](https://msbart2.github.io/CopilotTraining/) if you want the easiest browsing experience.

Use the repository directly if you want to:

- read the source Markdown behind a talk or module
- reuse or adapt the material for your own team
- inspect examples, images, and slide sources
- contribute new content or revise existing talks

## Repository Layout

| Path | Purpose |
|------|---------|
| [workshop](workshop/) | Hands-on training modules and persona-driven exercises |
| [tech-talks](tech-talks/) | Reader-first technical deep dives |
| [exec-talks](exec-talks/) | Leadership-focused thought leadership content |
| [slides](slides/) | Slidev slide decks for workshop, tech talks, and executive talks |
| [docs](docs/) | Supporting authoring documentation and internal guides |

## For Contributors

This repository also contains the source material and generation workflow behind the content, but that is secondary to the reader experience.

If you are here to create or update content, these are the most useful starting points:

- [tech-talks/README.md](tech-talks/README.md) for the tech talk authoring workflow
- [slides/TEMPLATE.md](slides/TEMPLATE.md) for slide design patterns
- [.github/copilot-instructions.md](.github/copilot-instructions.md) for repo-wide Copilot guidance
- [docs/github-configuration.md](docs/github-configuration.md) for the `.github` folder overview and workflow map
- [workshop/README.md](workshop/README.md) for the workshop narrative and module structure

## Core Point of View

This repository is built around a simple idea:

**The bottleneck is no longer only code production. It is clarity, context, judgment, and system design.**

That is why the content here spends so much time on instructions, prompts, skills, agents, workflows, repository design, and operating models. The value is not just that AI can write code. The value is that teams can shape how that labor is directed, reviewed, and scaled.

## License

This content is open source under the MIT License.
