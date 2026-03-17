---
status: active
updated: 2026-03-17
section: "Copilot Tools"
references:
  - url: https://docs.github.com/en/copilot/concepts/agents/copilot-cli/about-copilot-cli
    label: "About GitHub Copilot CLI"
    verified: 2026-03-17
  - url: https://docs.github.com/en/copilot/concepts/agents/copilot-cli/fleet
    label: "Running tasks in parallel with /fleet"
    verified: 2026-03-17
  - url: https://docs.github.com/en/copilot/how-tos/use-copilot-agents/use-copilot-cli
    label: "Use Copilot CLI"
    verified: 2026-02-10
  - url: https://docs.github.com/en/copilot/how-tos/set-up/install-copilot-cli
    label: "Install Copilot CLI"
    verified: 2026-02-10
  - url: https://docs.github.com/en/copilot/how-tos/use-copilot-agents/use-copilot-cli#use-custom-instructions
    label: "Copilot CLI custom instructions"
    verified: 2026-02-10
  - url: https://docs.github.com/en/copilot/how-tos/use-copilot-agents/use-copilot-cli#add-an-mcp-server
    label: "Add an MCP server to Copilot CLI"
    verified: 2026-02-10
  - url: https://docs.github.com/en/copilot/how-tos/copilot-cli/customize-copilot/plugins-finding-installing
    label: "Finding and installing plugins for Copilot CLI"
    verified: 2026-02-23
  - url: https://docs.github.com/en/copilot/concepts/agents/copilot-cli/about-cli-plugins
    label: "About plugins for Copilot CLI"
    verified: 2026-02-23
---

# GitHub Copilot CLI: Terminal-Native AI for Developers and DevOps

> **The Question This Talk Answers:**
> *"How do I bring AI into my terminal workflow — whether I'm building something new, debugging my own code, or managing infrastructure?"*

**Duration:** 45 minutes | **Target Audience:** Software Developers / DevOps Engineers / CLI Power Users

---

## 📊 Content Fitness

| Criterion | Assessment | Notes |
|-----------|-----------|-------|
| **Relevant** | 🟢 High | Developers building new software and DevOps engineers managing infrastructure both work primarily in terminals — context-switching to IDE/web for AI assistance breaks flow and forces re-explaining local context |
| **Compelling** | 🟢 High | Plan Mode transforms debugging from 8 attempts to 2; Docker troubleshooting drops from 45 min to 8 min |
| **Actionable** | 🟢 High | Install in 2 minutes, immediately usable for problem-solving, programmatic mode enables CI/CD automation |

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
7. **Mental Model Shift** ← Move-Toward/Away/Against
8. **When to Use Decision Tree** ← "When to Use This Pattern"
9. **Plan Mode & Real-Time Steering** ← 🎬 Section 1 (3-4 slides)
10. **Operating Modes & Delegation** ← 🎬 Section 2 (3-4 slides)
11. **Context Management & Memory** ← 🎬 Section 3 (2-3 slides)
12. **Built-in Specialized Agents** ← 🎬 Section 4 (2-3 slides)
13. **Use Cases** ← Real-World Use Cases (2-3 slides)
14. **Actionable Outcomes** ← What You Can Do Today
15. **Related Patterns** ← Related Patterns
16. **Official Documentation** ← 📚 section
17. **End Slide** ← Auto-generated

### Major Sections (TOC Entries)

```markdown
<!-- 🎬 MAJOR SECTION: Plan Mode & Steering -->
<!-- 🎬 MAJOR SECTION: Operating Modes -->
<!-- 🎬 MAJOR SECTION: Context Management -->
<!-- 🎬 MAJOR SECTION: Built-in Agents -->
<!-- 🎬 MAJOR SECTION: Plugins -->
```

---

## The Problem

### Key Points

- **The IDE only sees code; the terminal sees everything**
  When you're debugging a failure, the information that matters — container logs, environment variables, process state, network traffic, file system layout — isn't in your source files. It's in what's running. An AI that lives in the terminal has access to all of it. One that lives in the editor is context-blind to most of what's actually wrong

- **AI tools target 16% of your day**
  Research from Bicameral AI: developers spend just 16% of their time writing code. The other 84% — deployments, debugging failures, requirements clarification, log analysis, CI triage — all happens in the terminal. Most AI coding tools optimize the 16% and leave the 84% untouched

- **AI guesses when requirements are ambiguous. You pay for that later**
  A human developer hits an edge case in a spec and asks a question. AI hits the same ambiguity and picks one interpretation — confidently. You don't find out the guess was wrong until code review, or production. The right moment to catch this is before the first line of code is written, in a conversation that asks the questions a senior engineer would ask

---

## The Solution: GitHub Copilot CLI

### What It Does

GitHub Copilot CLI brings conversational AI directly into terminal workflows with two operating modes: interactive sessions for collaborative problem-solving and programmatic execution for CI/CD automation. Plan Mode enables collaborative planning before code generation, reducing debugging cycles from 8 attempts to 2.

### Key Capabilities

