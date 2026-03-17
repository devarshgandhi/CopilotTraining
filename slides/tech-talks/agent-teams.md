---
theme: default
class: text-center
highlighter: shiki
lineNumbers: false
info: |
  ## Agent Teams: Coordinating Specialized AI Roles
  CopilotTraining Tech Talk
drawings:
  persist: false
transition: slide-left
title: Agent Teams - Coordinating Specialized AI Roles
module: tech-talks/agent-teams
mdc: true
status: active
updated: 2026-03-17
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
Agent Teams
</h1>
<div class="mt-4 relative z-10">
<span class="px-6 py-2 bg-gradient-to-r from-cyan-600/80 to-blue-600/80 rounded-full text-white text-xl font-medium shadow-lg shadow-cyan-500/25">
Coordinating Specialized AI Roles
</span>
</div>
<div class="mt-8 text-lg opacity-70 relative z-10">
Complex development requires specialized teams
</div>
<div class="mt-6 w-32 h-1 bg-gradient-to-r from-transparent via-cyan-400 to-transparent rounded-full relative z-10"></div>
</div>

<div class="abs-br m-6 flex gap-2">
<span class="text-sm opacity-50">Tech Talk · 45 minutes</span>
</div>

---
layout: center
---

# The Question

<div class="mt-8 p-6 bg-gradient-to-br from-cyan-900/40 to-blue-900/40 rounded-xl border-2 border-cyan-500/30 max-w-4xl mx-auto">
<div class="text-2xl font-bold text-cyan-300 mb-4">
How do I coordinate multiple specialized agents to handle complex development tasks that exceed single-agent capacity?
</div>
</div>

<div class="mt-8 text-lg opacity-80">
When one agent juggling everything isn't enough
</div>

---

# Table of Contents

<div class="mt-6 grid grid-cols-2 gap-4">

<div @click="$nav.go(7)" class="cursor-pointer p-4 bg-gradient-to-br from-cyan-900/40 to-cyan-900/20 rounded-xl border border-cyan-500/30 hover:border-cyan-400 transition-all">
  <div class="text-2xl mb-2">🏗️</div>
  <div class="font-bold text-cyan-300">Core Architecture</div>
  <div class="text-sm text-gray-400 mt-1">Conductor-delegate, context isolation</div>
</div>

<div @click="$nav.go(11)" class="cursor-pointer p-4 bg-gradient-to-br from-blue-900/40 to-blue-900/20 rounded-xl border border-blue-500/30 hover:border-blue-400 transition-all">
  <div class="text-2xl mb-2">🎯</div>
  <div class="font-bold text-blue-300">Squad System</div>
  <div class="text-sm text-gray-400 mt-1">Production teams, persistent memory</div>
</div>

<div @click="$nav.go(17)" class="cursor-pointer p-4 bg-gradient-to-br from-violet-900/40 to-violet-900/20 rounded-xl border border-violet-500/30 hover:border-violet-400 transition-all">
  <div class="text-2xl mb-2">⚖️</div>
  <div class="font-bold text-violet-300">Agent Council</div>
  <div class="text-sm text-gray-400 mt-1">Cross-model deliberation, two modes</div>
</div>

<div @click="$nav.go(20)" class="cursor-pointer p-4 bg-gradient-to-br from-purple-900/40 to-purple-900/20 rounded-xl border border-purple-500/30 hover:border-purple-400 transition-all">
  <div class="text-2xl mb-2">🎭</div>
  <div class="font-bold text-purple-300">Orchestration Patterns</div>
  <div class="text-sm text-gray-400 mt-1">4 proven coordination strategies</div>
</div>

</div>

---

# Mental Model Shift

<div class="mt-4">

<div class="grid grid-cols-2 gap-4 text-sm">

<div>
<div class="font-bold text-green-400 mb-3">✅ Move Toward</div>
<div class="space-y-2">
  <div class="p-2 bg-green-900/20 rounded border-l-3 border-green-500">Conductor-delegate architecture</div>
  <div class="p-2 bg-green-900/20 rounded border-l-3 border-green-500">Single responsibility per agent</div>
  <div class="p-2 bg-green-900/20 rounded border-l-3 border-green-500">Tool constraints = role enforcement</div>
  <div class="p-2 bg-green-900/20 rounded border-l-3 border-green-500">Persistent agent memory</div>
  <div class="p-2 bg-green-900/20 rounded border-l-3 border-green-500">Parallel independent work</div>
