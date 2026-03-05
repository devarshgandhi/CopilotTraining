---
status: active
updated: 2026-03-05
section: "Copilot Surfaces"
references:
  - url: https://code.visualstudio.com/updates/v1_110
    label: "VS Code release notes: February 2026 (v1.110)"
    verified: 2026-03-05
  - url: https://code.visualstudio.com/updates/v1_109
    label: "VS Code release notes: January 2026 (v1.109)"
    verified: 2026-03-05
  - url: https://code.visualstudio.com/updates/v1_108
    label: "VS Code release notes: December 2025 (v1.108)"
    verified: 2026-03-05
  - url: https://code.visualstudio.com/docs/copilot/overview
    label: "GitHub Copilot in VS Code documentation"
    verified: 2026-03-05
  - url: https://code.visualstudio.com/docs/copilot/customization/agent-plugins
    label: "Agent Plugins documentation"
    verified: 2026-03-05
  - url: https://code.visualstudio.com/docs/copilot/customization/agent-skills
    label: "Agent Skills documentation"
    verified: 2026-03-05
  - url: https://code.visualstudio.com/docs/copilot/agents/background-agents
    label: "Background Agents documentation"
    verified: 2026-03-05
---

# What's New in Copilot for VS Code: v1.108 – v1.110

> **The Question This Talk Answers:**
> *"What are the most impactful new Copilot features in VS Code's last three releases, and how do I start using them today?"*

**Duration:** 30-45 minutes | **Target Audience:** Developers using GitHub Copilot in VS Code

---

## 📊 Content Fitness

| Criterion | Assessment | Notes |
|-----------|-----------|-------|
| **Relevant** | 🟢 High | Every developer using Copilot in VS Code should know what shipped. These features are available today and change daily workflows. |
| **Compelling** | 🟢 High | Organized by theme so practitioners see how features connect. Concrete settings and demos for each capability. |
| **Actionable** | 🟢 High | Every feature is available now in VS Code 1.108+. Settings provided inline. Enable features during or right after the talk. |

**Overall Status:** 🟢 Ready to use

---

## 📽️ Slide Generation Mapping

### Slide Sequence (Generated Automatically)

1. **Title/Logo Slide** ← H1 title + subtitle
2. **Question/Objective Slide** ← "The Question This Talk Answers"
3. **Table of Contents Slide** ← Auto-generated from 🎬 sections
4. **Release Timeline** ← "Three Releases at a Glance"
5. **🧠 The Shift (Preview)** ← Core Insight one-liner
6. **[Agent Sessions & Orchestration] Divider** ← 🎬 Section 1
7. **[Agent Sessions Content]** ← 3-4 slides
8. **[Agent Customization] Divider** ← 🎬 Section 2
9. **[Skills & Custom Agents Content]** ← 3-4 slides
10. **[Claude & Anthropic] Divider** ← 🎬 Section 3
11. **[Claude Content]** ← 2-3 slides
12. **[Security & Trust] Divider** ← 🎬 Section 4
13. **[Sandboxing Content]** ← 2-3 slides
14. **[Chat UX & Productivity] Divider** ← 🎬 Section 5
15. **[UX Improvements Content]** ← 2-3 slides
16. **🧠 Mental Model Shift (Full)** ← Move-Toward/Away/Against grid
17. **Actionable Outcomes** ← "What You Can Do Today"
18. **📖 References** ← References section
19. **End Slide** ← Auto-generated

### Major Sections (TOC Entries)

```markdown
<!-- 🎬 MAJOR SECTION: Agent Sessions & Orchestration -->
<!-- 🎬 MAJOR SECTION: Agent Customization -->
<!-- 🎬 MAJOR SECTION: Claude & Anthropic Integration -->
<!-- 🎬 MAJOR SECTION: Security & Trust -->
<!-- 🎬 MAJOR SECTION: Chat UX & Productivity -->
```

---

## Three Releases at a Glance

