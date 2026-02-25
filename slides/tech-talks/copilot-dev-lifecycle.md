---
theme: default
background: https://source.unsplash.com/collection/94734566/1920x1080
class: text-center
highlighter: shiki
lineNumbers: false
info: |
  ## The Complete Copilot Lifecycle: From Idea to Deployment and Beyond
  CopilotTraining Tech Talk
drawings:
  persist: false
transition: slide-left
title: Copilot Dev Lifecycle
module: tech-talks/copilot-dev-lifecycle
mdc: true
status: active
updated: 2026-02-25
---

<div class="h-full flex flex-col items-center justify-center relative overflow-hidden">
<div class="absolute inset-0 bg-gradient-to-br from-cyan-900/20 via-blue-900/10 to-indigo-900/20"></div>
<div class="absolute top-1/4 left-1/2 -translate-x-1/2 -translate-y-1/2 w-96 h-96 bg-gradient-to-r from-cyan-500/20 via-blue-500/20 to-indigo-500/20 rounded-full blur-3xl"></div>
<div class="relative z-10">
<div class="absolute inset-0 blur-2xl opacity-80">
<img src="./sdp-logo.png" class="w-64" alt="" />
</div>
<img src="./sdp-logo.png" class="w-64 relative" alt="SDP Logo" />
</div>
<h1 class="!text-5xl !font-bold !mt-8 bg-gradient-to-r from-cyan-400 via-blue-400 to-indigo-400 bg-clip-text text-transparent relative z-10">
The Complete Copilot Lifecycle
</h1>
<div class="mt-4 relative z-10">
<span class="px-6 py-2 bg-gradient-to-r from-cyan-600/80 to-blue-600/80 rounded-full text-white text-xl font-medium shadow-lg shadow-cyan-500/25">
From Idea to Deployment and Beyond
</span>
</div>
<div class="mt-8 text-lg opacity-90 relative z-10">Copilot at every phase — not just code completion</div>
<div class="mt-6 w-32 h-1 bg-gradient-to-r from-transparent via-cyan-400 to-transparent rounded-full relative z-10"></div>
</div>

<div class="abs-br m-6 flex gap-2">
<span class="text-sm opacity-80">Tech Talk · 30 minutes</span>
</div>

---

# The Question This Talk Answers

<div class="flex items-center justify-center h-full">
<div class="max-w-4xl">
<div class="text-3xl font-bold mb-8 text-center bg-gradient-to-r from-cyan-400 to-blue-400 bg-clip-text text-transparent">
"How does GitHub Copilot participate at every phase of the development lifecycle — and how do Agentic Workflows extend this into continuous, autonomous automation?"
</div>
<div class="grid grid-cols-3 gap-6 mt-12">
<div class="p-6 bg-cyan-900/40 rounded-lg border-2 border-cyan-500">
<div class="text-4xl mb-3">🔧</div>
<div class="text-lg font-bold text-cyan-300 mb-2">80% Untapped</div>
<div class="text-sm text-gray-100">Most teams only use autocomplete</div>
</div>
<div class="p-6 bg-blue-900/40 rounded-lg border-2 border-blue-500">
<div class="text-4xl mb-3">🔄</div>
<div class="text-lg font-bold text-blue-300 mb-2">Full Lifecycle</div>
<div class="text-sm text-gray-100">Plan → Code → Review → Automate</div>
</div>
<div class="p-6 bg-indigo-900/40 rounded-lg border-2 border-indigo-500">
<div class="text-4xl mb-3">🤖</div>
<div class="text-lg font-bold text-indigo-300 mb-2">Continuous AI</div>
<div class="text-sm text-gray-100">Repos improve while you sleep</div>
</div>
</div>
</div>
</div>

---
layout: default
---

# 📖 Navigate by Section

