# Slide Index Sections

> **Single source of truth** for the section/sub-group taxonomy used in:
> - `slides/index-custom.html` (rendered HTML structure)
> - `.github/agents/slide-generator.agent.md` (card placement logic)
> - `.github/copilot-instructions.md` (valid `section:` frontmatter values)
>
> **To rename or add a section:** edit this file, then update `index-custom.html` to match.
> Agents read this file at runtime — they will pick up changes automatically.

---

## Section Map

Each entry defines:
- **Section name** — the exact string used in README frontmatter `section:` field
- **Icon** — emoji used in the index sub-group header
- **Parent container** — which top-level `<div class="section ...">` block it belongs to
- **Contents** — what talks belong here (informational, not exhaustive)

---

### 🔬 Tech Talks

Top-level container class: `section tech-talks`

| Section Name | Icon | Slug | Tagline | Contents |
|---|---|---|---|---|
| `Copilot Tools` | 💬 | `copilot-tools` | Where you interact with Copilot every day | Chat Internals, CLI, Code Review, Web, What's New in VS Code |
| `Customization & Context` | 🧩 | `customization-context` | Making it yours — instructions, skills, and integrations | Primitives, Hooks, Memory, SDK, MCP Apps |
| `Agent Architecture` | 🤖 | `agent-architecture` | Patterns for composing and orchestrating multi-agent systems | Agent Teams, Multi-Step Tasks, Parallel Execution, ACP |
| `Agentic SDLC` | 🚀 | `agentic-sdlc` | Transforming the full software delivery lifecycle with AI agents | Agentic Workflows, Journey, SDLC, Enterprise Patterns |

---

### 💼 Executive Talks

Top-level container class: `section exec-talks`

| Section Name | Icon | Slug | Contents |
|---|---|---|---|
| `Executive Talks` | 💼 | `exec-talks` | Agentic Delivery, Agentic Economics, Agentic Labor |

> Executive Talks have no sub-groups — cards go directly in the `exec-talks` section grid.

---

### 🎓 Workshop

Top-level container class: `section workshop`

| Section Name | Icon | Slug | Contents |
|---|---|---|---|
| `Workshop` | 🎓 | `workshop` | Modules 00–06 (numbered, no sub-groups) |

> Workshop modules are numbered, not grouped into sub-groups.

---

## index-custom.html Structure Reference

```
<div class="section tech-talks">
  <div class="sub-group">  ← Copilot Tools (💬)
  <div class="sub-group">  ← Customization & Context (🧩)
  <div class="sub-group">  ← Agent Architecture (🤖)
  <div class="sub-group">  ← Agentic SDLC (🚀)

<div class="section exec-talks">
  <div class="grid">       ← Executive Talks (no sub-groups)

<div class="section workshop">
  <div class="grid">       ← Workshop modules (no sub-groups)

<div class="section repos">
  <div class="grid">       ← Related Repos (external links, not talk slides)
```

---

## Changing Sections

When you rename, add, or remove a section:

1. **Edit this file** — update the table above
2. **Edit `slides/index-custom.html`** — update the corresponding `sub-group-label` span text and icon; add/remove `<div class="sub-group">` blocks as needed
3. **Agents pick up the change automatically** — they read this file before placing cards

> The `section:` field in README frontmatter must exactly match the **Section Name** column above (case-sensitive).