| Release | Date | Headline Theme |
|---------|------|----------------|
| **v1.108** | December 2025 | Agent Skills (experimental), agent sessions UX improvements, terminal IntelliSense rework, 6,000 issues closed [^3] |
| **v1.109** | January 2026 | Claude Agent preview, Agent Skills GA, terminal sandboxing, Copilot Memory, MCP Apps, integrated browser [^2] |
| **v1.110** | February 2026 | Agent Plugins, agentic browser tools, context compaction, session forking, /create-* commands, Explore subagent [^1] |

---

## 🧠 The Shift

> **The Core Insight:** From **one AI assistant you converse with** to **a team of specialized AI agents you orchestrate across local, background, cloud, and Claude sessions**

---

<!-- 🎬 MAJOR SECTION: Agent Sessions & Orchestration -->
## Agent Sessions & Orchestration

The biggest evolution across these three releases is how VS Code manages multiple agent sessions. What started as a single Chat view conversation is now a unified multi-agent platform [^6].

### Agent Sessions in the Chat View (v1.108)

Agent sessions are integrated directly into the Chat view [^3]:

- **Compact mode** — Shows the three most recent sessions when Chat view is narrow
- **Side-by-side mode** — Full session list with search and filters when Chat view is wide
- **Status indicators** — In-progress, unread, needs attention (visible in the VS Code command center)

```json
// Control orientation
"chat.viewSessions.orientation": "sideBySide"  // or "stacked", "auto"
```

### Switching and Delegating Between Agent Types (v1.108 → v1.110)

VS Code now supports four agent types optimized for different workflows [^1] [^2]:

| Agent Type | Best For | Key Trait |
|-----------|---------|----------|
| **Local** | Interactive planning, exploration | Real-time in Chat view |
| **Background** | Autonomous multi-file tasks | Runs in isolated Git worktree |
| **Cloud** | Cross-repo operations at scale | GitHub-hosted infrastructure |
| **Claude** | Complex reasoning, architecture | Anthropic SDK with thinking tokens |

The session type picker lets you start in one mode and hand off to another — plan locally, then click **Continue in → Background** to let the agent implement autonomously while you continue working [^2].

### Background Agents with Git Worktree Isolation (v1.108)

Background agents run in dedicated Git worktrees, preventing conflicts with your active workspace [^3]:

- Agent creates a new worktree automatically for the session
- Changes are committed per turn to the worktree — your main workspace is untouched
- Review via diff view when the agent completes; apply all, cherry-pick, or discard
- Multiple background agents can run simultaneously in separate worktrees

```json
// Copy extra files into worktrees (e.g., git-ignored config)
"git.worktreeIncludeFiles": ["config/local.json", ".env.local"]
```

**New in v1.110:** Background agents now support `/compact` for manual context compaction, slash commands for prompts/hooks/skills, and session renaming [^1].

### Parallel Subagents & Explore (v1.108 → v1.110)

Agents can delegate subtasks to **subagents** that operate in their own context windows [^2] [^3]. Subagents run in parallel, significantly speeding up tasks that can be split into independent parts.

**New in v1.110:** A dedicated **Explore subagent** handles all codebase research for the Plan agent [^1]. Explore is read-only, uses only search and file read tools, and runs on fast models (Claude Haiku 4.5, Gemini 3 Flash) by default.

```json
// Override the model used by Explore
"chat.exploreAgent.defaultModel": "claude-haiku-4-5"
```

### Session Management (v1.109 → v1.110)

A new experimental welcome page surfaces your agent sessions front and center when you open VS Code [^2]:

```json
"workbench.startupEditor": "agentSessionsWelcomePage"
```

**New in v1.110:** Fork sessions with `/fork` to branch conversations without losing context. Context compaction (`/compact`) manually summarizes history when approaching context limits. Plans persist to session memory across turns [^1].

---

<!-- 🎬 MAJOR SECTION: Agent Customization -->
## Agent Customization

### Agent Skills — From Experimental to GA (v1.108 → v1.109)

Agent Skills package domain expertise into reusable folders that agents load on-demand. Skills went from experimental in v1.108 to **generally available and enabled by default** in v1.109 [^2] [^3]:

```
.github/skills/
  api-design/
    SKILL.md          # Instructions, templates, validation
  security-review/
    SKILL.md
```

Each `SKILL.md` has a description in its frontmatter — agents match skills to tasks automatically.

```json
// Skills are enabled by default in v1.109+
"chat.useAgentSkills": true,

// Add custom skill locations
"chat.agentSkillsLocations": {
  "~/.copilot/skills": true,
  "shared/team-skills": true
}
```

Extension authors can also package skills using the `chatSkills` contribution point [^2].

### Agent Plugins (Experimental, v1.110)

Agent Plugins are prepackaged bundles of chat customizations — skills, commands, agents, MCP servers, and hooks — installable directly from the Extensions view [^1]:

```json
// Enable agent plugins
"chat.plugins.enabled": true,

// Add additional plugin marketplaces (GitHub repos)
"chat.plugins.marketplaces": ["copilot-plugins", "awesome-copilot"],

// Register local plugin directories
"chat.plugins.paths": {"/path/to/local/plugin": true}
```

Search and install plugins with `@agentPlugins` in the Extensions view or via the **Chat: Plugins** command.

### Custom Agent Controls (v1.109)

Custom agents (`.agent.md` files) gained powerful new attributes [^2]:

- **`user-invokable: false`** — Create agents accessible only as subagents, not from the agents dropdown
- **`disable-model-invocation`** — Prevent an agent from being invoked automatically by other agents
- **`agents: ['Modify', 'Search']`** — Restrict which subagents a given agent can invoke
- **Multiple model support** — Specify fallback models in order of preference

```markdown
---
name: architect
model: ['Claude Sonnet 4.5 (copilot)', 'GPT-5 (copilot)']
tools: ['readFiles', 'codeSearch', 'agent']
agents: ['Modify', 'Search']
user-invokable: true
---

You are an experienced software architect...
```

### Organization-Wide Instructions (v1.108 → v1.109)

**Org-level custom agents** and **org-level custom instructions** let GitHub organizations enforce consistent AI guidance across all developers [^2] [^3]:

```json
// Enabled by default in v1.109+
"github.copilot.chat.organizationInstructions.enabled": true
```

### Create Agent Customizations from Chat (v1.110)

Generate agent customization files directly from conversations using `/create-*` slash commands [^1]:

- `/create-prompt` — Generate a reusable prompt file
- `/create-instruction` — Generate an instruction file for project conventions
- `/create-skill` — Extract a multi-step workflow into a skill package
- `/create-agent` — Create a specialized custom agent persona
- `/create-hook` — Create a hook configuration for lifecycle automation

After debugging an issue, use `/create-skill` to capture the procedure as reusable expertise. Natural language works too: "save this workflow as a skill".

### `/init` — Bootstrap Your Workspace for AI (v1.109)

The new `/init` slash command analyzes your project structure and generates a tailored `copilot-instructions.md` or `AGENTS.md` file automatically [^2].

### Agent Debug Panel (Preview, v1.110)

The new Agent Debug panel provides deep visibility into chat sessions and customization loading [^1]:

- Real-time chat events including system prompts, tool calls, and customization events
- See exactly which prompt files, skills, hooks, and agents are loaded for a session
- Chart view displays visual hierarchy of events for quick structural understanding
- Replaces the old Diagnostics chat action with richer detail

Open from Command Palette: **Developer: Open Agent Debug Panel**, or select the gear icon in Chat view → **View Agent Logs**.

---

<!-- 🎬 MAJOR SECTION: Claude & Anthropic Integration -->
## Claude & Anthropic Integration

### Claude Agent (v1.109 → v1.110)

VS Code supports the **Claude Agent SDK** directly — delegate tasks using the Anthropic agent harness with models from your GitHub Copilot subscription [^2]. Claude Agent appears as a session type alongside Local, Background, and Cloud.

**New in v1.110:** Steering and queuing for mid-conversation redirects, session renaming, context window rendering with compaction, additional slash commands (`/compact`, `/agents`, `/hooks`), and significant performance improvements [^1].