</div>
</div>

<div>
<div class="font-bold text-red-400 mb-3">🛑 Move Away From</div>
<div class="space-y-2">
  <div class="p-2 bg-red-900/20 rounded border-l-3 border-red-500">Single agent for everything</div>
  <div class="p-2 bg-red-900/20 rounded border-l-3 border-red-500">Universal tool access</div>
  <div class="p-2 bg-red-900/20 rounded border-l-3 border-red-500">Implicit phase transitions</div>
  <div class="p-2 bg-red-900/20 rounded border-l-3 border-red-500">Raw data returns from subagents</div>
  <div class="p-2 bg-red-900/20 rounded border-l-3 border-red-500">Sequential when parallel possible</div>
</div>
</div>

</div>

<div class="mt-4 p-3 bg-cyan-900/20 rounded-lg border border-cyan-500/20 text-sm text-gray-300">
  <b class="text-cyan-300">Example:</b> Before: Single agent with 15 tools, 80% context on prep work, mediocre output after 4 hours. After: Coordinator delegates to specialists (isolated contexts), each at 90%+ effectiveness. Total time: 1.5 hours with approval gates.
</div>

</div>

---

# When to Use This Pattern

<div class="mt-4">

<div class="grid grid-cols-2 gap-4 text-sm">

<div>
<div class="font-bold text-green-400 mb-2">✅ Use Agent Teams When</div>
<div class="space-y-2">
  <div class="p-2 bg-green-900/20 rounded">3+ cognitive modes needed (plan/code/review)</div>
  <div class="p-2 bg-green-900/20 rounded">Context window hits 70-80%+ before implementation</div>
  <div class="p-2 bg-green-900/20 rounded">Separation of concerns matters</div>
  <div class="p-2 bg-green-900/20 rounded">Knowledge should compound across sessions</div>
</div>
</div>

<div>
<div class="font-bold text-red-400 mb-2">❌ Don't Use When</div>
<div class="space-y-2">
  <div class="p-2 bg-red-900/20 rounded">Simple task (&lt;200 LOC) → use Plan Mode</div>
  <div class="p-2 bg-red-900/20 rounded">Sequential phases only → multi-step-tasks</div>
  <div class="p-2 bg-red-900/20 rounded">Branch-level parallelism → parallel-execution</div>
  <div class="p-2 bg-red-900/20 rounded">&lt;5 agent tasks/week → overhead exceeds benefit</div>
</div>
</div>

</div>

</div>

---
layout: center
class: text-center
name: core-architecture
---

<div class="relative">
  <div class="text-6xl mb-6">🏗️</div>
  <h1 class="!text-4xl bg-gradient-to-r from-cyan-400 to-blue-400 bg-clip-text text-transparent">
    Core Architecture
  </h1>
  <p class="text-gray-400 mt-4 text-lg">Conductor-delegate pattern with tool-enforced boundaries</p>
</div>

---

# The Coordinator Pattern

<div class="mt-2">

<div class="grid grid-cols-5 gap-2 text-center text-xs mb-3">

<div class="col-span-5 p-3 bg-gradient-to-r from-cyan-900/40 to-blue-900/40 rounded-lg border border-cyan-500/30">
  <div class="font-bold text-cyan-300 text-sm">🎼 COORDINATOR</div>
  <div class="text-gray-400 text-xs mt-1">Interprets requests → routes via table → spawns specialists → validates → aggregates</div>
  <div class="text-yellow-400 text-xs mt-1 font-bold">NEVER implements directly</div>
</div>

<div class="col-span-5 text-center text-gray-500 text-xs">↓ delegates to isolated subagents ↓</div>

<div class="p-2 bg-green-900/30 rounded-lg border border-green-500/30">
  <div class="font-bold text-green-300 text-xs">🏗️ Lead</div>
  <div class="text-xs text-gray-400 mt-1">Scope, review</div>
</div>

<div class="p-2 bg-blue-900/30 rounded-lg border border-blue-500/30">
  <div class="font-bold text-blue-300 text-xs">⚛️ Frontend</div>
  <div class="text-xs text-gray-400 mt-1">UI, React</div>
