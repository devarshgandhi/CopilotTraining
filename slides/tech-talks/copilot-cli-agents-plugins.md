---
theme: default
class: text-center
highlighter: shiki
lineNumbers: false
info: |
  ## Copilot CLI: Agents, Skills & the Plugin Ecosystem
  CopilotTraining Tech Talk
drawings:
  persist: false
transition: slide-left
title: Copilot CLI - Agents, Skills & Plugins
module: tech-talks/copilot-cli-agents-plugins
mdc: true
status: active
updated: 2025-07-17
---

<div class="h-full flex flex-col items-center justify-center relative overflow-hidden">
<div class="absolute inset-0 bg-gradient-to-br from-cyan-900/20 via-blue-900/10 to-indigo-900/20"></div>
<div class="absolute top-1/4 left-1/2 -translate-x-1/2 -translate-y-1/2 w-96 h-96 bg-gradient-to-r from-cyan-500/20 via-blue-500/20 to-indigo-500/20 rounded-full blur-3xl"></div>
<div class="relative z-10">
<div class="absolute inset-0 blur-2xl opacity-50">
<img src="./sdp-logo.png" class="w-64" alt="" />
</div>
<img src="./sdp-logo.png" class="w-64 relative" alt="SDP Logo" />
</div>
<h1 class="!text-5xl !font-bold !mt-8 bg-gradient-to-r from-cyan-400 via-blue-400 to-indigo-400 bg-clip-text text-transparent relative z-10">
Copilot CLI: Agents, Skills & Plugins
</h1>
<div class="mt-4 relative z-10">
<span class="px-6 py-2 bg-gradient-to-r from-cyan-600/80 to-blue-600/80 rounded-full text-white text-xl font-medium shadow-lg shadow-cyan-500/25">
Extending Copilot Beyond Defaults
</span>
</div>
<div class="mt-8 text-lg opacity-70 relative z-10">
⏰ <strong>30 minutes</strong> · Developers already using Copilot who want to go deeper
</div>
<div class="mt-6 w-32 h-1 bg-gradient-to-r from-transparent via-cyan-400 to-transparent rounded-full relative z-10"></div>
</div>

<div class="abs-br m-6 flex gap-2">
<span class="text-sm opacity-50">Tech Talk · 30 minutes</span>
</div>

---

# The Central Question

<div class="h-full flex items-center justify-center">
<div class="max-w-4xl">
<div class="text-6xl text-center mb-8">🤔</div>
<div class="text-3xl font-bold text-center bg-gradient-to-r from-cyan-400 to-blue-400 bg-clip-text text-transparent mb-6 leading-snug">
"How do I extend Copilot CLI beyond its defaults — building custom agents, migrating skills from IDE to CLI, and distributing reusable capabilities through plugins?"
</div>
<div class="mt-8 flex gap-6 justify-center text-sm">
<div class="px-4 py-2 bg-cyan-900/40 rounded-lg border border-cyan-500/50 text-center">
<div class="font-bold text-cyan-300">🤖 Custom Agents</div>
<div class="text-xs opacity-80 mt-1">Specialized AI personas</div>
</div>
<div class="px-4 py-2 bg-blue-900/40 rounded-lg border border-blue-500/50 text-center">
<div class="font-bold text-blue-300">⚡ Fleet Mode</div>
<div class="text-xs opacity-80 mt-1">Parallel orchestration</div>
</div>
<div class="px-4 py-2 bg-indigo-900/40 rounded-lg border border-indigo-500/50 text-center">
<div class="font-bold text-indigo-300">📋 Skills</div>
<div class="text-xs opacity-80 mt-1">Portable procedures</div>
</div>
<div class="px-4 py-2 bg-purple-900/40 rounded-lg border border-purple-500/50 text-center">
<div class="font-bold text-purple-300">📦 Plugins</div>
<div class="text-xs opacity-80 mt-1">Team distribution</div>
</div>
</div>
</div>
</div>

---

# 📖 Navigate by Section

