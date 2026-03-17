---
theme: default
class: text-center
highlighter: shiki
lineNumbers: false
info: |
  ## Building Agent Systems: Subagents, Teams, and Autonomous Execution
  CopilotTraining
drawings:
  persist: false
transition: slide-left
title: Building Agent Systems
module: tech-talks/agent-teams
status: active
updated: 2026-03-17
mdc: true
---

<div class="h-full flex flex-col items-center justify-center relative overflow-hidden">
<div class="absolute inset-0 bg-gradient-to-br from-cyan-900/20 via-blue-900/10 to-indigo-900/20"></div>
<div class="absolute top-1/4 left-1/2 -translate-x-1/2 -translate-y-1/2 w-96 h-96 bg-gradient-to-r from-cyan-500/20 via-blue-500/20 to-indigo-500/20 rounded-full blur-3xl"></div>
<div class="relative z-10">
<div class="absolute inset-0 blur-2xl opacity-50"><img src="./sdp-logo.png" class="w-64" alt="" /></div>
<img src="./sdp-logo.png" class="w-64 relative" alt="SDP Logo" />
</div>
<h1 class="!text-5xl !font-bold !mt-8 bg-gradient-to-r from-cyan-400 via-blue-400 to-indigo-400 bg-clip-text text-transparent relative z-10">Building Agent Systems</h1>
<div class="mt-4 relative z-10">
<span class="px-6 py-2 bg-gradient-to-r from-cyan-600/80 to-blue-600/80 rounded-full text-white text-xl font-medium shadow-lg shadow-cyan-500/25">Subagents, Teams, and Autonomous Execution</span>
</div>
<div class="mt-8 text-lg opacity-70 relative z-10">Mechanisms for composing multi-agent AI systems</div>
<div class="mt-6 w-32 h-1 bg-gradient-to-r from-transparent via-cyan-400 to-transparent rounded-full relative z-10"></div>
</div>
<div class="abs-br m-6 flex gap-2"><span class="text-sm opacity-50">Tech Talk · 60 minutes</span></div>

---
layout: center
---

# 🎯 The Core Question

<div class="p-6 bg-gradient-to-br from-cyan-900/30 to-blue-900/30 rounded-xl border-2 border-cyan-500/50 max-w-4xl mx-auto mt-6">
<div class="text-2xl font-semibold text-cyan-300 mb-4">"What are the mechanisms that make multi-agent AI work?"</div>
<div class="text-lg opacity-90">...and how do I compose them into systems that handle complex tasks, run autonomously, and improve over time?</div>
</div>

<div class="mt-8 grid grid-cols-3 gap-4 text-sm">
<div class="p-3 bg-gradient-to-br from-cyan-900/20 to-cyan-800/20 rounded-lg border border-cyan-500/20">
<div class="text-cyan-400 font-semibold mb-1">Context Isolation</div>
<div class="opacity-80">Each agent focuses without pollution</div>
</div>
<div class="p-3 bg-gradient-to-br from-blue-900/20 to-blue-800/20 rounded-lg border border-blue-500/20">
<div class="text-blue-400 font-semibold mb-1">Parallel Execution</div>
<div class="opacity-80">3 agents = 3x throughput</div>
</div>
<div class="p-3 bg-gradient-to-br from-indigo-900/20 to-indigo-800/20 rounded-lg border border-indigo-500/20">
<div class="text-indigo-400 font-semibold mb-1">Autonomous Work</div>
<div class="opacity-80">85 minutes → 27 active</div>
</div>
</div>


---
layout: center
---

# 📖 Table of Contents

<div class="grid grid-cols-3 gap-4 mt-4">
<div @click="$nav.go(5)" class="cursor-pointer group">
<div class="p-4 bg-gradient-to-br from-cyan-900/40 to-blue-900/40 rounded-xl border-2 border-cyan-500/50 hover:border-cyan-400 hover:scale-105 transition-all duration-300">
<div class="text-3xl mb-2">🧱</div>
<div class="text-lg font-bold bg-gradient-to-r from-cyan-300 to-blue-300 bg-clip-text text-transparent">1. Subagents</div>
<div class="text-sm text-gray-300 mt-1">The building block</div>
<div class="text-xs text-cyan-400/70 mt-2">Context isolation + parallel execution</div>
</div>
</div>
<div @click="$nav.go(9)" class="cursor-pointer group">
<div class="p-4 bg-gradient-to-br from-blue-900/40 to-indigo-900/40 rounded-xl border-2 border-blue-500/50 hover:border-blue-400 hover:scale-105 transition-all duration-300">
<div class="text-3xl mb-2">👥</div>
<div class="text-lg font-bold bg-gradient-to-r from-blue-300 to-indigo-300 bg-clip-text text-transparent">2. Agent Teams</div>
<div class="text-sm text-gray-300 mt-1">Organized specialists</div>
<div class="text-xs text-blue-400/70 mt-2">Coordinator + Squad</div>
</div>
</div>
<div @click="$nav.go(13)" class="cursor-pointer group">
<div class="p-4 bg-gradient-to-br from-indigo-900/40 to-purple-900/40 rounded-xl border-2 border-indigo-500/50 hover:border-indigo-400 hover:scale-105 transition-all duration-300">
<div class="text-3xl mb-2">🤖</div>
<div class="text-lg font-bold bg-gradient-to-r from-indigo-300 to-purple-300 bg-clip-text text-transparent">3. Autonomous Execution</div>
<div class="text-sm text-gray-300 mt-1">Background agents + worktrees</div>
<div class="text-xs text-indigo-400/70 mt-2">9.7 hrs/week reclaimed</div>
</div>
</div>
<div @click="$nav.go(16)" class="cursor-pointer group">
<div class="p-4 bg-gradient-to-br from-purple-900/40 to-pink-900/40 rounded-xl border-2 border-purple-500/50 hover:border-purple-400 hover:scale-105 transition-all duration-300">
<div class="text-3xl mb-2">🎭</div>
<div class="text-lg font-bold bg-gradient-to-r from-purple-300 to-pink-300 bg-clip-text text-transparent">4. AgentCouncil</div>
<div class="text-sm text-gray-300 mt-1">Multi-model deliberation</div>
<div class="text-xs text-purple-400/70 mt-2">Claude + GPT + Gemini in parallel</div>
</div>
</div>
<div @click="$nav.go(19)" class="cursor-pointer group">
<div class="p-4 bg-gradient-to-br from-pink-900/40 to-rose-900/40 rounded-xl border-2 border-pink-500/50 hover:border-pink-400 hover:scale-105 transition-all duration-300">
<div class="text-3xl mb-2">🎯</div>
<div class="text-lg font-bold bg-gradient-to-r from-pink-300 to-rose-300 bg-clip-text text-transparent">5. Orchestration Patterns</div>
<div class="text-sm text-gray-300 mt-1">4 proven strategies</div>
<div class="text-xs text-pink-400/70 mt-2">Linear · Iterative · Parallel · Hierarchical</div>
</div>
</div>
<div class="p-4 bg-gradient-to-br from-gray-900/40 to-gray-800/40 rounded-xl border border-gray-600/30 flex flex-col justify-center items-center text-center">
<div class="text-2xl mb-2">📦</div>
<div class="text-sm font-semibold text-gray-300">All compose naturally</div>
<div class="text-xs text-gray-500 mt-1">0 → 5 → 10 min setup</div>
</div>
</div>
<div class="mt-4 text-center text-sm opacity-60">Click any section to jump directly there</div>

