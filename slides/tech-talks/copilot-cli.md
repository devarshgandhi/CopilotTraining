---
theme: default
class: text-center
highlighter: shiki
lineNumbers: false
info: |
  ## GitHub Copilot CLI
  Terminal-Native AI for Developers and DevOps
drawings:
  persist: false
transition: slide-left
title: GitHub Copilot CLI
module: tech-talks/copilot-cli
status: active
updated: 2026-03-17
mdc: true
---

<div class="h-full flex flex-col items-center justify-center relative overflow-hidden">
<div class="absolute inset-0 bg-gradient-to-br from-cyan-900/20 via-blue-900/10 to-indigo-900/20"></div>
<div class="absolute top-1/4 left-1/2 -translate-x-1/2 -translate-y-1/2 w-96 h-96 bg-gradient-to-r from-cyan-500/20 via-blue-500/20 to-indigo-500/20 rounded-full blur-3xl"></div>
<div class="relative z-10">
<div class="absolute inset-0 blur-2xl opacity-50"><img src="../sdp-logo.png" class="w-64" alt="" /></div>
<img src="../sdp-logo.png" class="w-64 relative" alt="SDP Logo" />
</div>
<h1 class="!text-5xl !font-bold !mt-8 bg-gradient-to-r from-cyan-400 via-blue-400 to-indigo-400 bg-clip-text text-transparent relative z-10">GitHub Copilot CLI</h1>
<div class="mt-4 relative z-10">
<span class="px-6 py-2 bg-gradient-to-r from-cyan-600/80 to-blue-600/80 rounded-full text-white text-xl font-medium shadow-lg shadow-cyan-500/25">Terminal-Native AI</span>
</div>
<div class="mt-8 text-lg opacity-70 relative z-10">For Developers & DevOps Engineers</div>
<div class="mt-6 w-32 h-1 bg-gradient-to-r from-transparent via-cyan-400 to-transparent rounded-full relative z-10"></div>
</div>
<div class="abs-br m-6 flex gap-2"><span class="text-sm opacity-50">Tech Talk · 45 minutes</span></div>

---
layout: center
---

# 🎯 The Question This Talk Answers

<div class="p-8 bg-gradient-to-r from-cyan-500/10 to-blue-500/10 rounded-xl border border-cyan-500/30 mb-8 text-center max-w-4xl mx-auto">
<div class="text-2xl font-medium mb-4">How do I bring AI into my terminal workflow?</div>
<div class="text-lg opacity-90">Whether building something new, debugging my own code, or managing infrastructure</div>
</div>

<div class="grid grid-cols-3 gap-6 max-w-5xl mx-auto">
<div class="p-5 bg-gradient-to-br from-cyan-900/30 to-blue-900/30 rounded-xl border border-cyan-500/30">
<div class="text-3xl mb-3">🔧</div>
<div class="text-lg font-medium">Developers</div>
<div class="text-sm opacity-80 mt-2">Building new software, scaffolding projects</div>
</div>
<div class="p-5 bg-gradient-to-br from-blue-900/30 to-indigo-900/30 rounded-xl border border-blue-500/30">
<div class="text-3xl mb-3">🐛</div>
<div class="text-lg font-medium">Debugging</div>
<div class="text-sm opacity-80 mt-2">Troubleshooting your own failing code</div>
</div>
<div class="p-5 bg-gradient-to-br from-indigo-900/30 to-purple-900/30 rounded-xl border border-indigo-500/30">
<div class="text-3xl mb-3">⚙️</div>
<div class="text-lg font-medium">DevOps</div>
<div class="text-sm opacity-80 mt-2">Managing infrastructure and deployments</div>
</div>
</div>

---
layout: center
---

# 📖 Table of Contents

<div class="grid grid-cols-2 gap-6 max-w-4xl mx-auto">
<div @click="$nav.go(6)" class="cursor-pointer p-6 bg-gradient-to-br from-cyan-900/30 to-blue-900/30 rounded-xl border border-cyan-500/30 hover:scale-105 transition-all">
<div class="text-3xl mb-3">🎯</div>
<div class="text-xl font-bold bg-gradient-to-r from-cyan-400 to-blue-400 bg-clip-text text-transparent">Plan Mode</div>
<div class="text-sm opacity-80 mt-2">Collaborative planning before implementation</div>
</div>
<div @click="$nav.go(10)" class="cursor-pointer p-6 bg-gradient-to-br from-blue-900/30 to-indigo-900/30 rounded-xl border border-blue-500/30 hover:scale-105 transition-all">
<div class="text-3xl mb-3">⚡</div>
<div class="text-xl font-bold bg-gradient-to-r from-blue-400 to-indigo-400 bg-clip-text text-transparent">Operating Modes</div>
<div class="text-sm opacity-80 mt-2">Interactive, programmatic, and cloud delegation</div>
</div>
<div @click="$nav.go(14)" class="cursor-pointer p-6 bg-gradient-to-br from-indigo-900/30 to-purple-900/30 rounded-xl border border-indigo-500/30 hover:scale-105 transition-all">
<div class="text-3xl mb-3">🧠</div>
<div class="text-xl font-bold bg-gradient-to-r from-indigo-400 to-purple-400 bg-clip-text text-transparent">Built-in Agents</div>
<div class="text-sm opacity-80 mt-2">Specialized agents and parallel execution</div>
</div>
<div @click="$nav.go(17)" class="cursor-pointer p-6 bg-gradient-to-br from-purple-900/30 to-pink-900/30 rounded-xl border border-purple-500/30 hover:scale-105 transition-all">
<div class="text-3xl mb-3">🚀</div>
<div class="text-xl font-bold bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">Use Cases</div>
<div class="text-sm opacity-80 mt-2">Real-world patterns with metrics</div>
</div>
</div>

---

# 🎯 Objectives

<div class="mb-3 text-base font-medium opacity-80">By the end of this talk, you will:</div>

<div class="grid grid-cols-2 auto-rows-fr gap-3" style="height: 430px">

<div class="p-5 bg-gradient-to-r from-cyan-500/10 to-blue-500/10 rounded-lg border border-cyan-500/20 flex items-start gap-3">
<span class="text-xl flex-shrink-0">✅</span><div><div class="font-semibold text-base">Understand when CLI beats IDE</div><div class="text-sm opacity-70 mt-1">Terminal sees runtime context; IDE only sees source files</div></div>
</div>

<div class="p-5 bg-gradient-to-r from-blue-500/10 to-indigo-500/10 rounded-lg border border-blue-500/20 flex items-start gap-3">
<span class="text-xl flex-shrink-0">✅</span><div><div class="font-semibold text-base">Leverage /fleet for parallel orchestration</div><div class="text-sm opacity-70 mt-1">Explicitly decompose work across subagents</div></div>
</div>

<div class="p-5 bg-gradient-to-r from-cyan-500/10 to-blue-500/10 rounded-lg border border-cyan-500/20 flex items-start gap-3">
<span class="text-xl flex-shrink-0">✅</span><div><div class="font-semibold text-base">Use Plan Mode to reduce debugging cycles</div><div class="text-sm opacity-70 mt-1">8 attempts → 2 with collaborative planning</div></div>
</div>

<div class="p-5 bg-gradient-to-r from-blue-500/10 to-indigo-500/10 rounded-lg border border-blue-500/20 flex items-start gap-3">
<span class="text-xl flex-shrink-0">✅</span><div><div class="font-semibold text-base">Integrate GitHub.com workflows</div><div class="text-sm opacity-70 mt-1">Issues, PRs, and Actions from the terminal</div></div>
</div>

<div class="p-5 bg-gradient-to-r from-cyan-500/10 to-blue-500/10 rounded-lg border border-cyan-500/20 flex items-start gap-3">
<span class="text-xl flex-shrink-0">✅</span><div><div class="font-semibold text-base">Know when to delegate to cloud agents</div><div class="text-sm opacity-70 mt-1">Free your IDE and terminal for other work</div></div>
</div>

