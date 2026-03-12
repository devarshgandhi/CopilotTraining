---
theme: default
class: text-center
highlighter: shiki
lineNumbers: false
info: |
  ## What's New in Copilot for VS Code: v1.108 – v1.110
  CopilotTraining Tech Talks
drawings:
  persist: false
transition: slide-left
title: What's New in Copilot for VS Code
module: tech-talks/vscode-latest
mdc: true
status: active
updated: 2026-03-05
---

<div class="h-full flex flex-col items-center justify-center relative overflow-hidden">
  <!-- Gradient background -->
  <div class="absolute inset-0 bg-gradient-to-br from-cyan-900/20 via-blue-900/10 to-indigo-900/20"></div>

  <!-- Glowing orb -->
  <div class="absolute top-1/4 left-1/2 -translate-x-1/2 -translate-y-1/2 w-96 h-96 bg-gradient-to-r from-cyan-500/20 via-blue-500/20 to-indigo-500/20 rounded-full blur-3xl"></div>

  <!-- Logo with glow -->
  <div class="relative z-10">
    <div class="absolute inset-0 blur-2xl opacity-50">
      <img src="./sdp-logo.png" class="w-64" alt="" />
    </div>
    <img src="./sdp-logo.png" class="w-64 relative" alt="SDP Logo" />
  </div>

  <!-- Gradient text title -->
  <h1 class="!text-5xl !font-bold !mt-8 bg-gradient-to-r from-cyan-400 via-blue-400 to-indigo-400 bg-clip-text text-transparent relative z-10">
    What's New in Copilot for VS Code
  </h1>

  <!-- Pill subtitle -->
  <div class="mt-4 relative z-10">
    <span class="px-6 py-2 bg-gradient-to-r from-cyan-600/80 to-blue-600/80 rounded-full text-white text-xl font-medium shadow-lg shadow-cyan-500/25">
      v1.108 – v1.110
    </span>
  </div>

  <!-- Tagline -->
  <div class="mt-8 text-lg opacity-70 relative z-10">
    ⏰ <strong>30-45 minutes</strong> • Developers • Platform Teams • Tech Leads
  </div>

  <!-- Decorative line -->
  <div class="mt-6 w-32 h-1 bg-gradient-to-r from-transparent via-cyan-400 to-transparent rounded-full relative z-10"></div>
</div>

<div class="abs-br m-6 flex gap-2">
  <span class="text-sm opacity-50">Tech Talk · vscode-latest</span>
</div>

---
layout: center
---

<div class="text-center mb-6">
  <div class="text-5xl mb-4">🎯</div>
  <h1 class="!text-4xl bg-gradient-to-r from-cyan-400 to-blue-400 bg-clip-text text-transparent">The Question This Talk Answers</h1>
</div>

<div class="p-6 bg-gradient-to-r from-cyan-500/10 to-blue-500/10 rounded-xl border border-cyan-500/30 mb-6 text-center max-w-4xl mx-auto">
  <div class="text-2xl font-bold text-white italic leading-relaxed">"What are the most impactful new Copilot features in VS Code's last three releases, and how do I start using them today?"</div>
</div>

<div class="grid grid-cols-3 gap-6 max-w-3xl mx-auto">
  <div class="p-4 bg-cyan-900/30 rounded-lg border border-cyan-500/30 text-center">
    <div class="text-4xl font-bold text-cyan-400 mb-2">v1.108</div>
    <div class="text-sm opacity-70">December 2025</div>
  </div>
  <div class="p-4 bg-blue-900/30 rounded-lg border border-blue-500/30 text-center">
    <div class="text-4xl font-bold text-blue-400 mb-2">v1.109</div>
    <div class="text-sm opacity-70">January 2026</div>
  </div>
  <div class="p-4 bg-indigo-900/30 rounded-lg border border-indigo-500/30 text-center">
    <div class="text-4xl font-bold text-indigo-400 mb-2">v1.110</div>
    <div class="text-sm opacity-70">February 2026</div>
  </div>
</div>

---
layout: center
---

<div class="text-2xl font-bold mb-4">📖 Table of Contents</div>

<div class="grid grid-cols-3 gap-3">
  <div @click="$nav.go(5)" class="cursor-pointer p-3 bg-gradient-to-br from-cyan-500/10 to-blue-500/10 rounded-lg border border-cyan-500/20 hover:border-cyan-500/50 hover:shadow-lg hover:shadow-cyan-500/10 transition-all">
    <div class="text-2xl mb-1">🤖</div>
    <div class="text-sm font-semibold text-cyan-300">Agent Sessions</div>
    <div class="text-xs opacity-70">Multi-agent workflows</div>
  </div>

  <div @click="$nav.go(9)" class="cursor-pointer p-3 bg-gradient-to-br from-violet-500/10 to-purple-500/10 rounded-lg border border-violet-500/20 hover:border-violet-500/50 hover:shadow-lg hover:shadow-violet-500/10 transition-all">
    <div class="text-2xl mb-1">⚙️</div>
    <div class="text-sm font-semibold text-violet-300">Customization</div>
    <div class="text-xs opacity-70">Skills, agents, plugins</div>
  </div>

  <div @click="$nav.go(13)" class="cursor-pointer p-3 bg-gradient-to-br from-purple-500/10 to-fuchsia-500/10 rounded-lg border border-purple-500/20 hover:border-purple-500/50 hover:shadow-lg hover:shadow-purple-500/10 transition-all">
    <div class="text-2xl mb-1">🧠</div>
    <div class="text-sm font-semibold text-purple-300">Claude Integration</div>
    <div class="text-xs opacity-70">Thinking tokens</div>
  </div>

  <div @click="$nav.go(15)" class="cursor-pointer p-3 bg-gradient-to-br from-emerald-500/10 to-teal-500/10 rounded-lg border border-emerald-500/20 hover:border-emerald-500/50 hover:shadow-lg hover:shadow-emerald-500/10 transition-all">
    <div class="text-2xl mb-1">🔒</div>
    <div class="text-sm font-semibold text-emerald-300">Security & Trust</div>
    <div class="text-xs opacity-70">Terminal sandboxing</div>
  </div>

  <div @click="$nav.go(18)" class="cursor-pointer p-3 bg-gradient-to-br from-blue-500/10 to-indigo-500/10 rounded-lg border border-blue-500/20 hover:border-blue-500/50 hover:shadow-lg hover:shadow-blue-500/10 transition-all">
    <div class="text-2xl mb-1">✨</div>
    <div class="text-sm font-semibold text-blue-300">Chat UX</div>
    <div class="text-xs opacity-70">Memory, browser, diagrams</div>
  </div>

  <div @click="$nav.go(22)" class="cursor-pointer p-3 bg-gradient-to-br from-amber-500/10 to-orange-500/10 rounded-lg border border-amber-500/20 hover:border-amber-500/50 hover:shadow-lg hover:shadow-amber-500/10 transition-all">
    <div class="text-2xl mb-1">🚀</div>
    <div class="text-sm font-semibold text-amber-300">Get Started</div>
    <div class="text-xs opacity-70">Your next steps</div>
  </div>
</div>

---
layout: default
---

# 📅 Three Releases at a Glance

<div class="mt-6 space-y-4">

<div class="flex items-start bg-gradient-to-r from-cyan-500/15 to-cyan-500/5 rounded-lg p-5 border border-cyan-500/40 hover:border-cyan-400/60 transition-all">
<div class="text-cyan-400 font-bold text-2xl mr-6 min-w-[100px]">v1.108</div>
<div class="flex-1">
<div class="text-xs text-cyan-300/70 mb-2 uppercase tracking-wide">December 2025</div>
<div class="text-gray-200">Agent Skills (experimental), agent sessions UX improvements, terminal IntelliSense rework, 6,000 issues closed</div>
</div>
</div>