<div class="grid grid-cols-2 gap-6 mt-8">
<div @click="$nav.go(6)" class="cursor-pointer p-6 bg-cyan-900/40 rounded-lg border-2 border-cyan-500 hover:bg-cyan-900/60 transition-all">
<div class="text-2xl mb-2">🤖</div>
<div class="text-lg font-bold text-cyan-300">Custom Agents</div>
<div class="text-sm text-gray-300 mt-1">Specialized AI for Every Workflow</div>
<div class="text-xs text-gray-400 mt-2">.agent.md profiles · Scoped tools · Model selection</div>
</div>
<div @click="$nav.go(9)" class="cursor-pointer p-6 bg-blue-900/40 rounded-lg border-2 border-blue-500 hover:bg-blue-900/60 transition-all">
<div class="text-2xl mb-2">⚡</div>
<div class="text-lg font-bold text-blue-300">Fleet Mode</div>
<div class="text-sm text-gray-300 mt-1">Parallel Execution with Subagents</div>
<div class="text-xs text-gray-400 mt-2">45 min → 12 min · /fleet command</div>
</div>
<div @click="$nav.go(12)" class="cursor-pointer p-6 bg-indigo-900/40 rounded-lg border-2 border-indigo-500 hover:bg-indigo-900/60 transition-all">
<div class="text-2xl mb-2">📋</div>
<div class="text-lg font-bold text-indigo-300">Skills</div>
<div class="text-sm text-gray-300 mt-1">The Portable Procedural Standard</div>
<div class="text-xs text-gray-400 mt-2">SKILL.md · On-demand loading · Cross-IDE</div>
</div>
<div @click="$nav.go(14)" class="cursor-pointer p-6 bg-purple-900/40 rounded-lg border-2 border-purple-500 hover:bg-purple-900/60 transition-all">
<div class="text-2xl mb-2">📦</div>
<div class="text-lg font-bold text-purple-300">Plugins</div>
<div class="text-sm text-gray-300 mt-1">The Distribution Layer</div>
<div class="text-xs text-gray-400 mt-2">Installable packages · Marketplaces</div>
</div>
</div>

<div class="mt-8 p-4 bg-gradient-to-r from-cyan-900/30 to-purple-900/30 rounded-lg text-center">
<span class="text-white font-bold">💡 Click any section to jump directly there</span>
</div>

---

# The Problem

<div class="grid grid-cols-2 gap-4 mt-4 text-xs">
<div class="p-4 bg-red-900/30 rounded-lg border-l-4 border-red-500">
<div class="font-bold text-red-300 mb-2">🤷 Default Agents Are Generic</div>
<div class="text-gray-300">Built-in agents handle common patterns, but every team has domain-specific workflows — security audits, framework migrations, infrastructure runbooks — that require specialized knowledge</div>
</div>
<div class="p-4 bg-orange-900/30 rounded-lg border-l-4 border-orange-500">
<div class="font-bold text-orange-300 mb-2">🔒 IDE Customizations Don't Travel</div>
<div class="text-gray-300">Teams invest hours crafting copilot-instructions.md and IDE settings, but those customizations stay locked inside one editor. Switch to CLI or another IDE — start from scratch</div>
</div>
<div class="p-4 bg-yellow-900/30 rounded-lg border-l-4 border-yellow-500">
<div class="font-bold text-yellow-300 mb-2">🔧 Manual Setup for Every Project</div>
<div class="text-gray-300">Configuring agents, MCP servers, and skills manually in every repository means 30+ minutes of repetitive setup. Team expertise lives in wikis instead of installable packages</div>
</div>
<div class="p-4 bg-amber-900/30 rounded-lg border-l-4 border-amber-500">
<div class="font-bold text-amber-300 mb-2">🐌 Sequential Execution Bottleneck</div>
<div class="text-gray-300">Complex tasks like "refactor 8 services" execute one step at a time — turning a 2-hour task into an all-afternoon affair when components could run in parallel</div>
</div>
</div>

<div class="mt-4 p-3 bg-gradient-to-r from-red-600/40 to-orange-600/40 rounded-xl border border-red-500/50 text-center text-sm">
<div class="font-bold">You've hit the ceiling — Copilot CLI needs to be customizable, portable, parallel, and distributable</div>
</div>

