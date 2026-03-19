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
title: Agentic SDLC - Level 5 Infrastructure for AI Velocity
module: tech-talks/agentic-sdlc
mdc: true
status: active
updated: 2026-03-19
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

<div class="abs-br m-6 flex gap-2">
<span class="text-sm opacity-50">Tech Talk · 90 minutes</span>
</div>

---
layout: center
---

# 🔓 The Core Question

<div class="p-6 bg-gradient-to-br from-cyan-900/30 to-blue-900/30 rounded-xl border border-cyan-500/30 max-w-4xl mx-auto">
<div class="text-2xl font-bold text-cyan-300 mb-4">
"How do I rewire repositories, PR workflows, and CI/CD to scale from 2-3 features/week to 10-15 features/day with AI agents?"
</div>
</div>

<div class="mt-8 grid grid-cols-3 gap-4 text-sm">
<div class="p-4 bg-gradient-to-br from-amber-900/30 to-orange-900/30 rounded-lg border border-amber-500/30">
<div class="text-xl mb-2">📦</div>
<div class="font-semibold text-amber-300">Code Volume Explosion</div>
<div class="text-xs opacity-80 mt-1">500-2000 lines per feature in 15 minutes, 10-15x human output</div>
</div>
<div class="p-4 bg-gradient-to-br from-orange-900/30 to-red-900/30 rounded-lg border border-orange-500/30">
<div class="text-xl mb-2">🚧</div>
<div class="font-semibold text-orange-300">Review Capacity Bottleneck</div>
<div class="text-xs opacity-80 mt-1">Humans can't review 15,000 lines/day at 300 lines/day detail level</div>
</div>
<div class="p-4 bg-gradient-to-br from-red-900/30 to-purple-900/30 rounded-lg border border-red-500/30">
<div class="text-xl mb-2">⏱️</div>
<div class="font-semibold text-red-300">CI Becomes Critical Path</div>
<div class="text-xs opacity-80 mt-1">60-minute CI means agents idle 80% of time; test flake blocks 15 PRs/day</div>
</div>
</div>

---
layout: center
---

# 📖 Table of Contents

<div class="grid grid-cols-2 gap-6 mt-6 max-w-4xl mx-auto">
<div @click="$nav.go(5)" class="cursor-pointer group">
<div class="p-5 bg-gradient-to-br from-cyan-900/40 to-blue-900/40 rounded-xl border-2 border-cyan-500/50 hover:border-cyan-400 hover:scale-105 transition-all duration-300 shadow-lg shadow-cyan-500/10">
<div class="text-3xl mb-2">📐</div>
<div class="text-lg font-bold bg-gradient-to-r from-cyan-300 to-blue-300 bg-clip-text text-transparent">AgentRC Maturity Model</div>
<div class="text-sm text-gray-300 mt-1">5 levels from functional to autonomous</div>
<div class="text-xs text-cyan-400/70 mt-2">What each level unlocks for speed, automation, and safety</div>
</div>
</div>
<div @click="$nav.go(7)" class="cursor-pointer group">
<div class="p-5 bg-gradient-to-br from-blue-900/40 to-indigo-900/40 rounded-xl border-2 border-blue-500/50 hover:border-blue-400 hover:scale-105 transition-all duration-300 shadow-lg shadow-blue-500/10">
<div class="text-3xl mb-2">🏗️</div>
<div class="text-lg font-bold bg-gradient-to-r from-blue-300 to-indigo-300 bg-clip-text text-transparent">Repository Topology</div>
<div class="text-sm text-gray-300 mt-1">Agent-native monorepo patterns</div>
<div class="text-xs text-blue-400/70 mt-2">Eliminate coordination overhead, enable atomic changes</div>
</div>
</div>
<div @click="$nav.go(11)" class="cursor-pointer group">
<div class="p-5 bg-gradient-to-br from-indigo-900/40 to-purple-900/40 rounded-xl border-2 border-indigo-500/50 hover:border-indigo-400 hover:scale-105 transition-all duration-300 shadow-lg shadow-indigo-500/10">
<div class="text-3xl mb-2">📋</div>
<div class="text-lg font-bold bg-gradient-to-r from-indigo-300 to-purple-300 bg-clip-text text-transparent">PR Workflows</div>
<div class="text-sm text-gray-300 mt-1">Outcome validation at scale</div>
<div class="text-xs text-indigo-400/70 mt-2">From line-by-line review to evidence-based governance</div>
</div>
</div>
<div @click="$nav.go(15)" class="cursor-pointer group">
<div class="p-5 bg-gradient-to-br from-purple-900/40 to-pink-900/40 rounded-xl border-2 border-purple-500/50 hover:border-purple-400 hover:scale-105 transition-all duration-300 shadow-lg shadow-purple-500/10">
<div class="text-3xl mb-2">🏭</div>
<div class="text-lg font-bold bg-gradient-to-r from-purple-300 to-pink-300 bg-clip-text text-transparent">Trust Manufacturing</div>
<div class="text-sm text-gray-300 mt-1">CI as a trust factory</div>
<div class="text-xs text-purple-400/70 mt-2">&lt;10 min PR checks, zero-flake tolerance, attestations</div>
</div>
</div>
</div>