### Thinking Tokens (v1.108 → v1.110)

Anthropic models now show **thinking tokens** — visible reasoning that shows hypothesis formation, tool selection, and error recovery in real-time [^2]:

```json
// Configure extended thinking budget (default: 4000, set 0 to disable)
"github.copilot.chat.anthropic.thinking.budgetTokens": 10000,

// Choose detailed or compact thinking style
"chat.thinking.style": "detailed",

// Collapse tool sections to reduce noise
"chat.agent.thinking.collapsedTools": ["terminal", "search"],

// Auto-expand failing tool calls
"chat.tools.autoExpandFailures": true
```

The Messages API with **interleaved thinking** enables Claude to reason between tool calls, providing more contextual multi-step responses [^2].

### Additional Claude Features (v1.109 → v1.110)

- **Tool search tool** — Helps Claude discover the most relevant tools from a large pool [^2]
- **Context editing (Experimental)** — Clears tool results and thinking tokens from previous turns [^2]
- **`getDiagnostics` tool** — Let the agent access editor and workspace problems (v1.110) [^1]
- **Custom thinking phrases** — Customize loading text during reasoning (v1.110) [^1]

```json
"chat.agent.thinking.phrases": {
  "mode": "replace",
  "phrases": ["Analyzing architecture...", "Evaluating patterns..."]
}
```

---

<!-- 🎬 MAJOR SECTION: Security & Trust -->
## Security & Trust

### Terminal Sandboxing (v1.109 → v1.110)

OS-level sandboxing restricts agent-executed terminal commands [^2]:

- **File system**: Read/write only within the workspace directory
- **Network**: Blocked by default; specific domains can be allowlisted
- **Supported on**: macOS (`sandbox-exec`) and Linux (Landlock/seccomp)

```json
{
  "chat.tools.terminal.sandbox.enabled": true,
  "chat.tools.terminal.sandbox.network": ["github.com", "npmjs.com"]
}
```

**New in v1.110:** Trusted domains can be selected via `allowTrustedDomains` in network settings. No installation required on macOS; Linux works without ripgrep. Improved detection with clear feedback on blocked domains [^1].

### Auto-Approval & YOLO Mode (v1.108 → v1.110)

Auto-approval has expanded progressively across releases [^1] [^2] [^3]:

| Release | New Auto-Approved Commands |
|---------|---------------------------|
| v1.108 | `git ls-files`, `rg`, `sed`, workspace npm scripts via `npm`/`pnpm`/`yarn` |
| v1.109 | `Set-Location`, `dir`, `docker` (safe sub-commands), `npm`/`yarn`/`pnpm` (safe sub-commands) |
| v1.110 | `/autoApprove` and `/yolo` slash commands for global auto-approve toggle |

```json
"chat.tools.terminal.enableAutoApprove": true,
"chat.tools.terminal.autoApproveWorkspaceNpmScripts": true
```

**New in v1.110:** Toggle auto-approve directly from chat with `/autoApprove` or `/yolo` (and disable with `/disableAutoApprove` or `/disableYolo`) [^1].

### Terminal Tool Improvements (v1.109 → v1.110)

- **Richer command details** — Inline syntax highlighting for Python/Node/Ruby, working directory display, command intent description on hover [^2]
- **Output streaming** — Long-running commands auto-expand to show progress; quick commands stay collapsed [^2]
- **Interactive input** — Embedded terminals support direct typing for confirmation prompts [^2]
- **Timeout property** — Required on all terminal tool calls; prevents hung processes [^2]
- **Background management** — `awaitTerminal` and `killTerminal` tools for proper lifecycle control [^2]
- **No shell history** — Agent-executed commands no longer appear in shell history (v1.108) [^3]
- **Collapsible terminal calls** — Terminal output displayed as collapsible sections to reduce noise (v1.110) [^1]
- **Prevent auto-suspend** — VS Code asks the OS not to suspend while chat requests run (v1.110) [^1]

---