<div class="flex items-start bg-gradient-to-r from-blue-500/15 to-blue-500/5 rounded-lg p-5 border border-blue-500/40 hover:border-blue-400/60 transition-all">
<div class="text-blue-400 font-bold text-2xl mr-6 min-w-[100px]">v1.109</div>
<div class="flex-1">
<div class="text-xs text-blue-300/70 mb-2 uppercase tracking-wide">January 2026</div>
<div class="text-gray-200">Claude Agent preview, Agent Skills GA, terminal sandboxing, Copilot Memory, MCP Apps, integrated browser</div>
</div>
</div>

<div class="flex items-start bg-gradient-to-r from-indigo-500/15 to-indigo-500/5 rounded-lg p-5 border border-indigo-500/40 hover:border-indigo-400/60 transition-all">
<div class="text-indigo-400 font-bold text-2xl mr-6 min-w-[100px]">v1.110</div>
<div class="flex-1">
<div class="text-xs text-indigo-300/70 mb-2 uppercase tracking-wide">February 2026</div>
<div class="text-gray-200">Agent Plugins, agentic browser tools, context compaction, session forking, /create-* commands, Explore subagent</div>
</div>
</div>

</div>

---
layout: center
name: core-insight
---

<div class="text-center mb-6">
  <div class="text-5xl mb-4">🧠</div>
  <h1 class="!text-4xl bg-gradient-to-r from-cyan-400 to-indigo-400 bg-clip-text text-transparent">The Core Insight</h1>
</div>

<div class="p-8 bg-gradient-to-br from-cyan-500/10 via-blue-500/10 to-indigo-500/10 rounded-2xl border-2 border-cyan-500/30 max-w-3xl mx-auto text-center">
  <div class="opacity-60 mb-3">From</div>
  <div class="text-2xl font-bold text-cyan-300 mb-4">one AI assistant you converse with</div>
  <div class="w-16 h-1 bg-gradient-to-r from-cyan-400 via-blue-400 to-indigo-400 rounded-full mx-auto my-4"></div>
  <div class="opacity-60 mb-3">To</div>
  <div class="text-2xl font-bold text-indigo-300">a team of specialized AI agents you orchestrate</div>
</div>

<div class="mt-8 flex justify-center gap-4">
  <div class="px-4 py-2 bg-cyan-900/40 rounded-lg border border-cyan-500/40 text-center">
    <div class="font-bold text-cyan-300">🏠 Local</div>
  </div>
  <div class="px-4 py-2 bg-blue-900/40 rounded-lg border border-blue-500/40 text-center">
    <div class="font-bold text-blue-300">🔧 Background</div>
  </div>
  <div class="px-4 py-2 bg-indigo-900/40 rounded-lg border border-indigo-500/40 text-center">
    <div class="font-bold text-indigo-300">☁️ Cloud</div>
  </div>
  <div class="px-4 py-2 bg-purple-900/40 rounded-lg border border-purple-500/40 text-center">
    <div class="font-bold text-purple-300">🧠 Claude</div>
  </div>
</div>

---
layout: center
name: agent-sessions
---

<div class="text-center mb-6">
  <div class="text-5xl mb-4">🤖</div>
  <h1 class="!text-4xl bg-gradient-to-r from-cyan-400 to-blue-400 bg-clip-text text-transparent">Agent Sessions & Orchestration</h1>
  <p class="text-xl opacity-80 mt-2">Multi-agent workflows with session management</p>
</div>

<div class="grid grid-cols-4 gap-4 mt-8">
  <div class="p-4 bg-cyan-900/30 rounded-lg border border-cyan-500/30 text-center">
    <div class="text-3xl mb-2">🏠</div>
    <div class="font-semibold text-cyan-300">Local</div>
    <div class="text-xs opacity-70 mt-1">Interactive planning</div>
  </div>

  <div class="p-4 bg-blue-900/30 rounded-lg border border-blue-500/30 text-center">
    <div class="text-3xl mb-2">🔧</div>
    <div class="font-semibold text-blue-300">Background</div>
    <div class="text-xs opacity-70 mt-1">Autonomous tasks</div>
  </div>

  <div class="p-4 bg-indigo-900/30 rounded-lg border border-indigo-500/30 text-center">
    <div class="text-3xl mb-2">☁️</div>
    <div class="font-semibold text-indigo-300">Cloud</div>
    <div class="text-xs opacity-70 mt-1">Cross-repo scale</div>
  </div>

  <div class="p-4 bg-purple-900/30 rounded-lg border border-purple-500/30 text-center">
    <div class="text-3xl mb-2">🧠</div>
    <div class="font-semibold text-purple-300">Claude</div>
    <div class="text-xs opacity-70 mt-1">Complex reasoning</div>
  </div>
</div>

<div class="mt-6 p-4 bg-gradient-to-r from-cyan-500/10 via-blue-500/10 to-indigo-500/10 rounded-lg border border-cyan-500/20 text-center">
  <span class="text-cyan-300 font-semibold">Session Handoffs:</span>
  <span class="opacity-80">Plan locally → Continue in Background → Agent implements while you work</span>
</div>

---
layout: default
---

# Agent Sessions in Chat View

<div class="mt-4">

<div class="grid grid-cols-2 gap-5">

<div class="p-5 bg-gradient-to-br from-cyan-500/15 to-cyan-500/5 rounded-xl border border-cyan-500/40">
<div class="text-3xl mb-3">📱</div>
<div class="text-xl font-bold text-cyan-400 mb-2">Compact Mode</div>
<div class="text-gray-300">Shows the three most recent sessions when Chat view is narrow</div>
</div>

<div class="p-5 bg-gradient-to-br from-blue-500/15 to-blue-500/5 rounded-xl border border-blue-500/40">
<div class="text-3xl mb-3">📊</div>
<div class="text-xl font-bold text-blue-400 mb-2">Side-by-Side Mode</div>
<div class="text-gray-300">Full session list with search and filters when Chat view is wide</div>
</div>

</div>

<div class="mt-5 bg-black/30 rounded-lg p-4 font-mono text-sm">
<div class="text-gray-500">// Control orientation</div>
<div class="text-cyan-300">"chat.viewSessions.orientation"<span class="text-gray-400">:</span> <span class="text-green-400">"sideBySide"</span></div>
<div class="text-gray-500">// or "stacked", "auto"</div>
</div>

<div class="mt-4 p-3 bg-gradient-to-r from-cyan-500/10 to-blue-500/10 rounded-lg border border-cyan-500/20">
💡 Status indicators show in-progress, unread, and needs-attention states in the command center
</div>

</div>

---
layout: default
---

# Four Agent Types

<div class="mt-4">
<div class="grid grid-cols-2 gap-4">

<div class="p-5 bg-gradient-to-br from-cyan-500/20 to-cyan-500/5 rounded-xl border border-cyan-500/40 hover:scale-[1.02] transition-transform">
<div class="flex items-center gap-3 mb-3">
  <div class="text-3xl">🏠</div>
  <div class="text-2xl font-bold text-cyan-400">Local</div>
</div>
<div class="text-sm text-gray-400 mb-2">Interactive planning, exploration</div>
<div class="text-gray-300">Real-time in Chat view</div>
</div>

<div class="p-5 bg-gradient-to-br from-blue-500/20 to-blue-500/5 rounded-xl border border-blue-500/40 hover:scale-[1.02] transition-transform">
<div class="flex items-center gap-3 mb-3">
  <div class="text-3xl">🔧</div>
  <div class="text-2xl font-bold text-blue-400">Background</div>
</div>
<div class="text-sm text-gray-400 mb-2">Autonomous multi-file tasks</div>
<div class="text-gray-300">Runs in isolated Git worktree</div>
</div>

<div class="p-5 bg-gradient-to-br from-indigo-500/20 to-indigo-500/5 rounded-xl border border-indigo-500/40 hover:scale-[1.02] transition-transform">
<div class="flex items-center gap-3 mb-3">
  <div class="text-3xl">☁️</div>
  <div class="text-2xl font-bold text-indigo-400">Cloud</div>