<div class="mt-6 text-center text-sm opacity-60">Click any section to jump directly there</div>

---

# The AgentRC Levels: What Changes at Each Step

<div class="space-y-2 text-xs">
<div class="p-3 bg-gradient-to-br from-gray-800/40 to-gray-900/40 rounded-lg border border-gray-600/30">
<div class="flex items-center gap-3">
<div class="text-lg font-bold text-gray-400">L1</div>
<div class="flex-1">
<div class="font-semibold text-gray-300">Functional</div>
<div class="text-gray-400">Baseline build/test signals exist — scripts run reliably</div>
</div>
</div>
</div>

<div class="p-3 bg-gradient-to-br from-gray-800/40 to-gray-900/40 rounded-lg border border-gray-600/30">
<div class="flex items-center gap-3">
<div class="text-lg font-bold text-gray-400">L2</div>
<div class="flex-1">
<div class="font-semibold text-gray-300">Documented</div>
<div class="text-gray-400">Explicit context — agents follow documented conventions, fewer unforced errors</div>
</div>
</div>
</div>

<div class="p-3 bg-gradient-to-br from-blue-900/40 to-blue-800/40 rounded-lg border border-blue-500/30">
<div class="flex items-center gap-3">
<div class="text-lg font-bold text-blue-300">L3</div>
<div class="flex-1">
<div class="font-semibold text-blue-300">Standardized</div>
<div class="text-gray-300">CI/CD, policies, CODEOWNERS — repeatable automation and auditable review paths</div>
</div>
</div>
</div>

<div class="p-3 bg-gradient-to-br from-cyan-900/40 to-cyan-800/40 rounded-lg border border-cyan-500/30">
<div class="flex items-center gap-3">
<div class="text-lg font-bold text-cyan-300">L4</div>
<div class="flex-1">
<div class="font-semibold text-cyan-300">Optimized</div>
<div class="text-gray-300">MCP servers, custom agents, AI skills — multi-step workflows with tools and narrow risk</div>
</div>
</div>
</div>

<div class="p-3 bg-gradient-to-br from-green-900/40 to-green-800/40 rounded-lg border border-green-500/30">
<div class="flex items-center gap-3">
<div class="text-lg font-bold text-green-300">L5</div>
<div class="flex-1">
<div class="font-semibold text-green-300">Autonomous</div>
<div class="text-gray-300">Agents as primary producers — end-to-end delivery with minimal oversight, machine-paced</div>
</div>
</div>
</div>
</div>

<div class="mt-4 p-4 bg-gradient-to-r from-green-500/20 to-emerald-500/20 rounded-xl border border-green-500/30 text-center">
<div class="text-sm font-semibold text-green-300">This talk is about reaching Level 5, but it only works if Levels 1-4 are already doing their job</div>
</div>

---
layout: center
name: agentrc
---

<div class="text-center mb-6">
<div class="text-5xl mb-4">📐</div>
<h1 class="!text-4xl bg-gradient-to-r from-cyan-400 to-blue-400 bg-clip-text text-transparent">The Level 5 Breakpoint</h1>
<p class="text-xl opacity-80 mt-2">When infrastructure fails at autonomous delivery velocity</p>
</div>

<div class="p-5 bg-gradient-to-r from-cyan-500/10 to-blue-500/10 rounded-xl border border-cyan-500/30 mb-5 text-center max-w-3xl mx-auto">
<div class="text-lg">PR systems that feel fine through Levels 1-4 break when you try to operate at <span class="text-cyan-300 font-bold">Level 5 volume</span> using <span class="text-red-300 font-bold">Level 3 review habits</span></div>
</div>