---

# 🚧 The Problem with Single Agents

<div class="grid grid-cols-2 gap-4 mt-4">
<div class="p-4 bg-amber-900/20 rounded-lg border-l-4 border-amber-500">
<div class="font-bold text-amber-300 mb-1">Context Ceiling</div>
<div class="text-sm text-gray-300">Single agents hit a hard ceiling around 300-500 LOC. Planning notes pollute implementation, dead-end research stays forever. Quality degrades 30-40% as the window fills.</div>
</div>
<div class="p-4 bg-orange-900/20 rounded-lg border-l-4 border-orange-500">
<div class="font-bold text-orange-300 mb-1">Supervision Bottleneck</div>
<div class="text-sm text-gray-300">Traditional AI workflows demand continuous human guidance. Answering questions, approving approaches, monitoring progress — you cannot parallelize when you cannot look away.</div>
</div>
<div class="p-4 bg-red-900/20 rounded-lg border-l-4 border-red-500">
<div class="font-bold text-red-300 mb-1">Context Pollution</div>
<div class="text-sm text-gray-300">One agent juggling research + planning + implementation accumulates 50-80% irrelevant context before reaching execution. Output quality drops 30-40% measurably.</div>
</div>
<div class="p-4 bg-pink-900/20 rounded-lg border-l-4 border-pink-500">
<div class="font-bold text-pink-300 mb-1">Workspace Conflicts</div>
<div class="text-sm text-gray-300">Multiple agents sharing one workspace create merge conflicts and file collisions. Without isolation, parallelism is dangerous — an architecture problem, not a model problem.</div>
</div>
</div>
<div class="mt-4 p-4 bg-gradient-to-r from-green-500/10 to-emerald-500/10 rounded-xl border border-green-500/30 text-center">
<div class="text-green-300 font-semibold">The solution is not a smarter single agent — it is composing agents like you would compose a team</div>
</div>

---
layout: center
name: subagents
---

<div class="text-center">
<div class="text-6xl mb-4">🧱</div>
<h1 class="!text-4xl bg-gradient-to-r from-cyan-400 to-blue-400 bg-clip-text text-transparent">Section 1: Subagents</h1>
<p class="text-xl opacity-80 mt-2">The Building Block</p>
<div class="mt-6 p-4 bg-cyan-500/10 rounded-xl border border-cyan-500/30 max-w-2xl mx-auto">
<div class="text-lg">The primitive mechanism that makes all multi-agent patterns possible</div>
</div>
<div class="mt-6 grid grid-cols-3 gap-4 max-w-2xl mx-auto text-sm">
<div class="p-3 bg-cyan-900/20 rounded border border-cyan-500/20 text-center">
<div class="text-cyan-400 font-bold">0 setup</div>
<div class="opacity-70">Works today</div>
</div>
<div class="p-3 bg-blue-900/20 rounded border border-blue-500/20 text-center">
<div class="text-blue-400 font-bold">~30x</div>
<div class="opacity-70">Token reduction</div>
</div>
<div class="p-3 bg-indigo-900/20 rounded border border-indigo-500/20 text-center">
<div class="text-indigo-400 font-bold">2.75x</div>
<div class="opacity-70">Parallel speedup</div>
</div>
</div>
</div>

---

# 🧱 Context Isolation: The Core Mechanism

<div class="grid grid-cols-2 gap-4 mt-3 text-xs">
<div>
<div class="font-mono bg-gray-900/70 p-3 rounded-lg text-xs leading-relaxed">
<div class="text-cyan-300 font-bold mb-1">MAIN AGENT (coordinates)</div>
<div class="text-gray-300">│</div>
<div class="text-gray-300">├── SubAgent A: research auth patterns</div>
<div class="text-gray-500 ml-4">reads 30 files, explores 5 approaches</div>
<div class="text-green-400 ml-4">returns: 500-token summary ──→</div>
<div class="text-gray-300">│</div>
<div class="text-gray-300">├── SubAgent B: analyze test coverage</div>
<div class="text-gray-500 ml-4">runs coverage tools, finds gaps</div>
<div class="text-green-400 ml-4">returns: 300-token findings ──→</div>
<div class="text-gray-300">│</div>
<div class="text-gray-300">└── SubAgent C: security audit (parallel)</div>
<div class="text-gray-500 ml-4">checks OWASP patterns</div>
<div class="text-green-400 ml-4">returns: 400-token risk report ──→</div>
</div>
</div>
<div class="space-y-2">
<div class="p-3 bg-cyan-900/20 rounded border border-cyan-500/20">
<div class="font-bold text-cyan-300 text-xs mb-1">Isolated Context Windows</div>
<div class="text-gray-300">Each subagent runs in its own window — research, dead-ends, exploration never pollute the main session</div>
</div>
<div class="p-3 bg-blue-900/20 rounded border border-blue-500/20">
<div class="font-bold text-blue-300 text-xs mb-1">Summary-Only Returns</div>
<div class="text-gray-300">Only the final result passes back — 100-500 tokens vs. 5K-20K in main context (~30x reduction)</div>
</div>
<div class="p-3 bg-indigo-900/20 rounded border border-indigo-500/20">
<div class="font-bold text-indigo-300 text-xs mb-1">Simultaneous Execution</div>
<div class="text-gray-300">Multiple subagents run in parallel when tasks are independent — no shared state, no conflicts</div>
</div>
<div class="p-3 bg-purple-900/20 rounded border border-purple-500/20">
<div class="font-bold text-purple-300 text-xs mb-1">Inherited or Custom Agent</div>
<div class="text-gray-300">Inherits main session by default — override with custom agents for specialized behavior</div>
</div>
</div>
</div>

---

# 🧱 Invocation Patterns + Anti-Patterns