</div>
<div class="text-sm text-gray-400 mb-2">Cross-repo operations at scale</div>
<div class="text-gray-300">GitHub-hosted infrastructure</div>
</div>

<div class="p-5 bg-gradient-to-br from-purple-500/20 to-purple-500/5 rounded-xl border border-purple-500/40 hover:scale-[1.02] transition-transform">
<div class="flex items-center gap-3 mb-3">
  <div class="text-3xl">🧠</div>
  <div class="text-2xl font-bold text-purple-400">Claude</div>
</div>
<div class="text-sm text-gray-400 mb-2">Complex reasoning, architecture</div>
<div class="text-gray-300">Anthropic SDK with thinking tokens</div>
</div>

</div>

<div class="mt-5 p-4 bg-gradient-to-r from-blue-500/10 to-indigo-500/10 rounded-lg border border-blue-500/30">
<span class="text-blue-400 font-semibold">💡 Session handoffs:</span>
<span class="text-gray-200"> Plan locally → click <span class="text-cyan-300 font-mono">Continue in → Background</span> → agent implements autonomously</span>
</div>

</div>

---
layout: default
---

# Background Agents & Explore Subagent

<div class="mt-4 grid grid-cols-2 gap-5">

<div class="p-5 bg-gradient-to-br from-cyan-500/15 to-cyan-500/5 rounded-xl border border-cyan-500/40">
<div class="flex items-center gap-2 mb-3">
  <span class="text-2xl">🌳</span>
  <span class="text-xl font-bold text-cyan-400">Git Worktree Isolation</span>
</div>
<div class="space-y-2 text-sm text-gray-300">
<div class="flex items-center gap-2"><span class="text-cyan-400">✓</span> Agent creates new worktree automatically</div>
<div class="flex items-center gap-2"><span class="text-cyan-400">✓</span> Changes committed per turn — main untouched</div>
<div class="flex items-center gap-2"><span class="text-cyan-400">✓</span> Review via diff view when complete</div>
<div class="flex items-center gap-2"><span class="text-cyan-400">✓</span> Multiple background agents in parallel</div>
</div>

<div class="mt-4 bg-black/30 rounded p-3 font-mono text-xs">
<div class="text-gray-500">// Copy extra files into worktrees</div>
<div class="text-cyan-300">"git.worktreeIncludeFiles":</div>
<div class="text-gray-400 ml-4">["config/local.json"]</div>
</div>
</div>

<div class="p-5 bg-gradient-to-br from-indigo-500/15 to-indigo-500/5 rounded-xl border border-indigo-500/40">
<div class="flex items-center gap-2 mb-3">
  <span class="text-2xl">🔎</span>
  <span class="text-xl font-bold text-indigo-400">Explore Subagent</span>
</div>
<div class="space-y-2 text-sm text-gray-300">
<div class="flex items-center gap-2"><span class="text-indigo-400">🚀</span> Dedicated search/read agent for Plan</div>
<div class="flex items-center gap-2"><span class="text-indigo-400">🚀</span> Read-only, uses search + file read tools</div>
<div class="flex items-center gap-2"><span class="text-indigo-400">🚀</span> Fast models (Haiku, Gemini Flash)</div>
<div class="flex items-center gap-2"><span class="text-indigo-400">🚀</span> Runs in parallel with Plan agent</div>
</div>

<div class="mt-4 bg-black/30 rounded p-3 font-mono text-xs">
<div class="text-gray-500">// Override Explore model</div>
<div class="text-indigo-300">"chat.exploreAgent.defaultModel":</div>
<div class="text-green-400 ml-2">"claude-haiku-4-5"</div>
</div>
</div>

</div>

---
layout: center
name: customization
---

<div class="text-center mb-6">
  <div class="text-5xl mb-4">⚙️</div>
  <h1 class="!text-4xl bg-gradient-to-r from-violet-400 to-purple-400 bg-clip-text text-transparent">Agent Customization</h1>
  <p class="text-xl opacity-80 mt-2">Skills, custom agents, and workspace bootstrapping</p>
</div>

<div class="grid grid-cols-3 gap-4 mt-8">
  <div class="p-4 bg-violet-900/30 rounded-lg border border-violet-500/30 text-center">
    <div class="text-3xl mb-2">📚</div>
    <div class="font-semibold text-violet-300">Agent Skills</div>
    <div class="text-xs opacity-70 mt-1">Domain expertise bundles</div>
  </div>

  <div class="p-4 bg-purple-900/30 rounded-lg border border-purple-500/30 text-center">
    <div class="text-3xl mb-2">🧩</div>
    <div class="font-semibold text-purple-300">Agent Plugins</div>
    <div class="text-xs opacity-70 mt-1">Prepackaged customizations</div>
  </div>

  <div class="p-4 bg-fuchsia-900/30 rounded-lg border border-fuchsia-500/30 text-center">
    <div class="text-3xl mb-2">✨</div>
    <div class="font-semibold text-fuchsia-300">/create-* Commands</div>
    <div class="text-xs opacity-70 mt-1">Generate from conversations</div>
  </div>
</div>

---
layout: default
---

# Agent Skills & Agent Plugins

<div class="mt-4 grid grid-cols-2 gap-5">

<div class="p-5 bg-gradient-to-br from-violet-500/15 to-violet-500/5 rounded-xl border border-violet-500/40">
<div class="flex items-center gap-2 mb-3">
  <span class="text-2xl">📚</span>
  <span class="text-xl font-bold text-violet-400">Agent Skills</span>
  <span class="text-xs bg-green-500/20 text-green-300 px-2 py-0.5 rounded">GA v1.109</span>
</div>
<div class="space-y-2 text-sm text-gray-300">
<div class="flex items-center gap-2"><span class="text-violet-400">✨</span> Domain expertise in reusable folders</div>
<div class="flex items-center gap-2"><span class="text-violet-400">✨</span> Agents load on-demand automatically</div>
<div class="flex items-center gap-2"><span class="text-violet-400">✨</span> Experimental → GA in three releases</div>
</div>

<div class="mt-4 bg-black/30 rounded p-3 font-mono text-xs">
<div class="text-gray-500">.github/skills/</div>
<div class="text-violet-300 ml-2">api-design/SKILL.md</div>
<div class="text-violet-300 ml-2">security-review/SKILL.md</div>
</div>

<div class="mt-3 bg-black/30 rounded p-2 font-mono text-xs">
<div class="text-violet-300">"chat.useAgentSkills": <span class="text-green-400">true</span></div>
</div>
</div>

<div class="p-5 bg-gradient-to-br from-purple-500/15 to-purple-500/5 rounded-xl border border-purple-500/40">
<div class="flex items-center gap-2 mb-3">
  <span class="text-2xl">🧩</span>
  <span class="text-xl font-bold text-purple-400">Agent Plugins</span>
  <span class="text-xs bg-indigo-500/20 text-indigo-300 px-2 py-0.5 rounded">v1.110</span>
</div>
<div class="space-y-2 text-sm text-gray-300">
<div class="flex items-center gap-2"><span class="text-purple-400">🎁</span> Prepackaged customization bundles</div>
<div class="flex items-center gap-2"><span class="text-purple-400">🎁</span> Skills, commands, agents, MCP, hooks</div>
<div class="flex items-center gap-2"><span class="text-purple-400">🎁</span> Install from Extensions view</div>
</div>

<div class="mt-4 bg-black/30 rounded p-3 font-mono text-xs">
<div class="text-purple-300">"chat.plugins.enabled": <span class="text-green-400">true</span></div>
<div class="mt-2 text-purple-300">"chat.plugins.marketplaces":</div>
<div class="text-gray-400 ml-2">["copilot-plugins"]</div>
</div>

<div class="mt-3 p-2 bg-purple-500/10 rounded text-xs">
💡 Search with <span class="font-mono text-purple-300">@agentPlugins</span> in Extensions
</div>
</div>