<div class="grid grid-cols-2 gap-6 mt-6">
<div class="p-4 bg-gradient-to-br from-red-900/30 to-red-800/20 rounded-xl border-2 border-red-500/30">
<div class="text-center mb-3">
<div class="text-2xl">⚠️</div>
<div class="font-bold text-red-300">Level 3 Assumptions</div>
</div>
<div class="space-y-2 text-sm">
<div class="p-2 bg-red-900/30 rounded">50-200 line changes, human-readable</div>
<div class="p-2 bg-red-900/30 rounded">Line-by-line scrutiny, 30-min reviews</div>
<div class="p-2 bg-red-900/30 rounded">Synchronous collaboration forums</div>
<div class="p-2 bg-red-900/30 rounded">Trust through detailed inspection</div>
</div>
</div>
<div class="p-4 bg-gradient-to-br from-emerald-900/30 to-emerald-800/20 rounded-xl border-2 border-emerald-500/30">
<div class="text-center mb-3">
<div class="text-2xl">✨</div>
<div class="font-bold text-emerald-300">Level 5 Reality</div>
</div>
<div class="space-y-2 text-sm">
<div class="p-2 bg-emerald-900/30 rounded">500-2000 line payloads, feature-scale</div>
<div class="p-2 bg-emerald-900/30 rounded">Intent-driven, not implementation detail</div>
<div class="p-2 bg-emerald-900/30 rounded">Machine velocity: 15 PRs/day, 24/7</div>
<div class="p-2 bg-emerald-900/30 rounded">Trust through automated evidence</div>
</div>
</div>
</div>

---
layout: center
name: topology
---

<div class="text-center mb-6">
<div class="text-5xl mb-4">🏗️</div>
<h1 class="!text-4xl bg-gradient-to-r from-blue-400 to-indigo-400 bg-clip-text text-transparent">Repository Topology</h1>
<p class="text-xl opacity-80 mt-2">Rewiring code boundaries for agent-native delivery</p>
</div>

<div class="p-5 bg-gradient-to-r from-blue-500/10 to-indigo-500/10 rounded-xl border border-blue-500/30 mb-5 text-center max-w-3xl mx-auto">
<div class="text-lg">When agents touch 2+ repos for >30% of features, you pay exponential coordination costs</div>
</div>

---

# Monorepo: Default for Agent Velocity

<div class="grid grid-cols-2 gap-6">
<div class="p-4 bg-gradient-to-br from-green-900/30 to-green-800/20 rounded-xl border-2 border-green-500/30">
<div class="text-center mb-3">
<div class="text-2xl">✅</div>
<div class="font-bold text-green-300">Monorepo Benefits</div>
</div>
<div class="space-y-2 text-sm">
<div class="p-2 bg-green-900/30 rounded"><span class="font-bold text-green-400">Atomic changes:</span> API + 7 call sites in 1 PR, not 8</div>
<div class="p-2 bg-green-900/30 rounded"><span class="font-bold text-green-400">Agent navigation:</span> grep instead of GitHub search</div>
<div class="p-2 bg-green-900/30 rounded"><span class="font-bold text-green-400">Shared patterns:</span> Local imports, no "which version?"</div>
<div class="p-2 bg-green-900/30 rounded"><span class="font-bold text-green-400">Unified CI:</span> Consistent standards, shared cache</div>
</div>
</div>
<div class="p-4 bg-gradient-to-br from-orange-900/30 to-orange-800/20 rounded-xl border-2 border-orange-500/30">
<div class="text-center mb-3">
<div class="text-2xl">⚡</div>
<div class="font-bold text-orange-300">Multi-Repo: Only When Needed</div>
</div>
<div class="space-y-2 text-sm">
<div class="p-2 bg-orange-900/30 rounded">Hard access boundaries (PCI-regulated payment)</div>
<div class="p-2 bg-orange-900/30 rounded">Independent lifecycles (mobile vs web, truly separate)</div>
<div class="p-2 bg-orange-900/30 rounded">Regulatory mandates (physical separation required)</div>
<div class="p-2 bg-orange-900/30 rounded">Organizational constraints (acquired company, temporary)</div>
</div>
</div>
</div>

<div class="mt-4 p-4 bg-gradient-to-r from-cyan-600/80 to-blue-600/80 rounded-lg text-center">
<span class="text-white font-bold">🎯 Decision Rule: If agents touch >1 repo for >30% of features → consolidate to monorepo</span>
</div>

---

# War Story: The 6-Hour Feature