</div>

<div class="p-2 bg-indigo-900/30 rounded-lg border border-indigo-500/30">
  <div class="font-bold text-indigo-300 text-xs">🔧 Backend</div>
  <div class="text-xs text-gray-400 mt-1">API, DB</div>
</div>

<div class="p-2 bg-purple-900/30 rounded-lg border border-purple-500/30">
  <div class="font-bold text-purple-300 text-xs">🧪 Tester</div>
  <div class="text-xs text-gray-400 mt-1">Tests, QA</div>
</div>

<div class="p-2 bg-pink-900/30 rounded-lg border border-pink-500/30">
  <div class="font-bold text-pink-300 text-xs">📋 Scribe</div>
  <div class="text-xs text-gray-400 mt-1">Memory</div>
</div>

</div>

<div class="text-xs text-gray-400 text-center mb-2">Each specialist in <b class="text-cyan-300">isolated context window</b> — 6.6% coordinator overhead, 93%+ available for work</div>

<div class="grid grid-cols-2 gap-2 text-xs">
  <div class="p-2 bg-cyan-900/20 rounded border border-cyan-500/20">
    <div class="font-bold text-cyan-300">🎯 Focused Context</div>
    <div class="text-gray-300">Each agent gets only what it needs. Lead gets architecture, Frontend gets UI, Backend gets APIs.</div>
  </div>
  <div class="p-2 bg-blue-900/20 rounded border border-blue-500/20">
    <div class="font-bold text-blue-300">🔧 Right Tools</div>
    <div class="text-gray-300">Tool constraints = role enforcement. Planners can't edit; implementers can't over-research.</div>
  </div>
</div>

</div>

---

# Why This Works

<div class="mt-4 grid grid-cols-2 gap-3 text-xs">

<div class="p-3 bg-cyan-900/20 rounded-lg border border-cyan-500/20">
  <div class="font-bold text-cyan-300 mb-2">🎯 Focused Context</div>
  <div class="text-gray-300">Each agent gets only what it needs. No accumulated context from other domains. Lead at 1.7%, Frontend at 1.2%, Backend at 1.9% of 200K window.</div>
</div>

<div class="p-3 bg-blue-900/20 rounded-lg border border-blue-500/20">
  <div class="font-bold text-blue-300 mb-2">⚡ Parallel Execution</div>
  <div class="text-gray-300">"Team, build the login page" → all agents start simultaneously. 3-5x throughput on parallelizable work. Coordinator chains follow-up automatically.</div>
</div>

<div class="p-3 bg-indigo-900/20 rounded-lg border border-indigo-500/20">
  <div class="font-bold text-indigo-300 mb-2">✅ Quality Checkpoints</div>
  <div class="text-gray-300">Reviewer protocol: rejected work must be revised by a <i>different</i> agent. No self-review loops. 40-60% less rework.</div>
</div>

<div class="p-3 bg-purple-900/20 rounded-lg border border-purple-500/20">
  <div class="font-bold text-purple-300 mb-2">🧠 Persistent Memory</div>
  <div class="text-gray-300">Agents write learnings to history.md after every session. Knowledge compounds. Week 4 agents know your conventions, patterns, preferences.</div>
</div>

</div>

<div class="mt-3 p-3 bg-gradient-to-r from-green-900/30 to-blue-900/30 rounded-lg border border-green-500/20 text-xs">
  <div class="font-bold text-green-300 mb-1">💡 Specialization Advantage</div>
  <div class="text-gray-300">Backend agent tuned for APIs, auth, data modeling outperforms generalist by 20-30%. Same for Frontend (UI, state) and Testing (edge cases, integration). Team of specialists beats single generalist.</div>
</div>

---

# Tool Assignment Guidelines

<div class="mt-4">

<div class="text-xs">

| Agent Role | Appropriate Tools | Rationale |
|------------|-------------------|-----------|
| **Research / Discovery** | `search`, `fetch`, `githubRepo` | Read-only exploration, no modification risk |
| **Planning / Strategy** | `search`, `fetch`, `create` (docs only) | Can document plans, can't implement |
| **Implementation** | `edit`, `create`, `delete`, `search` | Full editing power, focused on execution |
| **Review / Validation** | `search`, `fetch`, `analysis`, `linter` | Read + analyze, can't modify implementation |
| **Testing** | `search`, `create`, `runTests` | Create tests + verify execution |