</div>

---
layout: default
---

# Custom Agent Controls

<div class="mt-4">

<div class="p-3 bg-gradient-to-r from-violet-500/10 to-purple-500/10 rounded-lg border border-violet-500/30 mb-5 text-center">
  <span class="opacity-80">New powerful attributes for </span>
  <span class="text-violet-300 font-semibold font-mono">.agent.md</span>
  <span class="opacity-80"> files</span>
</div>

<div class="grid grid-cols-2 gap-4">

<div class="space-y-3">

<div class="p-4 bg-gradient-to-br from-violet-500/15 to-violet-500/5 rounded-lg border border-violet-500/40">
<div class="text-violet-400 font-mono text-sm mb-2">user-invokable: false</div>
<div class="text-gray-300 text-sm">Create agents accessible only as subagents</div>
</div>

<div class="p-4 bg-gradient-to-br from-purple-500/15 to-purple-500/5 rounded-lg border border-purple-500/40">
<div class="text-purple-400 font-mono text-sm mb-2">disable-model-invocation</div>
<div class="text-gray-300 text-sm">Prevent automatic invocation by other agents</div>
</div>

<div class="p-4 bg-gradient-to-br from-fuchsia-500/15 to-fuchsia-500/5 rounded-lg border border-fuchsia-500/40">
<div class="text-fuchsia-400 font-mono text-sm mb-2">agents: ['Modify', 'Search']</div>
<div class="text-gray-300 text-sm">Restrict which subagents can be invoked</div>
</div>

</div>

<div>
<div class="bg-black/40 rounded-lg p-4 font-mono text-xs">
<div class="text-gray-500">---</div>
<div><span class="text-violet-300">name</span><span class="text-gray-400">:</span> architect</div>
<div><span class="text-violet-300">model</span><span class="text-gray-400">:</span> [<span class="text-green-400">'Claude Sonnet 4.5'</span>,</div>
<div class="ml-8"><span class="text-green-400">'GPT-5 (copilot)'</span>]</div>
<div><span class="text-violet-300">tools</span><span class="text-gray-400">:</span> [<span class="text-green-400">'readFiles'</span>, <span class="text-green-400">'agent'</span>]</div>
<div><span class="text-violet-300">agents</span><span class="text-gray-400">:</span> [<span class="text-green-400">'Modify'</span>, <span class="text-green-400">'Search'</span>]</div>
<div><span class="text-violet-300">user-invokable</span><span class="text-gray-400">:</span> <span class="text-green-400">true</span></div>
<div class="text-gray-500">---</div>
</div>

<div class="mt-4 p-3 bg-violet-500/10 rounded-lg border border-violet-500/30">
<p class="text-sm text-gray-300">
✨ Multiple model support with fallback order
</p>
</div>
</div>

</div>

</div>

---
layout: default
---

# Org-Level & /init Bootstrap

<div class="mt-4 grid grid-cols-2 gap-5">

<div class="p-5 bg-gradient-to-br from-violet-500/15 to-violet-500/5 rounded-xl border border-violet-500/40">
<div class="flex items-center gap-2 mb-3">
  <span class="text-2xl">🏢</span>
  <span class="text-xl font-bold text-violet-400">Organization-Wide</span>
</div>
<div class="space-y-2 text-sm text-gray-300">
<div class="flex items-center gap-2"><span class="text-violet-400">📋</span> Org-level custom agents (v1.108)</div>
<div class="flex items-center gap-2"><span class="text-violet-400">📋</span> Org-level custom instructions (v1.109)</div>
<div class="flex items-center gap-2"><span class="text-violet-400">📋</span> Enforce consistent AI guidance across teams</div>
</div>

<div class="mt-4 bg-black/30 rounded p-3 font-mono text-xs">
<div class="text-gray-500">// Enabled by default in v1.109</div>
<div class="text-violet-300">"github.copilot.chat</div>
<div class="text-violet-300 ml-0">&nbsp;&nbsp;.organizationInstructions</div>
<div class="text-violet-300 ml-0">&nbsp;&nbsp;.enabled": <span class="text-green-400">true</span></div>
</div>
</div>

<div class="p-5 bg-gradient-to-br from-purple-500/15 to-purple-500/5 rounded-xl border border-purple-500/40">
<div class="flex items-center gap-2 mb-3">
  <span class="text-2xl">🚀</span>
  <span class="text-xl font-bold text-purple-400">/init Command</span>
  <span class="text-xs bg-purple-500/20 text-purple-300 px-2 py-0.5 rounded">v1.109</span>
</div>
<div class="space-y-2 text-sm text-gray-300">
<div class="flex items-center gap-2"><span class="text-purple-400">🎯</span> Analyzes your project structure</div>
<div class="flex items-center gap-2"><span class="text-purple-400">🎯</span> Generates <span class="font-mono text-purple-300">copilot-instructions.md</span></div>
<div class="flex items-center gap-2"><span class="text-purple-400">🎯</span> Creates <span class="font-mono text-purple-300">AGENTS.md</span> automatically</div>
</div>

<div class="mt-4 p-3 bg-purple-500/10 rounded-lg border border-purple-500/30">
<p class="text-sm text-gray-300 font-semibold text-center">Bootstrap your workspace for AI in seconds</p>
</div>
</div>

</div>

---
layout: default
---

# /create-* Commands

<div class="mt-4">

<div class="p-3 bg-gradient-to-r from-fuchsia-500/10 to-pink-500/10 rounded-lg border border-fuchsia-500/30 mb-5 text-center">
  <span class="text-fuchsia-300 font-semibold">Generate agent customization files</span>
  <span class="opacity-80"> directly from conversations</span>
</div>

<div class="grid grid-cols-3 gap-3">

<div class="p-4 bg-gradient-to-br from-cyan-500/15 to-cyan-500/5 rounded-lg border border-cyan-500/40 hover:scale-[1.02] transition-transform">
<div class="text-cyan-400 font-mono text-sm mb-2">/create-prompt</div>
<div class="text-gray-300 text-xs">Generate a reusable prompt file</div>
</div>

<div class="p-4 bg-gradient-to-br from-blue-500/15 to-blue-500/5 rounded-lg border border-blue-500/40 hover:scale-[1.02] transition-transform">
<div class="text-blue-400 font-mono text-sm mb-2">/create-instruction</div>
<div class="text-gray-300 text-xs">Generate instruction file for conventions</div>
</div>

<div class="p-4 bg-gradient-to-br from-indigo-500/15 to-indigo-500/5 rounded-lg border border-indigo-500/40 hover:scale-[1.02] transition-transform">
<div class="text-indigo-400 font-mono text-sm mb-2">/create-skill</div>
<div class="text-gray-300 text-xs">Extract multi-step workflow into skill</div>
</div>

<div class="p-4 bg-gradient-to-br from-purple-500/15 to-purple-500/5 rounded-lg border border-purple-500/40 hover:scale-[1.02] transition-transform">
<div class="text-purple-400 font-mono text-sm mb-2">/create-agent</div>
<div class="text-gray-300 text-xs">Create specialized custom agent persona</div>
</div>

<div class="p-4 bg-gradient-to-br from-violet-500/15 to-violet-500/5 rounded-lg border border-violet-500/40 hover:scale-[1.02] transition-transform">
<div class="text-violet-400 font-mono text-sm mb-2">/create-hook</div>
<div class="text-gray-300 text-xs">Create hook for lifecycle automation</div>
</div>

<div class="p-4 bg-gradient-to-br from-fuchsia-500/15 to-fuchsia-500/5 rounded-lg border border-fuchsia-500/40 hover:scale-[1.02] transition-transform">
<div class="text-fuchsia-400 font-mono text-sm mb-2">/fork, /compact</div>
<div class="text-gray-300 text-xs">Branch sessions, compress history</div>
</div>

</div>

</div>

---
layout: center
name: claude
---