<div class="p-5 bg-gradient-to-r from-blue-500/10 to-indigo-500/10 rounded-lg border border-blue-500/20 flex items-start gap-3">
<span class="text-xl flex-shrink-0">✅</span><div><div class="font-semibold text-base">Automate CI/CD with programmatic mode</div><div class="text-sm opacity-70 mt-1">Build failure analysis in GitHub Actions</div></div>
</div>

</div>

---
layout: center
---

# 🧠 Mental Model Shift

<div class="max-w-5xl mx-auto">

<div class="text-center mb-8">
<div class="text-2xl font-bold bg-gradient-to-r from-cyan-400 to-blue-400 bg-clip-text text-transparent">From Command Execution to AI Collaboration</div>
<div class="text-lg opacity-80 mt-2">Terminal as a thought partner, not just a command processor</div>
</div>

<div class="grid grid-cols-2 gap-6">
<div class="space-y-4">
<div class="text-lg font-bold text-cyan-400 mb-3">✅ Move Toward</div>
<div class="p-4 bg-gradient-to-r from-green-500/10 to-emerald-500/10 rounded-lg border border-green-500/20">
<div class="font-medium mb-2">AI as thought partner for greenfield work</div>
<div class="text-sm opacity-80">90 min library research → 15 min with scaffold</div>
</div>
<div class="p-4 bg-gradient-to-r from-green-500/10 to-emerald-500/10 rounded-lg border border-green-500/20">
<div class="font-medium mb-2">Plan before you build (Shift+Tab)</div>
<div class="text-sm opacity-80">8 debugging attempts → 2</div>
</div>
<div class="p-4 bg-gradient-to-r from-green-500/10 to-emerald-500/10 rounded-lg border border-green-500/20">
<div class="font-medium mb-2">Delegate long-running tasks with `&`</div>
<div class="text-sm opacity-80">IDE and terminal stay completely free</div>
</div>
</div>
<div class="space-y-4">
<div class="text-lg font-bold text-red-400 mb-3">🛑 Move Against</div>
<div class="p-4 bg-gradient-to-r from-red-500/10 to-orange-500/10 rounded-lg border border-red-500/20">
<div class="font-medium mb-2">Pasting secrets into prompts</div>
<div class="text-sm opacity-80">Use env vars or secret managers</div>
</div>
<div class="p-4 bg-gradient-to-r from-red-500/10 to-orange-500/10 rounded-lg border border-red-500/20">
<div class="font-medium mb-2">`--yolo` outside sandboxed environments</div>
<div class="text-sm opacity-80">Approve per-tool or per-session</div>
</div>
<div class="p-4 bg-gradient-to-r from-red-500/10 to-orange-500/10 rounded-lg border border-red-500/20">
<div class="font-medium mb-2">Skipping Plan Mode when in a hurry</div>
<div class="text-sm opacity-80">Most valuable precisely when rushing</div>
</div>
</div>
</div>

</div>

---
layout: center
name: planmode
---

<div class="text-center mb-6">
<div class="text-5xl mb-4">🎯</div>
<h1 class="!text-4xl bg-gradient-to-r from-cyan-400 to-blue-400 bg-clip-text text-transparent">Plan Mode & Steering</h1>
<p class="text-xl opacity-80 mt-2">Collaborative planning before implementation</p>
</div>
<div class="p-5 bg-gradient-to-r from-cyan-500/10 to-blue-500/10 rounded-xl border border-cyan-500/30 mb-5 text-center max-w-3xl mx-auto">
<div class="text-lg">Transform debugging from trial-and-error to collaborative strategy</div>
</div>

---

# 🎯 Plan Mode: The Fundamental Shift

<div class="grid grid-cols-2 gap-8 max-w-6xl mx-auto">
<div class="p-6 bg-gradient-to-br from-red-900/30 to-orange-900/30 rounded-xl border border-red-500/30">
<div class="text-2xl font-bold text-red-400 mb-4">❌ Traditional Workflow</div>
<div class="space-y-3">
<div class="flex items-start gap-3">
<div class="text-2xl">1️⃣</div>
<div>
<div class="font-medium">Make request</div>
<div class="text-sm opacity-80">Describe what you want</div>
</div>
</div>
<div class="flex items-start gap-3">
<div class="text-2xl">2️⃣</div>
<div>
<div class="font-medium">AI generates solution</div>
<div class="text-sm opacity-80">Guesses at ambiguities</div>
</div>
</div>
<div class="flex items-start gap-3">
<div class="text-2xl">3️⃣</div>
<div>
<div class="font-medium">You review and fix</div>
<div class="text-sm opacity-80">Find where it guessed wrong</div>
</div>
</div>
<div class="flex items-start gap-3">
<div class="text-2xl">🔄</div>
<div>
<div class="font-medium text-red-400">Repeat (8 attempts average)</div>
<div class="text-sm opacity-80">Most rework from ambiguous starts</div>
</div>
</div>
</div>
</div>
<div class="p-6 bg-gradient-to-br from-green-900/30 to-emerald-900/30 rounded-xl border border-green-500/30">
<div class="text-2xl font-bold text-green-400 mb-4">✨ Plan Mode Workflow</div>
<div class="space-y-3">
<div class="flex items-start gap-3">
<div class="text-2xl">1️⃣</div>
<div>
<div class="font-medium">Make request</div>
<div class="text-sm opacity-80">Describe what you want</div>
</div>
</div>
<div class="flex items-start gap-3">
<div class="text-2xl">2️⃣</div>
<div>
<div class="font-medium">AI asks clarifying questions</div>
<div class="text-sm opacity-80">Uses `ask_user` tool for ambiguities</div>
</div>
</div>
<div class="flex items-start gap-3">
<div class="text-2xl">3️⃣</div>
<div>
<div class="font-medium">Collaborate on plan</div>
<div class="text-sm opacity-80">Review strategy before code</div>
</div>
</div>
<div class="flex items-start gap-3">
<div class="text-2xl">4️⃣</div>
<div>
<div class="font-medium text-green-400">Generate implementation (2 attempts)</div>
<div class="text-sm opacity-80">Misunderstandings caught early</div>
</div>
</div>
</div>
</div>
</div>

<div class="mt-6 p-4 bg-gradient-to-r from-cyan-500/10 to-blue-500/10 rounded-lg border border-cyan-500/20 text-center">
<div class="text-lg font-medium">Press <kbd class="px-2 py-1 bg-gray-800 rounded border border-gray-600">Shift+Tab</kbd> to toggle Plan Mode on/off</div>
</div>

---

# 🎯 Real-Time Steering

<div class="max-w-5xl mx-auto space-y-6">

<div class="p-6 bg-gradient-to-br from-cyan-900/30 to-blue-900/30 rounded-xl border border-cyan-500/30">
<div class="text-xl font-bold mb-4 text-cyan-400">Enqueue Additional Messages</div>
<div class="mb-3">Send follow-up instructions to adjust direction while Copilot is thinking:</div>
<div class="p-4 bg-gray-800/50 rounded-lg font-mono text-sm">
<div class="text-gray-400"># While Copilot analyzes Docker logs:</div>
<div class="text-cyan-300">&gt; "Also check if Redis is running"</div>
<div class="text-cyan-300">&gt; "Focus on authentication-related errors first"</div>
</div>
<div class="text-sm opacity-80 mt-3">Messages queue up and influence the current response</div>
</div>

<div class="p-6 bg-gradient-to-br from-blue-900/30 to-indigo-900/30 rounded-xl border border-blue-500/30">
<div class="text-xl font-bold mb-4 text-blue-400">Inline Feedback on Rejection</div>
<div class="mb-3">Reject tool permissions and explain why in one step:</div>
<div class="p-4 bg-gray-800/50 rounded-lg font-mono text-sm">
<div class="text-gray-400"># Copilot wants to run `rm -rf tmp/*`</div>
<div class="text-yellow-300">&gt; [Press Esc] "Don't delete tmp/ — it has cached artifacts we need"</div>
</div>
<div class="text-sm opacity-80 mt-3">Copilot adapts approach without stopping entirely</div>
</div>

<div class="p-4 bg-gradient-to-r from-green-500/10 to-emerald-500/10 rounded-lg border border-green-500/20 text-center">
<div class="font-medium">✅ Steering enables mid-flight corrections without restarting the entire conversation</div>
</div>

</div>

