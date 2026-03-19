---
theme: default
class: text-center
highlighter: shiki
lineNumbers: false
info: |
  ## Agentic SDLC: Infrastructure for AI Velocity
  CopilotTraining Tech Talk
drawings:
  persist: false
transition: slide-left
title: Agentic SDLC - Infrastructure for AI Velocity
module: tech-talks/agentic-sdlc
status: active
updated: 2026-03-19
mdc: true
---

<div class="h-full flex flex-col items-center justify-center relative overflow-hidden">
<div class="absolute inset-0 bg-gradient-to-br from-cyan-900/20 via-blue-900/10 to-indigo-900/20"></div>
<div class="absolute top-1/4 left-1/2 -translate-x-1/2 -translate-y-1/2 w-96 h-96 bg-gradient-to-r from-cyan-500/20 via-blue-500/20 to-indigo-500/20 rounded-full blur-3xl"></div>
<div class="relative z-10">
<div class="absolute inset-0 blur-2xl opacity-50"><img src="./sdp-logo.png" class="w-64" alt="" /></div>
<img src="./sdp-logo.png" class="w-64 relative" alt="SDP Logo" />
</div>
<h1 class="!text-5xl !font-bold !mt-8 bg-gradient-to-r from-cyan-400 via-blue-400 to-indigo-400 bg-clip-text text-transparent relative z-10">Agentic SDLC</h1>
<div class="mt-4 relative z-10">
<span class="px-6 py-2 bg-gradient-to-r from-cyan-600/80 to-blue-600/80 rounded-full text-white text-xl font-medium shadow-lg shadow-cyan-500/25">Level 5 Infrastructure for AI Velocity</span>
</div>
<div class="mt-8 text-lg opacity-70 relative z-10">Progress from standardized engineering to autonomous delivery without losing trust</div>
<div class="mt-6 w-32 h-1 bg-gradient-to-r from-transparent via-cyan-400 to-transparent rounded-full relative z-10"></div>
</div>
<div class="abs-br m-6 flex gap-2"><span class="text-sm opacity-50">Tech Talk · 90 minutes</span></div>

---
layout: center
---

# 🎯 The Core Question

<div class="p-6 bg-gradient-to-br from-cyan-900/30 to-blue-900/30 rounded-xl border-2 border-cyan-500/50 max-w-4xl mx-auto mt-6">
<div class="text-2xl font-semibold text-cyan-300 mb-4">"How do I rewire repositories, PR workflows, and CI/CD to scale from 2-3 features/week to 10-15 features/day with AI agents?"</div>
<div class="text-lg opacity-90">Not by making coding faster alone, but by making trust, review, and topology scale with machine-paced delivery.</div>
</div>

<div class="mt-8 grid grid-cols-4 gap-4 text-sm">
<div class="p-3 bg-cyan-900/20 rounded-lg border border-cyan-500/20">
<div class="text-cyan-400 font-semibold mb-1">Topology</div>
<div class="opacity-80">Atomic changes in one workspace</div>
</div>
<div class="p-3 bg-blue-900/20 rounded-lg border border-blue-500/20">
<div class="text-blue-400 font-semibold mb-1">Governance</div>
<div class="opacity-80">Outcome review, not line review</div>
</div>
<div class="p-3 bg-indigo-900/20 rounded-lg border border-indigo-500/20">
<div class="text-indigo-400 font-semibold mb-1">Trust Factory</div>
<div class="opacity-80">Under 10 minute PR checks</div>
</div>
<div class="p-3 bg-purple-900/20 rounded-lg border border-purple-500/20">
<div class="text-purple-400 font-semibold mb-1">Maturity</div>
<div class="opacity-80">Level 1 to Level 5 progression</div>
</div>
</div>

---
layout: center
---

# 📖 Table of Contents

