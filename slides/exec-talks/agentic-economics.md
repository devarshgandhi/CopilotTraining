---
theme: default
class: text-center
highlighter: shiki
lineNumbers: false
info: |
  ## Agentic Economics
  Making the Business Case for AI Agent Adoption
  CopilotTraining Executive Talk
drawings:
  persist: false
transition: slide-left
title: Agentic Economics - Making the Business Case
module: exec-talks/agentic-economics
mdc: true
status: active
updated: 2026-02-12
---

<div class="h-full flex flex-col items-center justify-center relative overflow-hidden">
<div class="absolute inset-0 bg-gradient-to-br from-blue-900/20 via-cyan-900/10 to-green-900/20"></div>
<div class="absolute top-1/4 left-1/2 -translate-x-1/2 -translate-y-1/2 w-96 h-96 bg-gradient-to-r from-blue-500/20 via-cyan-500/20 to-green-500/20 rounded-full blur-3xl"></div>
<div class="relative z-10">
<div class="absolute inset-0 blur-2xl opacity-50">
<img src="./sdp-logo.png" class="w-64" alt="" />
</div>
<img src="./sdp-logo.png" class="w-64 relative" alt="SDP Logo" />
</div>
<h1 class="!text-5xl !font-bold !mt-8 bg-gradient-to-r from-blue-400 via-cyan-400 to-green-400 bg-clip-text text-transparent relative z-10">
The Agentic Economics
</h1>
<div class="mt-4 relative z-10">
<span class="px-6 py-2 bg-gradient-to-r from-blue-600/80 to-cyan-600/80 rounded-full text-white text-xl font-medium shadow-lg shadow-blue-500/25">
Making the Business Case
</span>
</div>
<div class="mt-8 w-32 h-1 bg-gradient-to-r from-transparent via-cyan-400 to-transparent rounded-full relative z-10"></div>
</div>

---
layout: center
name: toc
---

# 📖 Table of Contents

<div class="grid grid-cols-2 gap-6 max-w-4xl mx-auto">
<div @click="$nav.go(3)" class="cursor-pointer p-6 bg-gradient-to-br from-blue-600/20 to-blue-800/20 rounded-xl hover:from-blue-600/30 hover:to-blue-800/30 transition-all border border-blue-500/30">
<div class="text-4xl mb-3">💰</div>
<div class="text-xl font-bold text-blue-300 mb-2">The $2/Hour Engineer</div>
<div class="text-sm text-gray-400">Compare agent costs to human labor</div>
</div>
<div @click="$nav.go(5)" class="cursor-pointer p-6 bg-gradient-to-br from-cyan-600/20 to-cyan-800/20 rounded-xl hover:from-cyan-600/30 hover:to-cyan-800/30 transition-all border border-cyan-500/30">
<div class="text-4xl mb-3">📊</div>
<div class="text-xl font-bold text-cyan-300 mb-2">The 20% Goal</div>
<div class="text-sm text-gray-400">Achievable targets and ROI math</div>
</div>
<div @click="$nav.go(8)" class="cursor-pointer p-6 bg-gradient-to-br from-green-600/20 to-green-800/20 rounded-xl hover:from-green-600/30 hover:to-green-800/30 transition-all border border-green-500/30">
<div class="text-4xl mb-3">🎯</div>
<div class="text-xl font-bold text-green-300 mb-2">Where to Attack</div>
<div class="text-sm text-gray-400">High-value targets by tier</div>
</div>
<div @click="$nav.go(13)" class="cursor-pointer p-6 bg-gradient-to-br from-purple-600/20 to-purple-800/20 rounded-xl hover:from-purple-600/30 hover:to-purple-800/30 transition-all border border-purple-500/30">
<div class="text-4xl mb-3">📈</div>
<div class="text-xl font-bold text-purple-300 mb-2">Investment Strategy</div>
<div class="text-sm text-gray-400">Phased approach and returns</div>
</div>
</div>

---

# The $2/Hour Engineer

<div class="p-4 bg-gradient-to-r from-blue-600 to-blue-800 rounded-xl shadow-lg text-center mb-4">
<div class="text-4xl font-bold text-white mb-2">$2-5/hour</div>
<div class="text-lg text-blue-100">Production-grade AI agent operational cost</div>
</div>
<div class="grid grid-cols-2 gap-4 text-sm">
<div class="p-3 bg-gray-800/60 rounded-lg border border-gray-700">
<div class="text-2xl mb-2">👨‍💻</div>
<div class="text-white font-bold">Junior Developer (US)</div>
<div class="text-gray-400">$70-90/hour</div>
<div class="text-red-400 font-semibold mt-1">14-45x more expensive</div>
</div>
<div class="p-3 bg-gray-800/60 rounded-lg border border-gray-700">
<div class="text-2xl mb-2">🎯</div>
<div class="text-white font-bold">Senior Developer (US)</div>
<div class="text-gray-400">$100-130/hour</div>
<div class="text-red-400 font-semibold mt-1">20-65x more expensive</div>
</div>
<div class="p-3 bg-gray-800/60 rounded-lg border border-gray-700">
<div class="text-2xl mb-2">⭐</div>
<div class="text-white font-bold">Staff Engineer (US)</div>
<div class="text-gray-400">$120-150/hour</div>
<div class="text-red-400 font-semibold mt-1">24-75x more expensive</div>
</div>
<div class="p-3 bg-gray-800/60 rounded-lg border border-gray-700">
<div class="text-2xl mb-2">🌍</div>
<div class="text-white font-bold">Offshore Developer</div>
<div class="text-gray-400">$25-85/hour</div>
<div class="text-red-400 font-semibold mt-1">5-42x more expensive</div>
</div>
</div>
<div class="mt-4 p-4 bg-gradient-to-r from-blue-600/30 to-cyan-600/30 rounded-xl border border-blue-500/50 text-center">
<div class="text-lg font-bold text-white">The question isn't whether agents are cheaper.</div>
<div class="text-base text-blue-200 mt-1">The question is: what work can we move to $2-5/hour?</div>
</div>