</div>

<div class="mt-4 p-3 bg-yellow-900/20 rounded-lg border-l-4 border-yellow-500 text-xs">
  <div class="font-bold text-yellow-400">Why Tool Restrictions?</div>
  <div class="text-gray-300 mt-1">Without constraints: Planner "helpfully" fixes typos → now it's implementing. Reviewer "just fixes this one thing" → now it's implementing + biasing review. <b>With constraints:</b> VS Code validates tool availability before invocation. No accidental context mixing possible.</div>
</div>

</div>

---
layout: center
class: text-center
name: squad-system
---

<div class="relative">
  <div class="text-6xl mb-6">🎯</div>
  <h1 class="!text-4xl bg-gradient-to-r from-blue-400 to-indigo-400 bg-clip-text text-transparent">
    Squad: Production-Ready Teams
  </h1>
  <p class="text-gray-400 mt-4 text-lg">A persistent AI development team that lives in your repo</p>
</div>

---

# Squad: What It Is & How It Works

<div class="mt-2 grid grid-cols-2 gap-3 text-xs">

<div>
<div class="p-3 bg-gradient-to-r from-cyan-900/40 to-blue-900/40 rounded-lg border border-cyan-500/30 mb-3">
  <div class="font-bold text-cyan-300 mb-1">github.com/bradygaster/squad</div>
  <div class="text-gray-300">Describe your project → Squad creates specialists (Lead, Frontend, Backend, Tester) that <b>persist as files in your repo</b>. Each runs in its own context window, reads its history, and writes back what it learned. <b>Knowledge compounds.</b></div>
</div>
<div class="p-2 bg-green-900/20 rounded border-l-4 border-green-500 text-xs">
  <b class="text-green-400">Commit .ai-team/</b> — anyone who clones your repo gets the team, with all accumulated knowledge.
</div>
</div>

<div class="font-mono bg-gray-900/60 p-3 rounded-lg text-xs leading-snug">
<div class="text-yellow-300 mb-1">"Team, build login page"  ← You</div>
<div class="text-cyan-300">        COORDINATOR</div>
<div class="text-gray-500">  Routes · Spawns · Validates</div>
<div class="text-gray-500">  NEVER implements directly</div>
<div class="mt-1 text-blue-300">   ↙    ↓    ↘     ↘</div>
<div class="grid grid-cols-4 gap-1 text-center mt-1">
  <div class="bg-blue-900/40 rounded p-1">🏗️<br/><span class="text-gray-400">Lead</span></div>
  <div class="bg-indigo-900/40 rounded p-1">⚛️<br/><span class="text-gray-400">FE</span></div>
  <div class="bg-purple-900/40 rounded p-1">🔧<br/><span class="text-gray-400">BE</span></div>
  <div class="bg-pink-900/40 rounded p-1">🧪<br/><span class="text-gray-400">Test</span></div>
</div>
<div class="text-gray-500 text-center mt-1">Own context window each</div>
<div class="text-violet-300 mt-1 text-center">↓  📋 Scribe (silent)</div>
<div class="text-cyan-300 mt-1 text-center">🧠 decisions.md · history.md</div>
</div>

</div>

---

# Squad: What Makes It Different

<div class="mt-3 grid grid-cols-2 gap-3 text-xs">

<div class="p-3 bg-blue-900/20 rounded-lg border border-blue-500/20">
  <div class="font-bold text-blue-300 mb-1">✅ Reviewer Protocol — No Self-Review Loops</div>
  <div class="text-gray-300">Agent A rejected → <b>locked out</b> → Agent B must revise. Prevents circular "fixing" loops that plague single-agent quality.</div>
</div>

<div class="p-3 bg-indigo-900/20 rounded-lg border border-indigo-500/20">
  <div class="font-bold text-indigo-300 mb-1">🤖 Ralph — Autonomous Work Monitor</div>
  <div class="text-gray-300">Polls open issues, draft PRs, CI failures → triage → assign → spawn. Team never sits idle when work exists.</div>
</div>