<div class="grid grid-cols-2 gap-4 mt-3 text-xs">
<div>
<div class="p-3 bg-gradient-to-br from-cyan-900/30 to-blue-900/30 rounded-lg border border-cyan-500/30 mb-3">
<div class="font-bold text-cyan-300 mb-2">Implicit (Chat Hints)</div>
<div class="font-mono bg-gray-900/60 p-2 rounded text-xs mb-2">Run a subagent to research OAuth2 patterns
in Node.js, focusing on token storage +
refresh rotation. Return: libraries, tradeoffs.</div>
<div class="text-gray-300 text-xs">Natural language delegation. Only the summary returns. Best for: exploratory research, ad-hoc tasks.</div>
</div>
<div class="p-3 bg-gradient-to-br from-blue-900/30 to-indigo-900/30 rounded-lg border border-blue-500/30">
<div class="font-bold text-blue-300 mb-2">Explicit (Prompt Files)</div>
<pre class="font-mono bg-gray-900/60 p-2 rounded text-xs mb-2 whitespace-pre-wrap">&#45;&#45;&#45;
tools: ['agent', 'read', 'search', 'edit']
&#45;&#45;&#45;
&#35;&#35; Phase 1: Research (Subagent)
Return: Patterns, Components, Constraints.
&#35;&#35; Phase 2: Implement
Use Phase 1 findings to implement.</pre>
<div class="text-gray-300 text-xs">Version-controlled. Best for: reproducible team workflows.</div>
</div>
</div>
<div>
<div class="font-bold text-red-400 mb-2">❌ Anti-Patterns</div>
<div class="space-y-1 mb-3">
<div class="p-2 bg-red-900/20 rounded border-l-2 border-red-500">
<div class="font-bold text-red-300">Over-delegation</div>
<div class="text-gray-300">Subagent to read one file. 2-3s overhead > 1s task. Delegate 5+ files or complex analysis.</div>
</div>
<div class="p-2 bg-red-900/20 rounded border-l-2 border-red-500">
<div class="font-bold text-red-300">Vague tasks</div>
<div class="text-gray-300">"Research authentication" — returns generic prose. Specify scope, output format, success criteria.</div>
</div>
<div class="p-2 bg-red-900/20 rounded border-l-2 border-red-500">
<div class="font-bold text-red-300">Raw returns</div>
<div class="text-gray-300">Post subagent summaries directly — user must synthesize. Let main agent synthesize into actions.</div>
</div>
</div>
<div class="p-2 bg-green-900/20 rounded border border-green-500/20">
<div class="font-bold text-green-300">⚡ Parallel speedup</div>
<div class="text-gray-300">Serial: 22 min for 3 tasks → Parallel: 8 min same tasks. <b class="text-green-400">2.75x faster</b>, with independent analysis.</div>
</div>
</div>
</div>

---
layout: center
name: agent-teams
---

<div class="text-center">
<div class="text-6xl mb-4">👥</div>
<h1 class="!text-4xl bg-gradient-to-r from-blue-400 to-indigo-400 bg-clip-text text-transparent">Section 2: Agent Teams</h1>
<p class="text-xl opacity-80 mt-2">Organized Specialists</p>
<div class="mt-6 p-4 bg-blue-500/10 rounded-xl border border-blue-500/30 max-w-2xl mx-auto">
<div class="text-lg">Role-based coordination via the coordinator-delegate pattern, with Squad as the production implementation</div>
</div>
<div class="mt-6 grid grid-cols-3 gap-4 max-w-2xl mx-auto text-sm">
<div class="p-3 bg-blue-900/20 rounded border border-blue-500/20 text-center">
<div class="text-blue-400 font-bold">10 min</div>
<div class="opacity-70">Squad setup</div>
</div>
<div class="p-3 bg-indigo-900/20 rounded border border-indigo-500/20 text-center">
<div class="text-indigo-400 font-bold">20-30%</div>
<div class="opacity-70">Specialist advantage</div>
</div>
<div class="p-3 bg-purple-900/20 rounded border border-purple-500/20 text-center">
<div class="text-purple-400 font-bold">6.6%</div>
<div class="opacity-70">Coordinator overhead</div>
</div>
</div>
</div>

---

# 👥 The Coordinator Pattern

<div class="grid grid-cols-2 gap-4 mt-3 text-xs">
<div>
<div class="font-mono bg-gray-900/70 p-3 rounded-lg text-xs leading-snug mb-3">
<div class="text-cyan-300 font-bold text-center">┌───── COORDINATOR ──────┐</div>
<div class="text-gray-400 text-center">Routes · Spawns specialists</div>
<div class="text-yellow-400 text-center font-bold">NEVER implements directly</div>
<div class="text-cyan-300 text-center">└────────────────────────┘</div>
<div class="text-gray-500 text-center mt-1">↓ delegates to isolated subagents ↓</div>
<div class="grid grid-cols-3 gap-1 mt-2 text-center text-xs">
<div class="bg-green-900/40 rounded p-1">🏗️ Lead<br/><span class="text-gray-400">Scope/Review</span></div>
<div class="bg-blue-900/40 rounded p-1">🔧 Dev(s)<br/><span class="text-gray-400">Build/Code</span></div>
<div class="bg-purple-900/40 rounded p-1">🧪 Tester<br/><span class="text-gray-400">Test/QA</span></div>
</div>
<div class="text-gray-500 text-center mt-1 text-xs">Each in own context window</div>
<div class="text-cyan-300 text-center mt-1">↓ → 🧠 Shared Memory (decisions.md)</div>
</div>
<div class="p-2 bg-yellow-900/20 rounded border border-yellow-500/20 text-xs">
<b class="text-yellow-400">Why tool restrictions?</b> Without them, planners "helpfully" fix typos (now implementing). Reviewers "just fix this one thing" (now biased). With restrictions: VS Code enforces at invocation — impossible, not just discouraged.
</div>
</div>
<div>
<div class="font-bold text-cyan-300 mb-2">Tool Assignment Enforces Role Boundaries</div>
<div class="text-xs">

| Role | Tools | Why Restricted |
|------|-------|----------------|
| Research | `search`, `fetch` | Read-only, no modify risk |
| Planning | `search`, `create` (docs) | Plan docs, cannot implement |
| Implementation | `edit`, `create`, `delete` | Full power, focused |
| Review | `search`, `analysis`, `linter` | Read + analyze, no changes |
| Testing | `search`, `create`, `runTests` | Create tests + verify |

</div>
<div class="mt-3 p-2 bg-cyan-900/20 rounded border border-cyan-500/20">
<b class="text-cyan-300">Result:</b> <span class="text-gray-300">40-60% reduction in context mixing. Planner CAN'T edit even if it wants to — request fails immediately at VS Code level.</span>
</div>
</div>
</div>

---

# 👥 Squad: Production Implementation