---

# The Solution: 4-Layer Extensibility Stack

<div class="grid grid-cols-4 gap-3 mt-6">
<div class="p-3 bg-cyan-900/40 rounded-lg border-2 border-cyan-500 text-center">
<div class="text-2xl mb-2">🤖</div>
<div class="font-bold text-cyan-300 text-sm">Custom Agents</div>
<div class="text-xs text-gray-400 mt-1">WHO does the work</div>
<div class="text-xs text-gray-300 mt-2">Specialized AI personas with tailored tools &amp; models</div>
</div>
<div class="p-3 bg-blue-900/40 rounded-lg border-2 border-blue-500 text-center">
<div class="text-2xl mb-2">📋</div>
<div class="font-bold text-blue-300 text-sm">Skills</div>
<div class="text-xs text-gray-400 mt-1">HOW they work</div>
<div class="text-xs text-gray-300 mt-2">Portable procedures loaded on-demand across all surfaces</div>
</div>
<div class="p-3 bg-indigo-900/40 rounded-lg border-2 border-indigo-500 text-center">
<div class="text-2xl mb-2">⚡</div>
<div class="font-bold text-indigo-300 text-sm">Fleet Mode</div>
<div class="text-xs text-gray-400 mt-1">WHEN they collaborate</div>
<div class="text-xs text-gray-300 mt-2">Parallel orchestration via subagents with isolated context</div>
</div>
<div class="p-3 bg-purple-900/40 rounded-lg border-2 border-purple-500 text-center">
<div class="text-2xl mb-2">📦</div>
<div class="font-bold text-purple-300 text-sm">Plugins</div>
<div class="text-xs text-gray-400 mt-1">HOW it all ships</div>
<div class="text-xs text-gray-300 mt-2">Bundle everything into discoverable, installable packages</div>
</div>
</div>

<div class="mt-6 text-center text-sm text-gray-400">
Each layer is <strong>optional and independent</strong> — use custom agents without skills, skills without plugins, or fleet mode alone
</div>

<div class="mt-4 p-3 bg-gradient-to-r from-cyan-600/80 to-purple-600/80 rounded-lg text-center">
<span class="text-white font-bold">Together: team expertise becomes infrastructure</span>
</div>

---
layout: center
name: custom-agents
---

# 🤖 Custom Agents

<div class="text-5xl font-bold bg-gradient-to-r from-cyan-400 to-blue-400 bg-clip-text text-transparent">
Specialized AI for Every Workflow
</div>

<div class="mt-6 text-xl opacity-80">
Section 1 of 4 · .agent.md profiles with tailored expertise
</div>

<div class="mt-8 text-sm opacity-60">
Define WHO does the work — scoped tools, model selection, behavioral instructions
</div>

---

# Custom Agent Anatomy

<div class="grid grid-cols-2 gap-4 mt-4">
<div>

```markdown
# .github/agents/security-reviewer.agent.md
---
description: "Reviews code for security
  vulnerabilities and OWASP compliance"
tools:
  - read
  - search
  - github-mcp-server
model: claude-opus-4.6
---

You are a senior security engineer.
## Review Process
1. Check OWASP Top 10 vulnerabilities
2. Verify input validation
3. Review dependency CVEs
4. Flag hardcoded secrets
```

</div>
<div class="text-sm space-y-3">
<div class="p-3 bg-cyan-900/40 rounded-lg border-l-4 border-cyan-500">
<div class="font-bold text-cyan-300">📝 description</div>
<div class="text-xs text-gray-300 mt-1">Controls when Copilot auto-routes work to this agent</div>
</div>
<div class="p-3 bg-blue-900/40 rounded-lg border-l-4 border-blue-500">
<div class="font-bold text-blue-300">🔧 tools</div>
<div class="text-xs text-gray-300 mt-1">Principle of least privilege — restrict what the agent can do</div>
</div>
<div class="p-3 bg-indigo-900/40 rounded-lg border-l-4 border-indigo-500">
<div class="font-bold text-indigo-300">🧠 model</div>
<div class="text-xs text-gray-300 mt-1">Right model for the task — Opus for deep review, Haiku for quick checks</div>
</div>
<div class="p-3 bg-purple-900/40 rounded-lg border-l-4 border-purple-500">
<div class="font-bold text-purple-300">📄 Markdown body</div>
<div class="text-xs text-gray-300 mt-1">Up to 30K chars of behavioral instructions — the agent's prompt</div>
</div>
</div>
</div>