- **Plan Mode**: Collaborative planning with clarifying questions before implementation — catch misunderstandings early, reduce iteration cycles
- **Configurable Reasoning Models**: Choose GPT-5.2-Codex and tune reasoning effort (low → extra high), with Ctrl+T to reveal reasoning steps
- **Interactive Mode**: Terminal-native conversations with context maintained across commands — perfect for "figure this out" scenarios
- **Programmatic Mode**: Single-command execution for scripts and pipelines — designed for headless CI/CD automation
- **Cloud Delegation**: Background execution frees terminal for other work — delegate large tasks with `&` prefix
- **Built-in Agents**: Specialized agents (Explore, Task, Plan, Code-review) automatically handle common patterns
- **`/fleet` Fan-Out**: Explicitly decompose a plan into parallel subtasks — orchestrator assigns work to subagents, each in their own context window; results are merged back automatically
- **IDE Bridge via `/ide`**: Open any file in VS Code mid-session — CLI context and conversation stay alive; use terminal and IDE simultaneously
- **Automatic Context Management**: Auto-compaction at 95% token limit enables virtually infinite sessions
- **Repository Memory**: AI remembers team conventions, patterns, and preferences across sessions
- **Performance & UX Upgrades**: Faster, more concise responses with improved diff/timeline views and better Windows/PowerShell support
- **MCP Registry Integration**: Discover and connect external tools/agents via GitHub MCP Registry with organization-level controls
- **Plugin Ecosystem**: Install community and team-created plugins from marketplaces — extend CLI functionality with specialized capabilities

### Architecture Overview

Three modes cover distinct workflows: **Interactive** for collaborative problem-solving with persistent context; **Plan Mode** (Shift+Tab) for clarifying requirements before any code is written; **Programmatic** (`copilot -p`) for headless CI/CD execution. Specialized built-in agents (Explore, Task, Plan, Code-review) are routed automatically. Cloud delegation (`&` prefix) offloads long-running work to GitHub's coding agent, freeing both your terminal and IDE. Auto-compaction and repository memory make sessions virtually infinite and cross-session aware.