<div class="grid grid-cols-2 gap-6 mt-6">
<div @click="$nav.go(5)" class="cursor-pointer group">
<div class="p-5 bg-gradient-to-br from-cyan-900/40 to-blue-900/40 rounded-xl border-2 border-cyan-500/50 hover:border-cyan-400 hover:scale-105 transition-all duration-300 shadow-lg shadow-cyan-500/10">
<div class="text-3xl mb-2">🏗️</div>
<div class="text-lg font-bold bg-gradient-to-r from-cyan-300 to-blue-300 bg-clip-text text-transparent">Part 1</div>
<div class="text-sm text-gray-300 mt-1">Repository Topology</div>
<div class="text-xs text-cyan-400/70 mt-2">One workspace for atomic agent change</div>
</div>
</div>
<div @click="$nav.go(9)" class="cursor-pointer group">
<div class="p-5 bg-gradient-to-br from-blue-900/40 to-indigo-900/40 rounded-xl border-2 border-blue-500/50 hover:border-blue-400 hover:scale-105 transition-all duration-300 shadow-lg shadow-blue-500/10">
<div class="text-3xl mb-2">📋</div>
<div class="text-lg font-bold bg-gradient-to-r from-blue-300 to-indigo-300 bg-clip-text text-transparent">Part 2</div>
<div class="text-sm text-gray-300 mt-1">PR Workflows</div>
<div class="text-xs text-blue-400/70 mt-2">Level 5 volume breaks Level 3 review habits</div>
</div>
</div>
<div @click="$nav.go(13)" class="cursor-pointer group">
<div class="p-5 bg-gradient-to-br from-indigo-900/40 to-purple-900/40 rounded-xl border-2 border-indigo-500/50 hover:border-indigo-400 hover:scale-105 transition-all duration-300 shadow-lg shadow-indigo-500/10">
<div class="text-3xl mb-2">🏭</div>
<div class="text-lg font-bold bg-gradient-to-r from-indigo-300 to-purple-300 bg-clip-text text-transparent">Part 3</div>
<div class="text-sm text-gray-300 mt-1">Trust Manufacturing</div>
<div class="text-xs text-indigo-400/70 mt-2">Fast, deterministic evidence at agent speed</div>
</div>
</div>
<div @click="$nav.go(17)" class="cursor-pointer group">
<div class="p-5 bg-gradient-to-br from-purple-900/40 to-pink-900/40 rounded-xl border-2 border-purple-500/50 hover:border-purple-400 hover:scale-105 transition-all duration-300 shadow-lg shadow-purple-500/10">
<div class="text-3xl mb-2">🚀</div>
<div class="text-lg font-bold bg-gradient-to-r from-purple-300 to-pink-300 bg-clip-text text-transparent">Part 4</div>
<div class="text-sm text-gray-300 mt-1">Implementation Roadmap</div>
<div class="text-xs text-purple-400/70 mt-2">Standardized → Optimized → Autonomous</div>
</div>
</div>
</div>
<div class="mt-6 text-center text-sm opacity-60">Click any section to jump directly there</div>

---

# AgentRC Maturity Model: What Each Level Unlocks

<div class="grid grid-cols-5 gap-3 mt-4 text-xs">
<div class="p-3 bg-gray-900/50 rounded-lg border border-gray-700/50">
<div class="text-lg font-bold text-gray-300 mb-1">1</div>
<div class="font-semibold text-gray-200 mb-2">Functional</div>
<div class="text-gray-400">Builds and tests run reliably</div>
<div class="mt-2 text-cyan-400">Automation</div>
<div class="text-gray-400">Basic scripts work</div>
</div>
<div class="p-3 bg-cyan-900/20 rounded-lg border border-cyan-500/30">
<div class="text-lg font-bold text-cyan-300 mb-1">2</div>
<div class="font-semibold text-cyan-200 mb-2">Documented</div>
<div class="text-gray-300">Docs and instructions reduce guessing</div>
<div class="mt-2 text-cyan-400">Speed</div>
<div class="text-gray-400">Routine tasks accelerate</div>
</div>
<div class="p-3 bg-blue-900/20 rounded-lg border border-blue-500/30">
<div class="text-lg font-bold text-blue-300 mb-1">3</div>
<div class="font-semibold text-blue-200 mb-2">Standardized</div>
<div class="text-gray-300">CI, policy, CODEOWNERS, observability</div>
<div class="mt-2 text-blue-400">Safety</div>
<div class="text-gray-400">Repeatable trust gates</div>
</div>
<div class="p-3 bg-indigo-900/20 rounded-lg border border-indigo-500/30">
<div class="text-lg font-bold text-indigo-300 mb-1">4</div>
<div class="font-semibold text-indigo-200 mb-2">Optimized</div>
<div class="text-gray-300">MCP, custom agents, AI skills</div>
<div class="mt-2 text-indigo-400">Flow</div>
<div class="text-gray-400">Tool-aware multi-step work</div>
</div>
<div class="p-3 bg-green-900/30 rounded-lg border-2 border-green-500/50">
<div class="text-lg font-bold text-green-300 mb-1">5</div>
<div class="font-semibold text-green-200 mb-2">Autonomous</div>
<div class="text-gray-200">Agents are primary producers</div>
<div class="mt-2 text-green-400">Outcome</div>
<div class="text-gray-300">Machine-paced delivery with minimal oversight</div>
</div>
</div>