---

# The Labor Arbitrage Opportunity

<div class="flex flex-col gap-3">
<div class="p-4 bg-blue-900/40 rounded-lg border-l-4 border-blue-400">
<div class="flex items-center gap-3 mb-2">
<span class="text-3xl">💰</span>
<h3 class="text-xl font-bold text-blue-300">HIGH-VALUE WORK</h3>
</div>
<div class="text-sm text-gray-300 ml-11">
<div class="mb-2">Architecture decisions • Strategic planning • Complex debugging</div>
<div class="text-blue-400 font-semibold">Must stay human • $150-250/hr is appropriate</div>
</div>
</div>
<div class="p-4 bg-yellow-900/40 rounded-lg border-l-4 border-yellow-500">
<div class="flex items-center gap-3 mb-2">
<span class="text-3xl">⚙️</span>
<h3 class="text-xl font-bold text-yellow-400">ROUTINE WORK</h3>
</div>
<div class="text-sm text-gray-300 ml-11">
<div class="mb-2">Code review • Test writing • Bug investigation • Documentation</div>
<div class="text-yellow-400 font-semibold">Could be $2/hr • Pattern-based • Context-gathering</div>
</div>
</div>
<div class="p-4 bg-green-900/40 rounded-lg border-l-4 border-green-400">
<div class="flex items-center gap-3 mb-2">
<span class="text-3xl">🔁</span>
<h3 class="text-xl font-bold text-green-300">PURE TOIL</h3>
</div>
<div class="text-sm text-gray-300 ml-11">
<div class="mb-2">Issue triage • Compliance checking • Status reports • Audit prep</div>
<div class="text-green-400 font-semibold">Best at $2/hr • Rule-following • Pattern matching</div>
</div>
</div>
</div>
<div class="mt-4 p-4 bg-gradient-to-r from-orange-600/30 to-red-600/30 rounded-xl border border-orange-500/50 text-center">
<div class="text-lg font-bold text-white">85-95% potential cost reduction on routine work</div>
<div class="text-base text-orange-200 mt-1">But requires significant infrastructure investment</div>
</div>

---

# The 20% Goal: Making It Concrete

<div class="grid grid-cols-2 gap-6">
<div>
<h3 class="text-xl font-bold text-cyan-400 mb-3">📊 The Math (50-person team)</h3>
<div class="space-y-2 text-sm">
<div class="p-2 bg-gray-800/60 rounded-lg">
<div class="text-gray-400">Total labor hours/year</div>
<div class="text-white font-bold">100,000 hours</div>
</div>
<div class="p-2 bg-gray-800/60 rounded-lg">
<div class="text-gray-400">Current cost @ $100/hr avg</div>
<div class="text-white font-bold">$10,000,000/year</div>
</div>
<div class="p-2 bg-blue-800/60 rounded-lg border border-blue-500">
<div class="text-blue-300">20% target (agent labor)</div>
<div class="text-white font-bold">20,000 hours/year</div>
</div>
<div class="p-2 bg-green-800/60 rounded-lg border border-green-500">
<div class="text-green-300">Agent cost for those hours</div>
<div class="text-white font-bold">$60,000/year</div>
</div>
<div class="p-2 bg-red-800/60 rounded-lg border border-red-500">
<div class="text-red-300">Previous human cost</div>
<div class="text-white font-bold">$2,000,000/year</div>
</div>
</div>
</div>
<div>
<h3 class="text-xl font-bold text-green-400 mb-3">💰 The Returns</h3>
<div class="p-4 bg-gradient-to-br from-green-600/30 to-green-800/30 rounded-xl border border-green-500/50 mb-4">
<div class="text-3xl font-bold text-white mb-1">$1,940,000</div>
<div class="text-base text-green-200">Annual savings potential</div>
</div>
<div class="space-y-2 text-sm">
<div class="p-3 bg-orange-900/40 rounded-lg border border-orange-500/50">
<div class="font-bold text-orange-300 mb-1">⚠️ The Catch</div>
<div class="text-gray-300">Requires $800K-1.6M investment</div>
<div class="text-gray-300">12-18 month disciplined execution</div>
<div class="text-gray-300">Without proper infrastructure, actual savings 50-70% lower</div>
</div>
</div>
</div>
</div>