<div class="p-3 bg-cyan-900/20 rounded-lg border border-cyan-500/20 col-span-2">
  <div class="font-bold text-cyan-300 mb-2">🧠 Knowledge Compounds Over Time</div>
  <div class="grid grid-cols-3 gap-3 text-gray-300">
    <div class="text-center">
      <div class="font-bold text-green-400">🌱 Week 1</div>
      <div>Project description, tech stack, your name</div>
    </div>
    <div class="text-center">
      <div class="font-bold text-blue-400">🌿 Week 4</div>
      <div>Conventions, patterns, API design, test strategies</div>
    </div>
    <div class="text-center">
      <div class="font-bold text-purple-400">🌳 Week 12</div>
      <div>Full architecture, tech debt map, performance patterns</div>
    </div>
  </div>
</div>

</div>

---
layout: center
class: text-center
name: agent-council
---

<div class="relative">
  <div class="text-6xl mb-6">⚖️</div>
  <h1 class="!text-4xl bg-gradient-to-r from-violet-400 to-fuchsia-400 bg-clip-text text-transparent">
    Agent Council
  </h1>
  <p class="text-gray-400 mt-4 text-lg">Cross-model deliberation — when different AI families think differently</p>
</div>

---

# Agent Council: Model Diversity vs. Role Specialization

<div class="mt-3 text-xs">

<div class="p-3 bg-gradient-to-r from-violet-900/40 to-fuchsia-900/40 rounded-lg border-2 border-violet-500/30 mb-3">
  <div class="text-sm font-bold text-violet-300 mb-1">github.com/Sentry01/AgentCouncil</div>
  <div class="text-gray-300">A Copilot CLI skill that runs <b>Claude, GPT, and Gemini in parallel</b> — then has them build on each other's ideas (collaborative) or attack each other's positions (adversarial). The insight: different models have different blind spots. Running them together surfaces what no single model produces alone.</div>
</div>

<div class="grid grid-cols-2 gap-3">

<div class="p-3 bg-violet-900/20 rounded-lg border border-violet-500/20">
  <div class="font-bold text-violet-300 mb-2">🤝 Collaborative Mode (Default)</div>
  <div class="text-gray-300 mb-2">Agents draft independently → read each other → improve → orchestrator synthesizes. <b>7 calls total.</b></div>
  <div class="text-gray-400 italic">Best for: brainstorming, design exploration, research synthesis</div>
</div>

<div class="p-3 bg-fuchsia-900/20 rounded-lg border border-fuchsia-500/20">
  <div class="font-bold text-fuchsia-300 mb-2">🗡️ Adversarial Mode</div>
  <div class="text-gray-300 mb-2">Agents draft → orchestrator picks winner → others attack → verdict: <b>SURVIVED / MODIFIED / OVERTURNED</b>. <b>6 calls total.</b></div>
  <div class="text-gray-400 italic">Best for: architecture decisions, security reviews, A vs B comparisons</div>
</div>

</div>

<div class="mt-2 grid grid-cols-4 gap-2">
  <div class="p-2 bg-gray-900/50 rounded border border-gray-700 text-center">
    <div class="font-bold text-orange-300">Alpha</div>
    <div class="text-gray-400">Deep Explorer</div>
    <div class="text-xs text-gray-500">claude-opus</div>
  </div>
  <div class="p-2 bg-gray-900/50 rounded border border-gray-700 text-center">
    <div class="font-bold text-blue-300">Beta</div>
    <div class="text-gray-400">Practical Builder</div>
    <div class="text-xs text-gray-500">gpt-5.4</div>
  </div>
  <div class="p-2 bg-gray-900/50 rounded border border-gray-700 text-center">
    <div class="font-bold text-green-300">Gamma</div>
    <div class="text-gray-400">Elegant Minimalist</div>
    <div class="text-xs text-gray-500">gemini-3.1</div>
  </div>
  <div class="p-2 bg-gray-900/50 rounded border border-gray-700 text-center">
    <div class="font-bold text-violet-300">Orchestrator</div>
    <div class="text-gray-400">Author / Judge</div>
    <div class="text-xs text-gray-500">claude-opus</div>
  </div>
</div>

</div>

---

# AgentCouncil: Deliberate → Then Build