<div class="grid grid-cols-2 gap-6">
<div class="p-4 bg-gradient-to-br from-red-900/30 to-red-800/20 rounded-xl border-2 border-red-500/30">
<div class="text-center mb-3">
<div class="text-2xl">❌</div>
<div class="font-bold text-red-300">Before: 18 Microservice Repos</div>
</div>
<div class="space-y-2 text-xs">
<div class="p-2 bg-red-900/30 rounded"><span class="font-bold text-red-400">Day 1:</span> Open PR in repo A, wait CI (45 min), wait review (4 hours)</div>
<div class="p-2 bg-red-900/30 rounded"><span class="font-bold text-red-400">Day 2:</span> Open PR in repo B, discover contract mismatch, return to repo A</div>
<div class="p-2 bg-red-900/30 rounded"><span class="font-bold text-red-400">Day 3:</span> Coordinate deploy order, staging fails, debug across repos</div>
</div>
<div class="mt-3 text-center text-sm font-bold text-red-300">6 hours agent work · 3 days coordination · 2 rollbacks</div>
</div>
<div class="p-4 bg-gradient-to-br from-emerald-900/30 to-emerald-800/20 rounded-xl border-2 border-emerald-500/30">
<div class="text-center mb-3">
<div class="text-2xl">✨</div>
<div class="font-bold text-emerald-300">After: Monorepo Migration</div>
</div>
<div class="space-y-2 text-xs">
<div class="p-2 bg-emerald-900/30 rounded"><span class="font-bold text-emerald-400">Single PR:</span> All 3 modules touched atomically in one changeset</div>
<div class="p-2 bg-emerald-900/30 rounded"><span class="font-bold text-emerald-400">Fast CI:</span> Affected analysis tested only changed modules (8 min)</div>
<div class="p-2 bg-emerald-900/30 rounded"><span class="font-bold text-emerald-400">One deploy:</span> Coordinated release, no contract mismatches</div>
</div>
<div class="mt-3 text-center text-sm font-bold text-emerald-300">6 hours agent work · 45 minutes end-to-end · 0 rollbacks</div>
</div>
</div>

<div class="mt-4 p-4 bg-gradient-to-r from-green-500/20 to-emerald-500/20 rounded-xl border border-green-500/30 text-center">
<div class="text-sm font-semibold text-green-300">Result: 3 days → 45 minutes, zero coordination overhead</div>
</div>

---

# Enforced Module Boundaries: Build-Time Failures

<div class="grid grid-cols-2 gap-6">
<div class="p-4 bg-gradient-to-br from-red-900/30 to-red-800/20 rounded-xl border-2 border-red-500/30">
<div class="text-center mb-3">
<div class="text-2xl">❌</div>
<div class="font-bold text-red-300">Suggested (Fails at Level 5)</div>
</div>
<div class="text-xs font-mono text-gray-300 bg-gray-900/50 p-2 rounded mb-2">
// @internal - Don't import this!<br />
export class PaymentProcessor {}
</div>
<div class="text-xs text-gray-400">Agents don't read comments — they follow import patterns they observe</div>
</div>
<div class="p-4 bg-gradient-to-br from-emerald-900/30 to-emerald-800/20 rounded-xl border-2 border-emerald-500/30">
<div class="text-center mb-3">
<div class="text-2xl">✅</div>
<div class="font-bold text-emerald-300">Enforced (Works at Level 5)</div>
</div>
<div class="text-xs font-mono text-gray-300 bg-gray-900/50 p-2 rounded mb-2">
// nx.json boundary enforcement<br />
{<br />
  "sourceTag": "scope:payment",<br />
  "onlyDependOnLibsWithTags": ["scope:shared"]<br />
}
</div>
<div class="text-xs text-gray-400">Build-time failures prevent violations; clear error messages guide corrections</div>
</div>
</div>

<div class="mt-4 space-y-2 text-xs">
<div class="p-2 bg-gray-800 rounded"><span class="text-cyan-400">✓ Architectural decay prevention:</span> Can't create circular dependencies</div>
<div class="p-2 bg-gray-800 rounded"><span class="text-green-400">✓ CI catches violations before merge:</span> Agent learns constraint from build failure</div>
<div class="p-2 bg-gray-800 rounded"><span class="text-blue-400">✓ Documentation via enforcement:</span> Rules ARE the documentation</div>
</div>

---
layout: center
name: pr-workflows
---

<div class="text-center mb-6">
<div class="text-5xl mb-4">📋</div>
<h1 class="!text-4xl bg-gradient-to-r from-indigo-400 to-purple-400 bg-clip-text text-transparent">PR Workflows</h1>
<p class="text-xl opacity-80 mt-2">Scaling governance from line-by-line review to outcome validation</p>
</div>

<div class="p-5 bg-gradient-to-r from-indigo-500/10 to-purple-500/10 rounded-xl border border-indigo-500/30 mb-5 text-center max-w-3xl mx-auto">
<div class="text-lg">Humans trained to review 300 lines/day can't scale to 15,000 lines/day at the same detail level</div>
</div>