---

# The Investment Gap: 5 Critical Barriers

<div class="grid grid-cols-2 gap-3 text-xs">
<div class="p-3 bg-red-900/30 rounded-lg border-2 border-red-500/50">
<div class="flex items-center gap-2 mb-2">
<span class="text-2xl">🚧</span>
<div class="text-red-400 font-bold text-sm">No Instrumentation</div>
</div>
<div class="text-gray-300">
Without automated tests and quality gates, teams can't verify output
</div>
<div class="text-red-400 mt-2 font-semibold">→ No time saved</div>
</div>
<div class="p-3 bg-red-900/30 rounded-lg border-2 border-red-500/50">
<div class="flex items-center gap-2 mb-2">
<span class="text-2xl">🧠</span>
<div class="text-red-400 font-bold text-sm">Tribal Knowledge</div>
</div>
<div class="text-gray-300">
Critical context lives in people's heads, not documentation
</div>
<div class="text-red-400 mt-2 font-semibold">→ Rework required</div>
</div>
<div class="p-3 bg-red-900/30 rounded-lg border-2 border-red-500/50">
<div class="flex items-center gap-2 mb-2">
<span class="text-2xl">⏸️</span>
<div class="text-red-400 font-bold text-sm">Approval Bottlenecks</div>
</div>
<div class="text-gray-300">
Agent finishes in 30 min, waits 2 days in review queue
</div>
<div class="text-red-400 mt-2 font-semibold">→ Total time unchanged</div>
</div>
<div class="p-3 bg-red-900/30 rounded-lg border-2 border-red-500/50">
<div class="flex items-center gap-2 mb-2">
<span class="text-2xl">❓</span>
<div class="text-red-400 font-bold text-sm">Undefined Boundaries</div>
</div>
<div class="text-gray-300">
Every task requires negotiating permissions and guardrails
</div>
<div class="text-red-400 mt-2 font-semibold">→ Paralysis</div>
</div>
<div class="p-3 bg-red-900/30 rounded-lg border-2 border-red-500/50">
<div class="flex items-center gap-2 mb-2">
<span class="text-2xl">🔧</span>
<div class="text-red-400 font-bold text-sm">Fragmented Tooling</div>
</div>
<div class="text-gray-300">
Context scattered across Jira, Slack, Confluence, GitHub, email
</div>
<div class="text-red-400 mt-2 font-semibold">→ Incomplete output</div>
</div>
</div>
<div class="mt-4 p-4 bg-gradient-to-r from-red-600/30 to-orange-600/30 rounded-xl border border-red-500/50 text-center">
<div class="text-base font-bold text-white">Most organizations are not ready to capture agentic economics</div>
<div class="text-sm text-orange-200 mt-1">The infrastructure gap must be closed first</div>
</div>

---

# Quick Wins: Issue Lifecycle Automation

<div class="grid grid-cols-2 gap-6">
<div>
<h3 class="text-xl font-bold text-blue-400 mb-3">📊 Current State (Manual)</h3>
<div class="space-y-2 text-sm">
<div class="p-2 bg-gray-800/60 rounded-lg">
<div class="text-gray-400">20 issues/week @ 10 hrs each</div>
<div class="text-white font-bold">200 hours/week</div>
</div>
<div class="p-2 bg-gray-800/60 rounded-lg">
<div class="text-gray-400">Annual labor (10,400 hrs)</div>
<div class="text-white font-bold">$1,040,000/year</div>
</div>
</div>
<h3 class="text-xl font-bold text-green-400 mb-3 mt-4">✨ With Agents</h3>
<div class="space-y-2 text-sm">
<div class="p-2 bg-blue-800/60 rounded-lg border border-blue-500">
<div class="text-blue-300">Agent time: 2.5 hrs/issue</div>
<div class="text-white font-bold">50 hrs/week @ $3 = $7,800/yr</div>
</div>
<div class="p-2 bg-blue-800/60 rounded-lg border border-blue-500">
<div class="text-blue-300">Human time: 0.3 hrs/issue</div>
<div class="text-white font-bold">6 hrs/week = $31,200/yr</div>
</div>
<div class="p-2 bg-green-800/60 rounded-lg border border-green-500">
<div class="text-green-300">Total cost</div>
<div class="text-white font-bold">$39,000/year</div>
</div>
</div>
</div>
<div>
<div class="p-6 bg-gradient-to-br from-green-600/30 to-green-800/30 rounded-xl border border-green-500/50 mb-4">
<div class="text-4xl font-bold text-white mb-2">$1,001,000</div>
<div class="text-lg text-green-200">Annual savings</div>
</div>
<div class="space-y-3 text-sm">
<div class="p-3 bg-yellow-900/40 rounded-lg border border-yellow-500/50">
<div class="font-bold text-yellow-300 mb-1">💡 Investment Required</div>
<div class="text-gray-300">Setup: 4-6 hours (one-time)</div>
<div class="text-gray-300">Annual cost: $10,200</div>
<div class="text-green-400 font-semibold mt-1">Payback: 3.6 days</div>
<div class="text-green-400 font-semibold">First-year ROI: 9,714%</div>
</div>
<div class="p-3 bg-blue-900/40 rounded-lg border border-blue-500/50">
<div class="font-bold text-blue-300 mb-1">🎯 Why This Works</div>
<div class="text-gray-300">• No repo restructuring</div>
<div class="text-gray-300">• No CI/CD rewrite</div>
<div class="text-gray-300">• Works with existing workflows</div>
</div>
</div>
</div>
</div>