<div class="mt-3 text-xs">

<div class="grid grid-cols-2 gap-3 mb-3">

<div>
<div class="font-bold text-violet-300 mb-2">Auto Mode Detection</div>
<div class="space-y-1 text-gray-300">
  <div class="p-2 bg-violet-900/20 rounded"><code class="text-green-400">council: How to structure the API?</code> → 🤝</div>
  <div class="p-2 bg-violet-900/20 rounded"><code class="text-green-400">brainstorm: Novel caching approaches</code> → 🤝</div>
  <div class="p-2 bg-fuchsia-900/20 rounded"><code class="text-green-400">debate: Monorepo vs polyrepo</code> → 🗡️</div>
  <div class="p-2 bg-fuchsia-900/20 rounded"><code class="text-green-400">stress-test: Is this auth secure?</code> → 🗡️</div>
  <div class="p-2 bg-violet-900/10 rounded"><code class="text-green-400">verbose council: ...</code> → shows each agent's draft</div>
</div>
</div>

<div>
<div class="font-bold text-fuchsia-300 mb-2">Install (No Build Required)</div>
<div class="font-mono text-green-400 bg-gray-900/60 p-3 rounded-lg text-xs mb-2">
git clone github.com/Sentry01/AgentCouncil<br/>
cp skills/agent-council/skill.md<br/>
&nbsp;&nbsp;~/.copilot/skills/agent-council/skill.md<br/>
<br/>
# or as a standalone agent:<br/>
cp agents/AgentCouncil.agent.md<br/>
&nbsp;&nbsp;~/.copilot/agents/
</div>
</div>

</div>

<div class="p-3 bg-gradient-to-r from-violet-900/30 to-blue-900/30 rounded-lg border border-violet-500/20">
  <div class="font-bold text-violet-300 mb-2">🎯 Combining Both: Deliberation → Execution</div>
  <div class="grid grid-cols-3 gap-3 text-gray-300">
    <div class="p-2 bg-fuchsia-900/20 rounded text-center">
      <div class="font-bold text-fuchsia-300">1. Deliberate</div>
      <div><code>debate: WebSockets vs SSE</code><br/>— adversarial council stress-tests decision across 3 models</div>
    </div>
    <div class="p-2 bg-gray-900/40 rounded text-center text-gray-500">
      <div class="text-2xl">→</div>
      <div>Validated decision + rationale</div>
    </div>
    <div class="p-2 bg-blue-900/20 rounded text-center">
      <div class="font-bold text-blue-300">2. Execute</div>
      <div>Hand to Squad → Backend Dev implements, Tester runs in parallel</div>
    </div>
  </div>
</div>

</div>

---
layout: center
class: text-center
name: orchestration-patterns
---

<div class="relative">
  <div class="text-6xl mb-6">🎭</div>
  <h1 class="!text-4xl bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">
    Orchestration Patterns
  </h1>
  <p class="text-gray-400 mt-4 text-lg">4 proven coordination strategies for different workflows</p>
</div>

---

# Four Orchestration Patterns

<div class="mt-3 grid grid-cols-2 gap-3 text-xs">

<div class="p-3 bg-cyan-900/20 rounded-lg border border-cyan-500/20">
  <div class="font-bold text-cyan-300 mb-2">1️⃣ Linear Pipeline</div>
  <div class="text-gray-400 text-xs mb-2">Discovery → Plan → Implement → Review → Test</div>
  <div class="text-gray-300">Well-defined features, clear requirements. Simple, predictable, easy to debug.</div>
  <div class="text-cyan-400 text-xs mt-2">Example: Adding a single REST endpoint</div>
</div>

<div class="p-3 bg-blue-900/20 rounded-lg border border-blue-500/20">
  <div class="font-bold text-blue-300 mb-2">2️⃣ Iterative Refinement</div>
  <div class="text-gray-400 text-xs mb-2">Implement → Review → [Pass?] → Loop or Continue</div>
  <div class="text-gray-300">Quality-critical code. Reviewer returns NEEDS_REVISION → loop until APPROVED.</div>
  <div class="text-blue-400 text-xs mt-2">Example: OAuth with token refresh edge cases</div>
</div>