---

# The Economic Shift: Where Scarcity Moves

<div class="grid grid-cols-2 gap-6">
<div class="p-4 bg-gradient-to-br from-red-900/30 to-red-800/20 rounded-xl border-2 border-red-500/30">
<div class="text-center mb-3">
<div class="text-2xl">⚠️</div>
<div class="font-bold text-red-300">Level 3 Scarcity</div>
</div>
<div class="space-y-2 text-sm">
<div class="p-2 bg-red-900/30 rounded">Developer time to write code</div>
<div class="p-2 bg-red-900/30 rounded">Code quality (bugs in implementation)</div>
<div class="p-2 bg-red-900/30 rounded">Implementation speed</div>
<div class="p-2 bg-red-900/30 rounded">Review thoroughness</div>
</div>
</div>
<div class="p-4 bg-gradient-to-br from-emerald-900/30 to-emerald-800/20 rounded-xl border-2 border-emerald-500/30">
<div class="text-center mb-3">
<div class="text-2xl">✨</div>
<div class="font-bold text-emerald-300">Level 5 Scarcity</div>
</div>
<div class="space-y-2 text-sm">
<div class="p-2 bg-emerald-900/30 rounded">Governance capacity to review</div>
<div class="p-2 bg-emerald-900/30 rounded">Trust at scale (can we ship this velocity?)</div>
<div class="p-2 bg-emerald-900/30 rounded">Architectural coherence</div>
<div class="p-2 bg-emerald-900/30 rounded">Compliance verification speed</div>
</div>
</div>
</div>

<div class="mt-4 p-4 bg-gradient-to-r from-purple-600/80 to-pink-600/80 rounded-lg text-center">
<span class="text-white font-bold">💡 The Shift: From "can we write it fast enough?" to "can we trust it at this velocity?"</span>
</div>

---

# Intent-Based PRs: Evidence Bundles

<div class="space-y-3 text-sm">
<div class="p-3 bg-gradient-to-br from-blue-900/40 to-blue-800/40 rounded-lg border border-blue-500/30">
<div class="font-bold text-blue-300 mb-2">1. Intent Specification (What Humans Provide)</div>
<div class="text-xs text-gray-300">Feature requirements, constraints, acceptance criteria — goal-level direction, not implementation detail</div>
</div>

<div class="p-3 bg-gradient-to-br from-cyan-900/40 to-cyan-800/40 rounded-lg border border-cyan-500/30">
<div class="font-bold text-cyan-300 mb-2">2. Policy Enforcement (Automated Checks)</div>
<div class="text-xs text-gray-300">Security scan, boundary enforcement, compliance validation — 90% automated, 10% human judgment</div>
</div>

<div class="p-3 bg-gradient-to-br from-purple-900/40 to-purple-800/40 rounded-lg border border-purple-500/30">
<div class="font-bold text-purple-300 mb-2">3. Outcome Validation (Human Review Focus)</div>
<div class="text-xs text-gray-300">Does implementation match intent? Edge cases handled? Feature integrates correctly? NOT "why Map on line 47?"</div>
</div>
</div>

<div class="mt-4 grid grid-cols-2 gap-4">
<div class="p-3 bg-red-900/30 rounded-lg">
<div class="text-sm font-bold text-red-300">Traditional Review</div>
<div class="text-xs text-gray-400">3 hours, 200-line limit, line-by-line scrutiny</div>
</div>
<div class="p-3 bg-green-900/30 rounded-lg">
<div class="text-sm font-bold text-green-300">Intent-Based Review</div>
<div class="text-xs text-gray-400">20 minutes, 2000-line payloads, outcome validation</div>
</div>
</div>

<div class="mt-3 p-3 bg-gradient-to-r from-green-500/20 to-emerald-500/20 rounded-xl border border-green-500/30 text-center">
<div class="text-xs font-semibold text-green-300">Result: 50x review capacity increase — 15,000 lines/day becomes manageable</div>
</div>

---

# The Governance Pyramid

<div class="flex flex-col items-center gap-3 mt-6">
<div class="p-4 bg-gradient-to-r from-blue-600 to-blue-800 rounded-xl shadow-lg text-center max-w-md">
<div class="text-sm font-bold text-white">Human Governance (10%)</div>
<div class="text-xs text-blue-200 mt-1">Strategic decisions · High-risk changes · Architectural fit</div>
</div>

<div class="text-3xl text-gray-500">↓</div>