---

# Where to Attack: Tier 1 Quick Wins

<div class="space-y-3 text-sm">
<div class="p-4 bg-green-900/30 rounded-lg border-l-4 border-green-500">
<div class="flex items-center justify-between mb-2">
<div class="flex items-center gap-3">
<span class="text-2xl">🔍</span>
<div class="font-bold text-green-300 text-base">Issue Triage</div>
</div>
<div class="text-right">
<div class="text-green-400 font-bold">$59,700/year</div>
<div class="text-gray-400 text-xs">100 issues/month</div>
</div>
</div>
<div class="grid grid-cols-3 gap-2 text-xs">
<div>
<div class="text-gray-400">Current</div>
<div class="text-white">30 min @ $100/hr = $50</div>
</div>
<div>
<div class="text-gray-400">Agent</div>
<div class="text-white">5 min @ $3/hr = $0.25</div>
</div>
<div>
<div class="text-gray-400">Infrastructure</div>
<div class="text-white">Issue tracker API</div>
</div>
</div>
</div>
<div class="p-4 bg-green-900/30 rounded-lg border-l-4 border-green-500">
<div class="flex items-center justify-between mb-2">
<div class="flex items-center gap-3">
<span class="text-2xl">📝</span>
<div class="font-bold text-green-300 text-base">PR Description Generation</div>
</div>
<div class="text-right">
<div class="text-green-400 font-bold">$59,760/year</div>
<div class="text-gray-400 text-xs">200 PRs/month</div>
</div>
</div>
<div class="grid grid-cols-3 gap-2 text-xs">
<div>
<div class="text-gray-400">Current</div>
<div class="text-white">15 min @ $100/hr = $25</div>
</div>
<div>
<div class="text-gray-400">Agent</div>
<div class="text-white">2 min @ $3/hr = $0.10</div>
</div>
<div>
<div class="text-gray-400">Infrastructure</div>
<div class="text-white">Git access, context</div>
</div>
</div>
</div>
<div class="p-4 bg-green-900/30 rounded-lg border-l-4 border-green-500">
<div class="flex items-center justify-between mb-2">
<div class="flex items-center gap-3">
<span class="text-2xl">🔄</span>
<div class="font-bold text-green-300 text-base">Dependency Updates</div>
</div>
<div class="text-right">
<div class="text-green-400 font-bold">$47,820/year</div>
<div class="text-gray-400 text-xs">20 updates/month</div>
</div>
</div>
<div class="grid grid-cols-3 gap-2 text-xs">
<div>
<div class="text-gray-400">Current</div>
<div class="text-white">2 hrs @ $100/hr = $200</div>
</div>
<div>
<div class="text-gray-400">Agent</div>
<div class="text-white">15 min @ $3/hr = $0.75</div>
</div>
<div>
<div class="text-gray-400">Infrastructure</div>
<div class="text-white">Basic CI pipeline</div>
</div>
</div>
</div>
</div>
<div class="mt-4 p-4 bg-gradient-to-r from-green-600/30 to-cyan-600/30 rounded-xl border border-green-500/50 text-center">
<div class="text-xl font-bold text-white">Tier 1 Total: ~$167,280/year</div>
<div class="text-base text-green-200 mt-1">Minimal infrastructure required • 0-3 months to deploy</div>
</div>

---

# Where to Attack: Tier 2 & 3