<div class="grid grid-cols-3 gap-6 mt-8">
<div @click="$nav.go(6)" class="cursor-pointer p-4 bg-cyan-900/40 rounded-lg border-2 border-cyan-500 hover:bg-cyan-900/60 transition-all">
<div class="text-2xl mb-2">🧠</div>
<div class="text-lg font-bold text-cyan-300">Pre-Coding</div>
<div class="text-sm text-gray-100 mt-1">Plan Mode, @workspace, MCP</div>
<div class="text-xs text-gray-200 mt-2">Understand before you code</div>
</div>

<div @click="$nav.go(7)" class="cursor-pointer p-4 bg-blue-900/40 rounded-lg border-2 border-blue-500 hover:bg-blue-900/60 transition-all">
<div class="text-2xl mb-2">⚡</div>
<div class="text-lg font-bold text-blue-300">Coding</div>
<div class="text-sm text-gray-100 mt-1">CCA, session logs, iteration</div>
<div class="text-xs text-gray-200 mt-2">Agentic implementation</div>
</div>

<div @click="$nav.go(8)" class="cursor-pointer p-4 bg-indigo-900/40 rounded-lg border-2 border-indigo-500 hover:bg-indigo-900/60 transition-all">
<div class="text-2xl mb-2">✅</div>
<div class="text-lg font-bold text-indigo-300">Post-Coding</div>
<div class="text-sm text-gray-100 mt-1">CCR, PR summaries, compliance</div>
<div class="text-xs text-gray-200 mt-2">Automated quality gates</div>
</div>
</div>

<div class="grid grid-cols-2 gap-6 mt-6">
<div @click="$nav.go(9)" class="cursor-pointer p-4 bg-purple-900/40 rounded-lg border-2 border-purple-500 hover:bg-purple-900/60 transition-all">
<div class="text-2xl mb-2">🤖</div>
<div class="text-lg font-bold text-purple-300">Agentic Workflows</div>
<div class="text-sm text-gray-100 mt-1">Continuous AI & Agent Factory</div>
<div class="text-xs text-gray-200 mt-2">Autonomous repo maintenance</div>
</div>

<div @click="$nav.go(10)" class="cursor-pointer p-4 bg-pink-900/40 rounded-lg border-2 border-pink-500 hover:bg-pink-900/60 transition-all">
<div class="text-2xl mb-2">🧬</div>
<div class="text-lg font-bold text-pink-300">Agentic Memory</div>
<div class="text-sm text-gray-100 mt-1">Cross-agent learning</div>
<div class="text-xs text-gray-200 mt-2">Agents that remember</div>
</div>
</div>

<div class="mt-8 p-4 bg-gradient-to-r from-cyan-900/30 to-pink-900/30 rounded-lg text-center">
<span class="text-white font-bold">💡 Click any section to jump directly there</span>
</div>

---

# The Problem

<div class="grid grid-cols-2 gap-8 mt-8">
<div class="p-6 bg-red-900/30 rounded-lg border-2 border-red-500">
<div class="text-4xl mb-4">😰</div>
<div class="space-y-3 text-sm">
<div><strong>Copilot = autocomplete?</strong></div>
<div class="text-gray-100">Most teams stop at inline suggestions — leaving 80% of AI capability untouched</div>
<div><strong>Pre-coding is still manual</strong></div>
<div class="text-gray-100">Hours reading code, writing plans, and researching approaches before a single line</div>
</div>
</div>
<div class="p-6 bg-blue-900/30 rounded-lg border-2 border-blue-500">
<div class="text-4xl mb-4">📋</div>
<div class="space-y-3 text-sm">
<div><strong>Post-coding is fragmented</strong></div>
<div class="text-gray-100">PR reviews, quality enforcement, and docs rely on separate tools and manual checklists</div>
<div><strong>Maintenance doesn't scale</strong></div>
<div class="text-gray-100">Issue triage, test gaps, stale docs accumulate faster than teams can address them</div>
</div>
</div>
</div>