<div class="p-6 bg-gradient-to-br from-cyan-900/40 to-blue-900/40 rounded-xl border-2 border-cyan-500/50 text-center max-w-2xl">
<div class="text-lg font-bold text-cyan-300 mb-3">Automated Governance (90%)</div>
<div class="grid grid-cols-3 gap-2 text-xs">
<div class="p-2 bg-cyan-900/50 rounded">Security scanning</div>
<div class="p-2 bg-blue-900/50 rounded">Test coverage</div>
<div class="p-2 bg-indigo-900/50 rounded">Performance benchmarks</div>
<div class="p-2 bg-purple-900/50 rounded">Architecture rules</div>
<div class="p-2 bg-pink-900/50 rounded">Compliance checks</div>
<div class="p-2 bg-cyan-900/50 rounded">Dependency audits</div>
</div>
</div>
</div>

<div class="mt-6 grid grid-cols-2 gap-4 text-sm">
<div class="p-3 bg-red-900/30 rounded-lg">
<div class="font-bold text-red-300">Traditional Governance</div>
<div class="text-xs text-gray-400">22 manual gates, 4-7 days PR→merge</div>
</div>
<div class="p-3 bg-green-900/30 rounded-lg">
<div class="font-bold text-green-300">Level 5 Governance</div>
<div class="text-xs text-gray-400">4 human checkpoints, 2-4 hours PR→merge</div>
</div>
</div>

---
layout: center
name: trust-factory
---

<div class="text-center mb-6">
<div class="text-5xl mb-4">🏭</div>
<h1 class="!text-4xl bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">Trust Manufacturing</h1>
<p class="text-xl opacity-80 mt-2">Transforming CI from quality gate to trust evidence production</p>
</div>

<div class="p-5 bg-gradient-to-r from-purple-500/10 to-pink-500/10 rounded-xl border border-purple-500/30 mb-5 text-center max-w-3xl mx-auto">
<div class="text-lg">Agents can write code faster than CI can prove it's safe to ship — trust production becomes the bottleneck</div>
</div>

---

# The 10-Minute Rule: Why Fast CI Matters

<div class="grid grid-cols-2 gap-6">
<div class="p-4 bg-gradient-to-br from-red-900/30 to-red-800/20 rounded-xl border-2 border-red-500/30">
<div class="text-center mb-3">
<div class="text-2xl">⏱️</div>
<div class="font-bold text-red-300">If CI Takes 60 Minutes</div>
</div>
<div class="space-y-2 text-xs">
<div class="p-2 bg-red-900/30 rounded">Generate code (5 min) → Wait CI (60 min) → Fix → Repeat</div>
<div class="p-2 bg-red-900/30 rounded">4 iterations = 4 hours total</div>
<div class="p-2 bg-red-900/30 rounded">Agent sits idle 80% of the time</div>
</div>
<div class="mt-3 text-center text-sm font-bold text-red-300">Effective velocity: 2-3 features/day</div>
</div>
<div class="p-4 bg-gradient-to-br from-emerald-900/30 to-emerald-800/20 rounded-xl border-2 border-emerald-500/30">
<div class="text-center mb-3">
<div class="text-2xl">⚡</div>
<div class="font-bold text-emerald-300">If CI Takes 8 Minutes</div>
</div>
<div class="space-y-2 text-xs">
<div class="p-2 bg-emerald-900/30 rounded">Generate code (5 min) → Wait CI (8 min) → Fix → Repeat</div>
<div class="p-2 bg-emerald-900/30 rounded">4 iterations = 52 minutes total</div>
<div class="p-2 bg-emerald-900/30 rounded">Agent productive 95% of the time</div>
</div>
<div class="mt-3 text-center text-sm font-bold text-emerald-300">Effective velocity: 10-15 features/day</div>
</div>
</div>

<div class="mt-4 p-4 bg-gradient-to-r from-green-600/80 to-blue-600/80 rounded-lg text-center">
<span class="text-white font-bold">🎯 Target: &lt;10 minutes for PR checks, &lt;30 minutes for full pipeline</span>
</div>

---

# How to Achieve Fast CI

<div class="grid grid-cols-5 gap-3 text-xs">
<div class="p-3 bg-gradient-to-br from-cyan-900/40 to-cyan-800/40 rounded-lg border border-cyan-500/30">
<div class="text-2xl mb-2">🎯</div>
<div class="font-bold text-cyan-300">Affected Analysis</div>
<div class="text-gray-400 mt-1">Test only changed modules: 80 min → 8 min</div>
</div>