<div class="p-3 bg-indigo-900/20 rounded-lg border border-indigo-500/20">
  <div class="font-bold text-indigo-300 mb-2">3️⃣ Parallel Specialists</div>
  <div class="text-gray-400 text-xs mb-2">Plan → [Security + Perf + Docs in parallel] → Integrate</div>
  <div class="text-gray-300">Independent cross-cutting concerns. 3-5x faster validation, comprehensive coverage.</div>
  <div class="text-indigo-400 text-xs mt-2">Example: Full-stack feature touching auth, DB, API</div>
</div>

<div class="p-3 bg-purple-900/20 rounded-lg border border-purple-500/20">
  <div class="font-bold text-purple-300 mb-2">4️⃣ Hierarchical</div>
  <div class="text-gray-400 text-xs mb-2">Master → [Frontend + Backend Conductors] → Specialists</div>
  <div class="text-gray-300">Full-stack spanning 5+ subsystems. Sub-conductors manage domain specialists.</div>
  <div class="text-purple-400 text-xs mt-2">Example: Complete e-commerce checkout flow</div>
</div>

</div>

---

# Use Case: Full-Stack Auth with Squad

<div class="mt-2 text-xs">

<div class="p-3 bg-gradient-to-r from-cyan-900/30 to-blue-900/30 rounded-lg border border-cyan-500/20 mb-3">
  <div class="font-bold text-cyan-300 mb-2">The Scenario</div>
  <div class="text-gray-300">
    Building a user authentication system requires coordinated work across frontend (login form, session management), backend (auth endpoints, token handling), testing (security edge cases), and architecture (token refresh, session storage). A single agent juggling all four domains loses context and produces mediocre results.
  </div>
</div>

<div class="p-3 bg-blue-900/20 rounded-lg border border-blue-500/20 mb-3">
  <div class="font-bold text-blue-300 mb-2">The Solution: Squad Fan-Out</div>
  <div class="font-mono text-green-400 text-xs mb-2">
    You: "Team, build the authentication system"
  </div>
  <div class="text-gray-300">
    🏗️ Lead — scoping requirements, defining contracts<br/>
    ⚛️ Frontend — building login form, session UI<br/>
    🔧 Backend — auth endpoints, JWT handling<br/>
    🧪 Tester — writing test cases from spec<br/>
    ↓ agents finish, coordinator chains follow-up<br/>
    🧪 Tester — edge cases reveal token refresh gap<br/>
    🔧 Backend — picks up edge case automatically
  </div>
</div>

<div class="grid grid-cols-2 gap-2">
  <div class="p-2 bg-green-900/20 rounded border border-green-500/20">
    <b class="text-green-400">Result:</b> <span class="text-gray-300">4 agents in parallel vs. 1 context-switching. Knowledge compounds after sessions. Lead reviews, can reject → different agent must revise.</span>
  </div>
  <div class="p-2 bg-cyan-900/20 rounded border border-cyan-500/20">
    <b class="text-cyan-400">Artifact:</b> <span class="text-gray-300">decisions.md captures JWT format, session storage, endpoint contracts for future reference.</span>
  </div>
</div>

</div>

---

# What You Can Do Today

<div class="mt-3 grid grid-cols-3 gap-3 text-xs">

<div class="p-3 bg-green-900/20 rounded-lg border border-green-500/20">
  <div class="font-bold text-green-300 mb-2">⏱️ 10 Minutes</div>
  <div class="space-y-1 text-gray-300 text-xs">
    <div>• Install Squad: <code>npx github:bradygaster/squad</code></div>
    <div>• Form your team by describing your project</div>
    <div>• Give first task: "Team, build [something small]"</div>
    <div>• Install AgentCouncil skill and try <code>council: [real question]</code></div>
  </div>
</div>

<div class="p-3 bg-blue-900/20 rounded-lg border border-blue-500/20">
  <div class="font-bold text-blue-300 mb-2">🔧 1-2 Hours</div>
  <div class="space-y-1 text-gray-300 text-xs">
    <div>• Run 3-5 tasks — watch agents stop asking questions they've answered</div>
    <div>• Try direct naming vs. fan-out ("Team, build...")</div>
    <div>• Check .ai-team/decisions.md for captured decisions</div>
    <div>• Run <code>debate: [A] vs [B]</code> on a real pending decision</div>
    <div>• Add a new team member: "I need a DevOps person"</div>
  </div>