<div class="mt-6 p-4 bg-gradient-to-r from-amber-500/10 to-red-500/10 rounded-xl border border-amber-500/30 text-center">
<div class="text-lg font-semibold text-amber-300">What many teams call “Gen-4 SDLC” maps most closely to <span class="text-green-300">Level 5: Autonomous</span>.</div>
<div class="text-sm opacity-80 mt-1">The real lesson: Level 5 only works when Levels 1-4 are already doing their job.</div>
</div>

---
layout: center
name: part1
---

<div class="text-center mb-6">
<div class="text-5xl mb-4">🏗️</div>
<h1 class="!text-4xl bg-gradient-to-r from-cyan-400 to-blue-400 bg-clip-text text-transparent">Part 1: Repository Topology</h1>
<p class="text-xl opacity-80 mt-2">Give agents one atomic workspace for the feature</p>
</div>
<div class="p-5 bg-gradient-to-r from-cyan-500/10 to-blue-500/10 rounded-xl border border-cyan-500/30 mb-5 text-center max-w-3xl mx-auto">
<div class="text-lg">If a single feature spans three repos, you pay coordination tax three times before you ship once.</div>
</div>

---

# Monorepo by Default for Product Code

<div class="grid grid-cols-2 gap-6 mt-4 text-sm">
<div class="p-4 bg-red-900/20 rounded-xl border border-red-500/30">
<div class="font-bold text-red-300 mb-3">Multi-repo at agent scale</div>
<div class="space-y-2 text-gray-300">
<div>• 3 PRs for one feature</div>
<div>• staggered reviews and deploy order</div>
<div>• contract drift between repos</div>
<div>• debugging across boundaries becomes normal</div>
</div>
</div>
<div class="p-4 bg-green-900/20 rounded-xl border border-green-500/30">
<div class="font-bold text-green-300 mb-3">Agent-native product monorepo</div>
<div class="space-y-2 text-gray-300">
<div>• one PR for the whole change</div>
<div>• one CI graph with affected analysis</div>
<div>• one review conversation around the outcome</div>
<div>• one deploy path and one rollback path</div>
</div>
</div>
</div>

<div class="mt-6 grid grid-cols-3 gap-4 text-xs">
<div class="p-3 bg-cyan-900/20 rounded border border-cyan-500/20">
<div class="text-cyan-300 font-semibold">Boundary enforcement</div>
<div class="opacity-80">Nx, Bazel, or similar tools turn architecture into code</div>
</div>
<div class="p-3 bg-blue-900/20 rounded border border-blue-500/20">
<div class="text-blue-300 font-semibold">Affected analysis</div>
<div class="opacity-80">Only test what changed and downstream dependents</div>
</div>
<div class="p-3 bg-indigo-900/20 rounded border border-indigo-500/20">
<div class="text-indigo-300 font-semibold">Hermetic builds</div>
<div class="opacity-80">Deterministic signals matter more when agents produce constantly</div>
</div>
</div>

---

# Enforced Boundaries Beat Suggested Boundaries

<div class="grid grid-cols-2 gap-6 mt-4 text-sm">
<div class="p-4 bg-amber-900/20 rounded-xl border border-amber-500/30">
<div class="font-bold text-amber-300 mb-2">Suggested boundary</div>
<pre class="text-xs bg-black/30 p-3 rounded text-left whitespace-pre-wrap">// @internal - do not import from payment into marketing</pre>
<div class="mt-3 text-gray-300">Humans may remember. Agents will simply attempt the import and keep going until something enforces reality.</div>
</div>
<div class="p-4 bg-emerald-900/20 rounded-xl border border-emerald-500/30">
<div class="font-bold text-emerald-300 mb-2">Enforced boundary</div>
<pre class="text-xs bg-black/30 p-3 rounded text-left whitespace-pre-wrap">{
  "sourceTag": "scope:payment",
  "onlyDependOnLibsWithTags": ["scope:shared", "scope:payment"]
}</pre>
<div class="mt-3 text-gray-300">Now the build rejects invalid imports immediately. Agents learn by constraint, not by reading comments.</div>
</div>
</div>