<div class="mt-6 p-4 bg-gradient-to-r from-red-600/30 to-blue-600/30 rounded-lg text-center">
<span class="text-white font-bold">Monday reality: 45 min reading code, 2-day review cycles, CI failures uninvestigated</span>
</div>

---

# The Solution: Copilot-Powered Lifecycle

<div class="grid grid-cols-2 gap-4 mt-4">
<div class="space-y-3">
<div class="p-3 bg-cyan-900/40 rounded-lg border-l-4 border-cyan-500">
<div class="text-sm font-bold text-cyan-300 mb-1">🧠 Phase 1 — Pre-Coding</div>
<div class="text-xs text-gray-100">@workspace analysis, CCA Plan Mode, MCP servers, session logs for persistent context</div>
</div>
<div class="p-3 bg-blue-900/40 rounded-lg border-l-4 border-blue-500">
<div class="text-sm font-bold text-blue-300 mb-1">⚡ Phase 2 — Coding</div>
<div class="text-xs text-gray-100">CCA agentic builder, multi-step execution, session-log iteration, PR/no-PR workflows</div>
</div>
<div class="p-3 bg-indigo-900/40 rounded-lg border-l-4 border-indigo-500">
<div class="text-sm font-bold text-indigo-300 mb-1">✅ Phase 3 — Post-Coding</div>
<div class="text-xs text-gray-100">Copilot Code Review, PR summaries, compliance via repo instructions, CI/CD integration</div>
</div>
</div>
<div class="space-y-3">
<div class="p-3 bg-purple-900/40 rounded-lg border-l-4 border-purple-500">
<div class="text-sm font-bold text-purple-300 mb-1">🤖 Layer 4 — Continuous AI</div>
<div class="text-xs text-gray-100">Agentic Workflows in Actions — triage, docs, tests, security scanning, all autonomous</div>
</div>
<div class="p-3 bg-pink-900/40 rounded-lg border-l-4 border-pink-500">
<div class="text-sm font-bold text-pink-300 mb-1">🧬 Cross-Cutting — Agentic Memory</div>
<div class="text-xs text-gray-100">What coding agent learns helps code review, CLI, and future sessions automatically</div>
</div>
</div>
</div>

<div class="mt-4 p-4 bg-gradient-to-r from-cyan-600/80 to-purple-600/80 rounded-lg text-center">
<span class="text-white font-bold">From "Copilot helps me write code" → "Copilot participates in every phase of delivery"</span>
</div>

---
layout: default
name: pre-coding
---

# Pre-Coding Intelligence

<div class="grid grid-cols-2 gap-6 mt-4">
<div class="space-y-3">
<div class="p-3 bg-cyan-900/40 rounded-lg border-l-4 border-cyan-500">
<div class="text-sm font-bold text-cyan-300 mb-2">🔍 @workspace Analysis</div>
<div class="text-xs font-mono bg-gray-800 p-2 rounded text-gray-100">
@workspace How is auth implemented?<br/>
@workspace What files for a new endpoint?<br/>
@workspace Show data flow to DB layer
</div>
<div class="text-xs text-gray-200 mt-2">Replaces "read code for 2 hours" — saves 30-60 min/feature</div>
</div>
<div class="p-3 bg-blue-900/40 rounded-lg border-l-4 border-blue-500">
<div class="text-sm font-bold text-blue-300 mb-2">📋 CCA Plan Mode</div>
<div class="text-xs font-mono bg-gray-800 p-2 rounded text-gray-100">
@copilot /plan Add rate limiting to API
</div>
<div class="text-xs text-gray-200 mt-2">Structured plans → session logs → persistent context across sessions</div>
</div>
</div>
<div class="space-y-3">
<div class="p-3 bg-indigo-900/40 rounded-lg border-l-4 border-indigo-500">
<div class="text-sm font-bold text-indigo-300 mb-2">🔗 MCP + Domain Context</div>
<div class="text-xs text-gray-100">MCP servers add domain-specific context — databases, APIs, design systems — to planning phase</div>
</div>
<div class="p-3 bg-purple-900/40 rounded-lg border-l-4 border-purple-500">
<div class="text-sm font-bold text-purple-300 mb-2">📝 Session Logs</div>
<div class="text-xs text-gray-100">Persistent artifacts bridging planning and coding. Decisions, context, and todos survive between sessions.</div>
</div>
</div>
</div>