<div class="grid grid-cols-2 gap-4 mt-3 text-xs">
<div>
<div class="p-3 bg-gradient-to-r from-blue-900/40 to-indigo-900/40 rounded-lg border border-blue-500/30 mb-3">
<div class="font-bold text-blue-300 mb-1">github.com/bradygaster/squad</div>
<div class="text-gray-300">Persistent AI development team living in your repo. Specialists know your codebase, share decisions, compound knowledge.</div>
<div class="font-mono text-green-400 mt-2">npx github:bradygaster/squad</div>
</div>
<div class="font-mono bg-gray-900/60 p-3 rounded text-xs leading-snug mb-2">
"Set up. I'm building React + Node recipe app."

Squad: 🏗️ Ripley — Lead (scope, decisions)
       ⚛️ Dallas — Frontend (React, UI)
       🔧 Kane   — Backend (APIs, DB)
       🧪 Lambert — Tester (QA, edge cases)
       📋 Scribe  — (silent) memory

> Team, build the login page  ← fans out ALL in parallel
> Ripley, fix API error handling  ← direct routing
</div>
</div>
<div>
<div class="font-bold text-blue-300 mb-2">Key Mechanisms</div>
<div class="space-y-2">
<div class="p-2 bg-blue-900/20 rounded border border-blue-500/20">
<div class="font-bold text-blue-300">✅ Reviewer Protocol</div>
<div>Agent A rejected → <b>locked out</b> → Agent B must revise. No self-review loops.</div>
</div>
<div class="p-2 bg-indigo-900/20 rounded border border-indigo-500/20">
<div class="font-bold text-indigo-300">🤖 Ralph (Work Monitor)</div>
<div>Polls open issues, draft PRs, CI failures → triage → assign → spawn. Team never idles.</div>
</div>
<div class="p-2 bg-purple-900/20 rounded border border-purple-500/20">
<div class="font-bold text-purple-300">💰 Cost-First Routing</div>
<div>docs/planning → Haiku; code → Sonnet; visual → Opus. Automatic.</div>
</div>
</div>
</div>
</div>

---

# 👥 Squad: Knowledge That Compounds

<div class="mt-4 text-xs">
<div class="grid grid-cols-2 gap-3 mb-4">
<div>
<div class="font-bold text-blue-300 mb-2">Memory Layers</div>

| Layer | What | Who Reads |
|-------|------|-----------|
| `charter.md` | Identity, expertise, boundaries, voice | The agent itself |
| `history.md` | Project-specific learnings per session | That agent only |
| `decisions.md` | Team-wide architectural decisions | All agents |
| `skills/` | Reusable patterns from real work | All agents |

</div>
<div>
<div class="font-bold text-blue-300 mb-2">Growth Over Time</div>
<div class="grid grid-cols-3 gap-2">
<div class="p-3 bg-green-900/20 rounded border border-green-500/20 text-center">
<div class="text-2xl">🌱</div>
<div class="font-bold text-green-400">First Session</div>
<div class="text-gray-300">Project description, tech stack</div>
<div class="text-xs text-gray-500 mt-1">~1,250 tokens/agent</div>
</div>
<div class="p-3 bg-blue-900/20 rounded border border-blue-500/20 text-center">
<div class="text-2xl">🌿</div>
<div class="font-bold text-blue-400">Week 4</div>
<div class="text-gray-300">Conventions, patterns, API design, test strategies</div>
<div class="text-xs text-gray-500 mt-1">~3,300 tokens/agent</div>
</div>
<div class="p-3 bg-purple-900/20 rounded border border-purple-500/20 text-center">
<div class="text-2xl">🌳</div>
<div class="font-bold text-purple-400">Week 12</div>
<div class="text-gray-300">Full architecture, tech debt map, perf patterns</div>
<div class="text-xs text-gray-500 mt-1">~9,000 tokens/agent</div>
</div>
</div>
</div>
</div>
<div class="p-3 bg-gradient-to-r from-cyan-900/20 to-blue-900/20 rounded-lg border border-cyan-500/20 text-center">
<b class="text-cyan-300">Commit `.ai-team/` to git</b> — anyone who clones your repo gets the team, with all accumulated knowledge
</div>
</div>

---
layout: center
name: autonomous-execution
---

<div class="text-center">
<div class="text-6xl mb-4">🤖</div>
<h1 class="!text-4xl bg-gradient-to-r from-indigo-400 to-purple-400 bg-clip-text text-transparent">Section 3: Autonomous Execution</h1>
<p class="text-xl opacity-80 mt-2">Background Agents + Git Worktrees</p>
<div class="mt-6 p-4 bg-indigo-500/10 rounded-xl border border-indigo-500/30 max-w-2xl mx-auto">
<div class="text-lg">Shift supervision from continuous to review-only — run multiple agents safely in parallel</div>
</div>
<div class="mt-6 grid grid-cols-3 gap-4 max-w-2xl mx-auto text-sm">
<div class="p-3 bg-indigo-900/20 rounded border border-indigo-500/20 text-center">
<div class="text-indigo-400 font-bold">85 → 27 min</div>
<div class="opacity-70">Active time per task</div>
</div>
<div class="p-3 bg-purple-900/20 rounded border border-purple-500/20 text-center">
<div class="text-purple-400 font-bold">9.7 hrs/wk</div>
<div class="opacity-70">Reclaimed</div>
</div>
<div class="p-3 bg-pink-900/20 rounded border border-pink-500/20 text-center">
<div class="text-pink-400 font-bold">0 setup</div>
<div class="opacity-70">Built into VS Code 1.109</div>
</div>
</div>
</div>

---

# 🤖 Worktree Isolation + The Hand-Off Workflow

<div class="grid grid-cols-2 gap-4 mt-3 text-xs">
<div>
<div class="font-bold text-indigo-300 mb-2">Git Worktrees: Isolated Parallel Workspaces</div>
<div class="font-mono bg-gray-900/70 p-3 rounded-lg text-xs leading-snug mb-3">repo/                    single .git/ shared
├── main/src/main.js     ← your active work (untouched)
├── worktree-agent-1/    ← Agent A workspace (own branch)
└── worktree-agent-2/    ← Agent B workspace (own branch)</div>
<div class="p-2 bg-indigo-900/20 rounded border border-indigo-500/20 mb-2 text-xs">
VS Code 1.109+: auto-creates worktrees. Agent A and B can both edit main.js — different worktrees, zero conflicts.</div>
<div class="grid grid-cols-2 gap-2 text-xs">
<div class="p-2 bg-red-900/20 rounded border border-red-500/20">
<div class="font-bold text-red-400">Supervised: failed experiment</div>
<div>90 min reverting commits</div>
</div>
<div class="p-2 bg-green-900/20 rounded border border-green-500/20">
<div class="font-bold text-green-400">Worktree: failed experiment</div>
<div>5 min removing worktree</div>
</div>
</div>
</div>
<div>
<div class="font-bold text-indigo-300 mb-2">The Hand-Off Workflow</div>
<pre class="font-mono bg-gray-900/60 p-3 rounded text-xs leading-relaxed mb-3 whitespace-pre-wrap">BEFORE (supervised, 1 task):
  Plan(15) → Implement(60 supervised) → Review(10)
  Active: 85 minutes