<div class="text-center mb-6">
  <div class="text-5xl mb-4">🧠</div>
  <h1 class="!text-4xl bg-gradient-to-r from-purple-400 to-fuchsia-400 bg-clip-text text-transparent">Claude & Anthropic Integration</h1>
  <p class="text-xl opacity-80 mt-2">Claude Agent SDK, thinking tokens, and interleaved reasoning</p>
</div>

<div class="flex justify-center gap-6 mt-8">
  <div class="p-4 bg-purple-900/30 rounded-lg border border-purple-500/40 text-center w-56">
    <div class="text-3xl mb-2">🤖</div>
    <div class="font-bold text-purple-300">Claude Agent</div>
    <div class="text-xs opacity-70 mt-1">Anthropic harness in VS Code</div>
  </div>

  <div class="text-3xl text-purple-400/60 self-center">+</div>

  <div class="p-4 bg-fuchsia-900/30 rounded-lg border border-fuchsia-500/40 text-center w-56">
    <div class="text-3xl mb-2">💭</div>
    <div class="font-bold text-fuchsia-300">Thinking Tokens</div>
    <div class="text-xs opacity-70 mt-1">Visible reasoning in real-time</div>
  </div>
</div>

<div class="mt-8 p-4 bg-gradient-to-r from-purple-500/10 via-fuchsia-500/10 to-pink-500/10 rounded-lg border border-purple-500/20 text-center max-w-2xl mx-auto">
  <span class="text-purple-300 font-semibold">Interleaved Thinking:</span>
  <span class="opacity-80">Claude reasons between tool calls, showing hypothesis and error recovery</span>
</div>

---
layout: default
---

# Claude Agent & Thinking Tokens

<div class="mt-4 grid grid-cols-2 gap-5">

<div class="p-5 bg-gradient-to-br from-purple-500/15 to-purple-500/5 rounded-xl border border-purple-500/40">
<div class="flex items-center gap-2 mb-3">
  <span class="text-2xl">🤖</span>
  <span class="text-xl font-bold text-purple-400">Claude Agent</span>
</div>
<div class="space-y-2 text-sm text-gray-300">
<div class="flex items-center gap-2"><span class="text-purple-400">✨</span> Anthropic agent harness in VS Code</div>
<div class="flex items-center gap-2"><span class="text-purple-400">✨</span> Models from GitHub Copilot subscription</div>
<div class="flex items-center gap-2"><span class="text-purple-400">✨</span> Session type alongside Local/Background/Cloud</div>
<div class="flex items-center gap-2"><span class="text-purple-400">✨</span> Steering, queuing, session renaming (v1.110)</div>
</div>
</div>

<div class="p-5 bg-gradient-to-br from-fuchsia-500/15 to-fuchsia-500/5 rounded-xl border border-fuchsia-500/40">
<div class="flex items-center gap-2 mb-3">
  <span class="text-2xl">💭</span>
  <span class="text-xl font-bold text-fuchsia-400">Thinking Tokens</span>
</div>
<div class="space-y-2 text-sm text-gray-300">
<div class="flex items-center gap-2"><span class="text-fuchsia-400">🧠</span> Visible reasoning shows hypothesis formation</div>
<div class="flex items-center gap-2"><span class="text-fuchsia-400">🧠</span> See tool selection and error recovery live</div>
<div class="flex items-center gap-2"><span class="text-fuchsia-400">🧠</span> Interleaved thinking between tool calls</div>
</div>

<div class="mt-4 bg-black/30 rounded p-3 font-mono text-xs">
<div class="text-gray-500">// Default: 4000, set 0 to disable</div>
<div class="text-fuchsia-300">"github.copilot.chat.anthropic</div>
<div class="text-fuchsia-300 ml-0">&nbsp;&nbsp;.thinking.budgetTokens": <span class="text-yellow-400">10000</span></div>
<div class="mt-2 text-fuchsia-300">"chat.thinking.style": <span class="text-green-400">"detailed"</span></div>
</div>
</div>

</div>

---
layout: center
name: security
---

<div class="text-center mb-6">
  <div class="text-5xl mb-4">🔒</div>
  <h1 class="!text-4xl bg-gradient-to-r from-emerald-400 to-teal-400 bg-clip-text text-transparent">Security & Trust</h1>
  <p class="text-xl opacity-80 mt-2">Terminal sandboxing, auto-approval, and command isolation</p>
</div>

<div class="p-5 bg-gradient-to-r from-emerald-500/10 to-teal-500/10 rounded-xl border border-emerald-500/30 mb-6 text-center max-w-3xl mx-auto">
  <div class="text-lg opacity-80 mb-2">How do we enable autonomous AI execution while maintaining security?</div>
</div>

<div class="flex justify-center gap-6 mb-6">
  <div class="p-4 bg-emerald-900/30 rounded-lg border border-emerald-500/40 text-center w-48">
    <div class="text-3xl mb-2">📁</div>
    <div class="font-bold text-emerald-300">File System</div>
    <div class="text-xs opacity-70 mt-1">Workspace-only access</div>
  </div>

  <div class="p-4 bg-teal-900/30 rounded-lg border border-teal-500/40 text-center w-48">
    <div class="text-3xl mb-2">🌐</div>
    <div class="font-bold text-teal-300">Network</div>
    <div class="text-xs opacity-70 mt-1">Allowlist domains</div>
  </div>

  <div class="p-4 bg-cyan-900/30 rounded-lg border border-cyan-500/40 text-center w-48">
    <div class="text-3xl mb-2">💻</div>
    <div class="font-bold text-cyan-300">Platform</div>
    <div class="text-xs opacity-70 mt-1">macOS & Linux support</div>
  </div>
</div>

---
layout: default
---

# Terminal Sandboxing

<div class="mt-4">

<div class="p-3 bg-gradient-to-r from-emerald-500/10 to-teal-500/10 rounded-lg border border-emerald-500/30 mb-5 text-center">
  <span class="text-emerald-300 font-semibold">OS-level sandboxing</span>
  <span class="opacity-80"> restricts agent-executed terminal commands</span>
</div>

<div class="grid grid-cols-2 gap-5">

<div class="space-y-3">

<div class="p-4 bg-gradient-to-br from-emerald-500/15 to-emerald-500/5 rounded-lg border border-emerald-500/40">
<div class="flex items-center gap-2 mb-2">
  <span class="text-xl">📁</span>
  <span class="font-bold text-emerald-400">File System</span>
</div>
<div class="text-sm text-gray-300">Read/write only within workspace directory</div>
</div>

<div class="p-4 bg-gradient-to-br from-teal-500/15 to-teal-500/5 rounded-lg border border-teal-500/40">
<div class="flex items-center gap-2 mb-2">
  <span class="text-xl">🌐</span>
  <span class="font-bold text-teal-400">Network</span>
</div>
<div class="text-sm text-gray-300">Blocked by default; allowlist specific domains</div>
</div>

<div class="p-4 bg-gradient-to-br from-cyan-500/15 to-cyan-500/5 rounded-lg border border-cyan-500/40">
<div class="flex items-center gap-2 mb-2">
  <span class="text-xl">💻</span>
  <span class="font-bold text-cyan-400">Platform Support</span>
</div>
<div class="text-sm text-gray-300">macOS (sandbox-exec), Linux (Landlock/seccomp)</div>
</div>

</div>

<div>
<div class="bg-black/40 rounded-lg p-4 font-mono text-sm">
<div class="text-gray-500 text-xs mb-2">// Enable sandboxing</div>
<div class="text-emerald-300">"chat.tools.terminal</div>
<div class="text-emerald-300 ml-0">&nbsp;&nbsp;.sandbox.enabled": <span class="text-green-400">true</span>,</div>
<div class="text-emerald-300 mt-2">"chat.tools.terminal</div>
<div class="text-emerald-300 ml-0">&nbsp;&nbsp;.sandbox.network": [</div>
<div class="text-green-400 ml-4">"github.com",</div>
<div class="text-green-400 ml-4">"npmjs.com"</div>
<div class="text-gray-400">]</div>
</div>