<div class="mt-3 p-3 bg-gradient-to-r from-cyan-600/30 to-indigo-600/30 rounded-lg text-center">
<span class="text-white font-bold text-sm">Pre-coding Copilot reduces ramp-up time by 40-60% on unfamiliar code</span>
</div>

---
layout: default
name: coding
---

# Coding Workflows

<div class="mt-4">
<table class="w-full text-sm">
<thead>
<tr class="bg-gray-800">
<th class="p-3 text-left text-cyan-300">Mode</th>
<th class="p-3 text-left text-cyan-300">Control</th>
<th class="p-3 text-left text-cyan-300">Best For</th>
</tr>
</thead>
<tbody>
<tr class="bg-cyan-900/40">
<td class="p-3 text-gray-100">Inline Completions</td>
<td class="p-3 text-gray-200">Developer-driven</td>
<td class="p-3 text-gray-200">Small edits, boilerplate</td>
</tr>
<tr class="bg-blue-900/40">
<td class="p-3 text-gray-100">Copilot Chat</td>
<td class="p-3 text-gray-200">Conversational</td>
<td class="p-3 text-gray-200">Exploration, debugging</td>
</tr>
<tr class="bg-indigo-900/40">
<td class="p-3 text-gray-100">Copilot Edits</td>
<td class="p-3 text-gray-200">Multi-file</td>
<td class="p-3 text-gray-200">Refactoring, features</td>
</tr>
<tr class="bg-purple-900/40">
<td class="p-3 text-gray-100">CCA (Coding Agent)</td>
<td class="p-3 text-gray-200">Autonomous</td>
<td class="p-3 text-gray-200">Multi-step tasks, full features</td>
</tr>
</tbody>
</table>
</div>

<div class="mt-4 p-3 bg-blue-900/40 rounded-lg border-l-4 border-blue-500">
<div class="text-sm font-bold text-blue-300 mb-2">🔄 Session-Log-Driven Iteration</div>
<div class="text-xs font-mono bg-gray-800 p-2 rounded text-gray-100">
Session 1: Plan Mode → session-log.md (plan + context)<br/>
Session 2: Read log → implement Phase 1 → update log<br/>
Session 3: Read log → implement Phase 2 → update log<br/>
Session 4: Final integration + tests
</div>
<div class="text-xs text-gray-200 mt-2">Iterative loops produce 2-3× better outcomes than one-shot prompts</div>
</div>

---
layout: default
name: post-coding
---

# Post-Coding Automation

