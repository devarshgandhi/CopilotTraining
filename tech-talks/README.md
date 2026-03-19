# Tech Talks — Creation Guide

This directory contains practitioner-focused technical deep dives. Each talk lives in its own subdirectory (e.g., `copilot-cli/`, `agent-teams/`) and follows a consistent structure defined by [TEMPLATE.md](TEMPLATE.md).

---

## 📁 Directory Structure

Every tech talk produces:

```
tech-talks/{topic}/
├── research.md          # Phase 1 — raw research and source analysis
├── plan.md              # Optional working outline / review notes before drafting
├── README.md            # Final reader-first tech talk
├── deck.recipe.yml      # Per-talk slide recipe for fast single-deck regeneration
├── images/              # Downloaded or referenced visuals
└── examples/            # Standalone code samples
```

The final `README.md` is the canonical, reader-first artifact for the talk. It follows the structure in [TEMPLATE.md](TEMPLATE.md) and is meant to stand on its own as a technical reference, not as a slide outline.

---

## 💻 Creating Tech Talks with the IDE Agent

Create a tech talk interactively in VS Code using Copilot Chat agents. This gives you more control — you can review and iterate between phases.

### How to Start

Open Copilot Chat and invoke:

```
@Tech Talk Generator create tech talk for [topic] using [URLs]
```

### The Three Phases

The agent follows a research-first workflow and pauses at the structure-selection point before it writes the README:

#### Phase 1: Research
- Agent fetches URLs, runs web searches, downloads images
- Synthesizes a compact research brief: topic signal, likely audience, artifacts, and decision areas

#### Phase 2: Structure Choice
- Agent proposes **one recommended outline** for the major sections
- Offers up to **two** bounded structural toggles and, only when justified, one alternate outline
- **⏸️ Pauses** — waits for you to choose `A`, apply a toggle, pick `B`, or request one structural tweak

#### Phase 3: Build
- Agent locks the selected structure and generates `README.md`
- Agent also creates `deck.recipe.yml` with the initial slide-adaptation choices for this talk
- Sets frontmatter (`status`, `updated`, `section`)
- **⏸️ Pauses** — shows the completed talk, offers handoff to slides

### Generating Slides (Separate Step)

Slides are **not** part of the tech-talk generator's workflow. After Phase 3, use the handoff buttons or invoke directly:

```
@Slide Generator generate slides for tech-talks/{topic}
```

Or for generation + verification:

```
@Slide Manager generate and verify slides for tech-talks/{topic}
```

The slide deck is a **separate artifact** at `slides/tech-talks/{topic}.md`. The slide generator derives it from the README's semantic structure — frontmatter, core sections, `<!-- 🎬 MAJOR SECTION: ... -->` markers, artifacts, and references. New tech-talk READMEs should **not** include slide-sequence tables or other visible presentation-planning content.

For tech talks, the recommended per-talk slide control point is `tech-talks/{topic}/deck.recipe.yml`. Adjust that file when you want to regenerate just one deck with a different intro, section order, emphasis, references behavior, or thank-you style.

### What the Structure Proposal Looks Like

Before drafting, the generator now shows:

- A compact **Research Brief** summarizing what the URLs actually support
- **Recommended Structure — A** with the framing question and major sections
- Up to **two** structural toggles that change emphasis or order without redesigning the whole talk
- **Alternate Structure — B** only if the sources genuinely support a different narrative arc

That means the agent does the background reading first, then gives you a small, meaningful decision before it writes the README.

### Deck Recipe Workflow

The Tech Talk Generator now creates an initial `deck.recipe.yml` for every new tech talk. The Slide Generator then:

- reads that recipe first when generating `slides/tech-talks/{topic}.md`
- uses it to keep deck-specific choices stable across reruns
- synthesizes and saves a recipe once if an older talk does not have one yet

Start from [DECK-RECIPE-TEMPLATE.yml](DECK-RECIPE-TEMPLATE.yml) if you want to understand or hand-edit the schema.

### Alternative: Skill-Based Workflow

You can also use the `@tech-talk-author` skill for a lighter-weight version:

```
@tech-talk-author create tech talk for [topic] using [URLs]
```

This follows the same 3-phase process but without the interactive pauses.

---

## 📄 TEMPLATE.md — The Source of Truth

[TEMPLATE.md](TEMPLATE.md) defines the canonical structure. Every tech talk README must include these sections:

1. **Title + Primary Question** — the ONE question the talk answers
2. **📊 Content Fitness** — quality rubric (Relevant / Compelling / Actionable)
3. **The Opportunity** — what this capability unlocks for practitioners
4. **How It Works** — the mechanism, architecture, and key capabilities
5. **🔑 Key Artifacts** — configs, files, commands, or workflows to know
6. **🧠 Mental Model Shift** — the core insight and concrete behavioral shift
7. **🎬 Major Sections** (3-6) — deep technical content with examples
8. **Use Cases** — real-world scenarios with measurable outcomes
9. **✅ What You Can Do Today** — immediate, short-term, and advanced actions
10. **Related Patterns** — adjacent talks and combination guidance
11. **📖 References** — numbered citations (`[^1]`, `[^2]`, etc.)

### Minimum README Contract for Slide Generation

The Slide Generator does **not** require a visible slide-mapping section. For new talks, it relies on:

- YAML frontmatter (`status`, `updated`, `section`, and `references` when available)
- The H1 title, guiding question, and duration/audience block
- Core narrative sections such as Opportunity, How It Works, Key Artifacts, Mental Model Shift, Use Cases, and References
- `<!-- 🎬 MAJOR SECTION: ... -->` comments before the deepest sections
- A strong `> **The Core Insight:** ...` line inside the mental model section

---

## 🗂️ Existing Tech Talks

| Directory | Topic |
|-----------|-------|
| `agentrc-maturity/` | AgentRC maturity model for AI-ready SDLC |
| `agent-teams/` | Multi-agent collaboration patterns |
| `agentic-journey/` | The evolution toward agentic development |
| `agentic-sdlc/` | AI across the software development lifecycle |
| `context-engineering-foundations/` | Foundational context engineering patterns |
| `copilot-chat/` | GitHub Copilot Chat fundamentals |
| `copilot-chat-internals/` | Under-the-hood: debug view, system prompts |
| `copilot-cli/` | Terminal-native AI with Copilot CLI |
| `copilot-hooks/` | Pre/post-processing hooks for Copilot |
| `copilot-acp/` | Agent Client Protocol for universal AI integration |
| `copilot-memory/` | Copilot memory and persistent context |
| `copilot-primitives/` | Core Copilot building blocks |
| `copilot-sdk/` | Programmatic Copilot integration |
| `copilot-web/` | Browser and mobile Copilot workflows |
| `enterprise-patterns/` | Enterprise-scale adoption patterns |
| `mcp-apps/` | Model Context Protocol applications |
| `multi-step-tasks/` | Complex multi-step agent tasks |
| `parallel-execution/` | Parallel agent execution strategies |
| `terminal-sandboxing/` | Sandboxed terminal execution |

For help choosing which talk to explore, see [DECISION-GUIDE.md](DECISION-GUIDE.md).