<div class="grid grid-cols-2 gap-4 text-xs">
<div>
<h3 class="text-lg font-bold text-yellow-400 mb-2">⚙️ Tier 2: Medium Effort (3-6 months)</h3>
<div class="space-y-2">
<div class="p-2 bg-yellow-900/30 rounded-lg border border-yellow-500/50">
<div class="flex justify-between items-center mb-1">
<div class="font-bold text-yellow-300">Test Generation</div>
<div class="text-yellow-400">$143K/yr</div>
</div>
<div class="text-gray-400">30 features/month</div>
<div class="text-gray-300">Needs: Test framework, coverage tools, CI</div>
</div>
<div class="p-2 bg-yellow-900/30 rounded-lg border border-yellow-500/50">
<div class="flex justify-between items-center mb-1">
<div class="font-bold text-yellow-300">Compliance Checking</div>
<div class="text-yellow-400">$240K/yr</div>
</div>
<div class="text-gray-400">50 PRs/month requiring compliance</div>
<div class="text-gray-300">Needs: Codified rules, scanning tools</div>
</div>
<div class="p-2 bg-yellow-900/30 rounded-lg border border-yellow-500/50">
<div class="flex justify-between items-center mb-1">
<div class="font-bold text-yellow-300">Documentation Sync</div>
<div class="text-yellow-400">$41K/yr</div>
</div>
<div class="text-gray-400">Continuous synchronization</div>
<div class="text-gray-300">Needs: Doc system access, comparison tools</div>
</div>
</div>
<div class="mt-2 p-2 bg-yellow-900/40 rounded-lg text-center">
<div class="font-bold text-white">Tier 2 Total: ~$424K/year</div>
</div>
</div>
<div>
<h3 class="text-lg font-bold text-orange-400 mb-2">🚀 Tier 3: High Investment (6-12 months)</h3>
<div class="space-y-2">
<div class="p-2 bg-orange-900/30 rounded-lg border border-orange-500/50">
<div class="flex justify-between items-center mb-1">
<div class="font-bold text-orange-300">Code Implementation</div>
<div class="text-orange-400">$333K/yr</div>
</div>
<div class="text-gray-400">40 features/month</div>
<div class="text-gray-300">Needs: Full test coverage, security scanning</div>
</div>
<div class="p-2 bg-orange-900/30 rounded-lg border border-orange-500/50">
<div class="flex justify-between items-center mb-1">
<div class="font-bold text-orange-300">Bug Investigation</div>
<div class="text-orange-400">$394K/yr</div>
</div>
<div class="text-gray-400">60 bugs/month</div>
<div class="text-gray-300">Needs: Logging, tracing, test harness</div>
</div>
<div class="p-2 bg-orange-900/30 rounded-lg border border-orange-500/50">
<div class="flex justify-between items-center mb-1">
<div class="font-bold text-orange-300">Refactoring</div>
<div class="text-orange-400">$167K/yr</div>
</div>
<div class="text-gray-400">10 refactors/month</div>
<div class="text-gray-300">Needs: Comprehensive tests, type safety</div>
</div>
</div>
<div class="mt-2 p-2 bg-orange-900/40 rounded-lg text-center">
<div class="font-bold text-white">Tier 3 Total: ~$894K/year</div>
</div>
</div>
</div>
<div class="mt-4 p-4 bg-gradient-to-r from-green-600/30 to-orange-600/30 rounded-xl border border-green-500/50 text-center">
<div class="text-xl font-bold text-white">Combined Potential: $1,485,404/year</div>
<div class="text-base text-gray-200 mt-1">Represents ~15% of total labor cost for 50-person team</div>
</div>

---

# Constraint Reality Check

<div class="grid grid-cols-2 gap-4 text-sm">
<div>
<h3 class="text-lg font-bold text-red-400 mb-3">⚠️ Without Automation</h3>
<div class="space-y-2">
<div class="p-3 bg-red-900/30 rounded-lg border border-red-500/50">
<div class="text-gray-400">Agent work</div>
<div class="text-white">1 hour @ $3/hr = $3</div>
</div>
<div class="p-3 bg-red-900/30 rounded-lg border border-red-500/50">
<div class="text-gray-400">Human review</div>
<div class="text-white">2 hours @ $100/hr = $200</div>
</div>
<div class="p-3 bg-red-900/30 rounded-lg border-2 border-red-500">
<div class="text-red-400 font-bold">Total cost: $203</div>
<div class="text-red-300 text-xs">vs. $200 human-only</div>
<div class="text-red-400 font-bold mt-1">Result: -$3 (LOSS!)</div>
</div>
</div>
</div>
<div>
<h3 class="text-lg font-bold text-green-400 mb-3">✅ With Automation</h3>
<div class="space-y-2">
<div class="p-3 bg-green-900/30 rounded-lg border border-green-500/50">
<div class="text-gray-400">Agent work</div>
<div class="text-white">1 hour @ $3/hr = $3</div>
</div>
<div class="p-3 bg-green-900/30 rounded-lg border border-green-500/50">
<div class="text-gray-400">Automated checks</div>
<div class="text-white">5 min @ $.10/check = $0.10</div>
</div>
<div class="p-3 bg-green-900/30 rounded-lg border border-green-500/50">
<div class="text-gray-400">Human spot-check</div>
<div class="text-white">15 min @ $100/hr = $25</div>
</div>
<div class="p-3 bg-green-900/30 rounded-lg border-2 border-green-500">
<div class="text-green-400 font-bold">Total cost: $28.10</div>
<div class="text-green-300 text-xs">vs. $200 human-only</div>
<div class="text-green-400 font-bold mt-1">Result: $171.90 saved (86%)</div>
</div>
</div>
</div>
</div>
<div class="mt-4 p-4 bg-gradient-to-r from-orange-600/30 to-red-600/30 rounded-xl border border-orange-500/50 text-center">
<div class="text-lg font-bold text-white">🔑 Key Insight: Automated verification is the multiplier</div>
<div class="text-base text-orange-200 mt-1">Without it, organizations pay twice—once for the agent, once for the human reviewer</div>
</div>

---

# The Iteration Cost Problem