──────────────────────────────────────────────
AFTER (background, 1 task):
  Plan(15) → Hand-off(2) → [background runs] → Review(10)
  Active: 27 minutes
──────────────────────────────────────────────
AFTER (3 parallel tasks):
  Plan all 3(15) → Hand-off×3(6) → [3 agents] → Review all(30)
  Active: 51 min  vs.  255 min serial supervised</pre>
<div class="p-3 bg-gradient-to-r from-green-900/20 to-emerald-900/20 rounded-lg border border-green-500/30 text-center">
<div class="font-bold text-green-300">10 tasks/week</div>
<div class="text-gray-300">850 min supervised → 270 min with background agents</div>
<div class="text-green-400 font-bold mt-1">9.7 hours reclaimed per week</div>
</div>
</div>
</div>

---

# 🤖 Three Autonomous Execution Patterns

<div class="mt-4 grid grid-cols-3 gap-4 text-xs">
<div class="p-4 bg-indigo-900/20 rounded-lg border border-indigo-500/20">
<div class="font-bold text-indigo-300 mb-2">1️⃣ Independent Features</div>
<div class="font-mono bg-gray-900/60 p-2 rounded text-xs mb-2 leading-snug">Plan A, B, C separately →
Agent 1: Feature A (worktree-a)
Agent 2: Feature B (worktree-b) ← parallel
Agent 3: Feature C (worktree-c)
→ Review 3 finished PRs</div>
<div class="text-gray-300">Parallelize independent roadmap tasks. Review when all are done.</div>
</div>
<div class="p-4 bg-purple-900/20 rounded-lg border border-purple-500/20">
<div class="font-bold text-purple-300 mb-2">2️⃣ Experimental Variants</div>
<div class="font-mono bg-gray-900/60 p-2 rounded text-xs mb-2 leading-snug">"Implement caching with:
 (1) Redis
 (2) In-memory LRU
 (3) Hybrid disk/memory"
→ 3 agents, parallel worktrees
→ Benchmark all 3, pick winner
→ Remove losers: 5 min</div>
<div class="text-gray-300">Empirical evaluation. Discard losing worktrees instantly.</div>
</div>
<div class="p-4 bg-pink-900/20 rounded-lg border border-pink-500/20">
<div class="font-bold text-pink-300 mb-2">3️⃣ Specialized Parallel Roles</div>
<div class="font-mono bg-gray-900/60 p-2 rounded text-xs mb-2 leading-snug">"Refactor the auth module" →
Agent A: Implements refactoring
Agent B: Writes migration tests ← parallel
Agent C: Updates API docs
→ Merge in dependency order</div>
<div class="text-gray-300">Parallel cross-concerns. Merge after review.</div>
</div>
</div>
<div class="mt-4 p-3 bg-gradient-to-r from-indigo-900/20 to-purple-900/20 rounded-lg border border-indigo-500/20 text-xs">
<b class="text-indigo-300">Clear Hand-Offs Required:</b> <span class="text-gray-300">Agents succeed autonomously when you provide explicit acceptance criteria, constraints ("do not modify API contracts"), and links to related context. Vague hand-offs produce mid-task questions — defeating the purpose.</span>
</div>
<div class="mt-3 p-3 bg-gradient-to-r from-cyan-900/20 to-indigo-900/20 rounded-lg border border-cyan-500/20 text-xs flex gap-4 items-start">
<div class="text-2xl">⚡</div>
<div>
<b class="text-cyan-300">Terminal fan-out: <code>/fleet</code> in Copilot CLI</b>
<div class="text-gray-300 mt-1">All three patterns above can be driven from the CLI. <code>/fleet</code> is the explicit fan-out command: the main agent orchestrates subtasks in parallel, each with its own context window. Works with plan mode: <span class="text-cyan-400">Shift+Tab → plan → "Accept plan and build on autopilot + /fleet"</span>. Custom agents (<code>@test-writer</code>, <code>@security-reviewer</code>) are matched to subtasks automatically.</div>
</div>
</div>

---
layout: center
name: agent-council
---

<div class="text-center">
<div class="text-6xl mb-4">🎭</div>
<h1 class="!text-4xl bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">Section 4: Agent Council</h1>
<p class="text-xl opacity-80 mt-2">When Different Models Think Differently</p>
<div class="mt-6 p-4 bg-purple-500/10 rounded-xl border border-purple-500/30 max-w-2xl mx-auto">
<div class="text-lg">Claude + GPT + Gemini in parallel — collaborative or adversarial</div>
</div>
<div class="mt-6 grid grid-cols-3 gap-4 max-w-2xl mx-auto text-sm">
<div class="p-3 bg-purple-900/20 rounded border border-purple-500/20 text-center">
<div class="text-purple-400 font-bold">No dependencies</div>
<div class="opacity-70">Just markdown files</div>
</div>
<div class="p-3 bg-pink-900/20 rounded border border-pink-500/20 text-center">
<div class="text-pink-400 font-bold">7 or 6 calls</div>
<div class="opacity-70">≈ 2 sequential subagents</div>
</div>
<div class="p-3 bg-rose-900/20 rounded border border-rose-500/20 text-center">
<div class="text-rose-400 font-bold">Auto-detected</div>
<div class="opacity-70">council: vs debate:</div>
</div>
</div>
</div>

---

# 🎭 AgentCouncil: Two Modes