<div class="mt-4 p-3 bg-green-500/10 rounded-lg border border-green-500/30">
<p class="text-sm text-gray-300">
✅ When sandboxing is enabled, commands run <span class="text-green-400 font-semibold">without confirmation dialogs</span>
</p>
</div>
</div>

</div>

</div>

---
layout: default
---

# Auto-Approval & /yolo Mode

<div class="mt-4">

<div class="p-3 bg-gradient-to-r from-cyan-500/10 to-indigo-500/10 rounded-lg border border-cyan-500/30 mb-5 text-center">
  <span class="opacity-80">Progressive expansion of </span>
  <span class="text-cyan-300 font-semibold">auto-approved commands</span>
</div>

<div class="space-y-3">

<div class="flex items-start bg-gradient-to-r from-cyan-500/15 to-cyan-500/5 rounded-lg p-4 border border-cyan-500/40">
<div class="text-cyan-400 font-bold text-lg mr-4 min-w-[90px]">v1.108</div>
<div class="text-gray-300 text-sm"><span class="font-mono text-cyan-300 bg-cyan-500/10 px-1 rounded">git ls-files</span>, <span class="font-mono text-cyan-300 bg-cyan-500/10 px-1 rounded">rg</span>, <span class="font-mono text-cyan-300 bg-cyan-500/10 px-1 rounded">sed</span>, workspace npm scripts</div>
</div>

<div class="flex items-start bg-gradient-to-r from-blue-500/15 to-blue-500/5 rounded-lg p-4 border border-blue-500/40">
<div class="text-blue-400 font-bold text-lg mr-4 min-w-[90px]">v1.109</div>
<div class="text-gray-300 text-sm"><span class="font-mono text-blue-300 bg-blue-500/10 px-1 rounded">Set-Location</span>, <span class="font-mono text-blue-300 bg-blue-500/10 px-1 rounded">dir</span>, <span class="font-mono text-blue-300 bg-blue-500/10 px-1 rounded">docker</span>, safe npm/yarn/pnpm commands</div>
</div>

<div class="flex items-start bg-gradient-to-r from-indigo-500/15 to-indigo-500/5 rounded-lg p-4 border border-indigo-500/40">
<div class="text-indigo-400 font-bold text-lg mr-4 min-w-[90px]">v1.110</div>
<div class="text-gray-300 text-sm"><span class="font-mono text-indigo-300 bg-indigo-500/10 px-1 rounded">/autoApprove</span>, <span class="font-mono text-indigo-300 bg-indigo-500/10 px-1 rounded">/yolo</span>, <span class="font-mono text-indigo-300 bg-indigo-500/10 px-1 rounded">/disableAutoApprove</span>, <span class="font-mono text-indigo-300 bg-indigo-500/10 px-1 rounded">/disableYolo</span></div>
</div>

</div>

<div class="mt-5 grid grid-cols-2 gap-4">
<div class="bg-black/30 rounded-lg p-4 font-mono text-sm">
<div class="text-cyan-300">"chat.tools.terminal.enableAutoApprove": <span class="text-green-400">true</span></div>
<div class="text-cyan-300">"chat.tools.terminal.autoApproveWorkspaceNpmScripts": <span class="text-green-400">true</span></div>
</div>

<div class="p-4 bg-indigo-500/10 rounded-lg border border-indigo-500/30">
<p class="text-sm text-gray-300">
💡 <span class="font-mono text-indigo-300">/yolo</span> — Toggle auto-approve directly from chat (v1.110)
</p>
</div>
</div>

</div>

---
layout: default
---

# Additional v1.110 Features

<div class="mt-4 grid grid-cols-2 gap-4">

<div class="p-4 bg-gradient-to-br from-cyan-500/15 to-cyan-500/5 rounded-xl border border-cyan-500/40">
<div class="flex items-center gap-2 mb-3">
  <span class="text-2xl">🌐</span>
  <span class="font-bold text-cyan-300">Agentic Browser Tools</span>
</div>
<div class="text-gray-300 text-sm space-y-1">
<div>🤖 Autonomous web interaction</div>
<div>🤖 Page navigation, reading, screenshots</div>
<div>🤖 Private, in-memory sessions</div>
</div>
<div class="mt-3 bg-black/30 rounded p-2 font-mono text-xs">
<div class="text-cyan-300">"workbench.browser</div>
<div class="text-cyan-300 ml-0">&nbsp;&nbsp;.enableChatTools": <span class="text-green-400">true</span></div>
</div>
</div>

<div class="p-4 bg-gradient-to-br from-blue-500/15 to-blue-500/5 rounded-xl border border-blue-500/40">
<div class="flex items-center gap-2 mb-3">
  <span class="text-2xl">🔍</span>
  <span class="font-bold text-blue-300">Agent Debug Panel</span>
</div>
<div class="text-gray-300 text-sm space-y-1">
<div>📊 Real-time event visibility</div>
<div>📊 System prompts, tool calls, customizations</div>
<div>📊 Chart view for event hierarchy</div>
</div>
<div class="mt-3 text-xs text-gray-400">
<span class="font-mono text-blue-300">Developer: Open Agent Debug Panel</span>
</div>
</div>

<div class="p-4 bg-gradient-to-br from-indigo-500/15 to-indigo-500/5 rounded-xl border border-indigo-500/40">
<div class="flex items-center gap-2 mb-3">
  <span class="text-2xl">🔨</span>
  <span class="font-bold text-indigo-300">Usages & Rename Tools</span>
</div>
<div class="text-gray-300 text-sm space-y-1">
<div>⚡ LSP-powered navigation</div>
<div>⚡ Precision refactoring</div>
<div>⚡ Hint: <span class="font-mono text-indigo-300">#rename</span>, <span class="font-mono text-indigo-300">#usages</span></div>
</div>
</div>

<div class="p-4 bg-gradient-to-br from-purple-500/15 to-purple-500/5 rounded-xl border border-purple-500/40">
<div class="flex items-center gap-2 mb-3">
  <span class="text-2xl">🍴</span>
  <span class="font-bold text-purple-300">Session Forking & Context</span>
</div>
<div class="text-gray-300 text-sm space-y-1">
<div>🌿 <span class="font-mono text-purple-300">/fork</span> — Branch conversations</div>
<div>📦 <span class="font-mono text-purple-300">/compact</span> — Compress history</div>
<div>💾 Plans persist to session memory</div>
</div>
</div>

</div>

---
layout: center
name: chat-ux
---

<div class="text-center mb-6">
  <div class="text-5xl mb-4">✨</div>
  <h1 class="!text-4xl bg-gradient-to-r from-blue-400 to-indigo-400 bg-clip-text text-transparent">Chat UX & Productivity</h1>
  <p class="text-xl opacity-80 mt-2">Mermaid diagrams, Copilot Memory, integrated browser, and more</p>
</div>

<div class="grid grid-cols-4 gap-4 mt-8">
  <div class="p-4 bg-blue-900/30 rounded-lg border border-blue-500/30 text-center">
    <div class="text-3xl mb-2">📊</div>
    <div class="font-semibold text-blue-300">Mermaid</div>
    <div class="text-xs opacity-70 mt-1">Interactive diagrams</div>
  </div>

  <div class="p-4 bg-indigo-900/30 rounded-lg border border-indigo-500/30 text-center">
    <div class="text-3xl mb-2">🧠</div>
    <div class="font-semibold text-indigo-300">Memory</div>
    <div class="text-xs opacity-70 mt-1">Persistent context</div>
  </div>

  <div class="p-4 bg-violet-900/30 rounded-lg border border-violet-500/30 text-center">
    <div class="text-3xl mb-2">🌐</div>
    <div class="font-semibold text-violet-300">Browser</div>
    <div class="text-xs opacity-70 mt-1">Full web integration</div>
  </div>

  <div class="p-4 bg-purple-900/30 rounded-lg border border-purple-500/30 text-center">
    <div class="text-3xl mb-2">🎨</div>
    <div class="font-semibold text-purple-300">MCP Apps</div>
    <div class="text-xs opacity-70 mt-1">Rich interactive UI</div>
  </div>