<div class="grid grid-cols-2 gap-4 text-xs">
<div>
<h3 class="text-base font-bold text-red-400 mb-2">❌ High-Iteration Case (Unclear Requirements)</h3>
<div class="space-y-1">
<div class="p-2 bg-gray-800/60 rounded">
<div class="text-gray-400">5 iterations × 30 min each @ $3/hr</div>
<div class="text-white">Agent cost: $7.50</div>
</div>
<div class="p-2 bg-gray-800/60 rounded">
<div class="text-gray-400">5 reviews × 30 min each @ $100/hr</div>
<div class="text-white">Human cost: $250</div>
</div>
<div class="p-2 bg-red-900/40 rounded border-2 border-red-500">
<div class="text-red-400 font-bold">Total: $257.50</div>
<div class="text-gray-300">vs. $200 for human to do it in 2 hours</div>
<div class="text-red-400 font-bold mt-1">Result: LOSS</div>
</div>
</div>
</div>
<div>
<h3 class="text-base font-bold text-green-400 mb-2">✅ Low-Iteration Case (Clear Requirements)</h3>
<div class="space-y-1">
<div class="p-2 bg-gray-800/60 rounded">
<div class="text-gray-400">Iteration 1: 30 min @ $3/hr</div>
<div class="text-white">Agent cost: $1.50</div>
</div>
<div class="p-2 bg-gray-800/60 rounded">
<div class="text-gray-400">Review 1: 15 min @ $100/hr</div>
<div class="text-white">Human cost: $25</div>
</div>
<div class="p-2 bg-gray-800/60 rounded">
<div class="text-gray-400">Iteration 2: 15 min @ $3/hr</div>
<div class="text-white">Agent cost: $0.75</div>
</div>
<div class="p-2 bg-gray-800/60 rounded">
<div class="text-gray-400">Final review: 15 min @ $100/hr</div>
<div class="text-white">Human cost: $25</div>
</div>
<div class="p-2 bg-green-900/40 rounded border-2 border-green-500">
<div class="text-green-400 font-bold">Total: $52.25</div>
<div class="text-gray-300">vs. $200 for human to do it in 2 hours</div>
<div class="text-green-400 font-bold mt-1">Result: 74% SAVINGS</div>
</div>
</div>
</div>
</div>
<div class="mt-4 p-4 bg-gradient-to-r from-blue-600/30 to-cyan-600/30 rounded-xl border border-blue-500/50 text-center">
<div class="text-base font-bold text-white">🎯 Iteration count is the primary driver of ROI</div>
<div class="text-sm text-blue-200 mt-1">Clear requirements → fewer iterations → better economics</div>
</div>

---

# Phased Investment Strategy

<div class="grid grid-cols-3 gap-3 text-xs">
<div class="p-3 bg-blue-900/30 rounded-lg border border-blue-500/50">
<h3 class="text-base font-bold text-blue-400 mb-2">Phase 1: Foundation</h3>
<div class="text-gray-400 mb-2">Months 1-3</div>
<div class="space-y-1">
<div class="text-white">• Issue triage automation</div>
<div class="text-white">• PR description generation</div>
<div class="text-white">• Dependency updates</div>
<div class="text-white">• Basic CI/CD improvements</div>
</div>
<div class="mt-2 p-2 bg-blue-900/50 rounded">
<div class="text-blue-300">Investment: $110K</div>
<div class="text-green-400 font-bold">Return: $168K/year</div>
<div class="text-yellow-400">Payback: 8 months</div>
</div>
</div>
<div class="p-3 bg-yellow-900/30 rounded-lg border border-yellow-500/50">
<h3 class="text-base font-bold text-yellow-400 mb-2">Phase 2: Scaling</h3>
<div class="text-gray-400 mb-2">Months 4-6</div>
<div class="space-y-1">
<div class="text-white">• Test coverage expansion</div>
<div class="text-white">• Test generation automation</div>
<div class="text-white">• Compliance rule codification</div>
<div class="text-white">• Documentation infrastructure</div>
</div>
<div class="mt-2 p-2 bg-yellow-900/50 rounded">
<div class="text-yellow-300">Investment: $375K</div>
<div class="text-green-400 font-bold">Return: $424K/year</div>
<div class="text-yellow-400">Payback: 11 months</div>
</div>
</div>
<div class="p-3 bg-orange-900/30 rounded-lg border border-orange-500/50">
<h3 class="text-base font-bold text-orange-400 mb-2">Phase 3: Transform</h3>
<div class="text-gray-400 mb-2">Months 7-12</div>
<div class="space-y-1">
<div class="text-white">• Code implementation infra</div>
<div class="text-white">• Bug investigation tooling</div>
<div class="text-white">• Refactoring infrastructure</div>
<div class="text-white">• Full automation suite</div>
</div>
<div class="mt-2 p-2 bg-orange-900/50 rounded">
<div class="text-orange-300">Investment: $575K</div>
<div class="text-green-400 font-bold">Return: $894K/year</div>
<div class="text-yellow-400">Payback: 8 months</div>
</div>
</div>
</div>
<div class="mt-4 p-4 bg-gradient-to-r from-blue-600/30 to-purple-600/30 rounded-xl border border-blue-500/50 text-center">
<div class="text-base font-bold text-white">Total Year 1 Investment: $1,060K | Annual Run Rate: $1,486K</div>
<div class="text-sm text-gray-200 mt-1">Disciplined execution required for these returns</div>
</div>

