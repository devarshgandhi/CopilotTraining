---
status: active
updated: 2026-02-25
section: "Agentic Transformation"
references:
  - url: https://docs.github.com/en/copilot
    label: "GitHub Copilot documentation"
    verified: 2026-02-25
  - url: https://docs.github.com/en/copilot/using-github-copilot/coding-agent
    label: "Copilot Coding Agent docs"
    verified: 2026-02-25
  - url: https://github.blog/ai-and-ml/automate-repository-tasks-with-github-agentic-workflows/
    label: "Automate repository tasks with GitHub Agentic Workflows"
    verified: 2026-02-25
  - url: https://github.github.com/gh-aw/
    label: "GitHub Agentic Workflows documentation"
    verified: 2026-02-25
  - url: https://github.com/githubnext/agentics
    label: "The Agentics — reusable agentic workflow collection"
    verified: 2026-02-25
  - url: https://github.github.com/gh-aw/blog/2026-01-12-welcome-to-pelis-agent-factory/
    label: "Peli's Agent Factory — workflow gallery"
    verified: 2026-02-25
  - url: https://github.github.com/gh-aw/introduction/architecture/
    label: "Agentic Workflows security architecture"
    verified: 2026-02-25
  - url: https://githubnext.com/projects/continuous-ai/
    label: "Continuous AI — GitHub Next project"
    verified: 2026-02-25
  - url: https://github.blog/changelog/2026-01-15-agentic-memory-for-github-copilot-is-in-public-preview/
    label: "Agentic memory for GitHub Copilot — public preview"
    verified: 2026-02-25
  - url: https://github.blog/ai-and-ml/github-copilot/building-an-agentic-memory-system-for-github-copilot/
    label: "Building an agentic memory system for GitHub Copilot"
    verified: 2026-02-25
---

# The Complete Copilot Lifecycle: From Idea to Deployment and Beyond

> **The Question This Talk Answers:**
> *"How does GitHub Copilot participate at every phase of the development lifecycle — not just code completion — and how do Agentic Workflows extend this into continuous, autonomous repository automation?"*

**Duration:** 30 minutes | **Target Audience:** Developers / Engineering Leaders / DevOps

---

## 📊 Content Fitness