<div class="mt-6 p-4 bg-gradient-to-r from-cyan-500/10 to-emerald-500/10 rounded-xl border border-cyan-500/30 text-center">
<div class="text-lg font-semibold text-cyan-300">Architecture that is not executable becomes optional under agent pressure.</div>
</div>

---

# The Coordination Tax: One Realistic Before / After

<div class="grid grid-cols-2 gap-6 mt-4 text-sm">
<div class="p-4 bg-red-900/20 rounded-xl border border-red-500/30">
<div class="font-bold text-red-300 mb-3">Before</div>
<div class="space-y-2 text-gray-300">
<div>Feature touches 3 repos</div>
<div>45 minute CI in each repo</div>
<div>Review in sequence, not in parallel</div>
<div>Contract mismatch discovered late</div>
<div>Deploy ordering becomes a coordination meeting</div>
</div>
</div>
<div class="p-4 bg-green-900/20 rounded-xl border border-green-500/30">
<div class="font-bold text-green-300 mb-3">After</div>
<div class="space-y-2 text-gray-300">
<div>One atomic PR across all modules</div>
<div>8 minute affected-only CI</div>
<div>20 minute outcome review</div>
<div>One deployment path</div>
<div>Rollback is a single motion</div>
</div>
</div>
</div>

<div class="mt-6 grid grid-cols-3 gap-4 text-center">
<div class="p-3 bg-gradient-to-br from-cyan-900/30 to-cyan-800/20 rounded-lg border border-cyan-500/30">
<div class="text-cyan-400 font-bold text-xl">3-5 days → 4-6 hours</div>
<div class="text-xs opacity-80">Time to production</div>
</div>
<div class="p-3 bg-gradient-to-br from-blue-900/30 to-blue-800/20 rounded-lg border border-blue-500/30">
<div class="text-blue-400 font-bold text-xl">60 min → 8 min</div>
<div class="text-xs opacity-80">CI on affected paths</div>
</div>
<div class="p-3 bg-gradient-to-br from-indigo-900/30 to-indigo-800/20 rounded-lg border border-indigo-500/30">
<div class="text-indigo-400 font-bold text-xl">40% → 5%</div>
<div class="text-xs opacity-80">Developer coordination time</div>
</div>
</div>

---
layout: center
name: part2
---

<div class="text-center mb-6">
<div class="text-5xl mb-4">📋</div>
<h1 class="!text-4xl bg-gradient-to-r from-blue-400 to-indigo-400 bg-clip-text text-transparent">Part 2: PR Workflows</h1>
<p class="text-xl opacity-80 mt-2">Governance has to move up-stack</p>
</div>
<div class="p-5 bg-gradient-to-r from-blue-500/10 to-indigo-500/10 rounded-xl border border-blue-500/30 mb-5 text-center max-w-3xl mx-auto">
<div class="text-lg">Level 5 volume fails when teams keep using Level 3 review habits.</div>
</div>

---

# The Breakpoint: Level 5 Volume vs. Level 3 Review Habits

<div class="grid grid-cols-2 gap-6 mt-4 text-sm">
<div class="p-4 bg-blue-900/20 rounded-xl border border-blue-500/30">
<div class="font-bold text-blue-300 mb-3">Level 3 review assumptions</div>
<div class="space-y-2 text-gray-300">
<div>• 50-200 line changes</div>
<div>• line-by-line scrutiny</div>
<div>• synchronous back-and-forth</div>
<div>• trust through detailed inspection</div>
</div>
</div>
<div class="p-4 bg-indigo-900/20 rounded-xl border border-indigo-500/30">
<div class="font-bold text-indigo-300 mb-3">Level 5 reality</div>
<div class="space-y-2 text-gray-300">
<div>• 500-2000 line feature payloads</div>
<div>• 15 minutes from intent to PR</div>
<div>• 10-15 PRs/day is realistic</div>
<div>• humans govern outcomes, not every line</div>
</div>
</div>
</div>

