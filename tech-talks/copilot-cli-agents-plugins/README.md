---
status: active
updated: 2026-03-11
section: "Agent Architecture"
references:
  - url: https://docs.github.com/en/copilot/how-tos/use-copilot-agents/use-copilot-cli
    label: "Using GitHub Copilot CLI"
    verified: 2026-03-11
  - url: https://docs.github.com/en/copilot/how-tos/use-copilot-agents/coding-agent/create-custom-agents
    label: "Creating custom agents for Copilot"
    verified: 2026-03-11
  - url: https://docs.github.com/en/copilot/how-tos/copilot-cli/customize-copilot/create-skills
    label: "Creating agent skills for Copilot CLI"
    verified: 2026-03-11
  - url: https://docs.github.com/en/copilot/concepts/agents/copilot-cli/about-cli-plugins
    label: "About plugins for Copilot CLI"
    verified: 2026-03-11
  - url: https://docs.github.com/en/copilot/concepts/agents/copilot-cli/fleet
    label: "Running tasks in parallel with /fleet"
    verified: 2026-03-11
  - url: https://docs.github.com/en/copilot/reference/cli-plugin-reference
    label: "Copilot CLI plugin reference"
    verified: 2026-03-11
  - url: https://github.com/github/copilot-plugins
    label: "Official Copilot plugins repository"
    verified: 2026-03-11
  - url: https://github.blog/changelog/2026-02-25-github-copilot-cli-is-now-generally-available/
    label: "Copilot CLI GA announcement"
    verified: 2026-03-11
---

# GitHub Copilot CLI: Agents, Skills & the Plugin Ecosystem

> **The Question This Talk Answers:**
> *"How do I extend Copilot CLI beyond its defaults — building custom agents, migrating skills from IDE to CLI, and distributing reusable capabilities through plugins?"*

**Duration:** 30 minutes | **Target Audience:** Developers already using Copilot who want to go deeper

---

## 📊 Content Fitness

| Criterion | Assessment | Notes |
|-----------|-----------|-------|
| **Relevant** | 🟢 High | Teams adopting Copilot CLI need to customize it for their domain — default agents and skills aren't enough for specialized workflows like security audits, infrastructure management, or framework-specific patterns |
| **Compelling** | 🟢 High | Fleet mode cuts multi-file refactoring from sequential 45-min tasks to parallel 12-min runs; skills migration enables write-once-run-everywhere portability across CLI, VS Code, JetBrains, and cloud |
| **Actionable** | 🟢 High | Create your first custom agent in 5 minutes; migrate an IDE instruction to a portable skill in 10 minutes; install a plugin from a marketplace in 30 seconds |

**Overall Status:** 🟢 Ready to use

---

## 📽️ Slide Generation Mapping

### Slide Sequence (Generated Automatically)

1. **Title/Logo Slide** ← H1 title + subtitle
2. **Question/Objective Slide** ← "The Question This Talk Answers"
3. **Table of Contents Slide** ← Auto-generated from 🎬 sections
4. **Problem Slide** ← "The Problem"
5. **Solution Overview** ← "The Solution"
6. **Key Artifacts** ← Primary artifacts inventory
7. **🧠 The Shift (Preview)** ← Core Insight one-liner
8. **When to Use Decision Tree** ← "When to Use This Pattern"
9. **Custom Agents Deep Dive** ← 🎬 Section 1 (3-4 slides)
10. **Fleet Mode & Subagents** ← 🎬 Section 2 (2-3 slides)
11. **Skills: The Portable Standard** ← 🎬 Section 3 (2-3 slides)
12. **Plugin Ecosystem** ← 🎬 Section 4 (2-3 slides)
13. **Use Cases** ← Real-World Use Cases (2 slides)
14. **🧠 Mental Model Shift (Full)** ← Move-Toward/Away/Against grid
15. **Actionable Outcomes** ← What You Can Do Today
16. **Related Patterns** ← Related Patterns
17. **📖 References** ← References section
18. **End Slide** ← Auto-generated

### Major Sections (TOC Entries)

```markdown
<!-- 🎬 MAJOR SECTION: Custom Agents -->
<!-- 🎬 MAJOR SECTION: Fleet Mode -->
<!-- 🎬 MAJOR SECTION: Skills -->
<!-- 🎬 MAJOR SECTION: Plugins -->
```

---

## The Problem

### Key Points