<div class="grid grid-cols-2 gap-6 mt-6">
<div class="space-y-3">
<div class="p-3 bg-cyan-900/40 rounded-lg border-l-4 border-cyan-500">
<div class="text-sm font-bold text-cyan-300 mb-2">🔍 Copilot Code Review (CCR)</div>
<div class="text-xs text-gray-100 space-y-1">
<div>• Identifies bugs, security issues, perf concerns</div>
<div>• Inline code suggestions for improvements</div>
<div>• Checks compliance with repo guidelines</div>
<div>• Runs in parallel with human reviewers</div>
</div>
</div>
<div class="p-3 bg-blue-900/40 rounded-lg border-l-4 border-blue-500">
<div class="text-sm font-bold text-blue-300 mb-2">📝 PR Summaries</div>
<div class="text-xs text-gray-100">Auto-generated structured descriptions + file-by-file change walkthroughs. Reduces reviewer ramp-up by 50-70%.</div>
</div>
</div>
<div class="space-y-3">
<div class="p-3 bg-indigo-900/40 rounded-lg border-l-4 border-indigo-500">
<div class="text-sm font-bold text-indigo-300 mb-2">📏 Repo Instructions</div>
<div class="text-xs font-mono bg-gray-800 p-2 rounded text-gray-100">
# copilot-instructions.md<br/>
- Sanitize all user input<br/>
- Use parameterized queries only<br/>
- Test coverage &gt; 80% for new modules
</div>
<div class="text-xs text-gray-200 mt-2">Respected by Chat, CCA, and CCR — consistent quality bar</div>
</div>
<div class="p-3 bg-purple-900/40 rounded-lg border-l-4 border-purple-500">
<div class="text-sm font-bold text-purple-300 mb-2">⚙️ DevOps Integration</div>
<div class="text-xs text-gray-100">CCA understands Actions workflows, explains CI failures, generates new pipelines from natural language</div>
</div>
</div>
</div>

---
layout: default
name: agentic-workflows
---

# Agentic Workflows & Continuous AI

<div class="grid grid-cols-2 gap-6 mt-4">
<div class="space-y-3">
<div class="p-3 bg-purple-900/40 rounded-lg border-l-4 border-purple-500">
<div class="text-sm font-bold text-purple-300 mb-2">📄 Markdown-Defined Automation</div>
<div class="text-xs font-mono bg-gray-800 p-2 rounded text-gray-100">
&#45;&#45;&#45;<br/>
on: { schedule: daily }<br/>
permissions: { contents: read }<br/>
safe-outputs:<br/>
&nbsp;&nbsp;create-issue: { labels: [report] }<br/>
&#45;&#45;&#45;<br/>
# Daily Repo Status Report<br/>
Create a daily status report...
</div>
<div class="text-xs text-gray-200 mt-2">Frontmatter = triggers + security. Body = natural language intent.</div>
</div>
</div>
<div class="space-y-3">
<div class="p-3 bg-pink-900/40 rounded-lg border-l-4 border-pink-500">
<div class="text-sm font-bold text-pink-300 mb-2">🏭 Peli's Agent Factory</div>
<div class="text-xs text-gray-100 space-y-1">
<div>• <strong>Triage</strong> — issue labeling, PR routing</div>
<div>• <strong>Docs</strong> — daily updater, link checker</div>
<div>• <strong>Quality</strong> — code simplifier, duplicate detector</div>
<div>• <strong>Testing</strong> — daily test improver</div>
<div>• <strong>Interactive</strong> — /plan, /fix commands</div>
</div>
<div class="text-xs text-gray-200 mt-2">100+ workflows in production</div>
</div>
<div class="p-3 bg-blue-900/40 rounded-lg border-l-4 border-blue-500">
<div class="text-sm font-bold text-blue-300 mb-2">🔒 Defense-in-Depth</div>
<div class="text-xs text-gray-100">Read-only default → Safe Outputs buffer all writes → humans review before merge</div>
</div>
</div>
</div>

---
layout: default
name: agentic-memory
---

# Agentic Memory: Cross-Agent Learning