<div class="mt-6 grid grid-cols-3 gap-4 text-center">
<div class="p-3 bg-red-900/20 rounded-lg border border-red-500/30">
<div class="text-red-400 font-bold text-xl">300 lines/day</div>
<div class="text-xs opacity-80">Human review training</div>
</div>
<div class="p-3 bg-amber-900/20 rounded-lg border border-amber-500/30">
<div class="text-amber-400 font-bold text-xl">15,000 lines/day</div>
<div class="text-xs opacity-80">Potential agent output</div>
</div>
<div class="p-3 bg-green-900/20 rounded-lg border border-green-500/30">
<div class="text-green-400 font-bold text-xl">50x</div>
<div class="text-xs opacity-80">Why the bottleneck becomes governance</div>
</div>
</div>

---

# Intent-Based PRs: Humans Review the Contract

<div class="grid grid-cols-2 gap-6 mt-4 text-xs">
<div class="p-4 bg-gradient-to-br from-blue-900/30 to-indigo-900/30 rounded-xl border border-blue-500/30">
<div class="font-bold text-blue-300 mb-3">Intent packet</div>
<div class="text-left bg-black/30 p-3 rounded space-y-3">
<div>
<div class="text-blue-200 font-semibold uppercase tracking-wide text-[11px] mb-1">Feature Intent</div>
<div class="text-gray-200">• Add password reset flow</div>
<div class="text-gray-200">• Email link expires in 1 hour</div>
<div class="text-gray-200">• Rate limit: 3 attempts/hour</div>
<div class="text-gray-200">• Audit every reset request</div>
</div>
<div>
<div class="text-blue-200 font-semibold uppercase tracking-wide text-[11px] mb-1">Constraints</div>
<div class="text-gray-200">• Use existing email service</div>
<div class="text-gray-200">• Follow OWASP guidance</div>
<div class="text-gray-200">• No auth middleware rewrite</div>
</div>
<div>
<div class="text-blue-200 font-semibold uppercase tracking-wide text-[11px] mb-1">Acceptance Criteria</div>
<div class="text-gray-200">• Email within 2 minutes</div>
<div class="text-gray-200">• Link expires correctly</div>
<div class="text-gray-200">• Rate limiting enforced</div>
<div class="text-gray-200">• Audit trail exists</div>
</div>
</div>
</div>
<div class="p-4 bg-gradient-to-br from-indigo-900/30 to-purple-900/30 rounded-xl border border-indigo-500/30">
<div class="font-bold text-indigo-300 mb-3">What humans now review</div>
<div class="space-y-2 text-gray-300 text-sm">
<div>• does the implementation match intent?</div>
<div>• are edge cases covered?</div>
<div>• do the policy checks and evidence bundle clear?</div>
<div>• should we approve, or should intent be clarified?</div>
</div>
<div class="mt-4 p-3 bg-green-900/20 rounded border border-green-500/20">
<div class="text-green-300 font-semibold">20 minutes vs. 3 hours</div>
<div class="text-xs opacity-80">Read intent, inspect evidence, validate outcomes</div>
</div>
</div>
</div>

---

# Governance Pyramid: 90% Automated, 10% Human Judgment

<div class="grid grid-cols-2 gap-6 mt-4 text-sm">
<div class="p-4 bg-gradient-to-br from-indigo-900/30 to-purple-900/30 rounded-xl border border-indigo-500/30">
<div class="font-bold text-indigo-300 mb-3">Automated governance</div>
<div class="space-y-2 text-gray-300">
<div>• security scanning</div>
<div>• dependency audit</div>
<div>• architecture boundaries</div>
<div>• coverage and performance budgets</div>
<div>• compliance rules and attestations</div>
</div>
</div>
<div class="p-4 bg-gradient-to-br from-purple-900/30 to-pink-900/30 rounded-xl border border-purple-500/30">
<div class="font-bold text-purple-300 mb-3">Human governance</div>
<div class="space-y-2 text-gray-300">
<div>• intent validation</div>
<div>• exception handling</div>
<div>• high-risk security decisions</div>
<div>• architectural fit and novelty</div>
</div>
</div>
</div>

<div class="mt-6 p-4 bg-gradient-to-r from-blue-600/30 to-purple-600/30 rounded-xl border border-blue-500/30 text-center">
<div class="text-lg font-semibold text-white">Scarcity moves from writing code to manufacturing trust.</div>
<div class="text-sm opacity-80 mt-1">That is the economic shift behind Level 5 delivery.</div>
</div>

