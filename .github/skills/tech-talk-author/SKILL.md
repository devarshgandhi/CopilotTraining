---
name: tech-talk-author
description: Generates tech talk content using the same phased workflow as the GitHub Issue pipeline. Produces research.md, plan.md, and README.md using shared prompt templates.
infer: true
---

# Tech Talk Author Skill

Generate tech talks following the same 4-phase structure as the GitHub Issue workflow.

## Usage

```
@tech-talk-author create tech talk for [topic] using [URLs]
```

## Process

Follow the prompt templates in `.github/prompts/tech-talk/`:

1. **Research** (`research-instructions.md`) — Fetch URLs + web search for additional references → `research.md`
2. **Plan** (`planning-instructions.md`) — Create content outline → `plan.md`
3. **Build** (`build-instructions.md`) — Generate README.md with inline `[^n]` citations
4. **Slides** (`slides-instructions.md`) — Generate Slidev slides with footnotes

## Key Requirements

- Follow `tech-talks/TEMPLATE.md` structure
- Produce intermediate artifacts (research.md, plan.md) before README
- Include 8-15 numbered references with inline citations
- Web search for additional references beyond provided URLs
- Pause for review between phases