---

# Cumulative Investment & Returns

<div class="grid grid-cols-2 gap-6">
<div>
<h3 class="text-xl font-bold text-cyan-400 mb-4">📊 Year-by-Year View</h3>
<div class="space-y-3 text-sm">
<div class="p-3 bg-orange-900/30 rounded-lg border border-orange-500/50">
<div class="font-bold text-orange-300 mb-1">End of Year 1</div>
<div class="text-gray-300">Total Investment: $1,060,000</div>
<div class="text-gray-300">Savings Realized: $635,000</div>
<div class="text-red-400 font-bold mt-1">Net Position: -$425,000 (investment phase)</div>
</div>
<div class="p-3 bg-green-900/30 rounded-lg border border-green-500/50">
<div class="font-bold text-green-300 mb-1">End of Year 2</div>
<div class="text-gray-300">Additional Investment: $0</div>
<div class="text-gray-300">Annual Savings: $1,486,000</div>
<div class="text-green-400 font-bold mt-1">Cumulative Net: +$1,061,000</div>
</div>
<div class="p-3 bg-green-900/30 rounded-lg border border-green-500/50">
<div class="font-bold text-green-300 mb-1">End of Year 3</div>
<div class="text-gray-300">Cumulative Savings: $3,607,000</div>
<div class="text-gray-300">Total Investment: $1,060,000</div>
<div class="text-green-400 font-bold mt-1">Net Position: +$2,547,000</div>
<div class="text-cyan-400 font-bold">3-Year ROI: 240%</div>
</div>
</div>
</div>
<div>
<h3 class="text-xl font-bold text-green-400 mb-4">📈 The Multiplier Effect</h3>
<div class="space-y-3 text-sm">
<div class="p-3 bg-blue-900/40 rounded-lg border border-blue-500/50">
<div class="font-bold text-blue-300 mb-1">1. Infrastructure Amortization</div>
<div class="text-gray-300">Same $1M investment for 50 or 500 engineers</div>
<div class="text-blue-400 mt-1">At 500 engineers: ~1 month payback</div>
</div>
<div class="p-3 bg-purple-900/40 rounded-lg border border-purple-500/50">
<div class="font-bold text-purple-300 mb-1">2. Learning Curve Benefits</div>
<div class="text-gray-300">Rules become comprehensive, docs improve, coverage increases</div>
<div class="text-purple-400 mt-1">Each improvement reduces future iteration costs</div>
</div>
<div class="p-3 bg-cyan-900/40 rounded-lg border border-cyan-500/50">
<div class="font-bold text-cyan-300 mb-1">3. Capacity Multiplication</div>
<div class="text-gray-300">Shift from 60/40 routine/strategic to 20/80</div>
<div class="text-cyan-400 mt-1">50% more strategic output per developer</div>
</div>
</div>
</div>
</div>

---

# Critical Success Factors

<div class="grid grid-cols-2 gap-3 text-xs">
<div class="p-3 bg-red-900/30 rounded-lg border border-red-500/50">
<div class="flex items-center gap-2 mb-1">
<span class="text-xl">⚠️</span>
<div class="text-red-400 font-bold text-sm">Quality Assurance</div>
</div>
<div class="text-gray-300 mb-1">25% AI code error rate without verification</div>
<div class="text-white">• 80%+ test coverage (mandatory)</div>
<div class="text-white">• Security scanning in CI/CD</div>
<div class="text-white">• Budget 30-50% time for review</div>
</div>
<div class="p-3 bg-orange-900/30 rounded-lg border border-orange-500/50">
<div class="flex items-center gap-2 mb-1">
<span class="text-xl">🏢</span>
<div class="text-orange-400 font-bold text-sm">Organizational Readiness</div>
</div>
<div class="text-gray-300 mb-1">Only 5% of AI pilots deliver bottom-line impact</div>
<div class="text-white">• Executive sponsorship</div>
<div class="text-white">• Change management: 20-30% of budget</div>
<div class="text-white">• Cross-functional collaboration</div>
</div>
<div class="p-3 bg-yellow-900/30 rounded-lg border border-yellow-500/50">
<div class="flex items-center gap-2 mb-1">
<span class="text-xl">🎓</span>
<div class="text-yellow-400 font-bold text-sm">Skill Development</div>
</div>
<div class="text-gray-300 mb-1">Prevent developer skill atrophy</div>
<div class="text-white">• Ongoing training in fundamentals</div>
<div class="text-white">• Rotate AI-assisted & manual work</div>
<div class="text-white">• Treat AI output as "junior developer code"</div>
</div>
<div class="p-3 bg-blue-900/30 rounded-lg border border-blue-500/50">
<div class="flex items-center gap-2 mb-1">
<span class="text-xl">📊</span>
<div class="text-blue-400 font-bold text-sm">Realistic Expectations</div>
</div>
<div class="text-gray-300 mb-1">Actual gains after review time</div>
<div class="text-white">• First 6 months: Learning curve</div>
<div class="text-white">• Months 6-12: 5-10% improvement</div>
<div class="text-white">• Year 2: Full 15-20% labor shift</div>
</div>
<div class="p-3 bg-purple-900/30 rounded-lg border border-purple-500/50">
<div class="flex items-center gap-2 mb-1">
<span class="text-xl">🔒</span>
<div class="text-purple-400 font-bold text-sm">Security & Compliance</div>
</div>
<div class="text-gray-300 mb-1">45% fail standard security tests</div>
<div class="text-white">• Automated security scanning</div>
<div class="text-white">• Dependency vulnerability analysis</div>
<div class="text-white">• Compliance rule codification</div>
</div>
<div class="p-3 bg-cyan-900/30 rounded-lg border border-cyan-500/50">
<div class="flex items-center gap-2 mb-1">
<span class="text-xl">💰</span>
<div class="text-cyan-400 font-bold text-sm">Hidden Costs</div>
</div>
<div class="text-gray-300 mb-1">Add 40-60% contingency</div>
<div class="text-white">• Legacy system integration</div>
<div class="text-white">• Technical debt remediation</div>
<div class="text-white">• Extended change management</div>
</div>
</div>