</div>

---
layout: default
---

# Chat Experience Enhancements

<div class="mt-4 grid grid-cols-2 gap-4">

<div class="p-4 bg-gradient-to-br from-blue-500/15 to-blue-500/5 rounded-xl border border-blue-500/40">
<div class="flex items-center gap-2 mb-3">
  <span class="text-2xl">📊</span>
  <span class="font-bold text-blue-300">Mermaid Diagrams</span>
</div>
<div class="text-gray-300 text-sm space-y-1">
<div>✨ Interactive diagrams in chat responses</div>
<div>✨ Pan, zoom, and open in full editor</div>
<div>✨ Flowcharts, sequence diagrams, more</div>
</div>
</div>

<div class="p-4 bg-gradient-to-br from-indigo-500/15 to-indigo-500/5 rounded-xl border border-indigo-500/40">
<div class="flex items-center gap-2 mb-3">
  <span class="text-2xl">❓</span>
  <span class="font-bold text-indigo-300">Ask Questions Tool</span>
</div>
<div class="text-gray-300 text-sm space-y-1">
<div>🤔 Agent presents clarifying questions</div>
<div>🤔 Single/multi-select, free text options</div>
<div>🤔 Discovery → Alignment → Refinement</div>
</div>
</div>

<div class="p-4 bg-gradient-to-br from-violet-500/15 to-violet-500/5 rounded-xl border border-violet-500/40">
<div class="flex items-center gap-2 mb-3">
  <span class="text-2xl">📈</span>
  <span class="font-bold text-violet-300">Context Window Details</span>
</div>
<div class="text-gray-300 text-sm space-y-1">
<div>📊 Token usage breakdown on hover</div>
<div>📊 See usage by category</div>
<div>📊 Understand context budget allocation</div>
</div>
</div>

<div class="p-4 bg-gradient-to-br from-purple-500/15 to-purple-500/5 rounded-xl border border-purple-500/40">
<div class="flex items-center gap-2 mb-3">
  <span class="text-2xl">🧠</span>
  <span class="font-bold text-purple-300">Copilot Memory</span>
</div>
<div class="text-gray-300 text-sm space-y-1">
<div>💾 Persistent context across sessions</div>
<div>💾 Store preferences and conventions</div>
<div>💾 Recall project context automatically</div>
</div>
<div class="mt-3 bg-black/30 rounded p-2 font-mono text-xs">
<div class="text-purple-300">"github.copilot.chat</div>
<div class="text-purple-300 ml-0">&nbsp;&nbsp;.copilotMemory.enabled": <span class="text-green-400">true</span></div>
</div>
</div>

</div>

---
layout: default
---

# More Chat Enhancements

<div class="mt-4 grid grid-cols-2 gap-4">

<div class="p-4 bg-gradient-to-br from-cyan-500/15 to-cyan-500/5 rounded-xl border border-cyan-500/40">
<div class="flex items-center gap-2 mb-3">
  <span class="text-2xl">🌐</span>
  <span class="font-bold text-cyan-300">Integrated Browser</span>
</div>
<div class="text-gray-300 text-sm space-y-1">
<div>🌍 Full browser replaces Simple Browser</div>
<div>🌍 Sign into websites, use DevTools</div>
<div>🌍 Send elements to chat for AI assistance</div>
</div>
<div class="mt-3 bg-black/30 rounded p-2 font-mono text-xs">
<div class="text-cyan-300">"workbench.browser</div>
<div class="text-cyan-300 ml-0">&nbsp;&nbsp;.openLocalhostLinks": <span class="text-green-400">true</span></div>
</div>
</div>

<div class="p-4 bg-gradient-to-br from-blue-500/15 to-blue-500/5 rounded-xl border border-blue-500/40">
<div class="flex items-center gap-2 mb-3">
  <span class="text-2xl">🎨</span>
  <span class="font-bold text-blue-300">MCP Apps</span>
</div>
<div class="text-gray-300 text-sm space-y-1">
<div>📊 Rich interactive UI in the client</div>
<div>📊 Flame graphs, custom visualizations</div>
<div>📊 MCP servers display UI elements</div>
</div>
</div>

<div class="p-4 bg-gradient-to-br from-indigo-500/15 to-indigo-500/5 rounded-xl border border-indigo-500/40">
<div class="flex items-center gap-2 mb-3">
  <span class="text-2xl">🔍</span>
  <span class="font-bold text-indigo-300">External Indexing</span>
</div>
<div class="text-gray-300 text-sm space-y-1">
<div>🔎 Non-GitHub workspaces get remote indexing</div>
<div>🔎 Fast semantic search via <span class="font-mono text-indigo-300">#codebase</span></div>
<div>🔎 Same experience as GitHub-hosted repos</div>
</div>
</div>

<div class="p-4 bg-gradient-to-br from-purple-500/15 to-purple-500/5 rounded-xl border border-purple-500/40">
<div class="flex items-center gap-2 mb-3">
  <span class="text-2xl">⚙️</span>
  <span class="font-bold text-purple-300">Language Models Editor</span>
</div>
<div class="text-gray-300 text-sm space-y-1">
<div>🎛️ Centralized model management</div>
<div>🎛️ Toggle visibility, configure API keys</div>
<div>🎛️ Stored in <span class="font-mono text-purple-300">chatLanguageModels.json</span></div>
</div>
</div>

</div>

---
layout: center
name: mental-model
---

<div class="text-center mb-4">
  <div class="text-5xl mb-3">🧠</div>
  <h1 class="!text-4xl bg-gradient-to-r from-cyan-400 to-indigo-400 bg-clip-text text-transparent">Mental Model Shift</h1>
  <p class="text-lg opacity-80 mt-2">The Complete Picture</p>
</div>

<div class="grid grid-cols-3 gap-4">

<div class="p-4 bg-gradient-to-br from-emerald-500/15 to-green-500/15 rounded-lg border border-emerald-500/30">
  <div class="flex items-center gap-2 mb-3">
    <span class="text-2xl">✅</span>
    <span class="font-bold text-emerald-300">Move Toward</span>
  </div>
  <div class="space-y-1 text-sm">
    <div class="flex items-center gap-2"><span class="text-emerald-400">✓</span> Multi-session workflows</div>
    <div class="flex items-center gap-2"><span class="text-emerald-400">✓</span> Domain-specific Skills</div>
    <div class="flex items-center gap-2"><span class="text-emerald-400">✓</span> Visible reasoning</div>
    <div class="flex items-center gap-2"><span class="text-emerald-400">✓</span> Sandboxed autonomy</div>
    <div class="flex items-center gap-2"><span class="text-emerald-400">✓</span> Org-level consistency</div>
  </div>
</div>

<div class="p-4 bg-gradient-to-br from-amber-500/15 to-yellow-500/15 rounded-lg border border-amber-500/30">
  <div class="flex items-center gap-2 mb-3">
    <span class="text-2xl">⚠️</span>
    <span class="font-bold text-amber-300">Move Away From</span>
  </div>
  <div class="space-y-1 text-sm">
    <div class="flex items-center gap-2"><span class="text-amber-400">⚠</span> Single long conversations</div>
    <div class="flex items-center gap-2"><span class="text-amber-400">⚠</span> Manual approval fatigue</div>
    <div class="flex items-center gap-2"><span class="text-amber-400">⚠</span> Per-dev divergence</div>
    <div class="flex items-center gap-2"><span class="text-amber-400">⚠</span> Context overflow</div>
  </div>
</div>