<div class="mt-3 text-xs">
<div class="grid grid-cols-4 gap-2 mb-3">
<div class="p-2 bg-gray-900/50 rounded border border-gray-600/30 text-center">
<div class="font-bold text-orange-300">Alpha</div>
<div class="text-gray-400 text-xs">Deep Explorer / Drafter</div>
<div class="text-xs text-gray-500">claude-opus-4.6</div>
</div>
<div class="p-2 bg-gray-900/50 rounded border border-gray-600/30 text-center">
<div class="font-bold text-blue-300">Beta</div>
<div class="text-gray-400 text-xs">Practical Builder / Fact-Checker</div>
<div class="text-xs text-gray-500">gpt-5.4</div>
</div>
<div class="p-2 bg-gray-900/50 rounded border border-gray-600/30 text-center">
<div class="font-bold text-green-300">Gamma</div>
<div class="text-gray-400 text-xs">Elegant Minimalist / Devil's Advocate</div>
<div class="text-xs text-gray-500">gemini-3.1-pro</div>
</div>
<div class="p-2 bg-gray-900/50 rounded border border-gray-600/30 text-center">
<div class="font-bold text-violet-300">Orchestrator</div>
<div class="text-gray-400 text-xs">Author / Judge</div>
<div class="text-xs text-gray-500">claude-opus-4.6</div>
</div>
</div>
<div class="grid grid-cols-2 gap-4">
<div class="p-3 bg-violet-900/20 rounded-lg border border-violet-500/20">
<div class="font-bold text-violet-300 mb-2">🤝 Collaborative (Default) — 7 calls</div>
<div class="font-mono bg-gray-900/60 p-2 rounded text-xs mb-2">Phase 1 (parallel): Alpha, Beta, Gamma draft
Phase 2 (parallel): Each reads others → improves
Phase 3:            Orchestrator synthesizes all three</div>
<div class="text-gray-300">Best for: brainstorming, design exploration, research synthesis</div>
<div class="font-mono text-green-400 mt-2">council: How should we structure the API?</div>
</div>
<div class="p-3 bg-fuchsia-900/20 rounded-lg border border-fuchsia-500/20">
<div class="font-bold text-fuchsia-300 mb-2">🗡️ Adversarial — 6 calls</div>
<div class="font-mono bg-gray-900/60 p-2 rounded text-xs mb-2">Phase 1 (parallel): Alpha, Beta, Gamma draft
Phase 2:            Orchestrator picks dominant position
Phase 3 (parallel): Others attempt to tear it apart
Phase 4:            Verdict: SURVIVED / MODIFIED / OVERTURNED</div>
<div class="text-gray-300">Best for: architecture decisions, security reviews, A vs B comparisons</div>
<div class="font-mono text-green-400 mt-2">debate: WebSockets vs SSE at 10K users</div>
</div>
</div>
</div>

---

# 🎭 AgentCouncil: Usage + Combining with Squad

<div class="grid grid-cols-2 gap-4 mt-3 text-xs">
<div>
<div class="font-bold text-violet-300 mb-2">Auto Mode Detection</div>
<div class="space-y-1 mb-3">
<div class="p-2 bg-violet-900/20 rounded"><code class="text-green-400">council:</code> or <code class="text-green-400">brainstorm:</code> → 🤝 Collaborative</div>
<div class="p-2 bg-fuchsia-900/20 rounded"><code class="text-green-400">debate:</code> or <code class="text-green-400">stress-test:</code> → 🗡️ Adversarial</div>
<div class="p-2 bg-violet-900/10 rounded"><code class="text-green-400">verbose council:</code> → shows each agent's draft</div>
</div>
<div class="font-bold text-violet-300 mb-2">Install (No Build Required)</div>
```bash
git clone github.com/Sentry01/AgentCouncil

cp skills/agent-council/skill.md \
   ~/.copilot/skills/agent-council/skill.md

# or as standalone agent:
cp agents/AgentCouncil.agent.md \
   ~/.copilot/agents/
```
</div>
<div>
<div class="font-bold text-violet-300 mb-2">AgentCouncil vs. Squad</div>

| Situation | Use |
|-----------|-----|
| "What's the right architecture?" | 🗡️ Council |
| "Brainstorm caching strategies" | 🤝 Council |
| "Build the auth system" | Squad |
| "Review this PR for security" | 🗡️ Council |
| "We agreed — now implement it" | Squad |

<div class="mt-3 p-3 bg-gradient-to-r from-violet-900/30 to-blue-900/30 rounded-lg border border-violet-500/20">
<div class="font-bold text-violet-300 mb-1">🎯 Deliberation → Execution Pipeline</div>
<div class="text-gray-300">Use AgentCouncil to stress-test the decision → hand validated decision to Squad for implementation. Decision flows to decisions.md — future agents cannot accidentally reverse it.</div>
</div>
</div>
</div>

---
layout: center
name: orchestration-patterns
---

<div class="text-center">
<div class="text-6xl mb-4">🎯</div>
<h1 class="!text-4xl bg-gradient-to-r from-pink-400 to-rose-400 bg-clip-text text-transparent">Section 5: Orchestration Patterns</h1>
<p class="text-xl opacity-80 mt-2">4 Proven Coordination Strategies</p>
<div class="mt-6 p-4 bg-pink-500/10 rounded-xl border border-pink-500/30 max-w-2xl mx-auto">
<div class="text-lg">Common coordination strategies across all agent system types</div>
</div>
<div class="mt-6 grid grid-cols-4 gap-3 max-w-2xl mx-auto text-sm">
<div class="p-2 bg-pink-900/20 rounded border border-pink-500/20 text-center text-xs">Linear</div>
<div class="p-2 bg-rose-900/20 rounded border border-rose-500/20 text-center text-xs">Iterative</div>
<div class="p-2 bg-red-900/20 rounded border border-red-500/20 text-center text-xs">Parallel</div>
<div class="p-2 bg-orange-900/20 rounded border border-orange-500/20 text-center text-xs">Hierarchical</div>
</div>
</div>

---

# 🎯 Four Proven Orchestration Patterns

<div class="mt-3 grid grid-cols-2 gap-3 text-xs">
<div class="p-4 bg-cyan-900/20 rounded-lg border border-cyan-500/20">
<div class="font-bold text-cyan-300 mb-2">1️⃣ Linear Pipeline</div>
<div class="font-mono text-gray-400 text-xs mb-2">Research → Planning → Implement → Review → Test</div>
<div class="text-gray-300 mb-2">Sequential, predictable. Each phase depends strictly on the previous.</div>
<div class="text-cyan-400">✅ Simple features, clear requirements</div>
<div class="text-gray-400">Example: Adding a single REST endpoint</div>
<div class="text-red-400 text-xs mt-1">Trade-off: No parallelization</div>
</div>
<div class="p-4 bg-blue-900/20 rounded-lg border border-blue-500/20">
<div class="font-bold text-blue-300 mb-2">2️⃣ Iterative Refinement</div>
<div class="font-mono text-gray-400 text-xs mb-2">Implement → Review → [Pass?] → Loop or Continue</div>
<div class="text-gray-300 mb-2">Quality-critical code. Reviewer returns NEEDS_REVISION → loop until APPROVED (max 3).</div>
<div class="text-blue-400">✅ Security-critical, high failure risk</div>
<div class="text-gray-400">Example: OAuth with token refresh edge cases</div>
<div class="text-red-400 text-xs mt-1">Trade-off: Unpredictable duration</div>
</div>
<div class="p-4 bg-indigo-900/20 rounded-lg border border-indigo-500/20">
<div class="font-bold text-indigo-300 mb-2">3️⃣ Parallel Specialists</div>
<div class="font-mono text-gray-400 text-xs mb-2">Plan → [Security + Perf + Docs parallel] → Integrate</div>
<div class="text-gray-300 mb-2">Independent cross-cutting concerns. 3-5x faster validation.</div>
<div class="text-indigo-400">✅ Full-stack features, multiple concerns</div>
<div class="text-gray-400">Example: Auth feature touching DB, API, UI</div>
<div class="text-red-400 text-xs mt-1">Trade-off: Complexity if results conflict</div>
</div>
<div class="p-4 bg-purple-900/20 rounded-lg border border-purple-500/20">
<div class="font-bold text-purple-300 mb-2">4️⃣ Hierarchical</div>
<div class="font-mono text-gray-400 text-xs mb-2">Master → [FE Conductor + BE Conductor] → Specialists</div>
<div class="text-gray-300 mb-2">Full-stack spanning 5+ subsystems. Sub-conductors manage domain specialists.</div>
<div class="text-purple-400">✅ Large features, clear domain boundaries</div>
<div class="text-gray-400">Example: Complete e-commerce checkout flow</div>
<div class="text-red-400 text-xs mt-1">Trade-off: Complex to debug</div>
</div>
</div>