---

# The Leadership Calculation

<div class="p-6 bg-gradient-to-br from-blue-900/40 to-cyan-900/40 rounded-xl border border-blue-500/50">
<h3 class="text-2xl font-bold text-cyan-400 mb-4 text-center">Executive Summary</h3>
<div class="grid grid-cols-2 gap-4 text-sm">
<div>
<div class="mb-3">
<div class="font-bold text-green-400 mb-1">💰 The Opportunity</div>
<div class="text-gray-300">• Agent labor: $2-5/hr vs. $85-130/hr human</div>
<div class="text-gray-300">• 20% of work suitable for agents</div>
<div class="text-gray-300">• $1.5-2M savings per 50 engineers</div>
</div>
<div class="mb-3">
<div class="font-bold text-blue-400 mb-1">📊 The Investment</div>
<div class="text-gray-300">• Infrastructure: $800K-1.6M (+ contingency)</div>
<div class="text-gray-300">• Timeline: 12-18 months</div>
<div class="text-gray-300">• 3-year ROI: 240-350%</div>
</div>
</div>
<div>
<div class="mb-3">
<div class="font-bold text-orange-400 mb-1">⚠️ The Constraints</div>
<div class="text-gray-300">• Automated verification (non-negotiable)</div>
<div class="text-gray-300">• Knowledge codification required</div>
<div class="text-gray-300">• Only 13-15% of AI projects achieve ROI</div>
<div class="text-gray-300">• Success rate requires exceptional execution</div>
</div>
<div>
<div class="font-bold text-cyan-400 mb-1">🎯 The Recommendation</div>
<div class="text-gray-300">• Start with quick wins</div>
<div class="text-gray-300">• Invest in instrumentation</div>
<div class="text-gray-300">• Set realistic expectations (5-10% initial)</div>
<div class="text-gray-300">• Accept 12-18 month payback as normal</div>
</div>
</div>
</div>
</div>
<div class="mt-4 p-4 bg-gradient-to-r from-green-600/30 to-cyan-600/30 rounded-xl border border-green-500/50">
<div class="text-lg font-bold text-white text-center">🔑 The Bottom Line</div>
<div class="text-sm text-gray-200 mt-2 text-center">
Organizations that invest now with disciplined execution will achieve 15-20% labor arbitrage within 18-24 months.
Those that wait face a widening competitive gap. But success requires exceptional execution, honest expectations, and proper infrastructure investment.
</div>
</div>

---
layout: center
---

# The $2/Hour Future

<div class="max-w-4xl mx-auto">
<div class="p-8 bg-gradient-to-br from-blue-900/40 via-cyan-900/30 to-green-900/40 rounded-2xl border border-cyan-500/50 shadow-2xl">
<div class="text-center mb-6">
<div class="text-6xl font-bold bg-gradient-to-r from-blue-400 via-cyan-400 to-green-400 bg-clip-text text-transparent mb-3">
$2-5/hour
</div>
<div class="text-xl text-gray-300">AI agent labor vs. $85-130/hour human engineers</div>
</div>
<div class="space-y-4 text-base text-gray-300">
<p class="leading-relaxed">
The math is compelling. The barriers are real but surmountable. Organizations that do this work will operate with a fundamentally different cost structure—potentially <span class="text-green-400 font-semibold">15-20% more efficient</span> on significant portions of engineering labor.
</p>
<p class="leading-relaxed">
<span class="text-cyan-400 font-semibold">The question isn't whether we can afford to invest in agentic infrastructure.</span>
</p>
<p class="leading-relaxed">
<span class="text-orange-400 font-semibold">The question is whether we can afford not to—and whether we're willing to do it right.</span>
</p>
<div class="mt-6 p-4 bg-gradient-to-r from-cyan-600/30 to-blue-600/30 rounded-lg border border-cyan-500/50 text-center">
<div class="text-lg font-bold text-white italic">
"The organizations that win aren't those that hire the most engineers.<br/>They're those that multiply the capacity of the engineers they have."
</div>
</div>
</div>
</div>
</div>