<div class="p-4 bg-gradient-to-br from-red-500/15 to-rose-500/15 rounded-lg border border-red-500/30">
  <div class="flex items-center gap-2 mb-3">
    <span class="text-2xl">🛑</span>
    <span class="font-bold text-red-300">Move Against</span>
  </div>
  <div class="space-y-1 text-sm">
    <div class="flex items-center gap-2"><span class="text-red-400">✕</span> Unsandboxed agents</div>
    <div class="flex items-center gap-2"><span class="text-red-400">✕</span> Context dumping</div>
    <div class="flex items-center gap-2"><span class="text-red-400">✕</span> Unrestricted access</div>
  </div>
</div>

</div>

<div class="mt-6 p-4 bg-gradient-to-r from-cyan-500/10 via-blue-500/10 to-indigo-500/10 rounded-lg border border-cyan-500/20 text-center max-w-2xl mx-auto">
  <span class="text-lg font-bold bg-gradient-to-r from-cyan-300 to-indigo-300 bg-clip-text text-transparent">From one assistant → to a team of specialized agents you orchestrate</span>
</div>

---
layout: center
name: get-started
---

<div class="text-center mb-4">
  <div class="text-5xl mb-3">🚀</div>
  <h1 class="!text-4xl bg-gradient-to-r from-amber-400 to-orange-400 bg-clip-text text-transparent">What You Can Do Today</h1>
  <p class="text-lg opacity-80 mt-2">Get Started in 15 Minutes</p>
</div>

<div class="grid grid-cols-3 gap-5 max-w-4xl mx-auto">

<div class="p-5 bg-gradient-to-br from-cyan-500/15 to-cyan-500/5 rounded-xl border border-cyan-500/40">
<div class="flex items-center gap-2 mb-3">
  <span class="text-2xl">⚡</span>
  <span class="font-bold text-cyan-300">Immediate</span>
  <span class="text-xs opacity-50">(5 min)</span>
</div>
<div class="space-y-2 text-sm text-gray-300">
<div>📦 Update VS Code to v1.110+</div>
<div>🚀 Try <span class="font-mono text-cyan-300">/init</span> for bootstrap</div>
<div>💭 Enable thinking tokens</div>
<div>🍴 Try <span class="font-mono text-cyan-300">/fork</span> to branch</div>
</div>
</div>

<div class="p-5 bg-gradient-to-br from-blue-500/15 to-blue-500/5 rounded-xl border border-blue-500/40">
<div class="flex items-center gap-2 mb-3">
  <span class="text-2xl">🔨</span>
  <span class="font-bold text-blue-300">Short-Term</span>
  <span class="text-xs opacity-50">(30 min)</span>
</div>
<div class="space-y-2 text-sm text-gray-300">
<div>🛡️ Enable terminal sandboxing</div>
<div>📚 Create first Agent Skill</div>
<div>🧩 Install an Agent Plugin</div>
<div>📦 Use <span class="font-mono text-blue-300">/compact</span></div>
</div>
</div>

<div class="p-5 bg-gradient-to-br from-indigo-500/15 to-indigo-500/5 rounded-xl border border-indigo-500/40">
<div class="flex items-center gap-2 mb-3">
  <span class="text-2xl">🎯</span>
  <span class="font-bold text-indigo-300">Explore</span>
  <span class="text-xs opacity-50">(1 hour)</span>
</div>
<div class="space-y-2 text-sm text-gray-300">
<div>🤖 Define custom agent</div>
<div>🧠 Enable Copilot Memory</div>
<div>🌐 Try agentic browser tools</div>
<div>✍️ Use <span class="font-mono text-indigo-300">/create-skill</span></div>
</div>
</div>

</div>

---
layout: center
---

<div class="text-center mb-6">
  <div class="text-5xl mb-4">💡</div>
  <h1 class="!text-4xl bg-gradient-to-r from-amber-400 to-yellow-400 bg-clip-text text-transparent">Key Takeaways</h1>
</div>

<div class="space-y-3 max-w-3xl mx-auto">

  <div class="flex items-center gap-4 p-3 bg-gradient-to-r from-cyan-500/10 to-blue-500/10 rounded-lg border border-cyan-500/20">
    <span class="text-2xl">🤖</span>
    <div><span class="font-semibold text-cyan-300">Four agent types for different workflows</span> <span class="opacity-70">— Local, Background, Cloud, Claude</span></div>
  </div>

  <div class="flex items-center gap-4 p-3 bg-gradient-to-r from-violet-500/10 to-purple-500/10 rounded-lg border border-violet-500/20">
    <span class="text-2xl">📚</span>
    <div><span class="font-semibold text-violet-300">Agent Skills & Plugins for customization</span> <span class="opacity-70">— domain expertise at scale</span></div>
  </div>

  <div class="flex items-center gap-4 p-3 bg-gradient-to-r from-purple-500/10 to-fuchsia-500/10 rounded-lg border border-purple-500/20">
    <span class="text-2xl">🧠</span>
    <div><span class="font-semibold text-purple-300">Claude with visible thinking tokens</span> <span class="opacity-70">— see AI reasoning in real-time</span></div>
  </div>

  <div class="flex items-center gap-4 p-3 bg-gradient-to-r from-emerald-500/10 to-teal-500/10 rounded-lg border border-emerald-500/20">
    <span class="text-2xl">🔒</span>
    <div><span class="font-semibold text-emerald-300">Terminal sandboxing enables safe autonomy</span> <span class="opacity-70">— auto-approve without risk</span></div>
  </div>

  <div class="flex items-center gap-4 p-3 bg-gradient-to-r from-blue-500/10 to-indigo-500/10 rounded-lg border border-blue-500/20">
    <span class="text-2xl">✨</span>
    <div><span class="font-semibold text-blue-300">/create-* commands bootstrap customization</span> <span class="opacity-70">— from conversation to config</span></div>
  </div>

</div>

---
layout: center
---

<div class="text-center mb-6">
  <div class="text-5xl mb-4">🙏</div>
  <h1 class="!text-4xl bg-gradient-to-r from-cyan-400 via-blue-400 to-indigo-400 bg-clip-text text-transparent">Thank You</h1>
  <p class="text-xl opacity-80 mt-2">What's New in Copilot for VS Code • v1.108 – v1.110</p>
</div>

<div class="grid grid-cols-2 gap-3 max-w-3xl mx-auto text-sm">
  <a href="https://code.visualstudio.com/updates/v1_110" target="_blank" class="p-3 bg-indigo-500/10 rounded-lg border border-indigo-500/20 hover:border-indigo-500/50 transition-all no-underline">
    <div class="font-semibold text-indigo-300">📚 v1.110 Release Notes</div>
    <div class="text-xs opacity-60 mt-1">February 2026</div>
  </a>

  <a href="https://code.visualstudio.com/updates/v1_109" target="_blank" class="p-3 bg-blue-500/10 rounded-lg border border-blue-500/20 hover:border-blue-500/50 transition-all no-underline">
    <div class="font-semibold text-blue-300">📚 v1.109 Release Notes</div>
    <div class="text-xs opacity-60 mt-1">January 2026</div>
  </a>

  <a href="https://code.visualstudio.com/updates/v1_108" target="_blank" class="p-3 bg-cyan-500/10 rounded-lg border border-cyan-500/20 hover:border-cyan-500/50 transition-all no-underline">
    <div class="font-semibold text-cyan-300">📚 v1.108 Release Notes</div>
    <div class="text-xs opacity-60 mt-1">December 2025</div>
  </a>

  <a href="https://code.visualstudio.com/docs/copilot/overview" target="_blank" class="p-3 bg-purple-500/10 rounded-lg border border-purple-500/20 hover:border-purple-500/50 transition-all no-underline">
    <div class="font-semibold text-purple-300">📖 Copilot Documentation</div>
    <div class="text-xs opacity-60 mt-1">Comprehensive guide</div>
  </a>
</div>

<div class="mt-6 text-center text-sm opacity-50">
  Update VS Code to v1.110+ and start experimenting today
</div>