---

# 📊 Three Real-World Use Cases

<div class="grid grid-cols-3 gap-3 mt-3 text-xs">
<div class="p-3 bg-cyan-900/20 rounded-lg border border-cyan-500/20">
<div class="font-bold text-cyan-300 mb-1">1️⃣ Parallel PR Review</div>
<div class="text-gray-500 mb-2">Zero setup — just chat prompts</div>
<div class="font-mono bg-gray-900/60 p-2 rounded text-xs mb-2">"Review this auth PR with 3
parallel subagents:
1. Security: vulnerabilities
2. Performance: N+1 queries
3. Testing: coverage gaps
→ Blockers / Recommended"</div>
<div class="text-gray-300"><b class="text-cyan-400">12 min parallel</b> vs. <b class="text-red-400">45 min sequential</b>. Each subagent forms conclusions independently.</div>
</div>
<div class="p-3 bg-blue-900/20 rounded-lg border border-blue-500/20">
<div class="font-bold text-blue-300 mb-1">2️⃣ Full-Stack Auth with Squad</div>
<div class="text-gray-500 mb-2">10 min setup (npx squad)</div>
<div class="font-mono bg-gray-900/60 p-2 rounded text-xs mb-2">"Team, build the auth system"
→ Lead: scopes, defines contracts
→ Frontend: login form, session
→ Backend: endpoints, JWT
→ Tester: tests from spec (parallel)
→ Tester finds token refresh gap
→ Backend picks it up: no asking</div>
<div class="text-gray-300">4 specialists simultaneously. <b class="text-blue-400">decisions.md</b> captures JWT format for future agents.</div>
</div>
<div class="p-3 bg-purple-900/20 rounded-lg border border-purple-500/20">
<div class="font-bold text-purple-300 mb-1">3️⃣ Deliberate → Execute</div>
<div class="text-gray-500 mb-2">AgentCouncil + Squad</div>
<div class="font-mono bg-gray-900/60 p-2 rounded text-xs mb-2">"debate: WebSockets+Redis vs
 SSE+MQ for 10K users"
→ Gamma: "wrong constraint"
→ Alpha+Beta attack Gamma
→ Gamma SURVIVES (MODIFIED)
→ SSE now, Redis path at 100K
"Team, implement SSE + MQ"
→ Backend + Tester in parallel</div>
<div class="text-gray-300"><b class="text-purple-400">12-min council</b> replaces 2-hour meeting. Decision flows to Squad decisions.md.</div>
</div>
</div>

---

# ✅ What You Can Do Today

<div class="mt-4 grid grid-cols-3 gap-4 text-xs">
<div class="p-4 bg-green-900/20 rounded-lg border border-green-500/20">
<div class="font-bold text-green-300 mb-3">⏱️ Right Now (0 setup)</div>
<div class="space-y-2">
<div class="p-2 bg-green-900/30 rounded">
<div class="font-bold text-green-400">Implicit subagent</div>
<div class="text-gray-300">"Run a subagent to research how auth works in this codebase and return a structured summary"</div>
</div>
<div class="p-2 bg-green-900/30 rounded">
<div class="font-bold text-green-400">Parallel review</div>
<div class="text-gray-300">"Analyze this PR using 3 parallel subagents: Security, Performance, Testing"</div>
</div>
<div class="p-2 bg-green-900/30 rounded">
<div class="font-bold text-green-400">Background hand-off</div>
<div class="text-gray-300">VS Code 1.109 session picker — start a background session for any well-defined task</div>
</div>
</div>
</div>
<div class="p-4 bg-blue-900/20 rounded-lg border border-blue-500/20">
<div class="font-bold text-blue-300 mb-3">🔧 Today (1-2 hours)</div>
<div class="space-y-2">
<div class="p-2 bg-blue-900/30 rounded">
<div class="font-bold text-blue-400">Install Squad</div>
<div class="font-mono text-green-400">npx github:bradygaster/squad</div>
<div class="text-gray-300">Form your team, run 3-5 "Team, ..." tasks. Check decisions.md after.</div>
</div>
<div class="p-2 bg-blue-900/30 rounded">
<div class="font-bold text-blue-400">Install AgentCouncil</div>
<div class="text-gray-300">Try adversarial mode on a real pending decision: <code class="text-green-400">debate: [A] vs [B]</code></div>
</div>
</div>
</div>
<div class="p-4 bg-purple-900/20 rounded-lg border border-purple-500/20">
<div class="font-bold text-purple-300 mb-3">🚀 This Week</div>
<div class="space-y-2">
<div class="p-2 bg-purple-900/30 rounded">Enable GitHub Issues integration (label-based triage)</div>
<div class="p-2 bg-purple-900/30 rounded">Activate Ralph for autonomous backlog processing</div>
<div class="p-2 bg-purple-900/30 rounded">Combine: AgentCouncil decisions → Squad execution pipeline</div>
<div class="p-2 bg-purple-900/30 rounded">Measure: implementation time, rework iterations, context switching overhead</div>
</div>
</div>
</div>

---

# 🔗 References