---

# Agent Scope & Built-in Agents

<div class="grid grid-cols-2 gap-4 mt-4">
<div>
<div class="text-sm font-bold text-cyan-300 mb-3">📂 Scope Hierarchy</div>
<div class="space-y-2 text-xs">
<div class="p-2 bg-purple-900/40 rounded-lg border-l-4 border-purple-500">
<span class="font-bold text-purple-300">Enterprise</span> — <code>.github-private</code> repo · Governance &amp; policy
</div>
<div class="p-2 bg-indigo-900/40 rounded-lg border-l-4 border-indigo-500">
<span class="font-bold text-indigo-300">Organization</span> — <code>.github-private</code> repo · Company standards
</div>
<div class="p-2 bg-blue-900/40 rounded-lg border-l-4 border-blue-500">
<span class="font-bold text-blue-300">Repository</span> — <code>.github/agents/</code> · Project-specific workflows
</div>
<div class="p-2 bg-cyan-900/40 rounded-lg border-l-4 border-cyan-500">
<span class="font-bold text-cyan-300">User</span> — <code>~/.copilot/agents/</code> · Personal productivity
</div>
</div>
</div>
<div>
<div class="text-sm font-bold text-blue-300 mb-3">🤖 Built-in Agents</div>
<div class="space-y-2 text-xs">
<div class="p-2 bg-gray-800 rounded-lg">
<span class="font-bold text-emerald-300">Explore</span> — Fast codebase Q&amp;A and structure analysis
</div>
<div class="p-2 bg-gray-800 rounded-lg">
<span class="font-bold text-teal-300">Task</span> — Command execution, brief on success, verbose on failure
</div>
<div class="p-2 bg-gray-800 rounded-lg">
<span class="font-bold text-cyan-300">General-purpose</span> — Complex multi-step tasks, full toolset
</div>
<div class="p-2 bg-gray-800 rounded-lg">
<span class="font-bold text-blue-300">Code-review</span> — High signal-to-noise review, genuine bugs only
</div>
</div>
<div class="mt-3 p-2 bg-gray-900 rounded-lg text-xs font-mono text-gray-300">
/agent → browse &amp; select interactively<br />
copilot --agent=security-reviewer
</div>
</div>
</div>

---
layout: center
name: fleet-mode
---

# ⚡ Fleet Mode

<div class="text-5xl font-bold bg-gradient-to-r from-blue-400 to-indigo-400 bg-clip-text text-transparent">
Parallel Execution with Subagents
</div>

<div class="mt-6 text-xl opacity-80">
Section 2 of 4 · /fleet command for parallel task orchestration
</div>

<div class="mt-8 text-sm opacity-60">
45 min sequential → 12 min parallel · Each subagent gets its own context window
</div>

---

# Fleet Mode: How It Works

<div class="mt-4">
<div class="p-3 bg-gray-800 rounded-lg text-xs font-mono text-gray-300 mb-4">
/fleet Refactor all 6 API controllers to use the new middleware pattern
</div>