<!-- 🎬 MAJOR SECTION: Chat UX & Productivity -->
## Chat UX & Productivity

### Agentic Browser Tools (Experimental, v1.110)

Agents can now autonomously interact with the integrated browser to validate web app changes while building them [^1]:

- **Page navigation**: `openBrowserPage`, `navigatePage`
- **Page content**: `readPage`, `screenshotPage`
- **User interaction**: `clickElement`, `hoverElement`, `dragElement`, `typeInPage`, `handleDialog`
- **Custom automation**: `runPlaywrightCode`

```json
"workbench.browser.enableChatTools": true
```

Pages opened by agents run in private, in-memory sessions. Explicitly share a page to give the agent temporary access.

### Tools for Usages and Rename (v1.110)

New `usages` and `rename` tools leverage existing LSP capabilities for precise code navigation and refactoring [^1]. Agents should pick these up automatically, but you can hint with `#rename` or `#usages`.

### Mermaid Diagrams in Chat (v1.109)

Chat responses can now render interactive Mermaid diagrams — flowcharts, sequence diagrams, and more. Pan, zoom, and open in a full-sized editor [^2].

### Ask Questions Tool (v1.109 → v1.110)

Instead of making assumptions, the agent can present clarifying questions with single/multi-select options, free text, and recommended answers. The **Plan agent** uses this in a structured 4-phase workflow: Discovery → Alignment → Design → Refinement [^2].

**New in v1.110:** The tool moved into VS Code core for improved reliability. Send steering messages without dismissing questions first. Keyboard navigation with Alt+N/Alt+P [^1].

### Context Window & Compaction (v1.109 → v1.110)

A context window indicator in the chat input area shows token usage breakdown by category on hover [^2].

**New in v1.110:** Manual context compaction with `/compact` summarizes conversation history to free up space. Add instructions like `/compact focus on database decisions`. Available for local, background, and Claude sessions [^1].

### Copilot Memory (Preview, v1.109)

Persistent context across sessions — the agent can store and recall important information like preferences, conventions, and project context [^2]:

```json
"github.copilot.chat.copilotMemory.enabled": true
```

**New in v1.110:** Plans created by the Plan agent persist to session memory and stay available across turns, including after context compaction [^1].

### Integrated Browser (Preview, v1.109)

A full integrated browser replaces the limited Simple Browser. Sign into websites, use DevTools, send elements to chat for AI assistance [^2]:

```json
"workbench.browser.openLocalhostLinks": true,
"simpleBrowser.useIntegratedBrowser": true
```

### MCP Apps (v1.109)

MCP servers can display rich interactive UI in the client — flame graphs, custom visualizations, and more [^2].

### Chat UX Improvements (v1.110)

- **Redesigned model picker** — Organized sections (Auto, Featured, Recent, Other), search box, rich hover with model capabilities [^1]
- **Contextual tips** — Feature discovery suggestions based on your usage patterns (`chat.tips.enabled`) [^1]
- **Inline chat hover mode** — New lightweight UI via `inlineChat.renderMode` [^1]
- **Inline chat affordance** — Easier access to inline chat via `inlineChat.affordance` (editor or gutter) [^1]
- **Edit mode deprecated** — Agent mode now handles everything; edit mode hidden by default [^1]

### External Indexing for Non-GitHub Workspaces (v1.109)

Workspaces not hosted on GitHub can now be remotely indexed for fast semantic search (`#codebase`), providing the same code search experience as GitHub-hosted repos [^2].

### Language Models Editor (v1.108 → v1.109)

A centralized editor for managing all language models — toggle visibility, add providers, configure API keys, manage multiple configurations per provider [^2] [^3]. Model configurations are now stored in a dedicated `chatLanguageModels.json` file.

### Inline Chat UX Revamp (v1.108 → v1.110)

Inline chat is optimized for quick single-file code changes, with a lightweight contextual rendering mode [^2] [^3]. In v1.110, inline chat queues messages into existing agent sessions when files have pending changes [^1].

---

## 🧠 Mental Model Shift