<div class="grid grid-cols-2 gap-5 mt-4 text-xs">
<div>
<div class="font-bold text-cyan-300 mb-2 text-sm">📖 Official Docs</div>
<div class="space-y-1">
<div class="p-2 bg-gray-900/50 rounded border border-gray-700/50">
<a href="https://code.visualstudio.com/docs/copilot/agents/subagents" class="text-cyan-400 hover:text-cyan-300 font-medium">VS Code Subagents</a>
<div class="text-gray-400 mt-0.5">Invocation, parallel execution, context isolation, frontmatter</div>
</div>
<div class="p-2 bg-gray-900/50 rounded border border-gray-700/50">
<a href="https://code.visualstudio.com/docs/copilot/customization/custom-agents" class="text-cyan-400 hover:text-cyan-300 font-medium">Custom Agents in VS Code</a>
<div class="text-gray-400 mt-0.5">Agent structure, YAML frontmatter, tool restrictions, model selection</div>
</div>
<div class="p-2 bg-gray-900/50 rounded border border-gray-700/50">
<a href="https://code.visualstudio.com/docs/copilot/agents/background-agents" class="text-cyan-400 hover:text-cyan-300 font-medium">Background Agents</a>
<div class="text-gray-400 mt-0.5">Autonomous execution, hand-off workflow, worktree integration</div>
</div>
<div class="p-2 bg-gray-900/50 rounded border border-gray-700/50">
<a href="https://code.visualstudio.com/updates/v1_109#_agent-orchestration" class="text-cyan-400 hover:text-cyan-300 font-medium">VS Code 1.109 Agent Orchestration</a>
<div class="text-gray-400 mt-0.5">Invocation controls, parallel execution support, session management</div>
</div>
<div class="p-2 bg-gray-900/50 rounded border border-gray-700/50">
<a href="https://docs.github.com/en/copilot/concepts/agents/copilot-cli/fleet" class="text-cyan-400 hover:text-cyan-300 font-medium">Copilot CLI /fleet</a>
<div class="text-gray-400 mt-0.5">Terminal fan-out: parallel subagent execution from the CLI</div>
</div>
<div class="p-2 bg-gray-900/50 rounded border border-gray-700/50">
<a href="https://docs.github.com/en/copilot/how-tos/use-copilot-agents/coding-agent/create-custom-agents" class="text-cyan-400 hover:text-cyan-300 font-medium">Creating Custom Agents (GitHub Docs)</a>
<div class="text-gray-400 mt-0.5">User-level, repo-level, and org-level agent definitions</div>
</div>
<div class="p-2 bg-gray-900/50 rounded border border-gray-700/50">
<a href="https://git-scm.com/docs/git-worktree" class="text-cyan-400 hover:text-cyan-300 font-medium">Git Worktree Reference</a>
<div class="text-gray-400 mt-0.5">Parallel workspace isolation — technical lifecycle and commands</div>
</div>
</div>
</div>
<div>
<div class="font-bold text-purple-300 mb-2 text-sm">🛠️ Examples & Tools</div>
<div class="space-y-1">
<div class="p-2 bg-gray-900/50 rounded border border-gray-700/50">
<a href="https://github.com/bradygaster/squad" class="text-purple-400 hover:text-purple-300 font-medium">github.com/bradygaster/squad</a>
<div class="text-gray-400 mt-0.5">Production agent team: persistent memory, parallel execution, GitHub Issues, Ralph monitor</div>
</div>
<div class="p-2 bg-gray-900/50 rounded border border-gray-700/50">
<a href="https://github.com/bradygaster/squad/blob/main/docs/guide.md" class="text-purple-400 hover:text-purple-300 font-medium">Squad Product Guide</a>
<div class="text-gray-400 mt-0.5">Setup, ceremonies, memory layers, reviewer protocol</div>
</div>
<div class="p-2 bg-gray-900/50 rounded border border-gray-700/50">
<a href="https://github.com/Sentry01/AgentCouncil" class="text-purple-400 hover:text-purple-300 font-medium">github.com/Sentry01/AgentCouncil</a>
<div class="text-gray-400 mt-0.5">Multi-model deliberation: Claude + GPT + Gemini, collaborative and adversarial modes</div>
</div>
<div class="p-2 bg-gray-900/50 rounded border border-gray-700/50">
<a href="https://docs.github.com/en/copilot/how-tos/copilot-cli/speeding-up-task-completion" class="text-purple-400 hover:text-purple-300 font-medium">Using /fleet — How-To Guide</a>
<div class="text-gray-400 mt-0.5">Step-by-step: plan mode → autopilot + /fleet for parallel execution</div>
</div>
</div>
</div>
</div>

---
class: text-center
---

<div class="h-full flex flex-col items-center justify-center relative overflow-hidden">
<div class="absolute inset-0 bg-gradient-to-br from-cyan-900/20 via-blue-900/10 to-indigo-900/20"></div>
<div class="absolute top-1/4 left-1/2 -translate-x-1/2 -translate-y-1/2 w-96 h-96 bg-gradient-to-r from-cyan-500/20 via-blue-500/20 to-indigo-500/20 rounded-full blur-3xl"></div>
<div class="relative z-10">
<div class="absolute inset-0 blur-2xl opacity-50"><img src="./sdp-logo.png" class="w-48" alt="" /></div>
<img src="./sdp-logo.png" class="w-48 relative" alt="SDP Logo" />
</div>
<h1 class="!text-5xl !font-bold !mt-6 bg-gradient-to-r from-cyan-400 via-blue-400 to-indigo-400 bg-clip-text text-transparent relative z-10">Thank You!</h1>
<div class="mt-4 relative z-10">
<span class="px-6 py-2 bg-gradient-to-r from-cyan-600/80 to-blue-600/80 rounded-full text-white text-lg font-medium shadow-lg shadow-cyan-500/25">Building Agent Systems: Subagents, Teams, and Autonomous Execution</span>
</div>
<div class="mt-8 grid grid-cols-3 gap-4 text-sm max-w-3xl mx-auto relative z-10">
<div class="p-3 bg-gradient-to-br from-cyan-900/30 to-cyan-800/20 rounded-lg border border-cyan-500/30">
<div class="text-cyan-400 font-bold text-lg">~30x</div>
<div class="opacity-80 text-xs">Context reduction via subagent isolation</div>
</div>
<div class="p-3 bg-gradient-to-br from-blue-900/30 to-blue-800/20 rounded-lg border border-blue-500/30">
<div class="text-blue-400 font-bold text-lg">9.7 hrs/wk</div>
<div class="opacity-80 text-xs">Reclaimed with background agents</div>
</div>
<div class="p-3 bg-gradient-to-br from-indigo-900/30 to-indigo-800/20 rounded-lg border border-indigo-500/30">
<div class="text-indigo-400 font-bold text-lg">3 layers</div>
<div class="opacity-80 text-xs">Subagents → Teams → Autonomous</div>
</div>
</div>
<div class="mt-6 text-sm opacity-60 relative z-10">Questions? Let's discuss orchestration patterns and agent system design</div>
<div class="mt-4 w-32 h-1 bg-gradient-to-r from-transparent via-cyan-400 to-transparent rounded-full relative z-10"></div>
</div>