- **Default agents are generic**
  Built-in agents (Explore, Task, Code-review) handle common patterns, but every team has domain-specific workflows — security review processes, framework migration checklists, infrastructure runbooks — that require specialized knowledge beyond what defaults provide

- **IDE customizations don't travel**
  Teams invest hours crafting `copilot-instructions.md` and IDE-specific settings, but those customizations stay locked inside one editor. Switch to CLI or another IDE, and you start from scratch — duplicating effort across surfaces

- **Manual setup for every project**
  Configuring agents, MCP servers, LSP servers, and skills manually in every repository means 30+ minutes of repetitive setup. Without a distribution mechanism, team expertise lives in wiki pages and Slack threads instead of installable packages

- **Sequential execution bottleneck**
  Complex tasks like "refactor these 8 services" or "write tests for all endpoints" execute one step at a time, with the developer waiting through each iteration — turning a 2-hour task into an all-afternoon affair

### Narrative

You've installed Copilot CLI and it's changed your terminal workflow. Plan Mode is saving you debugging cycles, interactive sessions feel natural, and you can't imagine going back. But after a few weeks, you hit the ceiling.

Your team's React codebase has specific patterns — custom hooks, a particular testing strategy, a deployment workflow that's unique to your infrastructure. The default Explore and Task agents don't know any of this. You've written great custom instructions for VS Code, but when you switch to the CLI for a deployment debugging session, that knowledge is gone. And when a new team member joins, they spend their first day manually setting up the same agents, MCP servers, and skills that everyone else already has.

Meanwhile, that large refactoring task you need — updating 12 microservices to a new API contract — still requires you to sit there watching Copilot process one service at a time. There has to be a better way.

---

## The Solution: Copilot CLI's Extensibility Stack

### What It Does

Copilot CLI provides a four-layer extensibility model: **custom agents** for specialized AI personas, **skills** for portable procedural knowledge, **fleet mode** for parallel task execution, and **plugins** for distributing all of the above as installable packages. Together, they transform Copilot CLI from a conversational tool into a customizable, team-aware development platform. [^1]

### Key Capabilities

- **Custom Agents (.agent.md)**: Define specialized AI assistants with tailored expertise, tool access, and model selection — scoped to user, repository, or organization level [^2]
- **Agent Skills (SKILL.md)**: Portable, on-demand procedural knowledge that works identically across CLI, VS Code, JetBrains, and cloud agents — loaded only when relevant [^3]
- **Fleet Mode (/fleet)**: Parallel task execution via subagents, each with their own context window — orchestrated by the main agent with dependency management [^5]
- **Plugin Ecosystem**: Bundle agents, skills, hooks, and MCP/LSP configs into installable packages — distributed through marketplaces or direct repository install [^4]

### Architecture Overview

The extensibility stack builds upward. At the base, **custom agents** define *who* does the work — specialized personas with scoped tools and specific models. **Skills** define *how* they work — portable procedures loaded on-demand. **Fleet mode** defines *when* they work together — parallel orchestration for multi-part tasks. **Plugins** define *how it all ships* — bundling everything into discoverable, installable packages.

Each layer is optional and independent. You can use custom agents without skills, skills without plugins, or fleet mode without custom agents. But together, they create a composable system where team expertise becomes infrastructure.