<div class="grid grid-cols-2 gap-6 mt-6">
<div class="space-y-3">
<div class="p-3 bg-cyan-900/40 rounded-lg border-l-4 border-cyan-500">
<div class="text-sm font-bold text-cyan-300 mb-2">🧬 How It Works</div>
<div class="text-xs text-gray-100">Agents capture tightly scoped memories with citations to specific code locations. Before using a memory, agents verify citations in real time against the current branch.</div>
</div>
<div class="p-3 bg-blue-900/40 rounded-lg border-l-4 border-blue-500">
<div class="text-sm font-bold text-blue-300 mb-2">🔄 Cross-Agent Sharing</div>
<div class="text-xs text-gray-100">What coding agent learns → helps code review catch inconsistencies → helps CLI navigate logs. Knowledge transfers automatically.</div>
</div>
</div>
<div class="space-y-3">
<div class="p-3 bg-indigo-900/40 rounded-lg border-l-4 border-indigo-500">
<div class="text-sm font-bold text-indigo-300 mb-2">🔧 Self-Healing</div>
<div class="text-xs text-gray-100">Code changes invalidate a memory → agents detect contradiction → store corrected version. Auto-expire after 28 days.</div>
</div>
<div class="p-3 bg-purple-900/40 rounded-lg border-l-4 border-purple-500">
<div class="text-sm font-bold text-purple-300 mb-2">📊 Measured Impact</div>
<div class="text-xs text-gray-100 space-y-1">
<div>• PR merge rate: <strong>90% vs 83%</strong> (+7%)</div>
<div>• Positive review feedback: <strong>77% vs 75%</strong> (+2%)</div>
<div>• Both statistically significant (p &lt; 0.00001)</div>
</div>
</div>
</div>
</div>

<div class="mt-3 p-3 bg-gradient-to-r from-cyan-600/30 to-purple-600/30 rounded-lg text-center">
<span class="text-white font-bold text-sm">Agents learn from each other — knowledge compounds across the entire lifecycle</span>
</div>

---

# Mental Model Shift

<div class="grid grid-cols-3 gap-4 mt-6">
<div class="p-4 bg-green-900/40 rounded-lg border-2 border-green-500">
<div class="text-2xl mb-2">✅</div>
<div class="text-sm font-bold text-green-300 mb-2">Move Toward</div>
<div class="text-xs text-gray-100 space-y-2">
<div>• Lifecycle thinking — use Copilot from issue to post-merge</div>
<div>• Plan before you code — session logs for structured work</div>
<div>• Continuous AI — deploy Agentic Workflows alongside CI/CD</div>
<div>• Markdown-defined automation — anyone can author workflows</div>
</div>
</div>
<div class="p-4 bg-yellow-900/40 rounded-lg border-2 border-yellow-500">
<div class="text-2xl mb-2">⚠️</div>
<div class="text-sm font-bold text-yellow-300 mb-2">Move Away From</div>
<div class="text-xs text-gray-100 space-y-2">
<div>• Code-only Copilot — misses 80% of available AI assistance</div>
<div>• Manual triage and maintenance — doesn't scale, burns out maintainers</div>
<div>• One-shot agent usage — iterative loops produce dramatically better outcomes</div>
</div>
</div>
<div class="p-4 bg-red-900/40 rounded-lg border-2 border-red-500">
<div class="text-2xl mb-2">🛑</div>
<div class="text-sm font-bold text-red-300 mb-2">Move Against</div>
<div class="text-xs text-gray-100 space-y-2">
<div>• Unsandboxed agent execution — Safe Outputs exist for a reason</div>
<div>• Replacing CI/CD with Agentic Workflows — they augment, not replace</div>
</div>
</div>
</div>

<div class="mt-4 p-3 bg-gradient-to-r from-green-600/30 to-blue-600/30 rounded-lg">
<div class="text-xs text-gray-100">
<strong class="text-white">Before:</strong> Monday morning: 2h triaging issues, stale docs, uninvestigated CI failures.
<strong class="text-white">After:</strong> Agentic Workflows triaged overnight, flagged CI fix, updated docs — developer starts coding at 9 AM.
</div>
</div>

---

# What You Can Do Today