<div class="flex flex-col items-center gap-3">
<div class="p-3 bg-blue-900/60 rounded-lg border-2 border-blue-400 w-80 text-center">
<div class="font-bold text-blue-300">🎯 Main Agent (Orchestrator)</div>
<div class="text-xs text-gray-300 mt-1">Analyzes → Decomposes → Dispatches → Composes</div>
</div>
<div class="text-2xl text-gray-400">↓ ↓ ↓</div>
<div class="grid grid-cols-3 gap-2 w-full">
<div class="p-2 bg-cyan-900/40 rounded-lg border border-cyan-500/50 text-center text-xs">
<div class="font-bold text-cyan-300">Subagent 1</div>
<div class="text-gray-400">users-ctrl</div>
</div>
<div class="p-2 bg-cyan-900/40 rounded-lg border border-cyan-500/50 text-center text-xs">
<div class="font-bold text-cyan-300">Subagent 2</div>
<div class="text-gray-400">orders-ctrl</div>
</div>
<div class="p-2 bg-cyan-900/40 rounded-lg border border-cyan-500/50 text-center text-xs">
<div class="font-bold text-cyan-300">Subagent 3</div>
<div class="text-gray-400">products-ctrl</div>
</div>
<div class="p-2 bg-cyan-900/40 rounded-lg border border-cyan-500/50 text-center text-xs">
<div class="font-bold text-cyan-300">Subagent 4</div>
<div class="text-gray-400">payments-ctrl</div>
</div>
<div class="p-2 bg-cyan-900/40 rounded-lg border border-cyan-500/50 text-center text-xs">
<div class="font-bold text-cyan-300">Subagent 5</div>
<div class="text-gray-400">auth-ctrl</div>
</div>
<div class="p-2 bg-cyan-900/40 rounded-lg border border-cyan-500/50 text-center text-xs">
<div class="font-bold text-cyan-300">Subagent 6</div>
<div class="text-gray-400">search-ctrl</div>
</div>
</div>
</div>

<div class="mt-4 grid grid-cols-4 gap-2 text-xs">
<div class="p-2 bg-green-900/30 rounded-lg text-center">
<div class="font-bold text-green-300">🚀 Speed</div>
<div class="text-gray-400">6 files simultaneously</div>
</div>
<div class="p-2 bg-green-900/30 rounded-lg text-center">
<div class="font-bold text-green-300">🎯 Specialization</div>
<div class="text-gray-400">Custom agents per task</div>
</div>
<div class="p-2 bg-green-900/30 rounded-lg text-center">
<div class="font-bold text-green-300">🧠 Isolation</div>
<div class="text-gray-400">No context bleed</div>
</div>
<div class="p-2 bg-green-900/30 rounded-lg text-center">
<div class="font-bold text-green-300">🔀 Model Routing</div>
<div class="text-gray-400">Different models per task</div>
</div>
</div>
</div>

---

# Fleet Mode: When to Use

<div class="grid grid-cols-2 gap-6 mt-6">
<div>
<div class="text-lg font-bold text-green-300 mb-3">✅ Great Fit</div>
<div class="space-y-2 text-sm">
<div class="p-2 bg-green-900/30 rounded-lg border-l-4 border-green-500">Refactor multiple independent files</div>
<div class="p-2 bg-green-900/30 rounded-lg border-l-4 border-green-500">Generate tests for many endpoints</div>
<div class="p-2 bg-green-900/30 rounded-lg border-l-4 border-green-500">Update configs across services</div>
<div class="p-2 bg-green-900/30 rounded-lg border-l-4 border-green-500">Batch code reviews</div>
</div>
</div>
<div>
<div class="text-lg font-bold text-red-300 mb-3">❌ Poor Fit</div>
<div class="space-y-2 text-sm">
<div class="p-2 bg-red-900/30 rounded-lg border-l-4 border-red-500">Sequential data pipeline steps</div>
<div class="p-2 bg-red-900/30 rounded-lg border-l-4 border-red-500">Single complex algorithm design</div>
<div class="p-2 bg-red-900/30 rounded-lg border-l-4 border-red-500">Tasks requiring tight coordination</div>
<div class="p-2 bg-red-900/30 rounded-lg border-l-4 border-red-500">Exploratory/conversational work</div>
</div>
</div>
</div>

<div class="mt-6 p-3 bg-gray-800 rounded-lg text-sm text-center">
<span class="font-bold text-yellow-300">💰 Cost note:</span> Each subagent consumes premium requests independently. Use <code>/fleet</code> when the task has <strong>3+ parallelizable components</strong>.
</div>

---
layout: center
name: skills
---