---

# 🎯 Example: Docker Debugging with Plan Mode

<div class="max-w-5xl mx-auto">

<div class="p-5 bg-gray-800/50 rounded-xl border border-cyan-500/30 font-mono text-sm space-y-3">
<div><span class="text-blue-400">$</span> <span class="text-white">copilot</span></div>
<div><span class="text-cyan-300">&gt;</span> <span class="text-white">"Debug why the backend container won't start"</span></div>
<div class="h-px bg-gray-700 my-3"></div>
<div class="text-yellow-300">🤔 Copilot (Plan Mode):</div>
<div class="text-gray-300 ml-4">I can help with that. Before I start, a few questions:</div>
<div class="text-gray-300 ml-4">1. Should I check docker-compose configuration, container logs, or both?</div>
<div class="text-gray-300 ml-4">2. Do you want environment variable analysis?</div>
<div class="text-gray-300 ml-4">3. Any recent changes to services or network configuration?</div>
<div class="h-px bg-gray-700 my-3"></div>
<div><span class="text-cyan-300">&gt;</span> <span class="text-white">"Start with logs, then check config if needed"</span></div>
<div class="h-px bg-gray-700 my-3"></div>
<div class="text-yellow-300">🤔 Copilot:</div>
<div class="text-gray-300 ml-4">Understood. Here's my plan:</div>
<div class="text-gray-300 ml-4">1. Retrieve container logs for backend service</div>
<div class="text-gray-300 ml-4">2. Analyze error patterns and stack traces</div>
<div class="text-gray-300 ml-4">3. If logs suggest config issue, inspect docker-compose.yml</div>
<div class="text-gray-300 ml-4">4. Check environment variables if authentication/connection errors found</div>
<div class="text-gray-300 ml-4 mt-3">Proceed with this plan? (y/n)</div>
<div class="h-px bg-gray-700 my-3"></div>
<div><span class="text-cyan-300">&gt;</span> <span class="text-white">y</span></div>
<div class="h-px bg-gray-700 my-3"></div>
<div class="text-green-300">✅ Copilot:</div>
<div class="text-gray-300 ml-4">[Executes plan, finds misconfigured port binding in docker-compose.yml]</div>
<div class="text-gray-300 ml-4">Found: Port 5000 mapped to 5001, but app expects 5000 internally.</div>
<div class="text-gray-300 ml-4">Fix: Change service.ports from "5001:5000" to "5000:5000"</div>
<div class="text-gray-300 ml-4 mt-3">Apply this fix? (y/n)</div>
</div>

<div class="mt-6 p-5 bg-gradient-to-r from-green-500/10 to-emerald-500/10 rounded-xl border border-green-500/20">
<div class="grid grid-cols-2 gap-6">
<div>
<div class="text-sm opacity-70">Before Plan Mode</div>
<div class="text-2xl font-bold text-red-400">45 minutes</div>
<div class="text-sm opacity-80">8 trial-and-error attempts</div>
</div>
<div>
<div class="text-sm opacity-70">With Plan Mode</div>
<div class="text-2xl font-bold text-green-400">8 minutes</div>
<div class="text-sm opacity-80">2 targeted checks</div>
</div>
</div>
</div>

</div>

---
layout: center
name: operatingmodes
---

<div class="text-center mb-6">
<div class="text-5xl mb-4">⚡</div>
<h1 class="!text-4xl bg-gradient-to-r from-blue-400 to-indigo-400 bg-clip-text text-transparent">Operating Modes</h1>
<p class="text-xl opacity-80 mt-2">Interactive, programmatic, and cloud delegation</p>
</div>
<div class="p-5 bg-gradient-to-r from-blue-500/10 to-indigo-500/10 rounded-xl border border-blue-500/30 mb-5 text-center max-w-3xl mx-auto">
<div class="text-lg">Choose the right mode for the task — collaborative debugging, headless automation, or background execution</div>
</div>

---

# The Solution: GitHub Copilot CLI

<div class="text-sm space-y-4 mt-4">

**Conversational AI directly in terminal workflows — interactive, autonomous, and IDE-independent**

<div class="grid grid-cols-3 gap-4 mt-4">

<div class="p-3 bg-emerald-900/40 rounded-lg border border-emerald-500/50">
<div class="text-xl mb-1">🤝</div>
<div class="font-semibold mb-1">Plan Mode</div>
<div class="text-xs opacity-90">Collaborative planning with clarifying questions before code — reduces iterations from 8 to 2</div>
</div>

<div class="p-3 bg-teal-900/40 rounded-lg border border-teal-500/50">
<div class="text-xl mb-1">💬</div>
<div class="font-semibold mb-1">Interactive Mode</div>
<div class="text-xs opacity-90">Terminal-native conversations with persistent context — perfect for "figure this out" scenarios</div>
</div>

<div class="p-3 bg-cyan-900/40 rounded-lg border border-cyan-500/50">
<div class="text-xl mb-1">🔄</div>
<div class="font-semibold mb-1">Programmatic Mode</div>
<div class="text-xs opacity-90">Single-command headless execution for CI/CD pipelines — structured output for scripts</div>
</div>

<div class="p-3 bg-blue-900/40 rounded-lg border border-blue-500/50">
<div class="text-xl mb-1">☁️</div>
<div class="font-semibold mb-1">Cloud Delegation</div>
<div class="text-xs opacity-90"><code>&</code> prefix offloads long tasks to GitHub's agent — IDE and terminal both stay completely free</div>
</div>

<div class="p-3 bg-violet-900/40 rounded-lg border border-violet-500/50">
<div class="text-xl mb-1">🤖</div>
<div class="font-semibold mb-1">Built-in Agents</div>
<div class="text-xs opacity-90">Explore, Task, Plan, Code-review — routed automatically based on intent, run in parallel</div>
</div>

<div class="p-3 bg-indigo-900/40 rounded-lg border border-indigo-500/50">
<div class="text-xl mb-1">🪟</div>
<div class="font-semibold mb-1">IDE Bridge <code>/ide</code></div>
<div class="text-xs opacity-90">Open any file in VS Code mid-session — CLI context and conversation stay fully alive</div>
</div>

<div class="p-3 bg-sky-900/40 rounded-lg border border-sky-500/50 col-span-2">
<div class="text-xl mb-1">🧠</div>
<div class="font-semibold mb-1">Repository Memory + Auto-Compaction</div>
<div class="text-xs opacity-90">AI learns your conventions across sessions; auto-compaction at 95% token limit makes sessions virtually infinite</div>
</div>

<div class="p-3 bg-slate-900/40 rounded-lg border border-slate-500/50">
<div class="text-xl mb-1">🧩</div>
<div class="font-semibold mb-1">MCP Integration</div>
<div class="text-xs opacity-90">Discover and connect external tools via GitHub MCP Registry with org-level governance</div>
</div>

</div>

</div>

---

# Latest CLI Updates

<div class="grid grid-cols-2 gap-6 mt-6 text-xs">

<div class="p-4 bg-emerald-900/40 rounded-lg border border-emerald-500/50">
<div class="text-2xl mb-2">🧠</div>
<div class="font-bold mb-2">Configurable Reasoning Models</div>
<div class="opacity-90">GPT-5.2-Codex with effort tiers (low → extra high) and Ctrl+T reasoning visibility</div>
</div>

<div class="p-4 bg-teal-900/40 rounded-lg border border-teal-500/50">
<div class="text-2xl mb-2">⚡</div>
<div class="font-bold mb-2">Performance & UX Upgrades</div>
<div class="opacity-90">~45% faster output, richer diffs/timelines, prefix-aware history filtering, Windows/PowerShell polish</div>
</div>

</div>

---
layout: center
name: plan-mode
---

<!-- 🎬 MAJOR SECTION: Plan Mode & Steering -->

<div class="text-center">
  <div class="text-6xl mb-6">🎯</div>
  <h1 class="text-5xl font-bold bg-gradient-to-r from-emerald-400 to-teal-400 bg-clip-text text-transparent">
    Plan Mode
  </h1>
  <div class="text-2xl mt-4 opacity-80">
    Collaborative Planning Before Implementation
  </div>
</div>

---