</div>

<div class="p-3 bg-purple-900/20 rounded-lg border border-purple-500/20">
  <div class="font-bold text-purple-300 mb-2">🚀 1-2 Weeks</div>
  <div class="space-y-1 text-gray-300 text-xs">
    <div>• Enable GitHub Issues integration with label-based triage</div>
    <div>• Activate Ralph for autonomous backlog processing</div>
    <div>• Export/import trained teams across projects</div>
    <div>• Measure before/after: time, rework, quality metrics</div>
  </div>
</div>


</div>

---

# Related Patterns & Resources

<div class="mt-3 grid grid-cols-2 gap-3 text-xs">

<div>
<div class="font-bold text-cyan-300 mb-2">🔗 Related Patterns</div>
<div class="space-y-2">
  <div class="p-2 bg-gray-800/50 rounded">
    <span class="text-blue-300 font-medium">Multi-Step Tasks</span>
    <span class="text-gray-500"> — Sequential phases without role specialization</span>
  </div>
  <div class="p-2 bg-gray-800/50 rounded">
    <span class="text-blue-300 font-medium">Parallel Execution</span>
    <span class="text-gray-500"> — Branch-level parallelism with worktrees</span>
  </div>
  <div class="p-2 bg-gray-800/50 rounded">
    <span class="text-blue-300 font-medium">Agentic SDLC</span>
    <span class="text-gray-500"> — Org-wide agent scaling patterns</span>
  </div>
  <div class="p-2 bg-gray-800/50 rounded">
    <span class="text-blue-300 font-medium">Custom Agents (Workshop)</span>
    <span class="text-gray-500"> — Hands-on exercises for building agents</span>
  </div>
</div>
</div>

<div>
<div class="font-bold text-cyan-300 mb-2">📚 Official Docs</div>
<div class="space-y-2">
  <div class="p-2 bg-gray-800/50 rounded">
    📖 <a href="https://code.visualstudio.com/docs/copilot/customization/custom-agents" class="text-cyan-400">Custom Agents in VS Code</a>
  </div>
  <div class="p-2 bg-gray-800/50 rounded">
    📖 <a href="https://code.visualstudio.com/docs/copilot/agents/subagents" class="text-cyan-400">Subagents & Context Isolation</a>
  </div>
  <div class="p-2 bg-gray-800/50 rounded">
    📖 <a href="https://code.visualstudio.com/updates/v1_109#_agent-orchestration" class="text-cyan-400">VS Code 1.109 Agent Orchestration</a>
  </div>
  <div class="p-2 bg-gray-800/50 rounded">
    🐙 <a href="https://github.com/bradygaster/squad" class="text-cyan-400">Squad Repository</a>
  </div>
  <div class="p-2 bg-gray-800/50 rounded">
    📖 <a href="https://github.com/bradygaster/squad/blob/main/docs/guide.md" class="text-cyan-400">Squad Product Guide</a>
  </div>
  <div class="p-2 bg-gray-800/50 rounded">
    ⚖️ <a href="https://github.com/Sentry01/AgentCouncil" class="text-violet-400">AgentCouncil Repository</a>
  </div>
</div>
</div>

</div>

---
layout: end
---

<div class="h-full flex flex-col items-center justify-center">
  <h1 class="!text-5xl bg-gradient-to-r from-cyan-400 via-blue-400 to-indigo-400 bg-clip-text text-transparent font-bold">
    Thank You
  </h1>
  <div class="mt-6 w-32 h-1 bg-gradient-to-r from-transparent via-cyan-400 to-transparent rounded-full"></div>
  <p class="text-gray-300 mt-6 text-xl">Agent Teams: Coordinating Specialized AI Roles</p>
  <div class="mt-8 flex gap-6 text-sm text-gray-500">
    <span>🐙 <a href="https://github.com/bradygaster/squad" class="text-cyan-400">Squad</a></span>
    <span>⚖️ <a href="https://github.com/Sentry01/AgentCouncil" class="text-violet-400">AgentCouncil</a></span>
  </div>
  <div class="mt-6 text-sm text-gray-600">CopilotTraining · Tech Talk</div>
</div>