# 📋 Skills

<div class="text-5xl font-bold bg-gradient-to-r from-indigo-400 to-purple-400 bg-clip-text text-transparent">
The Portable Procedural Standard
</div>

<div class="mt-6 text-xl opacity-80">
Section 3 of 4 · SKILL.md format for cross-surface procedures
</div>

<div class="mt-8 text-sm opacity-60">
Write once → works in CLI, VS Code, JetBrains, GitHub.com, and cloud agents
</div>

---

# Skills: Anatomy & Comparison

<div class="grid grid-cols-2 gap-4 mt-4">
<div>

```markdown
# .github/skills/webapp-testing/SKILL.md
---
name: webapp-testing
description: >-
  E2E testing for web apps using
  Playwright. Use when asked to
  create tests or write E2E tests.
---

## Procedure
1. Analyze target component scope
2. Create tests using AAA pattern
3. Use Playwright with getByRole
4. Run with npx playwright test
5. Add screenshot comparison
```

</div>
<div class="text-xs space-y-2">
<div class="font-bold text-indigo-300 mb-2 text-sm">Skills vs Custom Instructions</div>
<div class="p-2 bg-gray-800 rounded-lg">
<div class="grid grid-cols-2 gap-2">
<div>
<div class="font-bold text-yellow-300">Instructions</div>
<div class="text-gray-400">Always loaded</div>
<div class="text-gray-400">Project conventions</div>
<div class="text-gray-400">Constant token cost</div>
</div>
<div>
<div class="font-bold text-indigo-300">Skills</div>
<div class="text-gray-400">On-demand only</div>
<div class="text-gray-400">Task procedures</div>
<div class="text-gray-400">Zero cost until needed</div>
</div>
</div>
</div>
<div class="p-2 bg-indigo-900/40 rounded-lg border-l-4 border-indigo-500">
<div class="font-bold text-indigo-300">💡 Key Insight</div>
<div class="text-gray-300 mt-1">The <code>description</code> controls <em>when</em> Copilot loads the skill. Vague descriptions → never triggered. Too broad → wasted context tokens.</div>
</div>
<div class="p-2 bg-gray-800 rounded-lg">
<div class="font-bold text-cyan-300 mb-1">📂 Skill Locations</div>
<div class="text-gray-400"><code>.github/skills/</code> → Repository scope</div>
<div class="text-gray-400"><code>~/.copilot/skills/</code> → Personal scope</div>
</div>
</div>
</div>

---
layout: center
name: plugins
---

# 📦 Plugins

<div class="text-5xl font-bold bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">
The Distribution Layer
</div>

<div class="mt-6 text-xl opacity-80">
Section 4 of 4 · Bundle agents, skills, hooks & configs as installable packages
</div>

<div class="mt-8 text-sm opacity-60">
Solve the last-mile problem: how to distribute team expertise as infrastructure
</div>

---

# Plugin Ecosystem