---
layout: center
name: part3
---

<div class="text-center mb-6">
<div class="text-5xl mb-4">🏭</div>
<h1 class="!text-4xl bg-gradient-to-r from-indigo-400 to-purple-400 bg-clip-text text-transparent">Part 3: Trust Manufacturing</h1>
<p class="text-xl opacity-80 mt-2">CI becomes the factory that produces ship confidence</p>
</div>
<div class="p-5 bg-gradient-to-r from-indigo-500/10 to-purple-500/10 rounded-xl border border-indigo-500/30 mb-5 text-center max-w-3xl mx-auto">
<div class="text-lg">The point of CI is no longer “did tests pass?” It is “do we have enough evidence to trust this change?”</div>
</div>

---

# The 10-Minute Rule

<div class="grid grid-cols-2 gap-6 mt-4 text-sm">
<div class="p-4 bg-red-900/20 rounded-xl border border-red-500/30">
<div class="font-bold text-red-300 mb-3">Slow CI</div>
<div class="space-y-2 text-gray-300">
<div>• 30-60 minute PR checks</div>
<div>• agents sit idle waiting for signals</div>
<div>• queues stack when volume rises</div>
<div>• teams start ignoring failed feedback loops</div>
</div>
</div>
<div class="p-4 bg-green-900/20 rounded-xl border border-green-500/30">
<div class="font-bold text-green-300 mb-3">Fast CI</div>
<div class="space-y-2 text-gray-300">
<div>• less than 10 minute PR checks</div>
<div>• affected-only execution</div>
<div>• fast retries with deterministic cache hits</div>
<div>• agents stay productive instead of blocked</div>
</div>
</div>
</div>

<div class="mt-6 grid grid-cols-3 gap-4 text-center">
<div class="p-3 bg-indigo-900/20 rounded-lg border border-indigo-500/30">
<div class="text-indigo-400 font-bold text-xl">80 min → 8 min</div>
<div class="text-xs opacity-80">Average CI time</div>
</div>
<div class="p-3 bg-purple-900/20 rounded-lg border border-purple-500/30">
<div class="text-purple-400 font-bold text-xl">50% → 95%</div>
<div class="text-xs opacity-80">Agent productive time</div>
</div>
<div class="p-3 bg-pink-900/20 rounded-lg border border-pink-500/30">
<div class="text-pink-400 font-bold text-xl">2-3 → 10-15</div>
<div class="text-xs opacity-80">Features/day per agent</div>
</div>
</div>

---

# How to Build a Trust Factory

<div class="grid grid-cols-2 gap-6 mt-4 text-sm">
<div class="space-y-3">
<div class="p-3 bg-indigo-900/20 rounded-lg border border-indigo-500/20">
<div class="font-bold text-indigo-300">1. Affected analysis</div>
<div class="text-gray-300">Test only the changed area and downstream dependents.</div>
</div>
<div class="p-3 bg-purple-900/20 rounded-lg border border-purple-500/20">
<div class="font-bold text-purple-300">2. Caching that actually hits</div>
<div class="text-gray-300">Dependency, build, and test cache keys must match your invalidation story.</div>
</div>
<div class="p-3 bg-pink-900/20 rounded-lg border border-pink-500/20">
<div class="font-bold text-pink-300">3. Parallel checks</div>
<div class="text-gray-300">Security, quality, performance, and compliance should not queue behind each other.</div>
</div>
</div>
<div class="space-y-3">
<div class="p-3 bg-blue-900/20 rounded-lg border border-blue-500/20">
<div class="font-bold text-blue-300">4. Context-aware validation</div>
<div class="text-gray-300">Use agents for judgment-heavy checks where regexes are not enough.</div>
</div>
<div class="p-3 bg-cyan-900/20 rounded-lg border border-cyan-500/20">
<div class="font-bold text-cyan-300">5. Attestations</div>
<div class="text-gray-300">Produce auditable, replayable evidence for regulated environments.</div>
</div>
<div class="p-3 bg-emerald-900/20 rounded-lg border border-emerald-500/20">
<div class="font-bold text-emerald-300">6. Rollback readiness</div>
<div class="text-gray-300">Trust rises when recovery is fast, rehearsed, and boring.</div>
</div>
</div>
</div>

---