# Plan Mode: The Fundamental Shift

<div class="mt-8 space-y-6 text-sm">

<div class="p-5 bg-red-900/40 rounded-lg border-2 border-red-500/50">
<div class="text-xl font-bold mb-3">❌ Traditional Workflow</div>
<div class="flex items-center gap-3">
<div>Request</div>
<div class="text-2xl">→</div>
<div>AI generates solution</div>
<div class="text-2xl">→</div>
<div>Review and fix</div>
<div class="text-2xl">→</div>
<div>Repeat (8 attempts average)</div>
</div>
</div>

<div class="p-5 bg-emerald-900/40 rounded-lg border-2 border-emerald-500/50">
<div class="text-xl font-bold mb-3">✅ Plan Mode Workflow</div>
<div class="flex items-center gap-3">
<div>Request</div>
<div class="text-2xl">→</div>
<div>AI asks questions</div>
<div class="text-2xl">→</div>
<div>Collaborate on plan</div>
<div class="text-2xl">→</div>
<div>Generate (2 attempts average)</div>
</div>
</div>

<div class="p-5 bg-gradient-to-r from-emerald-600 to-teal-600 rounded-xl text-center">
<div class="text-lg font-bold">Press Shift+Tab to toggle Plan Mode • Reduces debugging cycles by 75%</div>
</div>

</div>

---

# Real-Time Steering

<div class="grid grid-cols-2 gap-6 mt-6 text-sm">

<div class="p-5 bg-blue-900/40 rounded-lg border border-blue-500/50">
<div class="text-2xl mb-3">💬</div>
<div class="font-bold mb-3">Enqueue Messages</div>
<div class="space-y-2">
<div class="opacity-90">Send follow-up instructions mid-response:</div>
<div class="font-mono text-xs bg-black/40 p-3 rounded">
> "Also check if Redis is running"<br/>
> "Focus on auth errors first"
</div>
<div class="text-xs opacity-70 mt-2">Steer direction while Copilot is thinking</div>
</div>
</div>

<div class="p-5 bg-purple-900/40 rounded-lg border border-purple-500/50">
<div class="text-2xl mb-3">⏹️</div>
<div class="font-bold mb-3">Inline Feedback on Rejection</div>
<div class="space-y-2">
<div class="opacity-90">Reject with explanation:</div>
<div class="font-mono text-xs bg-black/40 p-3 rounded">
[Esc] "Don't delete tmp/ — it has<br/>
cached artifacts we need"
</div>
<div class="text-xs opacity-70 mt-2">Copilot adapts without stopping</div>
</div>
</div>

</div>

<div class="mt-6 p-4 bg-gradient-to-r from-blue-600/40 to-purple-600/40 rounded-lg">
<div class="font-semibold">Advanced: Ctrl+T toggles reasoning visibility to see AI's thought process</div>
</div>

---

# Example: Docker Debugging with Plan Mode

<div class="text-xs space-y-3 mt-4">

```bash
$ copilot
> "Debug why the backend container won't start"

🤔 Copilot (Plan Mode):
Before I start, a few questions:
1. Should I check docker-compose config, container logs, or both?
2. Do you want environment variable analysis?
3. Any recent changes to services or network?

> "Start with logs, then check config if needed"

🤔 Copilot: Here's my plan:
1. Retrieve container logs for backend service
2. Analyze error patterns and stack traces
3. If logs suggest config issue, inspect docker-compose.yml

Proceed? (y/n)
```

</div>

<div class="mt-4 p-4 bg-emerald-900/40 rounded-lg border border-emerald-500/50">
<div class="font-bold">✅ Outcome: 45 minutes → 8 minutes (83% reduction)</div>
<div class="text-sm mt-2">Root cause: Misconfigured port binding found in 2 targeted checks vs 8 trial-and-error attempts</div>
</div>

---
layout: center
name: operating-modes
---

<!-- 🎬 MAJOR SECTION: Operating Modes -->

<div class="text-center">
  <div class="text-6xl mb-6">⚙️</div>
  <h1 class="text-5xl font-bold bg-gradient-to-r from-teal-400 to-cyan-400 bg-clip-text text-transparent">
    Operating Modes
  </h1>
  <div class="text-2xl mt-4 opacity-80">
    Interactive • Programmatic • Cloud Delegation
  </div>
</div>

---

# Three Operating Modes

<div class="grid grid-cols-3 gap-4 mt-6 text-xs">

<div class="p-4 bg-emerald-900/40 rounded-lg border border-emerald-500/50">
<div class="text-3xl mb-2">💬</div>
<div class="font-bold text-lg mb-2">Interactive</div>
<div class="font-mono text-xs mb-2">$ copilot</div>
<div class="space-y-2 opacity-90">
<div>✓ Conversational sessions</div>
<div>✓ Persistent context</div>
<div>✓ Plan Mode support</div>
<div>✓ Multi-turn debugging</div>
</div>
<div class="mt-3 pt-3 border-t border-emerald-500/30 text-xs font-semibold">
Best for: Complex debugging, unknown root causes
</div>
</div>

<div class="p-4 bg-teal-900/40 rounded-lg border border-teal-500/50">
<div class="text-3xl mb-2">🔄</div>
<div class="font-bold text-lg mb-2">Programmatic</div>
<div class="font-mono text-xs mb-2">$ copilot -p</div>
<div class="space-y-2 opacity-90">
<div>✓ Single-command</div>
<div>✓ Structured output</div>
<div>✓ Headless operation</div>
<div>✓ CI/CD ready</div>
</div>
<div class="mt-3 pt-3 border-t border-teal-500/30 text-xs font-semibold">
Best for: Automation, pipelines, scripts
</div>
</div>

<div class="p-4 bg-cyan-900/40 rounded-lg border border-cyan-500/50">
<div class="text-3xl mb-2">☁️</div>
<div class="font-bold text-lg mb-2">Cloud Delegation</div>
<div class="font-mono text-xs mb-2">$ copilot<br/>> "&task"</div>
<div class="space-y-2 opacity-90">
<div>✓ Background execution</div>
<div>✓ Terminal stays free</div>
<div>✓ GitHub cloud agents</div>
<div>✓ PR created on completion</div>
</div>
<div class="mt-3 pt-3 border-t border-cyan-500/30 text-xs font-semibold">
Best for: Large refactors, security audits
</div>
</div>

</div>

---

# CI/CD Build Failure Automation

<div class="text-xs mt-4">

```yaml
# .github/workflows/build.yml
name: Build and Analyze
on: [push, pull_request]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Build application
        run: npm run build

      - name: Analyze failure with Copilot CLI
        if: failure()
        env:
          GITHUB_TOKEN: ${{ secrets.COPILOT_GITHUB_TOKEN }}
        run: |
          npm install -g @github/copilot
          copilot -p "Analyze build failure. Check commits, deps, error patterns." \
            --allow-tool 'shell(gh)' --allow-tool 'shell(git)' > analysis.txt

      - name: Post analysis as comment
        if: failure()
        run: gh pr comment ${{ github.event.pull_request.number }} --body-file analysis.txt
```

</div>

<div class="mt-4 p-4 bg-emerald-900/40 rounded-lg border border-emerald-500/50">
<div class="font-bold">Impact: 25 minutes → 5 minutes investigation time</div>
<div class="text-sm mt-1">Zero human intervention for known failure types • Pattern recognition across historical failures</div>
</div>

---
layout: center
name: context-management
---

<!-- 🎬 MAJOR SECTION: Context Management -->

<div class="text-center">
  <div class="text-6xl mb-6">🧠</div>
  <h1 class="text-5xl font-bold bg-gradient-to-r from-cyan-400 to-blue-400 bg-clip-text text-transparent">
    Context Management
  </h1>
  <div class="text-2xl mt-4 opacity-80">
    Infinite Sessions • Repository Memory
  </div>
</div>

---

# Automatic Context Management

<div class="grid grid-cols-2 gap-6 mt-6 text-sm">

<div>

### ♾️ Infinite Sessions

<div class="space-y-3 mt-4">

**The problem:**
- Traditional AI: 12-20 exchanges then loses context