<div class="grid grid-cols-2 gap-4 mt-4">
<div class="text-xs">
<div class="font-bold text-purple-300 text-sm mb-2">📁 Plugin Structure</div>
<div class="p-3 bg-gray-800 rounded-lg font-mono text-gray-300">
my-platform-toolkit/<br />
├── .github/plugin/<br />
│&nbsp;&nbsp; └── plugin.json<br />
├── agents/<br />
│&nbsp;&nbsp; ├── security-reviewer.agent.md<br />
│&nbsp;&nbsp; └── migration-helper.agent.md<br />
├── skills/<br />
│&nbsp;&nbsp; ├── webapp-testing/SKILL.md<br />
│&nbsp;&nbsp; └── api-debugging/SKILL.md<br />
├── hooks.json<br />
├── .mcp.json<br />
└── README.md
</div>
<div class="mt-3 p-2 bg-gray-800 rounded-lg font-mono text-gray-300">
<div class="text-purple-300 font-bold mb-1"># Installation</div>
/plugin install security-toolkit<br />
/plugin install myorg/platform-toolkit<br />
/plugin install ./my-local-plugin
</div>
</div>
<div class="text-xs space-y-2">
<div class="font-bold text-purple-300 text-sm mb-2">⚡ Plugin vs Manual Config</div>
<div class="p-2 bg-red-900/30 rounded-lg border-l-4 border-red-500">
<div class="font-bold text-red-300">Manual Config</div>
<div class="text-gray-400 mt-1">Single repo · Copy/paste sharing · Manual sync · Search repos for discovery</div>
</div>
<div class="p-2 bg-green-900/30 rounded-lg border-l-4 border-green-500">
<div class="font-bold text-green-300">Plugin</div>
<div class="text-gray-400 mt-1">Any project · <code>/plugin install</code> · Managed updates · Marketplace browsing</div>
</div>
<div class="font-bold text-purple-300 text-sm mt-3 mb-2">🏪 Marketplaces</div>
<div class="p-2 bg-purple-900/40 rounded-lg">
<div class="text-gray-300"><strong>copilot-plugins</strong> — Official GitHub-curated</div>
<div class="text-gray-300"><strong>awesome-copilot</strong> — Community collection</div>
<div class="text-gray-300 mt-1">+ Custom org marketplaces via <code>/plugin marketplace add</code></div>
</div>
<div class="p-2 bg-gray-800 rounded-lg">
<div class="font-bold text-gray-300">Lifecycle</div>
<div class="text-gray-400">Create → Publish → Discover → Install → Use → Update</div>
</div>
</div>
</div>

---
layout: two-cols
---

# Before vs After

::left::

### ❌ Before

<div class="space-y-2 text-sm mt-4">
<div class="p-2 bg-red-900/30 rounded-lg border-l-4 border-red-500">
<div class="font-bold text-red-300">Generic agents</div>
<div class="text-xs text-gray-400">Default agents don't know your domain</div>
</div>
<div class="p-2 bg-red-900/30 rounded-lg border-l-4 border-red-500">
<div class="font-bold text-red-300">IDE-locked knowledge</div>
<div class="text-xs text-gray-400">Customizations don't travel to CLI</div>
</div>
<div class="p-2 bg-red-900/30 rounded-lg border-l-4 border-red-500">
<div class="font-bold text-red-300">2+ hours onboarding</div>
<div class="text-xs text-gray-400">Manual agent/MCP/skill setup per repo</div>
</div>
<div class="p-2 bg-red-900/30 rounded-lg border-l-4 border-red-500">
<div class="font-bold text-red-300">45 min sequential</div>
<div class="text-xs text-gray-400">Multi-file refactoring one at a time</div>
</div>
</div>

::right::

### ✨ After

<div class="space-y-2 text-sm mt-4">
<div class="p-2 bg-green-900/30 rounded-lg border-l-4 border-green-500">
<div class="font-bold text-green-300">Specialized agents</div>
<div class="text-xs text-gray-400">.agent.md per workflow with scoped tools</div>
</div>
<div class="p-2 bg-green-900/30 rounded-lg border-l-4 border-green-500">
<div class="font-bold text-green-300">Portable skills</div>
<div class="text-xs text-gray-400">SKILL.md works in CLI, IDE, and cloud</div>
</div>
<div class="p-2 bg-green-900/30 rounded-lg border-l-4 border-green-500">
<div class="font-bold text-green-300">30 seconds onboarding</div>
<div class="text-xs text-gray-400">/plugin install — fully configured instantly</div>
</div>
<div class="p-2 bg-green-900/30 rounded-lg border-l-4 border-green-500">
<div class="font-bold text-green-300">12 min parallel</div>
<div class="text-xs text-gray-400">/fleet dispatches subagents simultaneously</div>
</div>
</div>

---

# 🧠 Mental Model Shift

<div class="mt-4 p-4 bg-gradient-to-r from-cyan-900/30 to-purple-900/30 rounded-xl border border-cyan-500/30 text-center mb-6">
<div class="text-lg font-bold bg-gradient-to-r from-cyan-400 to-purple-400 bg-clip-text text-transparent">From "smart terminal assistant" → "team of specialized AI agents with portable expertise, orchestrated in parallel, distributed as packages"</div>
</div>