<div class="grid grid-cols-3 gap-4 mt-6">
<div class="p-4 bg-cyan-900/40 rounded-lg border-2 border-cyan-500">
<div class="text-lg font-bold text-cyan-300 mb-3">⚡ 15 Minutes</div>
<div class="text-xs text-gray-100 space-y-2">
<div>☐ Try <code>@workspace</code> on unfamiliar code</div>
<div>☐ Use CCA Plan Mode on next feature</div>
<div>☐ Enable Copilot Code Review on PRs</div>
</div>
</div>
<div class="p-4 bg-blue-900/40 rounded-lg border-2 border-blue-500">
<div class="text-lg font-bold text-blue-300 mb-3">⏱️ 1 Hour</div>
<div class="text-xs text-gray-100 space-y-2">
<div>☐ Create <code>copilot-instructions.md</code></div>
<div>☐ Install <code>gh aw</code> + daily status workflow</div>
<div>☐ Try session-log-driven development</div>
</div>
</div>
<div class="p-4 bg-indigo-900/40 rounded-lg border-2 border-indigo-500">
<div class="text-lg font-bold text-indigo-300 mb-3">🚀 2-4 Hours</div>
<div class="text-xs text-gray-100 space-y-2">
<div>☐ Deploy 3-5 Agentic Workflows</div>
<div>☐ Create a custom Agentic Workflow</div>
<div>☐ Build an Agent MD definition</div>
</div>
</div>
</div>

<div class="mt-6 p-4 bg-gradient-to-r from-cyan-600/80 to-indigo-600/80 rounded-lg text-center">
<span class="text-white font-bold">Start today: @workspace → Plan Mode → CCR → Agentic Workflows</span>
</div>

---

# 📖 References

<div class="mt-6 space-y-3">
<div class="p-3 bg-cyan-900/40 rounded-lg border-l-4 border-cyan-500">
<div class="text-sm font-bold text-cyan-300 mb-2">📖 Official Documentation</div>
<div class="text-xs text-gray-100 space-y-1">
<div><strong>GitHub Copilot Docs</strong> — Core concepts and getting started</div>
<div class="font-mono text-blue-400">docs.github.com/en/copilot</div>
<div class="mt-1"><strong>Copilot Coding Agent</strong> — CCA, Plan Mode, session logs, PR workflows</div>
<div class="font-mono text-blue-400">docs.github.com/en/copilot/using-github-copilot/coding-agent</div>
</div>
</div>
<div class="p-3 bg-blue-900/40 rounded-lg border-l-4 border-blue-500">
<div class="text-sm font-bold text-blue-300 mb-2">🤖 Agentic Workflows</div>
<div class="text-xs text-gray-100 space-y-1">
<div><strong>Agentic Workflows Docs</strong> — Full reference for creating and deploying workflows</div>
<div><strong>The Agentics</strong> — 30+ reusable workflow templates</div>
<div><strong>Peli's Agent Factory</strong> — 100+ production workflow gallery</div>
</div>
</div>
<div class="p-3 bg-indigo-900/40 rounded-lg border-l-4 border-indigo-500">
<div class="text-sm font-bold text-indigo-300 mb-2">🧬 Related Talks</div>
<div class="text-xs text-gray-100 space-y-1">
<div><strong>Agentic Journey</strong> — Deep-dive on incremental CCA adoption</div>
<div><strong>Agentic SDLC</strong> — Infrastructure-level scaling for AI agents</div>
<div><strong>Copilot Code Review</strong> — Deep-dive on CCR capabilities</div>
</div>
</div>
</div>

---
layout: end
---

# Copilot Is Everywhere

<div class="flex flex-col items-center justify-center h-full">
<div class="text-6xl mb-8">🚀</div>
<div class="text-2xl font-bold mb-4">The Full Lifecycle Awaits</div>
<div class="text-lg opacity-80 max-w-2xl text-center">
Plan → Code → Review → Automate — Copilot participates at every phase, and Agentic Workflows keep improving repos even when you're not there
</div>
<div class="mt-8 p-4 bg-gradient-to-r from-cyan-600/80 to-purple-600/80 rounded-lg">
<span class="text-white font-bold">From code-completion tool to lifecycle-spanning AI platform</span>
</div>
</div>