<div class="p-3 bg-gradient-to-br from-blue-900/40 to-blue-800/40 rounded-lg border border-blue-500/30">
<div class="text-2xl mb-2">⚡</div>
<div class="font-bold text-blue-300">Parallelize</div>
<div class="text-gray-400 mt-1">Distribute across runners: 8 min → 4 min</div>
</div>

<div class="p-3 bg-gradient-to-br from-purple-900/40 to-purple-800/40 rounded-lg border border-purple-500/30">
<div class="text-2xl mb-2">💾</div>
<div class="font-bold text-purple-300">Cache Aggressively</div>
<div class="text-gray-400 mt-1">Dependencies, builds, test results</div>
</div>

<div class="p-3 bg-gradient-to-br from-pink-900/40 to-pink-800/40 rounded-lg border border-pink-500/30">
<div class="text-2xl mb-2">🔨</div>
<div class="font-bold text-pink-300">Incremental Builds</div>
<div class="text-gray-400 mt-1">Rebuild only what changed</div>
</div>

<div class="p-3 bg-gradient-to-br from-green-900/40 to-green-800/40 rounded-lg border border-green-500/30">
<div class="text-2xl mb-2">🚀</div>
<div class="font-bold text-green-300">Strategic Splitting</div>
<div class="text-gray-400 mt-1">Fast smoke tests first (fail fast)</div>
</div>
</div>

<div class="mt-6 space-y-2 text-sm">
<div class="p-3 bg-gradient-to-br from-gray-800 to-gray-900 rounded-lg">
<div class="font-bold text-gray-300">Example Impact</div>
<div class="text-xs text-gray-400 mt-1">First build: 23 minutes → Cached build with affected analysis: 3 minutes (7.6x speedup)</div>
</div>
</div>

---

# Zero-Flake Tolerance

<div class="p-4 bg-gradient-to-br from-red-900/30 to-red-800/20 rounded-xl border-2 border-red-500/30 mb-4">
<div class="font-bold text-red-300 mb-2">⚠️ The Problem with Flaky Tests</div>
<div class="text-xs text-gray-300 space-y-1">
<div>Single flaky test (5% failure rate) × 20 PRs/day = 1 spurious failure/day</div>
<div>10 flaky tests = 10 failures/day → Developers lose trust in CI</div>
<div>"Just rerun it" becomes default → Green builds mean nothing</div>
</div>
</div>

<div class="grid grid-cols-2 gap-4 text-sm">
<div class="p-3 bg-gradient-to-br from-orange-900/40 to-orange-800/40 rounded-lg border border-orange-500/30">
<div class="font-bold text-orange-300 mb-2">Zero Tolerance Policy</div>
<div class="space-y-1 text-xs text-gray-300">
<div>1. Quarantine on first flake</div>
<div>2. Fix within 2 days or delete</div>
<div>3. After 2 days: auto-disabled</div>
<div>4. Track flake rate: &lt;2% target</div>
</div>
</div>
<div class="p-3 bg-gradient-to-br from-green-900/40 to-green-800/40 rounded-lg border border-green-500/30">
<div class="font-bold text-green-300 mb-2">How to Fix Flaky Tests</div>
<div class="space-y-1 text-xs text-gray-300">
<div>Race conditions → waitFor(), not sleep()</div>
<div>External deps → Mock APIs</div>
<div>Time-dependent → Mock system time</div>
<div>Order-dependent → Unique IDs per test</div>
</div>
</div>
</div>

<div class="mt-4 p-3 bg-gradient-to-r from-green-500/20 to-emerald-500/20 rounded-xl border border-green-500/30 text-center">
<div class="text-sm font-semibold text-green-300">Real-world impact: 18% flake rate → 1.2% | Agent idle time: 35% → 8% | Manual reruns: 45/week → 2/week</div>
</div>

---

# ✅ Key Takeaways

<div class="grid grid-cols-2 gap-4 mt-4 max-w-4xl mx-auto">
<div class="p-4 bg-gradient-to-br from-cyan-900/30 to-blue-900/30 rounded-lg border border-cyan-500/30">
<div class="flex items-center gap-3">
<div class="text-2xl font-bold text-cyan-400">1</div>
<div>
<div class="font-semibold text-cyan-300">AgentRC Level 5 is a maturity target</div>
<div class="text-sm opacity-80">Autonomous delivery only works if Levels 1-4 foundations are solid</div>
</div>
</div>
</div>

<div class="p-4 bg-gradient-to-br from-blue-900/30 to-indigo-900/30 rounded-lg border border-blue-500/30">
<div class="flex items-center gap-3">
<div class="text-2xl font-bold text-blue-400">2</div>
<div>
<div class="font-semibold text-blue-300">Monorepo eliminates coordination overhead</div>
<div class="text-sm opacity-80">Default for 80% of product teams when agents touch 2+ repos frequently</div>
</div>
</div>
</div>