<div class="grid grid-cols-3 gap-3 text-xs">
<div class="p-3 bg-green-900/30 rounded-lg border-l-4 border-green-500">
<div class="font-bold text-green-300 mb-2">✅ Move Toward</div>
<div class="space-y-1 text-gray-300">
<div>• Agent-per-workflow design</div>
<div>• Skills as portable playbooks</div>
<div>• Parallel-first for 3+ tasks</div>
<div>• Plugins for team distribution</div>
</div>
</div>
<div class="p-3 bg-yellow-900/30 rounded-lg border-l-4 border-yellow-500">
<div class="font-bold text-yellow-300 mb-2">⚠️ Move Away From</div>
<div class="space-y-1 text-gray-300">
<div>• Monolithic instructions</div>
<div>• IDE-locked customizations</div>
<div>• Sequential complex tasks</div>
<div>• Wiki-based knowledge</div>
</div>
</div>
<div class="p-3 bg-red-900/30 rounded-lg border-l-4 border-red-500">
<div class="font-bold text-red-300 mb-2">🛑 Move Against</div>
<div class="space-y-1 text-gray-300">
<div>• Over-scoping agent perms</div>
<div>• Vague skill descriptions</div>
<div>• Fleet for sequential work</div>
</div>
</div>
</div>

---

# ✅ What You Can Do Today

<div class="grid grid-cols-3 gap-4 mt-6">
<div class="p-4 bg-cyan-900/40 rounded-lg border-2 border-cyan-500">
<div class="text-xl mb-2">⏱️</div>
<div class="font-bold text-cyan-300 text-sm">15 Minutes</div>
<div class="text-xs text-gray-300 mt-2 space-y-1">
<div>• Create your first <code>.agent.md</code></div>
<div>• Run <code>/agent</code> to list agents</div>
<div>• Try <code>/skills list</code> to see skills</div>
</div>
</div>
<div class="p-4 bg-blue-900/40 rounded-lg border-2 border-blue-500">
<div class="text-xl mb-2">🕐</div>
<div class="font-bold text-blue-300 text-sm">1 Hour</div>
<div class="text-xs text-gray-300 mt-2 space-y-1">
<div>• Audit instructions → extract skills</div>
<div>• Create first SKILL.md</div>
<div>• Try <code>/fleet</code> on multi-file task</div>
</div>
</div>
<div class="p-4 bg-purple-900/40 rounded-lg border-2 border-purple-500">
<div class="text-xl mb-2">🚀</div>
<div class="font-bold text-purple-300 text-sm">2-4 Hours</div>
<div class="text-xs text-gray-300 mt-2 space-y-1">
<div>• Build a team plugin</div>
<div>• Set up org marketplace</div>
<div>• Assign models per agent</div>
</div>
</div>
</div>

<div class="mt-6 p-4 bg-gradient-to-r from-cyan-600/80 to-purple-600/80 rounded-lg text-center">
<span class="text-white font-bold">🎯 Start with one custom agent → add skills → try /fleet → package as plugin</span>
</div>

---
layout: center
---

# 🎉 Thank You

<div class="text-2xl opacity-80 mt-4">
Copilot CLI: Agents, Skills & the Plugin Ecosystem
</div>

<div class="mt-8 grid grid-cols-2 gap-4 max-w-lg mx-auto text-sm">
<div class="p-3 bg-cyan-900/40 rounded-lg border border-cyan-500/50 text-center">
<div class="font-bold text-cyan-300">📖 Prerequisites</div>
<div class="text-xs text-gray-400 mt-1">Copilot CLI Fundamentals</div>
</div>
<div class="p-3 bg-blue-900/40 rounded-lg border border-blue-500/50 text-center">
<div class="font-bold text-blue-300">➡️ Next Up</div>
<div class="text-xs text-gray-400 mt-1">MCP Apps · Multi-Step Tasks</div>
</div>
</div>

<div class="mt-8 text-sm opacity-60">
<strong>30 seconds</strong> to install a team's entire AI configuration — that's the plugin promise
</div>