**The solution:**
- Auto-compaction at 95% token limit
- Important context persists
- Redundant details pruned
- No interruptions

**Monitoring tools:**
```bash
/context   # Token usage breakdown
/usage     # Session statistics
/compact   # Manually compress anytime
```

**Model & cost:**
- Default: `Claude Sonnet 4.5 (1x)`
- `/model` — switch models; multiplier shown per option
- 1x = 1 premium request per prompt; higher models cost more

</div>

</div>

<div>

### 🧠 Repository Memory

<div class="space-y-3 mt-4">

**What gets remembered:**
- Coding standards and conventions
- Project architecture patterns
- Preferred debugging approaches
- Configuration patterns

**Cross-session learning:**
```bash
Session 1 (Monday):
> [Explain docker-compose networking]

Session 2 (Wednesday):
> "Service A can't reach Service B"
✅ Copilot remembers network setup
```

</div>

</div>

</div>

---
layout: center
name: built-in-agents
---

<!-- 🎬 MAJOR SECTION: Built-in Agents -->

<div class="text-center">
  <div class="text-6xl mb-6">🤖</div>
  <h1 class="text-5xl font-bold bg-gradient-to-r from-blue-400 to-indigo-400 bg-clip-text text-transparent">
    Built-in Agents
  </h1>
  <div class="text-2xl mt-4 opacity-80">
    Automatic Expert Delegation
  </div>
</div>

---

# Four Specialized Agents

<div class="grid grid-cols-2 gap-4 mt-6 text-xs">

<div class="p-4 bg-blue-900/40 rounded-lg border border-blue-500/50">
<div class="text-2xl mb-2">🔍</div>
<div class="font-bold mb-2">Explore Agent</div>
<div class="opacity-90 mb-3">Fast codebase analysis</div>
<div class="space-y-1 text-xs">
<div>• Returns concise answers (&lt;300 words)</div>
<div>• Safe parallel execution</div>
<div>• Doesn't pollute main context</div>
</div>
<div class="font-mono text-xs mt-3 bg-black/40 p-2 rounded">
> "How does auth work?"
</div>
</div>

<div class="p-4 bg-indigo-900/40 rounded-lg border border-indigo-500/50">
<div class="text-2xl mb-2">⚡</div>
<div class="font-bold mb-2">Task Agent</div>
<div class="opacity-90 mb-3">Smart output filtering</div>
<div class="space-y-1 text-xs">
<div>• Brief summary on success</div>
<div>• Full output on failure</div>
<div>• Reduces conversation clutter</div>
</div>
<div class="font-mono text-xs mt-3 bg-black/40 p-2 rounded">
> "Run tests, tell me if failed"
</div>
</div>

<div class="p-4 bg-purple-900/40 rounded-lg border border-purple-500/50">
<div class="text-2xl mb-2">📋</div>
<div class="font-bold mb-2">Plan Agent</div>
<div class="opacity-90 mb-3">Multi-step strategies</div>
<div class="space-y-1 text-xs">
<div>• Analyzes dependencies</div>
<div>• Creates structured plans</div>
<div>• Surfaces risks upfront</div>
</div>
<div class="font-mono text-xs mt-3 bg-black/40 p-2 rounded">
> "Plan API versioning refactor"
</div>
</div>

<div class="p-4 bg-pink-900/40 rounded-lg border border-pink-500/50">
<div class="text-2xl mb-2">👀</div>
<div class="font-bold mb-2">Code-Review Agent</div>
<div class="opacity-90 mb-3">High signal-to-noise</div>
<div class="space-y-1 text-xs">
<div>• Only bugs and security issues</div>
<div>• Never style/formatting</div>
<div>• Focuses human attention</div>
</div>
<div class="font-mono text-xs mt-3 bg-black/40 p-2 rounded">
/review
</div>
</div>

</div>

<div class="mt-4 text-center text-sm">
<div class="font-semibold">✨ Copilot automatically routes tasks to the right agent — no explicit calls needed</div>
<div class="text-xs opacity-70 mt-1">Use <code>/ide &lt;file&gt;</code> at any point to open a file in VS Code — CLI conversation stays alive, use both tools simultaneously</div>
</div>

---

# ⚡ /fleet: Explicit Parallel Fan-Out

<div class="grid grid-cols-2 gap-6 mt-4 text-sm">
<div>
<div class="p-4 bg-cyan-900/30 rounded-lg border border-cyan-500/30 mb-3">
<div class="font-bold text-cyan-300 mb-2">What /fleet does</div>
<div class="text-xs space-y-1">
<div>1. Main agent <b>decomposes</b> your prompt into subtasks</div>
<div>2. Assesses dependencies — what can parallelize</div>
<div>3. Acts as <b>orchestrator</b>: assigns subtasks to subagents</div>
<div>4. Subagents run in <b>parallel</b>, each in own context window</div>
<div>5. Results merged back by orchestrator</div>
</div>
</div>
<div class="font-mono bg-gray-900/60 p-3 rounded text-xs">/fleet create a test suite:
  unit tests for auth,
  integration tests for API,
  e2e tests for login flow</div>