# Zero-Flake Tolerance Restores Trust

<div class="grid grid-cols-2 gap-6 mt-4 text-sm">
<div class="p-4 bg-red-900/20 rounded-xl border border-red-500/30">
<div class="font-bold text-red-300 mb-3">When teams tolerate flakes</div>
<div class="space-y-2 text-gray-300">
<div>• green builds stop meaning “safe”</div>
<div>• reruns become routine</div>
<div>• humans distrust automation</div>
<div>• agent throughput is throttled by uncertainty</div>
</div>
</div>
<div class="p-4 bg-green-900/20 rounded-xl border border-green-500/30">
<div class="font-bold text-green-300 mb-3">When teams quarantine flakes fast</div>
<div class="space-y-2 text-gray-300">
<div>• first flake triggers action</div>
<div>• fix or delete within days</div>
<div>• green builds regain credibility</div>
<div>• policy gates become dependable</div>
</div>
</div>
</div>

<div class="mt-6 grid grid-cols-3 gap-4 text-center">
<div class="p-3 bg-gradient-to-br from-red-900/30 to-red-800/20 rounded-lg border border-red-500/30">
<div class="text-red-400 font-bold text-xl">18% → 1.2%</div>
<div class="text-xs opacity-80">Flake rate</div>
</div>
<div class="p-3 bg-gradient-to-br from-indigo-900/30 to-indigo-800/20 rounded-lg border border-indigo-500/30">
<div class="text-indigo-400 font-bold text-xl">35% → 8%</div>
<div class="text-xs opacity-80">Agent idle time</div>
</div>
<div class="p-3 bg-gradient-to-br from-emerald-900/30 to-emerald-800/20 rounded-lg border border-emerald-500/30">
<div class="text-emerald-400 font-bold text-xl">45/week → 2/week</div>
<div class="text-xs opacity-80">Manual PR reruns</div>
</div>
</div>

---
layout: center
name: part4
---

<div class="text-center mb-6">
<div class="text-5xl mb-4">🚀</div>
<h1 class="!text-4xl bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">Part 4: Implementation Roadmap</h1>
<p class="text-xl opacity-80 mt-2">Progress through the maturity model on purpose</p>
</div>
<div class="p-5 bg-gradient-to-r from-purple-500/10 to-pink-500/10 rounded-xl border border-purple-500/30 mb-5 text-center max-w-3xl mx-auto">
<div class="text-lg">Do not jump straight to autonomy. Standardize first, optimize second, operate autonomously third.</div>
</div>

---

# A Practical Progression: Level 3 → Level 4 → Level 5

<div class="grid grid-cols-3 gap-4 mt-4 text-sm">
<div class="p-4 bg-blue-900/20 rounded-xl border border-blue-500/30">
<div class="text-blue-300 font-bold text-lg mb-2">Phase 1</div>
<div class="font-semibold mb-3">Reach Level 3: Standardized</div>
<div class="space-y-2 text-gray-300 text-xs">
<div>• set up CI/CD and branch protection</div>
<div>• establish boundary enforcement</div>
<div>• measure PR check time and flake rate</div>
<div>• create auditable review paths</div>
</div>
</div>
<div class="p-4 bg-indigo-900/20 rounded-xl border border-indigo-500/30">
<div class="text-indigo-300 font-bold text-lg mb-2">Phase 2</div>
<div class="font-semibold mb-3">Reach Level 4: Optimized</div>
<div class="space-y-2 text-gray-300 text-xs">
<div>• add MCP servers, custom agents, skills</div>
<div>• automate 80-90% of routine checks</div>
<div>• adopt evidence-bundle workflows</div>
<div>• use agent validation where rules alone fail</div>
</div>
</div>
<div class="p-4 bg-green-900/20 rounded-xl border border-green-500/30">
<div class="text-green-300 font-bold text-lg mb-2">Phase 3</div>
<div class="font-semibold mb-3">Operate at Level 5: Autonomous</div>
<div class="space-y-2 text-gray-300 text-xs">
<div>• target 10-15 features/day safely</div>
<div>• keep PR checks under 10 minutes</div>
<div>• train reviewers for outcome validation</div>
<div>• use humans for exceptions and strategic judgment</div>
</div>
</div>
</div>