> **The Core Insight:** From **one AI assistant you converse with** to **a team of specialized AI agents you orchestrate**

### Move Toward ✅

- ✅ **Multi-session workflows**: Plan locally → implement in background → review worktree diff → merge selectively
- ✅ **Domain-specific Skills**: Capture team expertise once in `SKILL.md` files; agents apply it automatically
- ✅ **Visible reasoning**: Enable thinking tokens on complex tasks to see hypotheses, tool choices, and error recovery
- ✅ **Sandboxed autonomy**: Auto-approve safe commands while sandboxing blocks system access
- ✅ **Organization consistency**: Org-level agents and instructions enforce standards across teams
- ✅ **Agent Plugins**: Install prepackaged customizations from Extensions view for instant capability boosts
- ✅ **Browser automation**: Let agents validate web apps autonomously with agentic browser tools

### Move Away From ⚠️

- ⚠️ **Single long conversations**: Context overflow degrades quality; use subagents and session handoffs instead
- ⚠️ **Manual approval fatigue**: Configure auto-approval rules and sandboxing instead of clicking "allow" 50 times
- ⚠️ **Per-developer customization**: Org-level customization replaces individual `copilot-instructions.md` divergence

### Move Against 🛑

- 🛑 **Unsandboxed autonomous agents**: Never run background agents with unrestricted system and network access
- 🛑 **Context dumping**: Never paste an entire codebase into one conversation — use `#codebase`, subagents, and targeted context

---

## ✅ What You Can Do Today

**Immediate (5 minutes):**
- [ ] Update VS Code to v1.110+
- [ ] Try `/init` to bootstrap workspace instructions for your project
- [ ] Enable thinking tokens: `"github.copilot.chat.anthropic.thinking.budgetTokens": 4000`
- [ ] Try `/fork` to branch a conversation for exploring alternatives

**Short-Term (30 minutes):**
- [ ] Enable terminal sandboxing: `"chat.tools.terminal.sandbox.enabled": true`
- [ ] Create your first Agent Skill in `.github/skills/` for a common team pattern
- [ ] Install an Agent Plugin via `@agentPlugins` in Extensions view
- [ ] Use `/compact` to manually compact a long conversation

**Explore Further (1 hour):**
- [ ] Define a custom agent (`.agent.md`) with subagent invocation and model fallback
- [ ] Enable Copilot Memory: `"github.copilot.chat.copilotMemory.enabled": true`
- [ ] Try agentic browser tools: `"workbench.browser.enableChatTools": true`
- [ ] Use `/create-skill` to extract a debugging workflow from a conversation
- [ ] Open Agent Debug Panel to understand customization loading
- [ ] Try agentic browser tools: `"workbench.browser.enableChatTools": true`
- [ ] Use `/create-skill` to extract a debugging workflow from a conversation
- [ ] Open Agent Debug Panel to understand customization loading
- [ ] Enable the GitHub MCP Server: `"github.copilot.chat.githubMcpServer.enabled": true`

---

## Key Settings Reference

Quick reference for all settings mentioned in this talk:

```json
{
  // Agent Sessions & Orchestration
  "chat.viewSessions.orientation": "sideBySide",
  "git.worktreeIncludeFiles": [],
  "chat.exploreAgent.defaultModel": "claude-haiku-4-5",

  // Agent Customization
  "chat.useAgentSkills": true,
  "chat.agentSkillsLocations": {},
  "chat.customAgentInSubagent.enabled": true,
  "github.copilot.chat.organizationInstructions.enabled": true,
  "chat.plugins.enabled": true,
  "chat.plugins.marketplaces": [],

  // Claude & Anthropic
  "github.copilot.chat.anthropic.thinking.budgetTokens": 4000,
  "chat.thinking.style": "detailed",
  "chat.tools.autoExpandFailures": true,
  "chat.agent.thinking.phrases": {},

  // Security & Trust
  "chat.tools.terminal.sandbox.enabled": true,
  "chat.tools.terminal.sandbox.network": [],
  "chat.tools.terminal.enableAutoApprove": true,
  "chat.tools.terminal.autoApproveWorkspaceNpmScripts": true,

  // Productivity
  "github.copilot.chat.copilotMemory.enabled": true,
  "workbench.browser.openLocalhostLinks": true,
  "workbench.browser.enableChatTools": true,
  "github.copilot.chat.githubMcpServer.enabled": true,
  "chat.tips.enabled": true,
  "inlineChat.renderMode": "hover",
  "inlineChat.affordance": "editor"
}
```