**Official Documentation:**
- 📖 [Using Copilot CLI](https://docs.github.com/en/copilot/how-tos/use-copilot-agents/use-copilot-cli) — Core CLI usage and commands
- 📖 [Creating Custom Agents](https://docs.github.com/en/copilot/how-tos/use-copilot-agents/coding-agent/create-custom-agents) — Agent profile configuration
- 📖 [Creating Agent Skills](https://docs.github.com/en/copilot/how-tos/copilot-cli/customize-copilot/create-skills) — SKILL.md format and usage

---

## 🖼️ Visual Assets

*Visual content will be generated during slide creation using styled HTML components.*

**Potential visual assets to generate:**
- Extensibility stack diagram (Agents → Skills → Fleet → Plugins)
- Agent scope hierarchy (User → Repository → Organization → Enterprise)
- Skills migration comparison (IDE instructions vs. SKILL.md)
- Fleet mode orchestration flow (Main agent → parallel subagents → composed result)
- Plugin structure anatomy (agents/ + skills/ + hooks.json + .mcp.json)

---

## 📦 Key Artifacts

**Primary Artifacts** — *Shown inline in major sections with detailed explanation*

- **Custom agent profile (`.agent.md`)** — Specialized agent with description, tools, model selection, and behavioral instructions
- **Skill definition (`SKILL.md`)** — Portable procedural knowledge with YAML frontmatter and step-by-step instructions
- **Fleet mode workflow** — `/fleet` command orchestrating parallel subagents for a multi-service refactoring task
- **Plugin manifest (`plugin.json`)** — Distribution package bundling agents, skills, hooks, and integrations

### Supporting Files

*Available in documentation references*

- **[Plugin Reference](https://docs.github.com/en/copilot/reference/cli-plugin-reference)** — Full plugin structure and manifest specification
- **[Custom Agent Configuration](https://docs.github.com/en/copilot/reference/custom-agents-configuration)** — YAML properties, tools, and MCP server setup
- **[Skills vs. Instructions](https://docs.github.com/en/copilot/concepts/agents/copilot-cli/comparing-cli-features)** — Comparing CLI customization features

---

## 🎯 Mental Model Shift

> **The Core Insight:** From "using Copilot CLI as a smart terminal assistant" to "building a team of specialized AI agents, each with portable expertise, orchestrated in parallel, and distributed as installable packages"

### Move Toward (Embrace These Patterns)

- ✅ **Agent-per-Workflow**: Create dedicated agents for distinct workflows (security review, migration, onboarding) with scoped tools and models → Each agent becomes an expert that new team members can invoke immediately without tribal knowledge
- ✅ **Skills as Portable Playbooks**: Encode domain procedures in SKILL.md format instead of wiki pages or Slack threads → Procedures travel across CLI, IDE, and cloud; Copilot loads them automatically when relevant
- ✅ **Parallel-First for Multi-Part Tasks**: Use `/fleet` for any task with 3+ independent components → Multi-service refactoring completes in 12 min instead of 45 min sequential
- ✅ **Plugins for Team Distribution**: Package your agents + skills + configs as plugins → New team members run `/plugin install` and get the entire team's AI configuration in 30 seconds
- ✅ **Model-per-Task Optimization**: Assign specific models to specific agents (Opus for architecture review, Haiku for quick checks) → Better quality where it matters, lower cost where it doesn't

### Move Away From (Retire These Habits)

- ⚠️ **Monolithic Custom Instructions**: Cramming everything into one `copilot-instructions.md` file → Context overload; skills load on-demand, instructions load always. Separate procedural workflows into skills
- ⚠️ **IDE-Locked Customizations**: Writing VS Code-specific Copilot configurations that don't work in CLI → Use .agent.md and SKILL.md formats that work everywhere
- ⚠️ **Sequential Complex Tasks**: Running large multi-part tasks one step at a time → Fleet mode exists; if subtasks are independent, parallelize them
- ⚠️ **Wiki-Based Knowledge Sharing**: Documenting agent setups and workflows in Confluence/Notion → Package them as plugins; they're executable, not just readable

### Move Against (Active Resistance Required)

- 🛑 **Over-Scoping Agent Permissions**: Giving custom agents access to all tools when they only need a few → Explicitly list tools in the agent profile; principle of least privilege applies to AI agents too
- 🛑 **Ignoring Skill Descriptions**: Writing vague SKILL.md descriptions → The description controls *when* Copilot loads the skill; vague descriptions mean the skill is never triggered or triggered incorrectly
- 🛑 **Fleet Mode for Sequential Work**: Using `/fleet` when tasks have strict dependencies → Fleet orchestrates parallel work; sequential chains don't benefit and may waste premium requests

> **Example Transformation:** Before: New team member spends 2 hours reading wiki docs, manually creating .agent.md files, configuring MCP servers, and writing instructions. After: `/plugin install team/platform-toolkit` — 30 seconds, fully configured with 5 agents, 8 skills, and 2 MCP servers.

---

## When to Use This Pattern

### Decision Tree

```
Q: What are you trying to customize about Copilot CLI?
├─ "I need AI with domain-specific expertise" → Create: Custom Agent (.agent.md)
│  └─ Best for: Framework patterns, review checklists, deployment workflows
│
├─ "I have procedures Copilot should follow for specific tasks" → Create: Skill (SKILL.md)
│  └─ Best for: Debugging playbooks, testing strategies, migration steps
│
├─ "I need to parallelize a large multi-part task" → Use: Fleet Mode (/fleet)
│  └─ Best for: Multi-service refactoring, test suite generation, batch operations
│
├─ "I need to distribute my setup to the team" → Create: Plugin
│  └─ Best for: Onboarding, team standardization, cross-project consistency
│
└─ "I just need project-level context for every prompt" → Use: Custom Instructions
   └─ Best for: Coding standards, naming conventions, architecture decisions
```

### Use This Pattern When

- Your team has domain-specific workflows that the default agents don't handle
- You're maintaining duplicate AI configurations across IDE and CLI
- Complex tasks could be parallelized but you're running them sequentially
- New team members spend significant time configuring their AI tooling

### Don't Use This Pattern When

- Default agents handle your workflow well → Stick with built-in Explore, Task, Code-review agents
- Your customization is simple project context → Use `copilot-instructions.md` instead of agents/skills
- Tasks are inherently sequential → Fleet mode won't help; use regular interactive mode
- You're the only user → Plugins add overhead for solo developers; use local agents/skills directly

### Comparison with Related Features

| Aspect | Custom Agents | Skills | Custom Instructions | Plugins |
|--------|--------------|--------|-------------------|---------|
| **Best For** | Specialized AI personas | Procedural task knowledge | Project-wide context | Team distribution |
| **Loading** | Selected explicitly or by AI | On-demand when relevant | Always loaded | Installed once |
| **Scope** | User / Repo / Org | Project / Personal | Repository | Any project |
| **Portability** | CLI + IDE + Cloud | CLI + IDE + Cloud | CLI + IDE | CLI (and expanding) |
| **Complexity** | Medium | Low | Low | Medium-High |

---

<!-- 🎬 MAJOR SECTION: Custom Agents -->
## Custom Agents: Specialized AI for Every Workflow

Custom agents are Markdown files (`.agent.md`) that define specialized AI assistants with tailored expertise, scoped tool access, and optional model selection. They transform Copilot from a generalist into a team of specialists. [^2]

### Agent Profile Anatomy

An agent profile combines YAML frontmatter (identity and capabilities) with Markdown body (behavioral instructions):

```markdown
# .github/agents/security-reviewer.agent.md
---
description: "Reviews code changes for security vulnerabilities, OWASP Top 10
  compliance, and dependency risks. Use for security-focused code review."
tools:
  - read
  - search
  - github-mcp-server
model: claude-opus-4.6
---

You are a senior security engineer reviewing code for vulnerabilities.

## Review Process
1. Check for OWASP Top 10 vulnerabilities (injection, XSS, auth issues)
2. Verify input validation on all external data entry points
3. Review dependency versions against known CVE databases
4. Flag hardcoded secrets or credentials
5. Assess authentication and authorization flows

## Output Format
- Use severity levels: 🔴 Critical | 🟡 Warning | 🟢 Info
- Include CWE numbers where applicable
- Provide remediation guidance for each finding
```

**Key Points:**
- `description` is critical — it controls when Copilot routes work to this agent automatically
- `tools` restricts what the agent can do (principle of least privilege)
- `model` lets you assign the right model for the task (Opus for deep review, Haiku for quick checks)
- The Markdown body is the agent's prompt — up to 30,000 characters of behavioral instructions

### Scope Hierarchy

Agents can be defined at four levels, with system-level overriding repository-level, and repository-level overriding organization-level:

| Scope | Location | Use Case |
|-------|----------|----------|
| **User** | `~/.copilot/agents/` | Personal productivity agents across all projects |
| **Repository** | `.github/agents/` | Project-specific workflows (testing, deployment) |
| **Organization** | `.github-private` repo `agents/` | Company-wide standards (security, compliance) |
| **Enterprise** | `.github-private` repo `agents/` | Enterprise governance and policy enforcement |

### Built-in Agents

Copilot CLI ships with four built-in agents that handle common delegation patterns: [^1]

| Agent | Purpose | When It's Used |
|-------|---------|----------------|
| **Explore** | Fast codebase analysis and Q&A | Questions about code structure, finding files, understanding patterns |
| **Task** | Command execution with smart output | Running tests, builds, lints — brief on success, verbose on failure |
| **General-purpose** | Complex multi-step tasks | Full toolset work in a separate context window |
| **Code-review** | High signal-to-noise review | Surfaces only genuine bugs, security issues, logic errors |

### Invoking Agents

Three ways to use custom agents:

```bash
# 1. Browse and select interactively
/agent

# 2. Reference naturally in your prompt
Use the security-reviewer agent to review my latest changes

# 3. Specify directly at launch
copilot --agent=security-reviewer --prompt "Review the auth module"
```

---

<!-- 🎬 MAJOR SECTION: Fleet Mode -->
## Fleet Mode: Parallel Execution with Subagents

The `/fleet` command transforms Copilot CLI from a single-threaded assistant into a parallel task orchestrator. The main agent analyzes your request, decomposes it into independent subtasks, and dispatches subagents to execute them simultaneously — each with their own context window. [^5]

### How Fleet Mode Works

```
Developer prompt: "/fleet Refactor all 6 API controllers to use the new middleware pattern"

Main Agent (Orchestrator)
├── Analyzes task → identifies 6 independent controller refactors
├── Checks dependencies → confirms controllers are independent
├── Dispatches subagents in parallel:
│   ├── Subagent 1: users-controller.ts    (uses @refactor-agent)
│   ├── Subagent 2: orders-controller.ts   (uses @refactor-agent)
│   ├── Subagent 3: products-controller.ts (uses @refactor-agent)
│   ├── Subagent 4: payments-controller.ts (uses @refactor-agent)
│   ├── Subagent 5: auth-controller.ts     (uses @refactor-agent)
│   └── Subagent 6: search-controller.ts   (uses @refactor-agent)
└── Composes results → verifies consistency → reports completion
```

### Key Benefits

- **Speed**: Parallel execution of independent subtasks — 6 controllers refactored simultaneously instead of sequentially
- **Specialization**: Subagents can use custom agents (e.g., `@test-writer` for test generation, `@security-reviewer` for audits)
- **Model routing**: Assign different models to different subtasks within the same prompt (`Use GPT-5.3-Codex to generate the schema, use Claude Opus to review it`)
- **Isolated context**: Each subagent gets its own context window, preventing context overload on complex tasks

### Fleet + Autopilot Workflow

The most powerful pattern combines Plan Mode, Fleet Mode, and Autopilot:

```
1. Shift+Tab           → Enter Plan Mode
2. Describe the task   → Copilot creates an implementation plan
3. Review the plan     → Identify parallelizable components
4. Accept plan + /fleet + autopilot → Copilot decomposes, parallelizes, and executes autonomously
```

### When Fleet Mode Shines

| ✅ Great Fit | ❌ Poor Fit |
|-------------|-----------|
| Refactor multiple independent files | Sequential data pipeline steps |
| Generate tests for many endpoints | Single complex algorithm design |
| Update configs across services | Tasks requiring tight coordination |
| Batch code reviews | Exploratory/conversational work |

**Cost consideration:** Each subagent consumes premium requests independently. For simple tasks, the overhead of orchestration may exceed the time saved. Use `/fleet` when the task genuinely has 3+ parallelizable components. [^5]

---

<!-- 🎬 MAJOR SECTION: Skills -->
## Skills: The Portable Procedural Standard

Agent skills are the answer to "how do I teach Copilot a specific procedure?" — not just project context (that's custom instructions), but step-by-step workflows that Copilot should follow for particular task types. Skills are portable across CLI, VS Code, JetBrains, and cloud agents. [^3]

### Skills vs. Custom Instructions

| Dimension | Custom Instructions | Skills (SKILL.md) |
|-----------|-------------------|--------------------|
| **Loading** | Always in context for every prompt | On-demand — loaded only when the task matches |
| **Purpose** | Project conventions, coding standards | Procedural workflows, task-specific playbooks |
| **Context cost** | Constant token overhead | Zero cost until needed |
| **Format** | Markdown file (`.md`) | Folder with `SKILL.md` + optional scripts/resources |
| **Trigger** | Automatic | Description-based matching or explicit `/skill-name` invocation |

### Anatomy of a Skill

A skill lives in its own directory with a `SKILL.md` file and optional supporting resources:

```
.github/skills/
  webapp-testing/
    SKILL.md           # Required: instructions + metadata
    scripts/
      setup-env.sh     # Optional: helper scripts
    templates/
      test-template.ts # Optional: reference templates
```

```markdown
# .github/skills/webapp-testing/SKILL.md
---
name: webapp-testing
description: >-
  End-to-end testing strategy for web applications using Playwright.
  Use when asked to create tests, write E2E tests, or test web UI.
license: MIT
---

## Procedure

1. Analyze the target component and determine testing scope
2. Create test files following the AAA pattern (Arrange, Act, Assert)
3. Use Playwright for browser automation — prefer `getByRole` selectors
4. Run tests with `npx playwright test` and verify all pass
5. Add screenshot comparison for visual regression tests

## Standards
- Test files: `*.spec.ts` in `tests/` directory
- Naming: `describe('ComponentName', () => { ... })`
- Coverage target: 80% for critical user flows

## Helper Scripts
- `scripts/setup-env.sh`: Configures test database and fixtures
```

### Migrating from IDE Instructions to Skills

If your team has built up domain knowledge in IDE-specific formats, here's the migration path:

| Before (IDE-Only) | After (Portable Skill) |
|--------------------|----------------------|
| Long `copilot-instructions.md` with mixed concerns | Split: conventions stay in instructions, procedures become skills |
| VS Code `settings.json` Copilot overrides | `.agent.md` profiles with explicit tool/model configuration |
| Tribal knowledge in wiki/Slack | `SKILL.md` with step-by-step procedures and helper scripts |
| IDE-locked behavior | Works across CLI, VS Code, JetBrains, GitHub.com, and cloud agents |

**Migration checklist:**
1. **Audit** your `copilot-instructions.md` — identify sections that describe *procedures* (step-by-step workflows)
2. **Extract** each procedure into its own skill directory under `.github/skills/`
3. **Write** clear `description` fields — this controls when Copilot loads the skill autonomously
4. **Add** any helper scripts or templates referenced by the procedure
5. **Test** with `/skills list` to confirm registration, then trigger with a relevant prompt
6. **Trim** the original instructions file to only project-wide conventions

### Skill Scope Options

| Location | Scope | Use Case |
|----------|-------|----------|
| `.github/skills/` | Repository | Project-specific testing, deployment, review procedures |
| `.claude/skills/` | Repository | Alternative location (cross-compatible with Claude Code) |
| `~/.copilot/skills/` | Personal | Your personal productivity workflows across all projects |
| `~/.claude/skills/` | Personal | Alternative personal location (cross-compatible) |

---

<!-- 🎬 MAJOR SECTION: Plugins -->
## Plugins: The Distribution Layer

Plugins solve the last-mile problem: you've built great agents and skills, but how do you distribute them to your team, standardize across repositories, and keep everything versioned? Plugins bundle agents, skills, hooks, and integrations into installable packages. [^4]

### What's in a Plugin?

A plugin is a structured directory with a manifest and any combination of components:

```
my-platform-toolkit/
├── .github/plugin/
│   └── plugin.json        # Manifest: name, version, contents
├── agents/
│   ├── security-reviewer.agent.md
│   └── migration-helper.agent.md
├── skills/
│   ├── webapp-testing/
│   │   └── SKILL.md
│   └── api-debugging/
│       └── SKILL.md
├── hooks.json              # Event handlers for agent behavior
├── .mcp.json               # MCP server configurations
├── lsp.json                # LSP server configurations
└── README.md
```

### Plugins vs. Manual Configuration

| Feature | Manual Config | Plugin |
|---------|--------------|--------|
| **Scope** | Single repository | Any project |
| **Sharing** | Manual copy/paste | `/plugin install` command |
| **Versioning** | Git history | Marketplace versions |
| **Discovery** | Searching repositories | Marketplace browsing |
| **Updates** | Manual sync | Managed updates |

### Installing Plugins

Three installation sources: [^4]

```bash
# From a marketplace (default: copilot-plugins, awesome-copilot)
/plugin install security-toolkit

# From a GitHub repository
/plugin install myorg/platform-toolkit

# From a local path (development/testing)
/plugin install ./my-local-plugin
```

### The Marketplace Model

Marketplaces are registries where plugins are published, discovered, and installed. Two official marketplaces ship by default: [^7]

- **[copilot-plugins](https://github.com/github/copilot-plugins)** — Official GitHub-curated plugins
- **[awesome-copilot](https://github.com/github/awesome-copilot)** — Community-curated collection

Organizations can add custom marketplaces for internal plugin distribution:

```bash
# Add your organization's internal marketplace
/plugin marketplace add myorg/copilot-marketplace
```

### Plugin Lifecycle

```
Create → Publish → Discover → Install → Use → Update
  │         │          │          │        │       │
  │    Push to     Browse      /plugin   Auto-    /plugin
  │    marketplace  /plugin    install   loaded    update
  │    repo         search              on start
  │
  Build agents + skills + hooks + MCP configs locally
```

---

## Real-World Use Cases

### Use Case 1: Platform Team Onboarding Kit

**The Problem:** New developers joining a platform team spend 2+ hours configuring Copilot CLI — creating agents for infrastructure review, adding MCP servers for cloud APIs, writing skills for deployment workflows, and configuring LSP servers for Terraform/Kubernetes.

**The Solution:** Package the entire team configuration as a plugin. New members install once and get everything:

```bash
/plugin install platform-team/infra-toolkit

# Installs:
# ✅ 4 custom agents (infra-reviewer, terraform-expert, k8s-debugger, cost-analyzer)
# ✅ 6 skills (deployment-checklist, incident-response, capacity-planning, ...)
# ✅ 2 MCP servers (AWS, Datadog)
# ✅ 1 LSP server (Terraform)
```

**Outcome:** 2+ hours of manual setup → 30 seconds. New team members are productive with AI-assisted infrastructure work from day one.

---

### Use Case 2: Fleet Mode for Microservice Migration

**The Problem:** Migrating 8 microservices from REST to gRPC requires updating proto definitions, service implementations, client libraries, and tests for each service — a sequential process that takes a full day with Copilot handling one service at a time.

**The Solution:** Plan the migration in Plan Mode, then execute with Fleet Mode:

```bash
# Step 1: Plan Mode
> Shift+Tab
> Plan the migration of our 8 services from REST to gRPC. Each service
> needs: proto definitions, server implementation, client library, and tests.

# Step 2: Review plan, then execute in parallel
> Accept plan and build on autopilot + /fleet

# Fleet dispatches 8 subagents, each using @migration-helper agent
# Each subagent has its own context window focused on one service
```

**Outcome:** 8 hours sequential → 2 hours parallel. Each subagent operates independently with focused context, and the orchestrator ensures consistency across services.

---

### Use Case 3: Cross-IDE Skill Portability

**The Problem:** A team has built detailed testing procedures as VS Code Copilot instructions. When developers use CLI for debugging or CI/CD, those testing procedures aren't available. When they use JetBrains, same problem.

**The Solution:** Migrate procedures to SKILL.md format:

```bash
# Before: Locked in VS Code copilot-instructions.md
"When writing tests, always use AAA pattern, prefer getByRole selectors..."

# After: Portable skill in .github/skills/testing-standards/SKILL.md
---
name: testing-standards
description: >-
  Testing procedures for our React application. Use when creating tests,
  reviewing test code, or discussing testing strategy.
---
## Procedure
1. Use AAA pattern (Arrange, Act, Assert)
2. Prefer getByRole selectors for accessibility
3. ...
```

**Outcome:** Write once, available everywhere — CLI, VS Code, JetBrains, GitHub.com code review, and Copilot coding agent in the cloud.

---

## ✅ What You Can Do Today

**Immediate Actions (15 minutes):**
- [ ] Create your first custom agent: write a `.agent.md` file in `.github/agents/` describing a workflow you repeat
- [ ] Run `/agent` in Copilot CLI to see all available agents (built-in + custom)
- [ ] Try `/skills list` to see currently loaded skills, and `/skills` to toggle them on/off

**Short-Term Implementation (1 hour):**
- [ ] Audit your `copilot-instructions.md` — identify 2-3 procedural sections to extract as skills
- [ ] Create your first SKILL.md under `.github/skills/` with a clear description and step-by-step procedure
- [ ] Try `/fleet` on a multi-file task (e.g., "add error handling to all API routes")

**Advanced Exploration (2-4 hours):**
- [ ] Build a team plugin: bundle your agents + skills + MCP configs into a plugin with `plugin.json` manifest
- [ ] Set up a custom marketplace for your organization's internal plugins
- [ ] Create agents with model-specific assignments (Opus for deep review, Haiku for quick checks)

**Next Steps After Completion:**
1. ✅ Complete the immediate actions above
2. 📖 Review related talk: [Copilot CLI Fundamentals](../copilot-cli/) for core CLI capabilities
3. 📖 Review related talk: [MCP Apps](../mcp-apps/) for extending agent capabilities with MCP
4. 🚀 Explore: [Plugin Reference](https://docs.github.com/en/copilot/reference/cli-plugin-reference) for full manifest specification

---

## Related Patterns

### Complementary Features

- **[Copilot CLI Fundamentals](../copilot-cli/)** — Core CLI capabilities (Plan Mode, operating modes, context management) — start here if you haven't used CLI yet
- **[MCP Apps](../mcp-apps/)** — Extending agent capabilities with external tools via Model Context Protocol — combine with agents for powerful integrations
- **[Copilot Hooks](../copilot-hooks/)** — Event-driven automation that intercepts agent behavior — hooks are bundled inside plugins
- **[Multi-Step Tasks](../multi-step-tasks/)** — Patterns for complex agentic workflows — fleet mode is one orchestration pattern among several

### Decision Flow

**If this talk doesn't fit your needs:**

```
Q: What's your actual goal?
├─ "I need CLI basics first" → See: [Copilot CLI Fundamentals](../copilot-cli/)
├─ "I want to extend agents with external tools" → See: [MCP Apps](../mcp-apps/)
├─ "I need enterprise-wide AI governance" → See: [Enterprise Patterns](../enterprise-patterns/)
└─ "I want to understand the full agentic journey" → See: [Agentic Journey](../agentic-journey/)
```

See [DECISION-GUIDE.md](../DECISION-GUIDE.md) for complete navigation help.

---

## 📖 References

### Official Documentation

[^1]: **[Using GitHub Copilot CLI](https://docs.github.com/en/copilot/how-tos/use-copilot-agents/use-copilot-cli)** — Core CLI usage, agents, and commands
[^2]: **[Creating Custom Agents](https://docs.github.com/en/copilot/how-tos/use-copilot-agents/coding-agent/create-custom-agents)** — Agent profile configuration and YAML properties
[^3]: **[Creating Agent Skills](https://docs.github.com/en/copilot/how-tos/copilot-cli/customize-copilot/create-skills)** — SKILL.md format, scope, and usage
[^4]: **[About Plugins for Copilot CLI](https://docs.github.com/en/copilot/concepts/agents/copilot-cli/about-cli-plugins)** — Plugin concepts, components, and marketplace model
[^5]: **[Running Tasks in Parallel with /fleet](https://docs.github.com/en/copilot/concepts/agents/copilot-cli/fleet)** — Fleet mode architecture and usage

### Blog Posts & Announcements

[^6]: **[Copilot CLI is Now Generally Available](https://github.blog/changelog/2026-02-25-github-copilot-cli-is-now-generally-available/)** — GA announcement with latest features and capabilities

### Community & Ecosystem

[^7]: **[Official Copilot Plugins Repository](https://github.com/github/copilot-plugins)** — Default marketplace for discovering and publishing plugins
[^8]: **[Copilot CLI Plugin Reference](https://docs.github.com/en/copilot/reference/cli-plugin-reference)** — Full plugin manifest specification and structure

---

## 🎭 Behind the Scenes

*For those who want to understand the deeper mechanics*

### How Skill Triggering Works

When you enter a prompt, Copilot evaluates the `description` field of every available skill against your request. If a skill's description matches the intent, its `SKILL.md` content is injected into the agent's context for that interaction only.

1. **Prompt analysis**: Copilot parses your request intent
2. **Description matching**: Each skill's `description` is compared against the intent
3. **Context injection**: Matching skills' `SKILL.md` content is added to the agent's context
4. **Execution**: The agent follows the skill's procedures while working on the task
5. **Cleanup**: Skill content is removed from context when no longer relevant

**Why This Matters:** The `description` field is the most important part of your SKILL.md. A vague description means the skill never triggers. A description that's too broad means it triggers on irrelevant tasks, wasting context tokens.

### Subagent Context Isolation in Fleet Mode

Each subagent spawned by `/fleet` operates in a completely independent context window. This isolation is key to fleet mode's effectiveness:

- **No context bleed**: Subagent working on `users-controller.ts` doesn't see context from `payments-controller.ts`
- **Focused attention**: Each subagent can use its full context window on its specific subtask
- **Custom agent inheritance**: If a subagent uses a custom agent profile, it inherits that agent's tools, model, and behavioral instructions
- **Result composition**: The orchestrator agent collects results from all subagents and verifies consistency

**Key Takeaway:** Fleet mode's power comes from context isolation + parallel execution. Design your tasks so subtasks are truly independent — shared state between subtasks forces sequential execution and negates fleet mode's benefits.