<div class="mt-6 p-4 bg-gradient-to-r from-green-500/10 to-emerald-500/10 rounded-xl border border-green-500/30 text-center">
<div class="text-lg font-semibold text-green-300">Autonomous delivery is not a shortcut around maturity. It is the compounding result of maturity.</div>
</div>

---

# 📚 References

<div class="grid grid-cols-2 gap-4 mt-6 text-sm">
<div class="p-4 bg-gradient-to-br from-cyan-900/30 to-blue-900/30 rounded-lg border border-cyan-500/30">
<div class="font-semibold mb-2">AgentRC</div>
<a href="https://github.com/microsoft/agentrc" class="text-cyan-400 opacity-80 hover:opacity-100 break-all">github.com/microsoft/agentrc</a>
<div class="text-gray-400 mt-2 text-xs">Measure, generate, and maintain repository AI readiness</div>
</div>
<div class="p-4 bg-gradient-to-br from-blue-900/30 to-indigo-900/30 rounded-lg border border-blue-500/30">
<div class="font-semibold mb-2">AgentRC Concepts</div>
<a href="https://github.com/microsoft/agentrc/blob/main/docs/concepts.md" class="text-blue-400 opacity-80 hover:opacity-100 break-all">github.com/microsoft/agentrc/.../docs/concepts.md</a>
<div class="text-gray-400 mt-2 text-xs">Level 1-5 maturity model and readiness pillars</div>
</div>
<div class="p-4 bg-gradient-to-br from-indigo-900/30 to-purple-900/30 rounded-lg border border-indigo-500/30">
<div class="font-semibold mb-2">GitHub Actions</div>
<a href="https://docs.github.com/en/actions" class="text-indigo-400 opacity-80 hover:opacity-100 break-all">docs.github.com/en/actions</a>
<div class="text-gray-400 mt-2 text-xs">Workflow automation, caching, and CI orchestration</div>
</div>
<div class="p-4 bg-gradient-to-br from-purple-900/30 to-pink-900/30 rounded-lg border border-purple-500/30">
<div class="font-semibold mb-2">Nx</div>
<a href="https://nx.dev/" class="text-purple-400 opacity-80 hover:opacity-100 break-all">nx.dev</a>
<div class="text-gray-400 mt-2 text-xs">Monorepo boundaries, affected analysis, and caching</div>
</div>
<div class="p-4 bg-gradient-to-br from-pink-900/30 to-rose-900/30 rounded-lg border border-pink-500/30 col-span-2">
<div class="font-semibold mb-2">SLSA</div>
<a href="https://slsa.dev/" class="text-pink-400 opacity-80 hover:opacity-100 break-all">slsa.dev</a>
<div class="text-gray-400 mt-2 text-xs">Supply chain attestation and trust evidence patterns for regulated delivery</div>
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
<span class="px-6 py-2 bg-gradient-to-r from-cyan-600/80 to-blue-600/80 rounded-full text-white text-lg font-medium shadow-lg shadow-cyan-500/25">Agentic SDLC: Level 5 Infrastructure for AI Velocity</span>
</div>
<div class="mt-8 grid grid-cols-3 gap-4 text-sm max-w-3xl mx-auto relative z-10">
<div class="p-3 bg-gradient-to-br from-cyan-900/30 to-cyan-800/20 rounded-lg border border-cyan-500/30">
<div class="text-cyan-400 font-bold text-lg">Levels 1-5</div>
<div class="opacity-80 text-xs">A maturity model for automation, speed, and safety</div>
</div>
<div class="p-3 bg-gradient-to-br from-blue-900/30 to-blue-800/20 rounded-lg border border-blue-500/30">
<div class="text-blue-400 font-bold text-lg">&lt;10 min</div>
<div class="opacity-80 text-xs">PR checks keep agents productive and trust current</div>
</div>
<div class="p-3 bg-gradient-to-br from-indigo-900/30 to-indigo-800/20 rounded-lg border border-indigo-500/30">
<div class="text-indigo-400 font-bold text-lg">10-15/day</div>
<div class="opacity-80 text-xs">The throughput target when the system is truly ready</div>
</div>
</div>
<div class="mt-6 text-sm opacity-60 relative z-10">Questions? Let's discuss the path from standardized engineering to autonomous delivery.</div>
<div class="mt-4 w-32 h-1 bg-gradient-to-r from-transparent via-cyan-400 to-transparent rounded-full relative z-10"></div>
</div>