| Criterion | Assessment | Notes |
|-----------|-----------|-------|
| **Relevant** | 🟢 High | Most teams still treat Copilot as a code-completion tool — this reveals the full lifecycle picture including pre-coding planning, post-coding automation, and Continuous AI |
| **Compelling** | 🟢 High | Combines the familiar (Copilot Chat, CCA) with the new (Agentic Workflows, Peli's Agent Factory) into one coherent narrative — "Copilot is everywhere" |
| **Actionable** | 🟢 High | Each phase includes concrete tools, commands, and patterns teams can adopt immediately — from Plan Mode to `gh aw` in 15 minutes |

**Overall Status:** 🟢 Ready to use

---

## 📽️ Slide Generation Mapping

### Slide Sequence (Generated Automatically) — Target: 12-15 slides

1. **Title/Logo Slide** ← H1 title + subtitle
2. **Question/Objective Slide** ← "The Question This Talk Answers"
3. **Problem Slide** ← "The Problem" section (condensed)
4. **Solution Overview** ← "The Solution" section (lifecycle diagram)
5. **🧠 The Shift (Preview)** ← Core Insight one-liner
6. **Pre-Coding** ← Combined: Plan Mode, @workspace, MCP, session logs
7. **Coding Workflows** ← Combined: CCA spectrum, session-log iteration
8. **Post-Coding** ← Combined: CCR, PR summaries, repo instructions
9. **Agentic Workflows** ← Combined: gh-aw, Peli's Agent Factory, Continuous AI
10. **Agentic Memory** ← Cross-agent learning, citation verification, measured impact
11. **🧠 Mental Model Shift (Full)** ← Move Toward/Away/Against grid
12. **Actionable Outcomes** ← "What You Can Do Today"
13. **📖 References** ← References section
14. **End Slide** ← Auto-generated

---

## The Problem

### Key Points

- **Copilot is misunderstood as a code-completion tool**
  Most teams adopt Copilot for inline suggestions and stop there — leaving 80% of its capability untouched across planning, review, testing, and automation.

- **The pre-coding phase is still manual**
  Developers spend hours reading codebases, writing plans, and researching approaches before writing a single line — all tasks Copilot can accelerate.

- **Post-coding automation is fragmented**
  PR reviews, quality enforcement, and documentation updates rely on separate tools, manual checklists, or brittle CI scripts that can't reason about code intent.

- **Repository maintenance doesn't scale**
  Issue triage, test coverage gaps, documentation drift, and CI failures accumulate faster than teams can address them — especially in large repos and open-source projects.

### Narrative

Picture a developer starting their Monday morning. They open a new feature issue and spend 45 minutes reading through unfamiliar code to understand the architecture. They draft a plan in a doc, research API patterns, and finally start coding after lunch. By end of day, they have a PR — but the review cycle takes two more days because the reviewer needs to understand the same context the author already built up.

Meanwhile, three CI failures from last week sit uninvestigated. Documentation for the last release is stale. Five issues need triage labels. None of this is anyone's explicit job, so it accumulates.

This is the reality for most engineering teams: Copilot helps with the coding part, but the surrounding lifecycle — understanding, planning, reviewing, maintaining — remains largely manual. The complete picture is bigger. GitHub Copilot now participates at every phase, and GitHub Agentic Workflows extend this into autonomous, continuous repository automation. Teams that see the full picture ship faster with fewer surprises.

---

## The Solution: The Copilot-Powered Development Lifecycle

### What It Does

GitHub Copilot is no longer just an editor companion — it's a lifecycle-spanning AI platform. From pre-coding planning through post-coding automation to continuous repository maintenance, Copilot and its ecosystem of agents provide AI assistance at every phase of software development.

### Key Capabilities

- **Pre-Coding Intelligence**: Codebase analysis, Plan Mode, issue-based workflows, MCP-powered domain planning, and session logs for structured research
- **Agentic Coding**: Context-aware generation, multi-step task execution, automated refactoring, testing, and PR/no-PR flexible workflows via CCA
- **Post-Coding Automation**: PR summaries, Copilot Code Review (CCR), compliance enforcement through repo instructions, and DevOps pipeline integration
- **Continuous AI**: GitHub Agentic Workflows running in Actions — autonomous triage, documentation, testing, and quality workflows defined in Markdown with defense-in-depth security
- **Cross-Agent Memory**: Copilot remembers validated insights across sessions and agents — what coding agent learns about your repo helps code review, CLI, and future coding sessions automatically [^9]

### Architecture Overview

The lifecycle breaks into three developer-facing phases and one autonomous layer:

**Phase 1 — Pre-Coding** leverages Copilot Chat (`@workspace`), CCA Plan Mode, and MCP servers to understand codebases, research requirements, and produce structured plans before any code is written. Session logs bridge planning and coding, creating persistent context.

**Phase 2 — Coding** uses CCA as the primary agentic builder: multi-step task execution, context-aware generation, chat-driven iteration, and MCP integrations for specialized tools. Developers choose between PR-based and PR-decoupled workflows depending on the task.

**Phase 3 — Post-Coding** applies Copilot Code Review for automated quality feedback, generates PR summaries, enforces compliance via `copilot-instructions.md`, and integrates with CI/CD pipelines.

**Layer 4 — Continuous AI** runs GitHub Agentic Workflows autonomously on schedules and events — triage, documentation, testing, security scanning, and reporting — without developer intervention. Peli's Agent Factory demonstrates 100+ such workflows in production.

**Cross-Cutting — Agentic Memory** ties all phases together. Copilot's memory system captures validated insights as agents work — repo conventions, synchronization requirements, coding patterns — and shares them across all Copilot surfaces. What coding agent learns while implementing a feature helps code review catch inconsistencies in future PRs, and helps CLI navigate logs correctly. Memories are repository-scoped, citation-verified in real time, and auto-expire after 28 days to prevent staleness [^9].

**Official Documentation:**
- 📖 [GitHub Copilot Documentation](https://docs.github.com/en/copilot) [^1] — Core concepts and getting started
- 📖 [Copilot Coding Agent](https://docs.github.com/en/copilot/using-github-copilot/coding-agent) [^2] — CCA capabilities and workflows
- 📖 [GitHub Agentic Workflows](https://github.github.com/gh-aw/) [^4] — Continuous AI automation platform

---

## 📦 Key Artifacts

### Primary Artifacts

- **`copilot-instructions.md`** — Repository-level instructions that shape Copilot behavior across all phases (planning, coding, review)
- **`.github/workflows/daily-repo-status.md`** — Example Agentic Workflow: daily status report defined in Markdown
- **`.github/workflows/issue-triage.md`** — Example Agentic Workflow: automated issue triage and labeling
- **`session-log.md`** — Plan Mode output: structured implementation plan with todos for later coding sequences

### Supporting Files

- **[Agentics Repository](https://github.com/githubnext/agentics)** [^5] — 30+ reusable agentic workflow templates
- **[Peli's Agent Factory](https://github.github.com/gh-aw/blog/2026-01-12-welcome-to-pelis-agent-factory/)** [^6] — Gallery of 100+ production workflows
- **[Architecture Guide](https://github.github.com/gh-aw/introduction/architecture/)** [^7] — Security model for Agentic Workflows

---

## 🎯 Mental Model Shift

> **The Core Insight:** From "Copilot helps me write code" to "Copilot participates in every phase of software delivery — and Agentic Workflows keep improving the repository even when I'm not there"

### Move Toward (Embrace These Patterns)

- ✅ **Lifecycle Thinking**: Use Copilot from the first moment you read an issue through to post-merge automation → Compound time savings across every phase, not just coding
- ✅ **Plan Before You Code**: Use CCA Plan Mode and session logs to structure work before implementation → Higher-quality first attempts, fewer revision cycles
- ✅ **Continuous AI**: Deploy Agentic Workflows for triage, docs, tests, and quality alongside CI/CD → Repository health improves autonomously every day
- ✅ **Markdown-Defined Automation**: Write agentic workflows in plain Markdown with natural language intent → Anyone on the team can author, review, and evolve automation

### Move Away From (Retire These Habits)

- ⚠️ **Code-Only Copilot**: Using Copilot exclusively for inline completions → Misses 80% of available AI assistance across planning, review, and automation
- ⚠️ **Manual Triage and Maintenance**: Relying on humans for issue labeling, doc updates, and test coverage → Doesn't scale, accumulates debt, burns out maintainers
- ⚠️ **One-Shot Agent Usage**: Running CCA once and expecting perfect results → Iterative loops with session logs produce dramatically better outcomes

### Move Against (Active Resistance Required)

- 🛑 **Unsandboxed Agent Execution**: Running coding agents with full write access in CI → Security risk; Agentic Workflows enforce read-only default + safe outputs for a reason
- 🛑 **Replacing CI/CD with Agentic Workflows**: Treating AI automation as a substitute for deterministic pipelines → Agentic Workflows augment CI/CD, they don't replace build/test/deploy

> **Example Transformation:** Before: Developer spends Monday morning manually triaging 15 issues, reading stale docs, and investigating a CI failure. After: Agentic Workflows triaged and labeled issues overnight, flagged the CI failure with a proposed fix PR, and updated docs from last week's merged PRs — developer starts coding at 9 AM.

---

## When to Use This Pattern

### Decision Tree

```
Q: What phase of development needs AI assistance?
├─ Understanding code / planning → Use: Pre-Coding tools (Plan Mode, @workspace, MCP)
│  └─ Best for: New features, unfamiliar codebases, complex refactors
│
├─ Writing / testing / refactoring code → Use: Coding tools (CCA, Chat, Copilot Edits)
│  └─ Best for: Implementation, test generation, multi-step tasks
│
├─ Reviewing / shipping code → Use: Post-Coding tools (CCR, PR summaries, repo instructions)
│  └─ Best for: Quality enforcement, compliance, release readiness
│
└─ Continuous repo maintenance → Use: Agentic Workflows (gh-aw)
   └─ Best for: Triage, docs, testing, security scanning at scale
```

### Use This Pattern When

- Your team treats Copilot as "just autocomplete" and wants to expand adoption
- Repository maintenance tasks (triage, docs, tests) are falling behind
- You need a structured narrative to explain Copilot's full value to leadership
- You're evaluating Agentic Workflows and want to understand where they fit

### Don't Use This Pattern When

- You need deep-dive on a single phase — see individual tech talks instead (agentic-sdlc, copilot-code-review, multi-step-tasks)
- You're looking for hands-on workshop exercises — see the workshop/ modules
- Your audience already uses Copilot across the full lifecycle and wants advanced patterns

### Comparison with Related Talks

| Aspect | **This Talk** (Full Lifecycle) | **Agentic Journey** | **Agentic SDLC** |
|--------|-------------------------------|---------------------|-------------------|
| **Best For** | Comprehensive overview of all phases | Incremental issue-to-PR adoption | Infrastructure/CI/CD scaling |
| **Audience** | Developers + Leaders | Developers + DevOps | Architects + Platform Eng |
| **Depth** | Breadth across all phases | Deep on CCA workflow | Deep on infrastructure |
| **Duration** | 30 min | 45 min | 90 min |
| **Agentic Workflows** | Covered as Phase 4 | Not covered | Referenced |

---

<!-- 🎬 MAJOR SECTION: Pre-Coding Intelligence -->
## Pre-Coding Intelligence: From Issue to Implementation Plan

Before writing a single line of code, Copilot helps developers understand, research, plan, and design. This is where the highest-leverage time savings occur — a well-structured plan eliminates wasted coding cycles.

### Codebase Analysis with `@workspace`

Copilot Chat's `@workspace` participant indexes your repository and answers structural questions:

```
@workspace How is authentication implemented in this project?
@workspace What files would I need to modify to add a new API endpoint?
@workspace Show me the data flow from the REST controller to the database layer
```

This replaces the "read code for 2 hours" phase with targeted, contextual answers. For unfamiliar codebases, this alone saves 30-60 minutes per feature.

### CCA Plan Mode

The Copilot Coding Agent's Plan Mode creates structured implementation plans without writing code:

```
@copilot /plan Add rate limiting to the API gateway

# Output:
## Implementation Plan
1. Add rate-limit middleware to src/middleware/
2. Configure Redis-backed token bucket in config/
3. Add rate-limit headers to API responses
4. Update API tests with rate-limit scenarios
5. Add monitoring dashboard metrics
```

Plan Mode produces session logs — persistent artifacts that capture the plan, decisions, and context. These logs can drive later coding sessions, ensuring nothing is lost between planning and implementation.

### Issue-Based and Decoupled Planning

Modern workflows separate planning from coding entirely:

- **Issue-based planning**: Write a detailed issue, assign to CCA, and let it plan implementation steps as sub-issues
- **Decoupled sessions**: Use Plan Mode to generate plans that are stored as session logs — then start a fresh coding session that reads the plan
- **`/plan` command** (Agentic Workflows): The ChatOps-style `/plan` command in issues breaks down work into actionable sub-tasks automatically [^5]

**Key Points:**
- Pre-coding Copilot usage reduces "ramp-up time" by 40-60% on unfamiliar code
- Session logs create persistent context that survives between sessions
- MCP servers add domain-specific context (databases, APIs, design systems) to planning
- Planning agents produce higher-quality first implementations — fewer revision cycles

---

<!-- 🎬 MAJOR SECTION: Coding Workflows -->
## Coding Workflows: Context-Aware Agentic Development

Once the plan exists, Copilot shifts into coding mode — from inline suggestions to full agentic task execution.

### The Coding Spectrum

Copilot offers a graduated spectrum of coding assistance:

| Mode | Control Level | Best For |
|------|--------------|----------|
| **Inline Completions** | Developer-driven, line-by-line | Small edits, boilerplate, known patterns |
| **Copilot Chat** | Conversational, developer-guided | Exploration, debugging, learning |
| **Copilot Edits** | Multi-file, developer-reviewed | Refactoring, feature implementation |
| **CCA (Coding Agent)** | Autonomous, goal-directed | Multi-step tasks, full feature implementation |

### CCA as the Primary Agentic Builder

The Copilot Coding Agent executes multi-step tasks autonomously:

1. **Reads the issue or prompt** — understands the goal and constraints
2. **Analyzes the codebase** — maps dependencies, patterns, and conventions
3. **Plans the approach** — determines which files to create/modify
4. **Implements iteratively** — writes code, runs tests, fixes failures
5. **Opens a PR** (or reports results in no-PR mode) — ready for human review

CCA follows `copilot-instructions.md` for repository-specific conventions, uses `.github/copilot-chat-instructions.md` for behavior tuning, and can invoke MCP servers for specialized tools (databases, APIs, design tokens).

### Session Log-Driven Iteration

For complex features, the most effective pattern is:

```
Session 1: Plan Mode → session-log.md (plan + context)
Session 2: Read session-log → implement Phase 1 → update log
Session 3: Read session-log → implement Phase 2 → update log
Session 4: Final integration + tests
```

Each session picks up exactly where the last one left off. The session log is the single source of truth for what's been done, what's next, and what decisions were made.

### PR and No-PR Workflows

- **PR workflow**: CCA opens a pull request with full implementation — standard for feature branches
- **No-PR workflow**: CCA reports results without creating a PR — useful for exploration, prototyping, and planning-only sessions
- **PR-decoupled workflow** (New in 2026): Plan in one session, code in another, with session logs bridging the gap [^2]

**Key Points:**
- Context-aware generation respects repo conventions via `copilot-instructions.md`
- MCP servers extend CCA with domain-specific tools (Figma, databases, Slack)
- Iterative loops driven by session logs produce 2-3x better outcomes than one-shot prompts
- Testing generation is integrated — CCA writes and runs tests as part of implementation

---

<!-- 🎬 MAJOR SECTION: Post-Coding Automation -->
## Post-Coding Automation: Quality, Review, and Compliance

After code is written, Copilot automates the quality gates that traditionally bottleneck delivery.

### PR Summaries and Copilot Code Review (CCR)

When CCA opens a PR, it automatically generates:
- **PR summary**: Structured description of what changed and why
- **Change walkthrough**: File-by-file explanation of modifications

Copilot Code Review (CCR) then provides automated review feedback:
- Identifies bugs, security issues, and performance concerns
- Suggests improvements with inline code suggestions
- Checks compliance with repository coding guidelines
- Runs in parallel with human reviewers — doesn't replace them, accelerates them

### Secure, Compliant Coding Through Repo Instructions

The `copilot-instructions.md` file enforces organizational standards at every phase:

```markdown
# copilot-instructions.md

## Security Requirements
- All user input must be sanitized before database queries
- Use parameterized queries exclusively — no string concatenation
- Authentication endpoints must include rate limiting

## Code Style
- Follow existing patterns for error handling (Result<T, Error>)
- All public APIs require JSDoc documentation
- Test coverage must exceed 80% for new modules
```

These instructions are respected by Copilot Chat, CCA, and CCR — creating a consistent quality bar across the entire lifecycle.

### DevOps Integration

Copilot integrates with CI/CD pipelines through:
- **GitHub Actions awareness**: CCA understands workflow files and can modify them
- **CI failure context**: Copilot Chat explains CI failures and suggests fixes
- **Pipeline generation**: CCA can create new Actions workflows from natural language descriptions

**Key Points:**
- CCR catches issues before human reviewers see the PR → faster review cycles
- Repo instructions create enforceable standards without manual review checklists
- PR summaries reduce reviewer ramp-up time by 50-70%
- Automated quality gates compound — each one reduces the burden on the next

---

<!-- 🎬 MAJOR SECTION: Agentic Workflows & Continuous AI -->
## Agentic Workflows & Continuous AI: The Autonomous Layer

GitHub Agentic Workflows represent the next frontier: AI-powered repository automation that runs continuously, without human initiation. This is where Copilot's lifecycle participation becomes truly autonomous.

### What Are Agentic Workflows?

Agentic Workflows are **Markdown-defined automation jobs** that run coding agents inside GitHub Actions [^3]:

```markdown
---
on:
  schedule: daily

permissions:
  contents: read
  issues: read
  pull-requests: read

safe-outputs:
  create-issue:
    title-prefix: "[repo status] "
    labels: [report]

tools:
  github:
---

# Daily Repo Status Report

Create a daily status report for maintainers.

Include:
- Recent repository activity (issues, PRs, releases, code changes)
- Progress tracking, goal reminders and highlights
- Actionable next steps for maintainers
```

That's it. The frontmatter defines triggers, permissions, and allowed outputs. The Markdown body is the natural language intent. The `gh aw compile` command generates a lock file (`.lock.yml`) that runs in GitHub Actions [^4].

### Defense-in-Depth Security

Agentic Workflows implement three security layers [^7]:

| Layer | What It Enforces | Trust Boundary |
|-------|-----------------|----------------|
| **Substrate** | Memory, CPU, and network isolation via containers | Hardware, kernel, container runtime |
| **Configuration** | Permissions, tool allowlists, network policies | Declarative YAML specs |
| **Plan** | Safe Outputs — buffered writes with sanitization | Staged execution, output filters |

**Key principle**: Agents run with **read-only permissions by default**. Write operations (creating PRs, issues, comments) go through Safe Outputs — a permission-isolated subsystem that buffers, validates, and sanitizes all external writes before execution.

### Peli's Agent Factory: 100+ Workflows in Production

Peli's Agent Factory is GitHub Next's exploration of "what happens when you max out on agentic workflows" [^6]. Over 100 specialized workflows have been built and operated, organized into categories:

| Category | Example Workflows | Output Type |
|----------|------------------|-------------|
| **Triage** | Issue triage, PR labeling | Comments, labels |
| **Documentation** | Daily doc updater, glossary maintainer, link checker | Pull requests |
| **Code Quality** | Code simplifier, duplicate detector, file diet | Pull requests |
| **Testing** | Daily test improver, performance improver | Pull requests |
| **Security** | Malicious code scanner, AI moderator | Issues, reports |
| **Reporting** | Daily/weekly status, research updates, team summaries | Issues |
| **Interactive** | `/plan` command, `/fix` command, repo-ask | Comments, PRs |

The [Agentics repository](https://github.com/githubnext/agentics) [^5] provides 30+ reusable, production-ready workflow templates that any team can install with `gh aw add`.

### Continuous AI: The New Layer of Automation

Continuous AI is the concept of making AI-enriched automation as routine as CI/CD [^8]:

| Traditional CI/CD | Continuous AI |
|-------------------|---------------|
| Build, test, deploy | Triage, document, improve, report |
| Deterministic scripts | Natural language intent |
| Triggered by code push | Triggered by schedule, events, commands |
| Pass/fail binary | Nuanced analysis and recommendations |

**Continuous AI doesn't replace CI/CD** — it augments it with capabilities that deterministic workflows can't express: understanding code intent, reasoning about quality, and generating human-readable analysis.

### Design Patterns for Agentic Workflows

Teams can adopt established patterns [^4]:

- **DailyOps**: Scheduled daily workflows (triage, reports, quality scans)
- **ChatOps**: Command-triggered workflows (`/plan`, `/fix`, `/ask`)
- **IssueOps**: Event-driven workflows (on issue creation, label changes)
- **ProjectOps**: Cross-issue coordination and planning
- **MultiRepoOps**: Organization-wide automation across repositories
- **Orchestration**: Multi-phase workflows with staged execution

**Key Points:**
- Start with read-only workflows (reports, analysis) before enabling PR creation
- Each workflow run typically costs 2 premium requests (work + guardrail check)
- Pull requests from Agentic Workflows are **never merged automatically** — humans always review
- Treat workflow Markdown as code: review changes, keep it small, evolve intentionally

---

<!-- 🎬 MAJOR SECTION: New in 2026 -->
## New in 2026: The Expanding Frontier

2026 brings significant expansions to the Copilot lifecycle platform.

### Copilot SDK Preview

The Copilot SDK enables developers to build custom AI-powered tools and integrations that leverage Copilot's infrastructure — extending the platform beyond GitHub's built-in features.

### Agentic Memory (Cross-Agent Learning)

Copilot memory enables agents to learn and retain repository-specific insights that improve quality over time [^9] [^10]:

- **How it works**: Agents capture tightly scoped "memories" — facts with citations to specific code locations — as they work. Before using a memory, agents verify citations in real time against the current branch.
- **Cross-agent sharing**: What coding agent learns (e.g., "API version must match across client SDK, server routes, and docs") is automatically available to code review and CLI — transferring knowledge between agents and team members.
- **Self-healing**: If code changes invalidate a memory, agents detect the contradiction during verification and store a corrected version. Memories auto-expire after 28 days.
- **Measured impact**: 7% increase in PR merge rates for coding agent (90% vs 83%), 2% increase in positive feedback for code review (77% vs 75%) — both statistically significant (p < 0.00001).

```
Example memory stored by code review:
{
  subject: "API version synchronization",
  fact: "API version must match between client SDK, server routes, and docs.",
  citations: ["src/client/sdk/constants.ts:12", "server/routes/api.go:8", "docs/api-reference.md:37"],
  reason: "Prevents versioning mismatch that could break integrations."
}
→ Next time coding agent updates any of these files, it updates all three automatically.
```

Enable memory in [personal Copilot settings](https://github.com/settings/copilot) or via organization/enterprise policy. Repository owners can review stored memories in **Settings > Copilot > Memory**.

### PR-Decoupled Workflows

Planning and coding are no longer forced into a single PR-oriented session. Developers can:
- Run Plan Mode sessions that produce plans without any code changes
- Store session logs as reusable artifacts
- Start coding sessions that consume plans from previous sessions
- Iterate across multiple sessions with persistent context

### Agent MD Instructions

The `.github/agents/*.agent.md` pattern allows teams to define specialized agent behaviors:
- Custom agent personas with specific expertise
- Tool configurations and MCP server bindings
- Guardrails and output constraints per agent type
- Composable agent definitions that reference shared instructions

### MCP-Native Workload Support

Model Context Protocol (MCP) servers are now first-class citizens:
- Domain-specific tools available during planning, coding, and review
- Custom MCP servers for enterprise data sources (design systems, internal APIs, databases)
- Agentic Workflows can configure MCP servers directly in workflow frontmatter
- Tool allowlisting ensures agents only access approved MCP servers

---

## Real-World Use Cases

### Use Case 1: Morning Calm — The Fully Automated Repository

**The Problem:** An open-source project with 1,000+ issues receives 20 new issues daily. Maintainers spend 2 hours each morning on triage, label assignment, and duplicate detection before doing any real work.

**The Solution:** Deploy three Agentic Workflows: issue triage (labels + priority), duplicate detection (links related issues), and daily status report (summarizes overnight activity).

**Implementation:**
```bash
gh extension install github/gh-aw
gh aw add githubnext/agentics issue-triage
gh aw add githubnext/agentics daily-repo-status
gh aw compile && git push
```

**Outcome:** Maintainer triage time drops from 2 hours → 15 minutes (reviewing agent decisions). Issues are labeled within minutes of creation. Daily report provides a prioritized starting point.

---

### Use Case 2: Feature Development with Session Logs

**The Problem:** A developer is assigned a complex feature spanning 8 files across 3 services. They spend a full day understanding the codebase before writing any code, and lose context between sessions.

**The Solution:** Use the pre-coding → coding lifecycle with session logs:

**Implementation:**
```
Day 1 Morning: @workspace analysis + CCA Plan Mode → session-log.md
Day 1 Afternoon: Read session-log → implement service A → update log
Day 2 Morning: Read session-log → implement service B → update log
Day 2 Afternoon: Integration tests + PR with auto-generated summary
```

**Outcome:** Codebase understanding time drops from 8 hours → 2 hours. Implementation spans 2 days instead of 4. PR includes auto-generated summary and passes CCR on first review.

---

### Use Case 3: Continuous Code Quality at Scale

**The Problem:** A 500K-line enterprise codebase accumulates tech debt faster than the team can address it. Code review catches style issues but misses deeper quality problems.

**The Solution:** Combine post-coding (CCR on every PR) with Continuous AI (weekly code simplifier, daily test improver, duplicate detector).

**Implementation:**
```markdown
# .github/workflows/weekly-code-quality.md
---
on:
  schedule: weekly
safe-outputs:
  create-pull-request:
    title-prefix: "[quality] "
    labels: [tech-debt, automated]
    max: 3
---

# Weekly Code Quality Improvement

Analyze the codebase for the top 3 most impactful simplification 
opportunities. For each, create a focused pull request with:
- Clear description of what was simplified and why
- Before/after complexity metrics
- Confirmation that all existing tests pass
```

**Outcome:** 3 quality PRs generated weekly. Tech debt reduction becomes continuous rather than sprint-based. CCR validates each quality PR before human review.

---

## ✅ What You Can Do Today

**Immediate Actions (15 minutes):**
- [ ] Try `@workspace` to analyze an unfamiliar area of your codebase
- [ ] Use CCA Plan Mode on your next feature: `@copilot /plan <description>`
- [ ] Enable Copilot Code Review on your repository's PR settings

**Short-Term Implementation (1 hour):**
- [ ] Create a `copilot-instructions.md` with your team's coding standards
- [ ] Install `gh aw` and add a daily-repo-status workflow: `gh aw add githubnext/agentics daily-repo-status`
- [ ] Try session-log-driven development on a multi-day feature

**Advanced Exploration (2-4 hours):**
- [ ] Deploy 3-5 Agentic Workflows from [the Agentics collection](https://github.com/githubnext/agentics)
- [ ] Create a custom Agentic Workflow tailored to your team's specific needs
- [ ] Build an Agent MD definition for a specialized team workflow

**Next Steps After Completion:**
1. ✅ Complete the immediate actions above
2. 📖 Review related talk: [Agentic Journey](../agentic-journey/) for incremental CCA adoption
3. 📖 Review related talk: [Agentic SDLC](../agentic-sdlc/) for infrastructure-level scaling
4. 🚀 Explore [Peli's Agent Factory](https://github.github.com/gh-aw/blog/2026-01-12-welcome-to-pelis-agent-factory/) for workflow inspiration

---

## Related Patterns

### Complementary Features

- **[Agentic Journey](../agentic-journey/)** — When you want a deeper dive into incremental CCA adoption from issue to PR
- **[Agentic SDLC](../agentic-sdlc/)** — When you need to rewire CI/CD infrastructure to scale agentic development
- **[Copilot Code Review](../copilot-code-review/)** — When you want deep-dive on CCR capabilities and configuration
- **[Multi-Step Tasks](../multi-step-tasks/)** — When you need advanced patterns for complex CCA task execution
- **[MCP Apps](../mcp-apps/)** — When you want to build or integrate MCP servers for domain-specific tools

### Decision Flow

**If this talk doesn't fit your needs:**

```
Q: What's your actual goal?
├─ Deep-dive on CCA workflows → See: Agentic Journey
├─ Scale infrastructure for agents → See: Agentic SDLC
├─ Automate code review specifically → See: Copilot Code Review
├─ Build MCP integrations → See: MCP Apps
└─ Hands-on exercises for team training → See: workshop/ modules
```

See [DECISION-GUIDE.md](../DECISION-GUIDE.md) for complete navigation help.

---

## 📖 References

### Official Documentation

[^1]: **[GitHub Copilot Documentation](https://docs.github.com/en/copilot)** — Core concepts, setup, and getting started with all Copilot features
[^2]: **[Copilot Coding Agent](https://docs.github.com/en/copilot/using-github-copilot/coding-agent)** — CCA capabilities, Plan Mode, session logs, and PR workflows

### Blog Posts & Announcements

[^3]: **[Automate repository tasks with GitHub Agentic Workflows](https://github.blog/ai-and-ml/automate-repository-tasks-with-github-agentic-workflows/)** — Launch blog post explaining Agentic Workflows (Feb 2026)

### Platform Documentation

[^4]: **[GitHub Agentic Workflows Documentation](https://github.github.com/gh-aw/)** — Full reference for creating, configuring, and deploying agentic workflows
[^5]: **[The Agentics](https://github.com/githubnext/agentics)** — Reusable collection of 30+ production-ready agentic workflow templates
[^6]: **[Peli's Agent Factory](https://github.github.com/gh-aw/blog/2026-01-12-welcome-to-pelis-agent-factory/)** — Gallery of 100+ specialized workflows with design patterns and lessons learned

### Architecture & Security

[^7]: **[Agentic Workflows Security Architecture](https://github.github.com/gh-aw/introduction/architecture/)** — Defense-in-depth model: substrate, configuration, and plan-level trust layers

### Concepts

[^8]: **[Continuous AI — GitHub Next](https://githubnext.com/projects/continuous-ai/)** — The vision for AI-enriched automation as routine as CI/CD

### Agentic Memory

[^9]: **[Agentic memory for GitHub Copilot (Public Preview)](https://github.blog/changelog/2026-01-15-agentic-memory-for-github-copilot-is-in-public-preview/)** — Changelog announcement with setup instructions
[^10]: **[Building an agentic memory system for GitHub Copilot](https://github.blog/ai-and-ml/github-copilot/building-an-agentic-memory-system-for-github-copilot/)** — Engineering deep-dive: citation verification, cross-agent sharing, measured impact

---

## 🎭 Behind the Scenes

### How Agentic Workflows Execute

Understanding the execution model helps you design effective workflows:

1. **Compilation**: `gh aw compile` converts your Markdown workflow into a `.lock.yml` GitHub Actions workflow file. The lock file pins action versions and encodes the security configuration.

2. **Trigger**: GitHub Actions fires the workflow on schedule, event, or manual dispatch. The runner VM provides substrate-level isolation.

3. **Agent Execution**: A coding agent (Copilot CLI, Claude Code, or OpenAI Codex) runs inside a containerized environment with read-only permissions. The Agent Workflow Firewall controls network egress via domain allowlisting.

4. **Safe Output Processing**: The agent produces structured output (JSON artifacts). A separate, privileged job validates the output — checking for secret leaks, malicious patches, and policy violations — before executing allowed write operations (PRs, issues, comments).

5. **Human Review**: All write operations are visible, inspectable, and require human approval for merging. The agent cannot merge its own PRs.

**Why This Matters:** This architecture means you can run agents autonomously with confidence — the security model ensures that even a compromised agent cannot directly modify repository state.

### The Cost Model

Each Agentic Workflow run typically incurs:
- **2 premium requests**: One for the agent work, one for the guardrail/safe-output check
- **Configurable models**: Choose cost-appropriate models per workflow (e.g., lighter models for triage, stronger models for code changes)
- **Token usage scales with repo size**: Larger repos = more context = higher per-run cost

**Key Takeaway:** Start with lightweight, read-only workflows (reports, triage) to understand cost patterns before deploying code-modifying workflows.