<div class="p-4 bg-gradient-to-br from-indigo-900/30 to-purple-900/30 rounded-lg border border-indigo-500/30">
<div class="flex items-center gap-3">
<div class="text-2xl font-bold text-indigo-400">3</div>
<div>
<div class="font-semibold text-indigo-300">PR review shifts to outcome validation</div>
<div class="text-sm opacity-80">Evidence bundles + automated gates + human judgment on intent match</div>
</div>
</div>
</div>

<div class="p-4 bg-gradient-to-br from-purple-900/30 to-pink-900/30 rounded-lg border border-purple-500/30">
<div class="flex items-center gap-3">
<div class="text-2xl font-bold text-purple-400">4</div>
<div>
<div class="font-semibold text-purple-300">CI becomes a trust factory</div>
<div class="text-sm opacity-80">&lt;10 min PR checks, &lt;2% flake rate, automated attestations at scale</div>
</div>
</div>
</div>
</div>

<div class="mt-6 p-4 bg-gradient-to-r from-green-500/20 to-emerald-500/20 rounded-xl border border-green-500/30 text-center">
<div class="text-lg font-semibold text-green-300">Result: 100x throughput scaling — 150 features/year → 3,600 features/year with maintained quality</div>
</div>

---

# 📚 References

<div class="grid grid-cols-2 gap-4 text-sm">
<div class="space-y-2">
<div class="p-3 bg-gradient-to-br from-cyan-900/40 to-cyan-800/40 rounded-lg border border-cyan-500/30">
<div class="font-bold text-cyan-300 mb-1">AgentRC Framework</div>
<div class="text-xs text-gray-400">Microsoft's repository AI-readiness maturity model and workflow</div>
</div>

<div class="p-3 bg-gradient-to-br from-blue-900/40 to-blue-800/40 rounded-lg border border-blue-500/30">
<div class="font-bold text-blue-300 mb-1">Nx Monorepo Tools</div>
<div class="text-xs text-gray-400">Build orchestration, module boundaries, affected analysis, caching</div>
</div>

<div class="p-3 bg-gradient-to-br from-purple-900/40 to-purple-800/40 rounded-lg border border-purple-500/30">
<div class="font-bold text-purple-300 mb-1">GitHub Actions</div>
<div class="text-xs text-gray-400">CI/CD workflow automation, parallelization, and caching strategies</div>
</div>
</div>

<div class="space-y-2">
<div class="p-3 bg-gradient-to-br from-pink-900/40 to-pink-800/40 rounded-lg border border-pink-500/30">
<div class="font-bold text-pink-300 mb-1">SLSA Framework</div>
<div class="text-xs text-gray-400">Supply chain security levels and attestation standards</div>
</div>

<div class="p-3 bg-gradient-to-br from-green-900/40 to-green-800/40 rounded-lg border border-green-500/30">
<div class="font-bold text-green-300 mb-1">Related Talks</div>
<div class="text-xs text-gray-400">Agentic Journey (quick wins), Agent Teams (multi-agent), Enterprise Patterns (org-wide)</div>
</div>

<div class="p-3 bg-gradient-to-br from-orange-900/40 to-orange-800/40 rounded-lg border border-orange-500/30">
<div class="font-bold text-orange-300 mb-1">Hermetic Builds Guide</div>
<div class="text-xs text-gray-400">Deterministic build principles for reproducible trust signals</div>
</div>
</div>
</div>

---
layout: center
---

<div class="h-full flex flex-col items-center justify-center relative overflow-hidden">
<div class="absolute inset-0 bg-gradient-to-br from-cyan-900/20 via-blue-900/10 to-indigo-900/20"></div>
<div class="absolute top-1/4 left-1/2 -translate-x-1/2 -translate-y-1/2 w-96 h-96 bg-gradient-to-r from-cyan-500/20 via-blue-500/20 to-indigo-500/20 rounded-full blur-3xl"></div>
<div class="text-6xl mb-6 relative z-10">💬</div>
<h1 class="!text-5xl !font-bold bg-gradient-to-r from-cyan-400 via-blue-400 to-indigo-400 bg-clip-text text-transparent relative z-10">Thank You</h1>
<div class="mt-6 text-xl opacity-80 relative z-10">Let's discuss your path to Level 5</div>
<div class="mt-8 w-32 h-1 bg-gradient-to-r from-transparent via-cyan-400 to-transparent rounded-full relative z-10"></div>
</div>