**Official Documentation:**
- 📖 [About GitHub Copilot CLI](https://docs.github.com/en/copilot/concepts/agents/about-copilot-cli) — Core concepts and capabilities
- 📖 [Using GitHub Copilot CLI](https://docs.github.com/en/copilot/how-tos/use-copilot-agents/use-copilot-cli) — Command syntax, options, and workflows
- 📖 [Installing GitHub Copilot CLI](https://docs.github.com/en/copilot/how-tos/set-up/install-copilot-cli) — Setup instructions for all platforms

---

## 📽️ Visual Assets

*This talk does not include extracted diagrams from source documentation. Visual content will be generated during slide creation using styled HTML components for architecture diagrams and workflow illustrations.*

**Potential visual assets to generate:**
- Interactive vs Programmatic mode comparison diagram
- Plan Mode workflow sequence
- Context management lifecycle (auto-compaction visualization)
- Built-in agent specialization matrix

---

## 📦 Key Artifacts

**Primary Artifacts** — *Shown inline in major sections with detailed explanation*

- **Interactive debugging session** — Terminal conversation demonstrating Plan Mode for Docker debugging
- **Programmatic CI/CD automation** — GitHub Actions workflow using `copilot -p` for build failure analysis
- **Context management commands** — `/compact`, `/context`, `/usage` for monitoring token usage
- **Cloud delegation example** — Using `&` prefix for background codebase analysis
- **Reasoning configuration** — Selecting GPT-5.2-Codex and tuning reasoning effort for depth vs speed

### Supporting Files

*Available in documentation references*

- **[Custom instructions guide](https://docs.github.com/en/copilot/how-tos/use-copilot-agents/use-copilot-cli#use-custom-instructions)** — Repository-specific behavior configuration. Note: all custom instruction files now **combine** (additive merge) instead of falling back to the highest-priority file — user-level + repo-level + org-level instructions are all applied together
- **[MCP server setup](https://docs.github.com/en/copilot/how-tos/use-copilot-agents/use-copilot-cli#add-an-mcp-server)** — Extending functionality with external tools
- **[Configure an MCP registry](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-mcp-usage/configure-mcp-registry)** — Organization-wide discovery and governance for MCP tools
- **[Built-in agents reference](https://docs.github.com/en/copilot/how-tos/use-copilot-agents/use-copilot-cli#use-custom-agents)** — Explore, Task, Plan, Code-review agent details

---

## 🎯 Mental Model Shift

> **The Core Insight:** From "execute commands manually and search docs when stuck" to "collaborate with AI in the terminal — whether building something new from scratch, debugging failing code, or automating infrastructure"

### Move Toward (Embrace These Patterns)

- ✅ **AI as Thought Partner for Greenfield Work**: Use Copilot CLI to explore library choices, scaffold projects, and talk through architecture decisions *before* writing code → 90 min of library research → 15 min with documented rationale and a working scaffold
- ✅ **Plan Before You Build**: Use Plan Mode (Shift+Tab) to clarify intent and approve a strategy before implementation begins → 8 debugging attempts → 2; most rework in development comes from ambiguous starts, not bad code
- ✅ **Delegate, Don't Block**: Long-running tasks (security audits, large refactors, doc generation) don't need to occupy your IDE or terminal — delegate with `& <task>` and get a PR when the agent finishes; both tools stay completely free
- ✅ **Let /fleet Execute the Plan**: Once Plan Mode produces a strategy, hand it off — `/fleet implement all phases of this plan` decomposes the work into parallel subtasks, assigns each to a subagent, and merges results; you review the outcome, not the steps

### Move Away From (Retire These Habits)

- ⚠️ **Starting new projects from the IDE**: Opening VS Code, creating a folder, and guessing at a tech stack before writing anything is the old way. The terminal is where you have the most context — what exists on disk, what's running, what the environment looks like. Use Copilot CLI as a design partner *before* you open the IDE: talk through the architecture, pick the libraries, generate the scaffold. Then open the IDE already oriented
- ⚠️ **Re-explaining your codebase every session**: Spending the first 10 minutes of each Copilot session giving context — "we use docker-compose networking, not host networking; we deploy to Kubernetes; our convention is X" — is a sign repository memory isn't working for you yet. Invest once in teaching Copilot your conventions; subsequent sessions inherit that knowledge automatically
- ⚠️ **Treating every long-running task as IDE-bound**: Kicking off a security audit, large refactor, or test suite generation from VS Code means your editor is occupied until the agent finishes. These tasks are better delegated from the CLI with `& <task>` — the agent runs in the cloud, both your IDE and terminal stay completely free, and a PR arrives when it's done

### Move Against (Active Resistance Required)

- 🛑 **Pasting secrets into prompts**: Credentials, tokens, and API keys typed into CLI sessions travel to GitHub's API as prompt content — the same way any other context does. It feels natural to give Copilot what it needs to help, but this is a data exposure risk. Use environment variables or secret managers; reference the name, not the value
- 🛑 **`--yolo` outside sandboxed environments**: Permission prompts feel like friction when you're in flow. `--allow-all-tools` or `--yolo` removes that friction instantly — and grants the agent permission to run any shell command, edit any file, make any API call with your current credentials. If you're authenticated to production, the agent has production access. Approve per-tool or per-session, never blanket
- 🛑 **Skipping Plan Mode because you're in a hurry**: When the deadline is close and you think you know what you need, Plan Mode feels like overhead. It isn't — it's most valuable precisely when you're rushing. The sessions that spiral into 8 failed attempts almost always started with "I'll just jump in." One minute of clarifying questions saves thirty minutes of rework

> **Developer:** 90 min of library research + second-guessing → 15 min with Plan Mode proposing options, tradeoffs, and scaffolding the chosen stack. ~75 minutes saved.

> **DevOps:** 45 min + 8 trial-and-error attempts debugging a Docker container → 8 min with Plan Mode asking the right questions first. 37 minutes saved, 6 fewer failed attempts.

---

## When to Use This Pattern

### Decision Tree

```
Q: What's your primary workflow environment?
├─ "Terminal/CLI — for development, infrastructure, or both"
│  → Use: Copilot CLI (this talk)
│  └─ Best for: Greenfield development, debugging, exploring libraries, Docker, CI/CD, log analysis
│
├─ "I want to fire off a long-running agentic task without it consuming my IDE"
│  → Use: Copilot CLI (this talk) — cloud delegation via `&` prefix
│  └─ Best for: Security audits, large refactors, test scaffolding, doc generation (20+ min tasks)
│  └─ IDE stays completely free; get notified when the PR is ready
│
├─ "IDE for active code editing, rarely use terminal"
│  → Use: VS Code Copilot or IDE extensions
│  └─ Best for: Inline code completion, editor-integrated assistance, rapid editing
│
├─ "Web for cross-repository analysis & PR review"
│  → Use: github.com/copilot
│  └─ Best for: Multi-repo context, architectural planning, stakeholder collaboration
│
└─ "Need AI across all interfaces"
   → Combine: All three interfaces
   └─ Repository instructions, agents, and memory work identically everywhere
```

### Use This Pattern When

- Building something new (greenfield) and want a thought partner for library choices, architecture, and scaffolding
- Debugging your own failing code, tests, or build environment from the terminal
- DevOps and infrastructure work happens primarily in terminals
- Debugging complex issues where root cause is unknown (Docker, networking, deployments)
- Automating CI/CD build failure analysis and triage
- Need intelligent command execution without leaving terminal flow
- Want to run long-running agentic tasks (security audits, large refactors, test scaffolding) independently of your IDE — delegate from the terminal, IDE stays completely free, PR arrives when done
- Want AI to remember team conventions and patterns over time
- Building automation that adapts to context (not fixed scripts)

### Don't Use This Pattern When

- Never leave the terminal at all for anything — CLI integrates alongside IDE and web, not instead of them
- Need graphical debugging with breakpoints → Use IDE tools
- Need rich cross-repository architectural analysis across many repos → Use Copilot Web
- Workflow is entirely GUI-based with no terminal use → No benefit to CLI-specific features

> 💡 **CLI and IDE work simultaneously, not in competition.** Use the `/ide` slash command from within a Copilot CLI session to open any file directly in VS Code — without losing your terminal context or conversation state. Identify the problem in the terminal, open the file in the IDE for editing, and return to the same CLI session. Both tools stay active and aware.
>
> ```bash
> $ copilot
> > "Debug why fetchUser() returns None intermittently"
> # Copilot identifies the file at fault
> /ide src/users/api.py
> # VS Code opens src/users/api.py — CLI session continues running
> ```

---

<!-- 🎬 MAJOR SECTION: Plan Mode & Steering -->
## Plan Mode: Collaborative Planning Before Implementation

*Transform debugging from trial-and-error to collaborative strategy*

### The Fundamental Shift

**Traditional workflow:**
Request → AI generates solution → You review and fix → Repeat (8 attempts average)

**Plan Mode workflow:**
Request → AI asks clarifying questions → Collaborate on plan → Review plan → Generate implementation (2 attempts average)

### How It Works

Press **Shift+Tab** to toggle Plan Mode on/off. Copilot uses the `ask_user` tool to ask clarifying questions before any code is written:

- **"Should I check docker-compose config, logs, or both?"**
- **"Do you want environment variable analysis included?"**
- **"Start with network configuration or service dependencies?"**

### Real-Time Steering

While Copilot is thinking, you can steer the conversation:

**Enqueue additional messages:**
Send follow-up instructions to adjust direction mid-response:
```bash
# While Copilot analyzes Docker logs:
> "Also check if Redis is running"
> "Focus on authentication-related errors first"
```

**Inline feedback on rejection:**
Reject tool permissions and explain why in one step:
```bash
# Copilot wants to run `rm -rf tmp/*`
> [Press Esc] "Don't delete tmp/ — it has cached artifacts we need"
```
Copilot adapts approach without stopping entirely.

### Example: Docker Debugging with Plan Mode

```bash
$ copilot
> "Debug why the backend container won't start"

🤔 Copilot (Plan Mode):
I can help with that. Before I start, a few questions:

1. Should I check docker-compose configuration, container logs, or both?
2. Do you want environment variable analysis?
3. Any recent changes to services or network configuration?

> "Start with logs, then check config if needed"

🤔 Copilot:
Understood. Here's my plan:
1. Retrieve container logs for backend service
2. Analyze error patterns and stack traces
3. If logs suggest config issue, inspect docker-compose.yml
4. Check environment variables if authentication/connection errors found

Proceed with this plan? (y/n)

> y

✅ Copilot:
[Executes plan, finds misconfigured port binding in docker-compose.yml]
Found: Port 5000 mapped to 5001, but app expects 5000 internally.
Fix: Change service.ports from "5001:5000" to "5000:5000"

Apply this fix? (y/n)
```

**Outcome:** Root cause identified in 8 minutes with 2 targeted checks (vs 45 minutes with 8 trial-and-error attempts manually).

### Advanced Reasoning Models

**GPT-5.2-Codex** optimized for code generation is available with configurable reasoning effort:

- **Low**: Fast responses for straightforward queries
- **Medium**: Balanced speed and depth (default)
- **High**: Extended reasoning for complex problems
- **Extra High**: Maximum depth for critical architectural decisions

**Toggle reasoning visibility:**
Press **Ctrl+T** to show/hide the model's thought process. Setting persists across sessions — useful for understanding how Copilot approaches complex problems and learning optimal prompting patterns.

**When to use High/Extra High reasoning:**
- Architectural refactoring decisions
- Multi-service debugging with unknown root cause
- Critical security or performance investigations

---

<!-- 🎬 MAJOR SECTION: Operating Modes -->
## Interactive Mode vs Programmatic Mode vs Cloud Delegation

*Choose the right mode for the task — collaborative debugging, headless automation, or background execution*

### Two Core Operating Modes

#### Interactive Mode (`copilot`)

**Purpose:** Conversational sessions for iterative problem-solving

```bash
$ copilot
> "Analyze the last 100 lines of application logs"
> "What's causing the memory spike?"
> "List all environment variables related to database connections"
```

**Characteristics:**
- Maintains context across commands and file operations
- Ideal for debugging with unknown root causes
- Perfect for "figure this out collaboratively" scenarios
- Supports Plan Mode, real-time steering, and clarifying questions
- Use `/ide` to open any identified workspace in VS Code mid-session — CLI context is preserved

**Best for:**
- Complex Docker networking issues
- Multi-service failures requiring investigation
- Configuration problems across multiple files
- Learning unfamiliar codebases or architectures

#### Programmatic Mode (`copilot -p`)

**Purpose:** Single-command execution for scripts and CI/CD pipelines

```bash
# In GitHub Actions workflow
- name: Analyze build failure
  if: failure()
  run: |
    copilot -p "Analyze build failure and suggest fixes" \
      --allow-tool 'shell(gh)' \
      --allow-tool 'shell(git)' \
      > analysis.txt
```

**Characteristics:**
- Designed for headless, non-interactive operation
- Produces structured output for script parsing
- Combined with approval options (`--allow-tool`, `--allow-all-tools`)
- No conversation history — stateless execution

**Best for:**
- CI/CD build failure analysis
- Automated test result interpretation
- Deployment validation checks in pipelines
- Scripted operations without human interaction

### Cloud Delegation with `&` Prefix

**Purpose:** Background execution frees terminal for other work

```bash
$ copilot
> "&Analyze entire codebase for security vulnerabilities"

✅ Copilot:
Task delegated to GitHub Copilot coding agent in the cloud.
I'll commit any unstaged changes and create a new branch.

Agent session: https://github.com/owner/repo/agent/session/abc123
Pull request will be created when analysis completes.

[Your terminal is now free for other work]
```

**Characteristics:**
- Runs completely independent of your IDE and local terminal — both stay fully free
- A PR is created automatically when the agent finishes; you get notified
- Best for 20+ minute tasks: security audits, large refactors, doc generation, test scaffolding

### Permission Management

**Session-level approvals:**
"Approve for session" auto-approves pending parallel requests of same type:
```bash
# First file edit request:
> [Approve for session]
# All subsequent file edits in this session: auto-approved
```

**Convenience flags** (use carefully in trusted environments):
```bash
copilot --allow-all-tools  # All permissions enabled
copilot --yolo              # Maximum autonomy (alias for --allow-all)
```

**Inline feedback on rejection:**
```bash
# AI wants to delete a file:
[Esc] "No, don't edit that file — it's auto-generated from schema"
# AI adapts without stopping
```

### Example: CI/CD Build Failure Automation

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
          copilot -p "Analyze the build failure. \
            Check recent commits, dependencies, and error patterns. \
            Suggest specific fixes." \
            --allow-tool 'shell(gh)' \
            --allow-tool 'shell(git)' \
            > failure-analysis.txt

      - name: Post analysis as comment
        if: failure()
        run: |
          gh pr comment ${{ github.event.pull_request.number }} \
            --body-file failure-analysis.txt
```

**Impact:** Investigation time drops from 25 minutes (manual) to 5 minutes (automated). Pattern recognition across historical failures. Zero human intervention for known failure types.

---

<!-- 🎬 MAJOR SECTION: Context Management -->
## Automatic Context Management and Repository Memory

*Virtually infinite sessions with cross-session learning*

### Infinite Sessions via Auto-Compaction

**The problem:** Traditional AI conversations hit token limits and lose context after 12-20 exchanges.

**The solution:** When conversation approaches 95% of token limit, Copilot CLI automatically compresses history in the background:

- **Important context persists:** Decisions made, approaches tried, facts learned
- **Redundant details pruned:** Verbose command outputs, repetitive exchanges
- **No interruptions:** Happens transparently during normal operation
- **Manual control available:** `/compact` command to compress anytime, `Escape` to cancel

**Monitoring tools:**
```bash
/context   # Visual token usage breakdown
/usage     # Session statistics: duration, lines edited, token usage per model
```

### Repository Memory: Cross-Session Learning

Copilot CLI stores learned facts about your codebase — conventions, patterns, preferred approaches — and applies them automatically in future sessions. This is covered in depth in the [Copilot Memory](../copilot-memory/) talk.

### Model Selection and Premium Request Cost

**Default model:** Claude Sonnet 4.5. Change model at any time:

```bash
/model   # Opens model picker showing all available models with their multiplier
```

The multiplier next to each model (`1x`, `2x`, etc.) shows how many premium requests one prompt consumes. Example: `Claude Sonnet 4.5 (1x)` means each prompt costs 1 premium request. Higher-capability models have higher multipliers. Use `/model` before starting a session to select the right cost/quality tradeoff for your task.

### Shell & Output Improvements

- **History filtering:** `!docker [↑]` cycles only through previous docker commands — prefix-aware
- **Clean history:** Shell commands are excluded from Bash/PowerShell history files
- **Tab title:** Current AI intent shows in terminal tab — useful for monitoring multiple sessions
- **Faster output:** Median completion time down ~45%; richer diffs and edit timelines
- **Platform polish:** Improved Windows/PowerShell ergonomics and accessibility shortcuts

---

<!-- 🎬 MAJOR SECTION: Built-in Agents -->
## Built-in Specialized Agents

*Copilot automatically delegates to expert agents based on your request*

### Four Agent Types

Copilot CLI includes built-in agents that handle common patterns automatically — you don't explicitly call them, Copilot routes tasks based on intent.

#### Explore Agent

**Purpose:** Fast codebase analysis without cluttering main context — returns focused answers under 300 words, safe to run in parallel.

```bash
> "How does authentication work in this service?"
```

#### Task Agent

**Purpose:** Execute commands with smart output filtering — brief summary on success, full output only on failure.

```bash
> "Run the test suite and tell me if anything failed"
```

#### Plan Agent

**Purpose:** Analyze dependencies and create multi-step implementation strategies you review before execution.

```bash
> "Plan how to refactor the API to support versioning"
```

#### Code-Review Agent

**Purpose:** High signal-to-noise review — only surfaces bugs, security issues, and logic errors. Never style or formatting.

```bash
/review
```

#### IDE Bridge (`/ide`)

**Purpose:** Open any file in VS Code from an active CLI session — terminal context, conversation, and reasoning all stay alive. Terminal for analysis, IDE for editing, simultaneously.

```bash
/ide src/users/api.py
# VS Code opens the file — CLI session continues uninterrupted
```

### Parallel Agent Execution

Multiple agents can work simultaneously:

```bash
> "Explore how auth works, run the test suite, and plan how to add OAuth"

✅ Explore agent: Analyzes auth implementation
✅ Task agent: Runs tests in parallel
✅ Plan agent: Creates OAuth integration strategy
```

**Result:** Three operations complete in the time of one — agents don't block each other.

### /fleet: Explicit Fan-Out Mode

While Copilot routes multiple agent types automatically from a single prompt, `/fleet` is the **explicit** fan-out command — designed for large, multi-part plans you want Copilot to decompose and execute in parallel with full orchestration.

```bash
# After working through a plan in plan mode:
/fleet implement all phases of this auth refactor plan

# Or directly:
/fleet create a test suite: unit tests for auth, integration tests for API, e2e tests for login flow
```

**How it works:**
1. The main agent analyzes the prompt and identifies subtasks
2. It assesses dependencies — what can run in parallel, what must be sequential
3. It acts as **orchestrator**: assigns subtasks to subagents, manages the workflow
4. Subagents run in parallel where possible, each in their own context window
5. Results are merged back by the orchestrator

**Benefits:**

| Benefit | Detail |
|---------|--------|
| **Speed** | Parallel subtasks complete in the time of the longest, not the sum |
| **Context isolation** | Each subagent has its own window — no context pollution between tasks |
| **Specialization** | Custom agents (`@test-writer`, `@security-reviewer`) are automatically used for matching subtasks |
| **Model selection** | Subagents default to low-cost models; specify per-subtask: `Use Claude Opus 4.5 to analyze...` |

**When to use `/fleet`:**
- Large tasks with multiple independent steps (refactor N files, update N dependencies)
- Tasks well-suited to parallelization: test suite creation, multi-module analysis, documentation
- Autopilot mode — pair with `Shift+Tab` to switch to plan mode, then accept the plan with *Accept plan and build on autopilot + /fleet*

**When NOT to use it:** If tasks are inherently sequential (step B requires step A's output), `/fleet` won't provide speedup — the orchestrator will simply run them in order.

**Cost note:** Each subagent makes independent LLM calls, so `/fleet` may consume more premium requests than a single-agent approach. Use `/model` to check your current model multiplier.

**Workflow with autopilot:**
```
Shift+Tab → plan mode
  └─ Work with Copilot to create an implementation plan
     └─ Plan complete → "Accept plan and build on autopilot + /fleet"
        └─ Copilot runs subtasks in parallel autonomously
           └─ You review finished results
```

See also: [Speeding up task completion with /fleet](https://docs.github.com/en/copilot/how-tos/copilot-cli/speeding-up-task-completion)

### Custom Agents

Beyond built-in agents, create specialized versions for your workflows:

**Locations:**
- **User-level:** `~/.copilot/agents/` (all projects)
- **Repository-level:** `.github/agents/` (current project)
- **Organization-level:** `.github-private/agents/` (all org projects)

**Usage:**
```bash
/agent               # Select from available agents
> "Use refactoring agent to improve this code block"
copilot --agent=refactor-agent  # Command-line option
```

For more information, see [Creating custom agents](https://docs.github.com/en/copilot/how-tos/use-copilot-agents/coding-agent/create-custom-agents).

---

<!-- 🎬 MAJOR SECTION: Plugins -->
## Plugins: Extending Copilot CLI

*Install community and team-created plugins to add specialized capabilities*

### What Plugins Are

Plugins are packages that extend Copilot CLI's functionality beyond its built-in capabilities. They can add new tools, specialized workflows, or domain-specific knowledge. Plugins are installed from marketplaces or directly from Git repositories.

```bash
# Browse and install from a marketplace
copilot plugin marketplace browse awesome-copilot
copilot plugin install database-data-management@awesome-copilot

$ copilot
> "Show me the schema for the users table"
# Plugin provides database introspection capabilities
```

**Outcome:** Extend Copilot CLI with specialized domain capabilities without writing custom agents — leverage the community ecosystem.

For plugin management, creating plugins, or hosting your own marketplace, see [Finding and Installing Plugins](https://docs.github.com/en/copilot/how-tos/copilot-cli/customize-copilot/plugins-finding-installing).

---

## Real-World Use Cases

### Use Case 1: Scaffolding a New Project with AI as Thought Partner

**The Problem:** 90+ minutes of library research and architecture debates before writing a line — often revisited later when the wrong choice surfaces.

**The Solution:** Use Copilot CLI with Plan Mode as an interactive design partner

```bash
$ copilot
> "I need to build a REST API with async support in Python. Walk me through framework and ORM options for my use case."

🤔 Copilot (Plan Mode):
A few questions first:
1. Async throughout, or mixed sync/async endpoints?
2. Will you deploy in containers or serverless?
3. Simple CRUD or complex query patterns?

> "Fully async, containers, complex queries with joins"

🤔 Copilot:
Given your requirements, here's the comparison:

Framework: FastAPI (async-native, auto OpenAPI) vs Litestar (newer, stricter typing)
ORM: SQLAlchemy 2.0 async (mature, complex query support) vs Tortoise-ORM (simpler, less powerful)

Recommendation: FastAPI + SQLAlchemy 2.0 async
Reason: Best ecosystem maturity and complex join support for your use case.

Shall I scaffold the project structure?

> "Yes, with auth middleware and Docker setup"

[Copilot scaffolds folder structure, creates pyproject.toml, Dockerfile, and main.py with async boilerplate]
```

**Outcome:**
- **90 minutes → 15 minutes** for library research and project setup
- **Documented rationale** for every architectural decision
- **Working scaffold** immediately, not just a chosen blank template
- **No second-guessing** — tradeoffs are explicit from the start

---

### Use Case 2: Debugging a Running System

**The Problem:** Service fails in staging, works fine locally. The relevant information — container logs, environment variables, network connectivity, process state — is in the runtime environment, not the source files. VS Code can read your code; it can't interrogate what's actually running.

**The Solution:** Copilot CLI runs commands against the live environment to gather its own context

```bash
$ copilot
> "My auth service is returning 503 in staging but works locally. Debug it."

🤔 Copilot: Let me check the running environment directly.

[runs: docker logs auth-service --tail 50]
[runs: docker exec auth-service env | grep -E 'DB|REDIS|JWT']
[runs: curl -sv http://redis-staging:6379/ping]

Found: JWT_SECRET is set locally but missing from the staging container.
Redis connectivity is fine. The service is failing silently on token validation
and returning 503 instead of 401.

Fix: Add JWT_SECRET to your staging environment secrets and restart the container.
The 503 vs 401 mismatch is a separate issue — I'll flag a bug for that too.
```

**What makes this different from VS Code:** Copilot ran `docker logs`, `env`, and `curl` itself — it gathered the evidence rather than asking you to paste it in. An IDE-based assistant can read your source files; it can't reach into what's running. The terminal is where the runtime lives.

**Outcome:**
- **Evidence gathered automatically** — no copy-pasting logs into chat
- **Cross-system diagnosis** — checks container, env, and network in one session
- **Root cause + side-effect** — finds the missing secret *and* flags the misleading status code

---

### Use Case 3: GitHub.com Integration — Issues, PRs, and Actions

**The Problem:** Context-switching between terminal and browser to manage GitHub tasks (triage issues, review PRs, create workflows) breaks flow and requires re-explaining what you were doing.

**The Solution:** Copilot CLI connects directly to GitHub.com — no browser required

```bash
$ copilot
# Working with issues
> "List all open issues assigned to me in my-org/my-repo"
> "I've been assigned this issue: https://github.com/my-org/my-repo/issues/42. Start working on it in a feature branch."
> "Raise an improvement issue in my-org/my-repo. In src/auth.py the file handle is never closed."

# Working with pull requests
> "List my open PRs"
> "Check the changes made in PR https://github.com/my-org/my-repo/pull/123. Report any serious errors."
> "Merge all the open PRs I've created in my-org/my-repo"

# Creating GitHub Actions workflows
> "Create a GitHub Actions workflow that runs eslint on PRs and fails if errors are found. Push and open a PR."

# Using the GitHub MCP server
> "Use the GitHub MCP server to find good first issues for a new team member in my-org/my-repo"
```

**Key insight:** Copilot CLI can create pull requests on your behalf — you're marked as the author. This means you can describe a change in plain English from your terminal and end up with a PR on GitHub.com, without ever leaving the CLI session.

**Outcome:**
- **Browser context switches eliminated** — GitHub.com tasks stay in terminal flow
- **Issue → branch → PR** completed without switching tools
- **Workflow creation** from natural language description, not YAML from scratch

---

## ✅ What You Can Do Today

**Immediate Actions (15 minutes):**
- [ ] Install Copilot CLI: `gh copilot` (auto-installs on first run) or `npm install -g @github/copilot`
- [ ] Try interactive mode: `copilot` and ask about your current project — "Explain how this module works" or "What library should I use for X?"
- [ ] Test Plan Mode: Press Shift+Tab, then describe a new feature you're about to build
- [ ] Try `/ide <filename>` from within a session — opens the file in VS Code while your CLI conversation stays alive (CLI + IDE simultaneously)

**Developer Short-Term (1 hour):**
- [ ] Use Copilot CLI to scaffold your next new project or module interactively
- [ ] Next time a test fails and you don't immediately know why, reach for `copilot` before print statements
- [ ] Delegate a long-running task with `& <task>` — verify your IDE stays completely free while the agent works in the cloud
- [ ] Create `.github/copilot-instructions.md` with your project conventions so Copilot learns your style
- [ ] Run `/context` and `/usage` to understand session management and auto-compaction

**DevOps Short-Term (1 hour):**
- [ ] Add Copilot CLI to one CI/CD pipeline for build failure analysis — use `copilot -p "Analyze build failure" --allow-tool 'shell(gh)'`
- [ ] Run a long-running agentic task with `& <task>` (security audit, doc generation) — confirm your IDE and terminal stay free while the agent runs in the cloud
- [ ] Try GitHub.com integration: manage issues and open PRs directly from your terminal (see Use Case 3)

**Next:** Review [Copilot CLI Best Practices](https://docs.github.com/en/copilot/how-tos/copilot-cli/cli-best-practices) · Share time-savings wins · Explore [Copilot Hooks](../copilot-hooks/) for governance

---

## Related Patterns

### Complementary Features

- **[Copilot Hooks](../copilot-hooks/)** — Add validation, logging, and security scanning at key execution points in CLI workflows
- **[MCP Apps](../mcp-apps/)** — Extend Copilot CLI with external tools and data sources via Model Context Protocol
- **[Terminal Sandboxing](../terminal-sandboxing/)** — Secure execution environments for untrusted Copilot CLI operations
- **[Context Engineering Foundations](../context-engineering-foundations/)** — Optimize prompt design for better Copilot CLI results

### Decision Flow

**If this talk doesn't fit your needs:**

```
Q: What's your actual goal?
├─ In-editor code assistance → See: VS Code Copilot documentation
├─ Cross-repository architectural analysis → See: Copilot Web (github.com/copilot)
├─ Organization-wide governance → See: Copilot Hooks
└─ Extending with external tools → See: MCP Apps
```

See [DECISION-GUIDE.md](../DECISION-GUIDE.md) for complete navigation help.

---

## 📚 Official Documentation

**Primary Documentation:**
- 📖 **[About GitHub Copilot CLI](https://docs.github.com/en/copilot/concepts/agents/about-copilot-cli)** — Core concepts, capabilities, modes of use
- 📖 **[Using GitHub Copilot CLI](https://docs.github.com/en/copilot/how-tos/use-copilot-agents/use-copilot-cli)** — Command syntax, options, workflows, and slash commands
- 📖 **[Installing GitHub Copilot CLI](https://docs.github.com/en/copilot/how-tos/set-up/install-copilot-cli)** — Setup instructions for npm, Homebrew, WinGet, and install scripts

**Additional Resources:**
- 🎓 [Copilot CLI Best Practices](https://docs.github.com/en/copilot/how-tos/copilot-cli/cli-best-practices) — Optimization patterns and anti-patterns
- 🎓 [Adding Custom Instructions for Copilot CLI](https://docs.github.com/en/copilot/how-tos/copilot-cli/add-custom-instructions) — Repository-specific behavior configuration
- 🔧 [GitHub Copilot CLI Command Reference](https://docs.github.com/en/copilot/reference/cli-command-reference) — Complete slash command and option reference
- 🔧 [Copilot CLI ACP Server](https://docs.github.com/en/copilot/reference/acp-server) — Using Copilot CLI via Agent Client Protocol
- 🔌 [Finding and Installing Plugins](https://docs.github.com/en/copilot/how-tos/copilot-cli/customize-copilot/plugins-finding-installing) — Plugin discovery, installation, and marketplace management
- 🔌 [About Plugins for Copilot CLI](https://docs.github.com/en/copilot/concepts/agents/copilot-cli/about-cli-plugins) — Plugin concepts and capabilities
- 🔌 [Creating a Plugin](https://docs.github.com/en/copilot/how-tos/copilot-cli/customize-copilot/plugins-creating) — Build your own plugins
- 🔌 [Creating a Plugin Marketplace](https://docs.github.com/en/copilot/how-tos/copilot-cli/customize-copilot/plugins-marketplace) — Host your team's or organization's plugins

**GitHub Resources:**
- 📋 [GitHub Blog: Plan Mode Announcement](https://github.blog/changelog/2026-01-21-github-copilot-cli-plan-before-you-build-steer-as-you-go/) — Plan Mode, reasoning models, and latest features
- 📋 [GitHub Blog: Faster, more concise, and prettier](https://github.blog/changelog/2025-10-10-github-copilot-cli-faster-more-concise-and-prettier/) — Performance improvements and output polish
- 🐙 [Copilot CLI Public Repository](https://github.com/github/copilot-cli) — Issue tracking and community discussions
- 📹 [About Agent Skills](https://docs.github.com/en/copilot/concepts/agents/about-agent-skills) — Enhancing Copilot with specialized tasks

---

## 🎭 Behind the Scenes

### Plan Mode Technical Mechanics

Plan Mode uses the `ask_user` tool to pause generation and prompt for clarification — this is a first-class model capability, not a prompt trick. The model predicts ambiguity, asks targeted questions, waits for answers, then commits to an approach. This eliminates the "assume and implement wrong" failure mode that causes 6-8 iteration cycles.



---

**Terminal-native AI for developers building new software and DevOps engineers managing infrastructure**