<div class="mt-2 text-xs opacity-70">Pair with plan mode: <b>Shift+Tab → plan → "Accept plan and build on autopilot + /fleet"</b></div>
</div>
<div>
<div class="space-y-2 text-xs">
<div class="p-2 bg-gray-900/50 rounded border border-green-500/30"><b class="text-green-400">Speed</b> — parallel subtasks complete in time of longest, not sum</div>
<div class="p-2 bg-gray-900/50 rounded border border-blue-500/30"><b class="text-blue-400">Context isolation</b> — each subagent has own window, no pollution</div>
<div class="p-2 bg-gray-900/50 rounded border border-purple-500/30"><b class="text-purple-400">Specialization</b> — custom agents (<code>@test-writer</code>, <code>@security-reviewer</code>) auto-matched to subtasks</div>
<div class="p-2 bg-gray-900/50 rounded border border-yellow-500/30"><b class="text-yellow-400">Model selection</b> — subagents default to low-cost; specify per-subtask in prompt</div>
</div>
<div class="mt-3 p-2 bg-orange-900/20 rounded border border-orange-500/20 text-xs">
<b class="text-orange-400">⚠️ Cost note:</b> Each subagent makes independent LLM calls — use <code>/model</code> to check multiplier before large /fleet runs
</div>
<div class="mt-2 p-2 bg-gray-900/40 rounded text-xs">
<b>Best for:</b> test suites, multi-module refactors, documentation across modules<br/>
<b>Not useful for:</b> inherently sequential tasks (step B needs step A's output)
</div>
</div>
</div>


---
layout: center
name: plugins
---

<!-- 🎬 MAJOR SECTION: Plugins -->

<div class="text-center">
  <div class="text-6xl mb-6">🔌</div>
  <h1 class="text-5xl font-bold bg-gradient-to-r from-violet-400 to-purple-400 bg-clip-text text-transparent">
    Plugins
  </h1>
  <div class="text-2xl mt-4 opacity-80">
    Extend CLI with Community Packages
  </div>
</div>

---

# Plugins: Extending Copilot CLI

<div class="grid grid-cols-2 gap-6 mt-6 text-xs">

<div class="space-y-4">

### What Plugins Are

<div class="opacity-90">
Packages that extend Copilot CLI's functionality beyond built-in capabilities — new tools, specialized workflows, domain-specific knowledge.
</div>

### Default Marketplaces

<div class="space-y-2 mt-3">
<div class="p-3 bg-violet-900/40 rounded-lg border border-violet-500/50">
<div class="font-bold">copilot-plugins</div>
<div class="text-xs opacity-80">GitHub's official plugin collection</div>
</div>
<div class="p-3 bg-purple-900/40 rounded-lg border border-purple-500/50">
<div class="font-bold">awesome-copilot</div>
<div class="text-xs opacity-80">Community-curated plugins</div>
</div>
</div>

</div>

<div class="space-y-4">

### Finding & Installing

```bash
# List registered marketplaces
copilot plugin marketplace list

# Browse a marketplace
copilot plugin marketplace browse awesome-copilot

# Install from marketplace
copilot plugin install database-data-management@awesome-copilot

# Install from GitHub repo
copilot plugin install OWNER/REPO

# Install from local path
copilot plugin install ./path/to/plugin
```

### Managing Plugins

```bash
copilot plugin list       # View installed
copilot plugin update X   # Update plugin
copilot plugin uninstall X
```

</div>

</div>

---

# Real-World Use Cases (1 of 2)

<div class="grid grid-cols-2 gap-4 mt-6 text-xs">
<div class="p-4 bg-emerald-900/40 rounded-lg border border-emerald-500/50">
<div class="font-bold text-sm mb-2">🌱 Greenfield Project Scaffolding</div>
<div class="opacity-90 mb-2">AI as thought partner for new projects</div>
<div class="space-y-1">
<div>⏱️ <strong>90 min → 15 min</strong> library research &amp; setup</div>
<div>🎯 <strong>Documented rationale</strong> for each decision</div>
<div>✅ Plan Mode clarifies requirements before code</div>
</div>
</div>
<div class="p-4 bg-teal-900/40 rounded-lg border border-teal-500/50">
<div class="font-bold text-sm mb-2">🐛 Debugging Your Own Failing Code</div>
<div class="opacity-90 mb-2">Async, CI vs local, intermittent failures</div>
<div class="space-y-1">
<div>⏱️ <strong>30 min → 5 min</strong> to root cause</div>
<div>🎯 <strong>Reads your actual code</strong>, not a description</div>
<div>✅ Fix + prevention, no re-explaining context</div>
</div>
</div>
<div class="p-4 bg-cyan-900/40 rounded-lg border border-cyan-500/50">
<div class="font-bold text-sm mb-2">🐳 Docker Debugging with Plan Mode</div>
<div class="opacity-90 mb-2">Container won't start investigation</div>
<div class="space-y-1">
<div>⏱️ <strong>45 min → 8 min</strong> (83% reduction)</div>
<div>🎯 <strong>8 attempts → 2 attempts</strong></div>
<div>✅ Collaborative strategy before execution</div>
</div>
</div>
<div class="p-4 bg-blue-900/40 rounded-lg border border-blue-500/50">
<div class="font-bold text-sm mb-2">🔄 CI/CD Build Failure Analysis</div>
<div class="opacity-90 mb-2">Programmatic automation in pipelines</div>
<div class="space-y-1">
<div>⏱️ <strong>25 min → 5 min</strong> investigation</div>
<div>🎯 <strong>12 steps → 3 automated steps</strong></div>
<div>✅ Pattern recognition across historical failures</div>
</div>
</div>
</div>

---

# Real-World Use Cases (2 of 2)

<div class="grid grid-cols-2 gap-4 mt-6 text-xs">
<div class="p-4 bg-indigo-900/40 rounded-lg border border-indigo-500/50">
<div class="font-bold text-sm mb-2">📚 Infrastructure Documentation</div>
<div class="opacity-90 mb-2">Auto-generated from docker-compose &amp; IaC</div>
<div class="space-y-1">
<div>⏱️ <strong>3 days → 30 min</strong> documentation</div>
<div>🎯 <strong>Automated diagram generation</strong> from config</div>
<div>✅ Always-current architecture docs</div>
</div>
</div>
<div class="p-4 bg-purple-900/40 rounded-lg border border-purple-500/50">
<div class="font-bold text-sm mb-2">🧠 Team Onboarding via Repository Memory</div>
<div class="opacity-90 mb-2">Institutional knowledge that compounds</div>
<div class="space-y-1">
<div>⏱️ <strong>2 weeks → 3 days</strong> to productivity</div>
<div>🎯 <strong>5-6 explanations → 1 explanation</strong></div>
<div>✅ AI retains conventions learned from senior engineers</div>
</div>
</div>
<div class="p-4 bg-cyan-900/40 rounded-lg border border-cyan-500/50">
<div class="font-bold text-sm mb-2">🐙 GitHub.com Integration</div>
<div class="opacity-90 mb-2">Issues, PRs, Actions — without leaving the terminal</div>
<div class="space-y-1">
<div>🎯 <strong>Issue → branch → PR</strong> entirely in CLI</div>
<div>🎯 Natural language → <strong>GitHub Actions workflow</strong></div>
<div>✅ Copilot creates PRs on your behalf (you're the author)</div>
<div class="font-mono bg-black/30 p-1 rounded mt-1 text-xs">&gt; "Work on issue #42 in a feature branch"<br/>&gt; "Create a PR that adds eslint to CI"</div>
</div>
</div>
</div>
<div class="mt-4 p-4 bg-gradient-to-r from-emerald-600/40 to-teal-600/40 rounded-xl">
<div class="font-bold text-sm mb-2">Aggregate Impact</div>
<div class="grid grid-cols-4 gap-2 text-xs text-center">
<div class="p-2 bg-black/30 rounded">
<div class="font-bold text-emerald-300">75 min saved</div>
<div class="opacity-70">per greenfield project</div>
</div>
<div class="p-2 bg-black/30 rounded">
<div class="font-bold text-teal-300">83% faster</div>
<div class="opacity-70">Docker debugging</div>
</div>
<div class="p-2 bg-black/30 rounded">
<div class="font-bold text-cyan-300">80% less</div>
<div class="opacity-70">CI investigation time</div>
</div>
<div class="p-2 bg-black/30 rounded">
<div class="font-bold text-blue-300">~11 days</div>
<div class="opacity-70">faster onboarding</div>
</div>
</div>
</div>

---

# 🐛 Use Case: Debugging a Running System

<div class="text-sm opacity-80 mb-4">The terminal is where the runtime lives — Copilot CLI gathers evidence from it directly</div>

<div class="grid grid-cols-2 gap-6 text-xs">
<div>
<div class="mb-3 p-3 bg-red-900/30 rounded-lg border border-red-500/30">
<div class="font-bold text-red-300 mb-1">The Problem</div>
<div class="opacity-90">Service fails in staging, works locally. The relevant information — container logs, env vars, network state — is not in your source files. It's in what's running. VS Code can't reach it.</div>
</div>

<div class="p-3 bg-emerald-900/30 rounded-lg border border-emerald-500/30">
<div class="font-bold text-emerald-300 mb-2">What makes this different from VS Code</div>
<div class="space-y-1.5">
<div class="flex gap-2"><span class="text-emerald-400">→</span><span>Copilot <strong>runs commands itself</strong> — no copy-pasting logs into chat</span></div>
<div class="flex gap-2"><span class="text-emerald-400">→</span><span>Checks container, env, and network <strong>in one session</strong></span></div>
<div class="flex gap-2"><span class="text-emerald-400">→</span><span>Finds <strong>root cause + side effects</strong>, not just symptoms</span></div>
</div>
</div>
</div>

<div class="font-mono text-xs bg-gray-900/80 rounded-xl p-4 border border-gray-600/40 leading-relaxed">
<div class="text-gray-400 mb-2"># Auth service returning 503 in staging</div>
<div class="text-cyan-300">&gt; "My auth service fails in staging. Debug it."</div>
<div class="mt-2 text-gray-400">&#91;runs: docker logs auth-service --tail 50&#93;</div>
<div class="text-gray-400">&#91;runs: docker exec auth-service env | grep JWT&#93;</div>
<div class="text-gray-400">&#91;runs: curl -sv http://redis-staging:6379/ping&#93;</div>
<div class="mt-2 text-yellow-300">Found: JWT_SECRET missing from staging container.</div>
<div class="text-yellow-300">Redis is fine. Service fails silently on token</div>
<div class="text-yellow-300">validation → returns 503 instead of 401.</div>
<div class="mt-2 text-emerald-300">Fix: Add JWT_SECRET to staging secrets.</div>
<div class="text-emerald-300">Note: 503 vs 401 mismatch is a separate bug →</div>
<div class="text-emerald-300">flagging that too.</div>
</div>
</div>

---

# Mental Model Shift

<div class="text-xs mt-2 mb-4 px-4 py-2 bg-gradient-to-r from-slate-700/60 to-slate-600/40 rounded-lg border border-slate-500/40 italic opacity-90 text-center">
From "execute commands manually and search docs when stuck" → "collaborate with AI in the terminal — whether building something new, debugging failing code, or running autonomous agents independently of your IDE"
</div>

<div class="grid grid-cols-2 gap-4 text-xs">

<div class="space-y-2">
<div class="text-sm font-bold text-emerald-300 flex items-center gap-2 mb-3">
  <span class="px-2 py-0.5 bg-emerald-500/20 rounded-full border border-emerald-500/40">✅ Move Toward</span>
</div>

<div class="p-2.5 bg-emerald-900/30 rounded-lg border border-emerald-500/30 flex gap-3 items-start">
  <span class="text-lg flex-shrink-0">🌱</span>
  <div><span class="font-semibold text-emerald-300">AI as Greenfield Thought Partner</span><br><span class="opacity-80">Explore library choices before committing → minutes vs hours of rework</span></div>
</div>

<div class="p-2.5 bg-emerald-900/30 rounded-lg border border-emerald-500/30 flex gap-3 items-start">
  <span class="text-lg flex-shrink-0">🤝</span>
  <div><span class="font-semibold text-emerald-300">Collaborative Planning First</span><br><span class="opacity-80">Plan Mode before coding → reduces debugging cycles from 8 to 2</span></div>
</div>

<div class="p-2.5 bg-emerald-900/30 rounded-lg border border-emerald-500/30 flex gap-3 items-start">
  <span class="text-lg flex-shrink-0">💻</span>
  <div><span class="font-semibold text-emerald-300">Terminal as Collaboration Space</span><br><span class="opacity-80">Eliminate 5-10 min context-switching overhead per switch</span></div>
</div>

<div class="p-2.5 bg-emerald-900/30 rounded-lg border border-emerald-500/30 flex gap-3 items-start">
  <span class="text-lg flex-shrink-0">☁️</span>
  <div><span class="font-semibold text-emerald-300">Cloud Delegation for Long Tasks</span><br><span class="opacity-80"><code>&</code> prefix runs agents independently — IDE and terminal both stay free</span></div>
</div>

</div>

<div class="space-y-2">
<div class="text-sm font-bold text-red-300 flex items-center gap-2 mb-3">
  <span class="px-2 py-0.5 bg-red-500/20 rounded-full border border-red-500/40">🛑 Move Against</span>
</div>

<div class="p-2.5 bg-red-900/25 rounded-lg border border-red-500/30 flex gap-3 items-start">
  <span class="text-lg flex-shrink-0">⚡</span>
  <div><span class="font-semibold text-red-300">Jumping to Implementation</span><br><span class="opacity-80">On greenfield work, explore options first — wrong library choice costs hours</span></div>
</div>

<div class="p-2.5 bg-red-900/25 rounded-lg border border-red-500/30 flex gap-3 items-start">
  <span class="text-lg flex-shrink-0">🔁</span>
  <div><span class="font-semibold text-red-300">Interactive Mode in CI/CD</span><br><span class="opacity-80">Builds break when it prompts for input → use <code>copilot -p</code></span></div>
</div>

<div class="p-2.5 bg-red-900/25 rounded-lg border border-red-500/30 flex gap-3 items-start">
  <span class="text-lg flex-shrink-0">⚠️</span>
  <div><span class="font-semibold text-red-300">Over-Approving Permissions</span><br><span class="opacity-80">Avoid <code>--yolo</code> in production — use targeted <code>--allow-tool</code></span></div>
</div>

<div class="p-2.5 bg-red-900/25 rounded-lg border border-red-500/30 flex gap-3 items-start">
  <span class="text-lg flex-shrink-0">🔀</span>
  <div><span class="font-semibold text-red-300">Context-Switching for AI Help</span><br><span class="opacity-80">Use <code>/ide</code> to bridge to VS Code mid-session instead</span></div>
</div>

</div>

</div>

---

# When to Use Copilot CLI

<div class="mt-6 text-sm">

<div class="grid grid-cols-2 gap-6">

<div class="space-y-3">

### ✅ Use This Pattern When

<div class="text-xs space-y-2">
<div>✓ Building something new and want a thought partner for options</div>
<div>✓ Debugging your own failing code, tests, or build environment</div>
<div>✓ DevOps and infrastructure work happens in terminals</div>
<div>✓ Automating CI/CD build failure analysis</div>
<div>✓ Want AI to remember team conventions across sessions</div>
</div>

</div>

<div class="space-y-3">

### ❌ Don't Use When

<div class="text-xs space-y-2">
<div>✗ Primary workflow is IDE code editing</div>
<div>✗ Need cross-repository analysis</div>
<div>✗ Want graphical debugging with breakpoints</div>
<div>✗ Workflow doesn't involve terminals</div>
</div>

</div>

</div>

<div class="mt-6 p-4 bg-gradient-to-r from-emerald-600/40 to-teal-600/40 rounded-lg border border-emerald-500/50">
<div class="font-bold mb-2">Quick Comparison</div>
<div class="grid grid-cols-3 gap-4 text-xs">
<div><strong>Copilot CLI:</strong> Terminal workflows, infrastructure</div>
<div><strong>VS Code Copilot:</strong> Code editing, rapid development</div>
<div><strong>Copilot Web:</strong> Cross-repo analysis, PR review</div>
</div>
</div>

</div>

---

# ✅ What You Can Do Today

<div class="grid grid-cols-3 gap-4 mt-6 text-xs">
<div class="p-5 bg-blue-900/40 rounded-lg border border-blue-500/50">
<div class="text-2xl mb-3">⚡</div>
<div class="font-bold mb-3">Immediate (15 min)</div>
<div class="space-y-2">
<div>□ Install: <code class="text-xs">npm install -g @github/copilot</code></div>
<div>□ Ask about your current project</div>
<div>□ Test Plan Mode (Shift+Tab)</div>
<div>□ Try <code>/ide</code> to open a file in VS Code</div>
</div>
</div>
<div class="p-5 bg-indigo-900/40 rounded-lg border border-indigo-500/50">
<div class="text-2xl mb-3">🚀</div>
<div class="font-bold mb-3">Short-term (1 hour)</div>
<div class="space-y-2">
<div>□ Scaffold next project interactively</div>
<div>□ Debug next failing test with Copilot</div>
<div>□ Create <code>.github/copilot-instructions.md</code></div>
<div>□ Add to one CI/CD pipeline</div>
</div>
</div>
<div class="p-5 bg-purple-900/40 rounded-lg border border-purple-500/50">
<div class="text-2xl mb-3">🎓</div>
<div class="font-bold mb-3">Advanced (2-4 hours)</div>
<div class="space-y-2">
<div>□ Create custom agents in <code>.github/agents/</code></div>
<div>□ Configure all CI/CD workflows</div>
<div>□ Browse plugins: <code>copilot plugin marketplace browse</code></div>
<div>□ Measure ROI: track before/after metrics</div>
</div>
</div>
</div>

<div class="mt-6 p-4 bg-gradient-to-r from-emerald-600 to-teal-600 rounded-xl text-center">
<div class="font-bold text-lg">Installation: 2 minutes • Immediate value for terminal workflows</div>
</div>

---

# Related Patterns

<div class="grid grid-cols-2 gap-4 mt-6 text-xs">

<div class="space-y-3">
<div class="text-sm font-bold opacity-60 mb-3 uppercase tracking-wider">Complementary Features</div>

<div class="p-3 bg-violet-900/35 rounded-lg border border-violet-500/40 flex gap-3 items-start">
  <span class="text-xl flex-shrink-0">🪝</span>
  <div><span class="font-semibold text-violet-300">Copilot Hooks</span><br><span class="opacity-80">Add validation, logging, and security scanning at key execution points in CLI workflows</span></div>
</div>

<div class="p-3 bg-blue-900/35 rounded-lg border border-blue-500/40 flex gap-3 items-start">
  <span class="text-xl flex-shrink-0">🔌</span>
  <div><span class="font-semibold text-blue-300">MCP Apps</span><br><span class="opacity-80">Extend Copilot CLI with external tools and data sources via Model Context Protocol</span></div>
</div>

<div class="p-3 bg-amber-900/35 rounded-lg border border-amber-500/40 flex gap-3 items-start">
  <span class="text-xl flex-shrink-0">🔒</span>
  <div><span class="font-semibold text-amber-300">Terminal Sandboxing</span><br><span class="opacity-80">Secure execution environments for untrusted Copilot CLI operations</span></div>
</div>

<div class="p-3 bg-teal-900/35 rounded-lg border border-teal-500/40 flex gap-3 items-start">
  <span class="text-xl flex-shrink-0">📡</span>
  <div><span class="font-semibold text-teal-300">Copilot CLI ACP</span><br><span class="opacity-80">Drive Copilot CLI programmatically via the Agent Client Protocol — embed it in your own tooling or automation</span></div>
</div>

</div>

<div class="space-y-3">
<div class="text-sm font-bold opacity-60 mb-3 uppercase tracking-wider">Decision Flow</div>

<div class="font-mono bg-black/50 p-4 rounded-lg border border-slate-600/40 text-xs space-y-1 leading-relaxed">
  <div class="opacity-70">Q: What's your actual goal?</div>
  <div class="flex gap-2"><span class="opacity-40">├─</span><span>In-editor code assistance</span></div>
  <div class="flex gap-2"><span class="opacity-40">│ </span><span class="text-emerald-400">→ VS Code Copilot</span></div>
  <div class="flex gap-2"><span class="opacity-40">├─</span><span>Cross-repo analysis</span></div>
  <div class="flex gap-2"><span class="opacity-40">│ </span><span class="text-emerald-400">→ Copilot Web</span></div>
  <div class="flex gap-2"><span class="opacity-40">├─</span><span>Organization-wide governance</span></div>
  <div class="flex gap-2"><span class="opacity-40">│ </span><span class="text-emerald-400">→ Copilot Hooks</span></div>
  <div class="flex gap-2"><span class="opacity-40">├─</span><span>Extending with external tools</span></div>
  <div class="flex gap-2"><span class="opacity-40">│ </span><span class="text-emerald-400">→ MCP Apps</span></div>
  <div class="flex gap-2"><span class="opacity-40">└─</span><span>Embed CLI in your own tooling</span></div>
  <div class="flex gap-2"><span class="opacity-40">  </span><span class="text-emerald-400">→ Copilot CLI ACP, Copilot SDK</span></div>
</div>

</div>

</div>

---

# � References

<div class="grid grid-cols-2 gap-4 mt-4 text-xs">

<div class="space-y-2">
<div class="text-sm font-bold text-cyan-400 mb-3">Core Documentation</div>

<div class="p-3 bg-white/5 rounded-lg border border-white/10 hover:border-cyan-500/40 transition-colors">
<div class="font-semibold mb-1">📖 About GitHub Copilot CLI</div>
<a href="https://docs.github.com/en/copilot/concepts/agents/about-copilot-cli" class="text-cyan-400 opacity-80 hover:opacity-100 break-all">docs.github.com/en/copilot/concepts/agents/about-copilot-cli</a>
</div>

<div class="p-3 bg-white/5 rounded-lg border border-white/10 hover:border-cyan-500/40 transition-colors">
<div class="font-semibold mb-1">📖 Using GitHub Copilot CLI</div>
<a href="https://docs.github.com/en/copilot/how-tos/use-copilot-agents/use-copilot-cli" class="text-cyan-400 opacity-80 hover:opacity-100 break-all">docs.github.com/en/.../use-copilot-cli</a>
</div>

<div class="p-3 bg-white/5 rounded-lg border border-white/10 hover:border-cyan-500/40 transition-colors">
<div class="font-semibold mb-1">📖 Installing GitHub Copilot CLI</div>
<a href="https://docs.github.com/en/copilot/how-tos/set-up/install-copilot-cli" class="text-cyan-400 opacity-80 hover:opacity-100 break-all">docs.github.com/en/.../install-copilot-cli</a>
</div>

<div class="p-3 bg-white/5 rounded-lg border border-white/10 hover:border-cyan-500/40 transition-colors">
<div class="font-semibold mb-1">🔧 CLI Command Reference</div>
<a href="https://docs.github.com/en/copilot/reference/cli-command-reference" class="text-cyan-400 opacity-80 hover:opacity-100 break-all">docs.github.com/en/copilot/reference/cli-command-reference</a>
</div>
</div>

<div class="space-y-2">
<div class="text-sm font-bold text-blue-400 mb-3">Guides & Announcements</div>

<div class="p-3 bg-white/5 rounded-lg border border-white/10 hover:border-blue-500/40 transition-colors">
<div class="font-semibold mb-1">🎓 CLI Best Practices</div>
<a href="https://docs.github.com/en/copilot/how-tos/copilot-cli/cli-best-practices" class="text-blue-400 opacity-80 hover:opacity-100 break-all">docs.github.com/en/.../cli-best-practices</a>
</div>

<div class="p-3 bg-white/5 rounded-lg border border-white/10 hover:border-blue-500/40 transition-colors">
<div class="font-semibold mb-1">🎓 Adding Custom Instructions</div>
<a href="https://docs.github.com/en/copilot/how-tos/copilot-cli/add-custom-instructions" class="text-blue-400 opacity-80 hover:opacity-100 break-all">docs.github.com/en/.../add-custom-instructions</a>
</div>

<div class="p-3 bg-white/5 rounded-lg border border-white/10 hover:border-blue-500/40 transition-colors">
<div class="font-semibold mb-1">📋 Plan Mode Announcement</div>
<a href="https://github.blog/changelog/2026-01-21-github-copilot-cli-plan-before-you-build-steer-as-you-go/" class="text-blue-400 opacity-80 hover:opacity-100 break-all">github.blog — Plan before you build, steer as you go</a>
</div>

<div class="p-3 bg-white/5 rounded-lg border border-white/10 hover:border-blue-500/40 transition-colors">
<div class="font-semibold mb-1">🚀 /fleet Fan-Out Documentation</div>
<a href="https://docs.github.com/en/copilot/how-tos/use-copilot-agents/use-copilot-cli#using-fleet-to-run-multiple-agents" class="text-blue-400 opacity-80 hover:opacity-100 break-all">docs.github.com/en/.../use-copilot-cli#using-fleet</a>
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
<div class="absolute inset-0 blur-2xl opacity-50"><img src="../sdp-logo.png" class="w-48" alt="" /></div>
<img src="../sdp-logo.png" class="w-48 relative" alt="SDP Logo" />
</div>
<h1 class="!text-5xl !font-bold !mt-6 bg-gradient-to-r from-cyan-400 via-blue-400 to-indigo-400 bg-clip-text text-transparent relative z-10">Thank You!</h1>
<div class="mt-4 relative z-10">
<span class="px-6 py-2 bg-gradient-to-r from-cyan-600/80 to-blue-600/80 rounded-full text-white text-lg font-medium shadow-lg shadow-cyan-500/25">Terminal-Native AI for Developers and DevOps</span>
</div>
<div class="mt-8 grid grid-cols-3 gap-4 text-sm max-w-3xl mx-auto relative z-10">
<div class="p-3 bg-gradient-to-br from-cyan-900/30 to-cyan-800/20 rounded-lg border border-cyan-500/30">
<div class="text-cyan-400 font-mono font-bold">npm install -g @github/copilot</div>
<div class="opacity-80 text-xs mt-1">Get started in 2 minutes</div>
</div>
<div class="p-3 bg-gradient-to-br from-blue-900/30 to-blue-800/20 rounded-lg border border-blue-500/30">
<div class="text-blue-400 font-bold text-lg">Shift+Tab</div>
<div class="opacity-80 text-xs">Activate Plan Mode</div>
</div>
<div class="p-3 bg-gradient-to-br from-indigo-900/30 to-indigo-800/20 rounded-lg border border-indigo-500/30">
<div class="text-indigo-400 font-mono font-bold">& &lt;task&gt;</div>
<div class="opacity-80 text-xs">Delegate to cloud agents</div>
</div>
</div>
<div class="mt-6 text-sm opacity-60 relative z-10">Questions? Let's discuss terminal workflows and AI collaboration</div>
<div class="mt-4 w-32 h-1 bg-gradient-to-r from-transparent via-cyan-400 to-transparent rounded-full relative z-10"></div>
</div>