---

## Related Patterns

- **[Copilot Chat](../copilot-chat/)** — Deep dive on context mechanisms and chat architecture
- **[Copilot CLI](../copilot-cli/)** — Command-line Copilot experience
- **[Custom Agents & Skills](../copilot-primitives/)** — Comprehensive guide to agent customization primitives
- **[Terminal Sandboxing](../terminal-sandboxing/)** — Deep dive on sandboxing configuration
- **[Copilot Memory](../copilot-memory/)** — Detailed exploration of persistent context

See [DECISION-GUIDE.md](../DECISION-GUIDE.md) for complete navigation help.

---

## 📖 References

[^1]: **[VS Code Release Notes: February 2026 (v1.110)](https://code.visualstudio.com/updates/v1_110)** — Agent Plugins, agentic browser tools, context compaction, session forking, /create-* commands, Explore subagent, Kitty graphics

[^2]: **[VS Code Release Notes: January 2026 (v1.109)](https://code.visualstudio.com/updates/v1_109)** — Chat UX, Agent Sessions, Agent Customization, Claude Agent, terminal sandboxing, Copilot Memory, MCP Apps

[^3]: **[VS Code Release Notes: December 2025 (v1.108)](https://code.visualstudio.com/updates/v1_108)** — Agent Skills experimental, Agent Sessions view, terminal IntelliSense rework, housekeeping

[^4]: **[GitHub Copilot in VS Code Documentation](https://code.visualstudio.com/docs/copilot/overview)** — Comprehensive guide to Copilot features, agent types, and customization

[^5]: **[Agent Plugins Documentation](https://code.visualstudio.com/docs/copilot/customization/agent-plugins)** — Installing and creating agent plugin bundles

[^6]: **[Agent Skills Documentation](https://code.visualstudio.com/docs/copilot/customization/agent-skills)** — Creating and using Agent Skills in VS Code

[^7]: **[Custom Agents Documentation](https://code.visualstudio.com/docs/copilot/customization/custom-agents)** — Defining custom agents with `.agent.md` files

[^8]: **[Background Agents Documentation](https://code.visualstudio.com/docs/copilot/agents/background-agents)** — Using background agents with Git worktree isolation

---

## 🎭 Behind the Scenes

### The Copilot Extension Unification

In v1.108, inline suggestions began being served from the GitHub Copilot **Chat** extension. By v1.109, the original GitHub Copilot extension was **fully deprecated** and auto-uninstalled on update [^2]. All AI functionality now lives in a single extension: GitHub Copilot Chat.

### Engineering Highlights

- **v1.108 Housekeeping**: The VS Code team closed **5,951 issues** across all repositories, including 2,872 in the core `microsoft/vscode` repo and 1,659 in `microsoft/vscode-copilot-release` [^3]
- **TypeScript-Go (tsgo)**: VS Code now defaults to TSGo for development, with built-in extensions compiling in under a second [^1]
- **Extension bundling with esbuild**: Most built-in extensions migrated from webpack to esbuild for faster builds [^1]
- **macOS DMG installer**: VS Code ships DMG images for native drag-and-drop installation [^2]
- **Windows 11 context menu**: Right-click in File Explorer now shows VS Code in the top-level context menu [^2]
- **Kitty graphics protocol**: Terminal now supports high-fidelity image rendering (v1.110) [^1]
- **Modal editors**: Experimental floating editor experience for Settings, Keyboard Shortcuts, etc. (v1.110) [^1]
- **Edit mode deprecated**: Hidden by default in v1.110, fully removed in v1.125 [^1]
