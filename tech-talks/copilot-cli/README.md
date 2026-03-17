---
status: active
updated: 2026-02-23
section: "Copilot Tools"
references:
  - url: https://docs.github.com/en/copilot/concepts/agents/about-copilot-cli
    label: "About GitHub Copilot CLI"
    verified: 2026-02-10
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

- **Greenfield development is decision-dense**
  Building something new means constant choices: which library, what architecture, how to handle edge cases — without institutional knowledge or a colleague to ask. Every decision competes for your attention while you're trying to maintain momentum

- **Terminal is the developer's workhorse, but it's silent**
  Developers scaffold projects, run tests, debug failures, and explore new libraries all from the terminal — but must context-switch to a browser or IDE to get AI help, forcing them to re-explain local context they already have at their fingertips

- **Manual investigation overhead**
  Debugging failures — whether a test suite, a Docker container, or a deployment — takes 45+ minutes of manual work: parsing stack traces, checking configuration files, verifying environment variables, searching documentation

- **Automation without understanding**
  Traditional CLI tools execute predefined commands without adapting to context or learning from failures

- **Long-running agent tasks consume your IDE**
  Firing off a 20-minute background task (security audit, large refactor, test scaffolding) from VS Code ties up your editor and its resources. The CLI runs agentic workloads completely independently — delegate from the terminal, close the session if you want, and get notified when the PR is ready

- **Context switching breaks flow**
  Moving between terminal and IDE/web for AI assistance costs 5-10 minutes per switch, disrupts concentration, and forces re-explaining what's already present in the terminal

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

- **[Custom instructions guide](https://docs.github.com/en/copilot/how-tos/use-copilot-agents/use-copilot-cli#use-custom-instructions)** — Repository-specific behavior configuration
- **[MCP server setup](https://docs.github.com/en/copilot/how-tos/use-copilot-agents/use-copilot-cli#add-an-mcp-server)** — Extending functionality with external tools
- **[Configure an MCP registry](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-mcp-usage/configure-mcp-registry)** — Organization-wide discovery and governance for MCP tools
- **[Built-in agents reference](https://docs.github.com/en/copilot/how-tos/use-copilot-agents/use-copilot-cli#use-custom-agents)** — Explore, Task, Plan, Code-review agent details

---

## 🎯 Mental Model Shift

> **The Core Insight:** From "execute commands manually and search docs when stuck" to "collaborate with AI in the terminal — whether building something new from scratch, debugging failing code, or automating infrastructure"

### Move Toward (Embrace These Patterns)

- ✅ **AI as Thought Partner for Greenfield Work**: Use interactive mode to explore library choices, scaffold new projects, and talk through architecture decisions before writing code → Reduces the "pick wrong library" tax and the decision paralysis that stalls new projects
- ✅ **Collaborative Planning Before Coding**: Use Plan Mode to ask clarifying questions and approve strategy before implementation → Reduces debugging cycles from 8 attempts to 2
- ✅ **Terminal as Collaboration Space**: Keep development and infrastructure work in the terminal with conversational AI → Eliminates context-switching overhead (5-10 min per switch) and avoids re-explaining local context
- ✅ **Programmatic AI for Automation**: Use `copilot -p` in CI/CD pipelines for intelligent build failure analysis → 25 min → 5 min investigation time
- ✅ **Cloud Delegation for IDE-Independent Execution**: Prefix prompts with `&` to run long-running agentic tasks (security audits, large refactors, test scaffolding) entirely in the cloud → IDE stays completely free, terminal stays free, PR arrives when the agent finishes
- ✅ **Repository Memory Accumulation**: Let AI learn and remember team conventions across sessions → Future interactions leverage institutional knowledge automatically

### Move Away From (Retire These Habits)

- ⚠️ **Building Without Talking Through Decisions First**: On greenfield work, jumping straight to implementation without exploring options → Use Copilot CLI as a thought partner before committing to an approach; the cost of exploring in conversation is minutes, the cost of redoing a bad library choice is hours
- ⚠️ **Immediate Code Generation**: Jumping straight to implementation without clarifying requirements → Leads to 6-8 iteration cycles when 2 would suffice with planning
- ⚠️ **Context-Switching to IDE for AI Help**: Leaving terminal to use IDE Copilot for terminal questions → Breaks flow, requires re-explaining context (5-10 min cost per switch)
- ⚠️ **Manual Log Parsing and Documentation Search**: Reading stack traces and searching docs manually for 45+ minutes → Automated analysis with Copilot CLI completes in 8 minutes
- ⚠️ **Fixed Automation Scripts**: Writing brittle shell scripts that can't adapt to context → Programmatic Copilot CLI understands failures and suggests fixes dynamically

### Move Against (Active Resistance Required)

- 🛑 **Using Interactive Mode in CI/CD**: Running interactive `copilot` sessions in automated pipelines → Use programmatic mode (`copilot -p`) designed for headless operation
- 🛑 **Over-Approving Permissions in Production**: Using `--yolo` flag in production environments without understanding scope → Maintain security boundaries; use targeted `--allow-tool` for specific commands only
- 🛑 **Ignoring Repository Memory**: Starting every session from scratch without leveraging learned conventions → Wastes time re-explaining patterns that AI could remember across sessions

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

### Comparison with Related Features

| Aspect | Copilot CLI | VS Code Copilot | Copilot Web |
|--------|-------------|-----------------|-------------|
| **Best For** | Terminal workflows: greenfield dev, debugging, infrastructure | Code editing, inline suggestions | Cross-repo analysis, PR review |
| **Strengths** | Plan Mode, programmatic automation, terminal-native, no re-explaining local context, IDE-independent long-running agent execution | Inline completions, edits in editor context | Multi-repo queries, architectural context |
| **Limitations** | Requires terminal comfort; no built-in graphical UI (use `/ide` to bridge to VS Code mid-session) | IDE-bound, not for terminal or infrastructure | No local file operations |
| **Setup Time** | 2 minutes (install + auth) | Built into VS Code | Zero (web browser) |

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

Copilot CLI stores learned facts about your codebase — conventions, patterns, preferred approaches — and applies them automatically in future sessions. New team members inherit institutional knowledge without re-explanation.

**Example:**
```bash
Session 1 (Monday):
> "Debug Docker networking issue"
[You explain services use docker-compose networking, not host networking]

Session 2 (Wednesday):
> "Service A can't reach Service B"
✅ Copilot: "Checking docker-compose networking configuration..."
[AI applies Monday's context without re-explaining]
```

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

### Finding Plugins via Marketplaces

Copilot CLI comes with two default marketplaces pre-registered:
- **`copilot-plugins`** — GitHub's official plugin collection
- **`awesome-copilot`** — Community-curated plugins

**Browse available marketplaces:**
```bash
# List registered marketplaces
copilot plugin marketplace list

# Or in an interactive session
/plugin marketplace list
```

**Browse plugins in a marketplace:**
```bash
# Browse a specific marketplace
copilot plugin marketplace browse awesome-copilot
```

### Installing Plugins

**From a registered marketplace:**
```bash
# Install from marketplace
copilot plugin install database-data-management@awesome-copilot

# Or in an interactive session
/plugin install database-data-management@awesome-copilot
```

**Directly from a GitHub repository:**
```bash
# From GitHub
copilot plugin install OWNER/REPO

# From any Git repository
copilot plugin install https://gitlab.com/OWNER/REPO.git
```

**From a subdirectory in a repository** (e.g., marketplace repos with multiple plugins):
```bash
copilot plugin install anthropics/claude-code:plugins/frontend-design
```

**From a local path:**
```bash
copilot plugin install ./path/to/my-plugin
```

> **Note:** For direct repository installs to work, the repository must contain a `plugin.json` file in `.github/plugin/`, `.claude-plugin/`, or the repository root.

### Managing Installed Plugins

```bash
copilot plugin list                    # View installed plugins
copilot plugin update PLUGIN-NAME      # Update plugin to latest version
copilot plugin uninstall PLUGIN-NAME   # Remove plugin completely
```

### Where Plugins Are Stored

Plugins are stored locally under `~/.copilot/installed-plugins/`:

```
~/.copilot/installed-plugins/
├── awesome-copilot/              # Plugins from marketplace
│   └── database-data-management/
├── copilot-plugins/
│   └── another-plugin/
└── _direct/                      # Plugins installed directly
    └── my-local-plugin/
```

### Adding and Removing Plugin Marketplaces

**Add a marketplace:**
```bash
# Add from GitHub repository
copilot plugin marketplace add anthropics/claude-code

# Add from any Git URL
copilot plugin marketplace add https://gitlab.com/OWNER/REPO.git

# Add from local path
copilot plugin marketplace add /path/to/marketplace-directory
```

**Remove a marketplace:**
```bash
# Remove by marketplace name (not OWNER/REPO)
copilot plugin marketplace remove MARKETPLACE-NAME

# Force remove (also uninstalls all plugins from that marketplace)
copilot plugin marketplace remove MARKETPLACE-NAME --force
```

### Example: Adding a Database Plugin

```bash
$ copilot plugin marketplace browse awesome-copilot
# Browse available plugins...

$ copilot plugin install database-data-management@awesome-copilot
Installing database-data-management from awesome-copilot...
✅ Plugin installed successfully.

$ copilot
> "Show me the schema for the users table"
# Plugin provides database introspection capabilities
```

**Outcome:** Extend Copilot CLI with specialized domain capabilities without writing custom agents — leverage the community ecosystem.

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

### Use Case 2: Debugging Your Own Failing Code

**The Problem:** Test passes locally, fails in CI. Something returns `None` when it shouldn't. 30+ minutes of print statements and grep before finding the cause.

**The Solution:** Use interactive Copilot CLI with full codebase context

```bash
$ copilot
> "My async fetch_user() returns None intermittently in CI but never locally. Help me debug."

🤔 Copilot:
I see a few possible causes for intermittent None in async code. Let me check:
1. Are there exception handlers that silently return None on failure?
2. Does the CI environment have different timeout or environment variable values?
3. Is the async context properly awaited at every call site?

> "Check exception handlers first"

[Copilot reads the relevant file, finds a bare except that swallows the ConnectionError and returns None]

Found: Line 47 — bare `except:` block returns None silently when a ConnectionError occurs.
In CI, the database connection times out because CI_DB_HOST isn't set.

Fix: Add specific exception handling and log the error. Add CI_DB_HOST to your workflow secrets.
```

**Outcome:**
- **30 minutes → 5 minutes** to root cause (test vs CI environment difference instantly surfaced)
- **Context-aware analysis** — Copilot reads your actual code, not a description of it
- **No re-explaining** — the codebase is already in context from the terminal
- **Fix + prevention** — solution addresses the symptom and the underlying config gap

---

### Use Case 3: Docker Debugging with Plan Mode

**The Problem:** 45 minutes manually checking logs, config, and env vars. 8 trial-and-error attempts before finding the cause.

**The Solution:** Use Copilot CLI with Plan Mode for collaborative investigation

```bash
$ copilot
> "Debug why the backend container won't start"

# Copilot asks clarifying questions:
# "Should I check docker-compose config, logs, or both?"
# "Do you want environment variable analysis?"

> "Start with logs, then check config if needed"

# Copilot creates plan, executes after approval
# Identifies misconfigured port binding in docker-compose.yml
```

**Outcome:**
- **45 minutes → 8 minutes** debug time (83% reduction)
- **8 attempts → 2 attempts** (AI asks right questions first)
- **Automated log analysis** with reasoning transparency
- **Documented workflow** reusable by entire team

---

### Use Case 4: CI/CD Build Failure Analysis

**The Problem:** 25 minutes per build failure — log analysis, commit archaeology, dependency checks — repeated manually every time with no pattern recognition.

**The Solution:** Programmatic Copilot CLI in GitHub Actions workflow

```yaml
# .github/workflows/build.yml
- name: Analyze build failure
  if: failure()
  run: |
    copilot -p "Analyze build failure and suggest fixes" \
      --allow-tools \
      --model gpt-5.2-codex > analysis.txt
    gh pr comment --body-file analysis.txt
```

**Outcome:**
- **25 minutes → 5 minutes** investigation time
- **12 manual steps → 3 automated steps**
- **Pattern recognition enabled** across historical failures
- **Zero human intervention** for known failure types

---

### Use Case 5: Infrastructure Documentation Generation

**The Problem:** Docs lag deployments by 3 days. Manual diagram creation from docker-compose.yml is tedious enough that it simply doesn't get done.

**The Solution:** Generate directly from infrastructure-as-code

```bash
# Generate docs from docker-compose.yml
$ copilot "Generate architecture documentation from docker-compose.yml"

# Create system diagrams
$ copilot "Create deployment diagram showing service dependencies"

# Update docs when config changes
$ copilot "Update architecture.md to reflect new Redis cache service"
```

**Outcome:**
- **3 days → 30 minutes** documentation time
- **Automated diagram generation** from infrastructure code
- **Real-time architecture updates** when configs change
- **Always-current docs** for stakeholder presentations

---

### Use Case 6: Cross-Session Learning with Repository Memory

**The Problem:** Senior engineer re-explains the same deployment conventions 5-6 times over 2 weeks to each new team member.

**The Solution:** Repository memory accumulates institutional knowledge

```bash
# Week 1: Senior explains conventions to Copilot during work
$ copilot
> "Deploy to staging"
# Copilot learns: staging uses blue-green deployment, requires approval, runs smoke tests

# Week 2: New team member uses same commands
$ copilot
> "Deploy to staging"
✅ Copilot: "Running blue-green deployment to staging..."
[Automatically follows learned conventions without re-explaining]
```

**Outcome:**
- **2 weeks → 3 days** onboarding for infrastructure work
- **5-6 explanations → 1 explanation** (AI remembers for team)
- **Consistent practices** across all team members
- **Institutional knowledge** persists beyond individual engineers

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
- [ ] Add Copilot CLI to one CI/CD pipeline for build failure analysis (see Use Case 4)
- [ ] Run a long-running agentic task with `& <task>` (security audit, doc generation) — confirm your IDE and terminal stay free while the agent runs in the cloud
- [ ] Test interactive Docker debugging instead of manual log parsing next time a container fails

**Advanced Exploration (2-4 hours):**
- [ ] Create custom agents in `.github/agents/` for specialized workflows
- [ ] Configure automatic build failure analysis in all CI/CD workflows
- [ ] Set up MCP servers via the GitHub MCP Registry (`/mcp add`)
- [ ] Browse and install plugins: `copilot plugin marketplace browse awesome-copilot`
- [ ] Measure ROI: Track before/after metrics for debugging time and iteration cycles

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

### Programmatic Mode Architecture

Programmatic mode (`copilot -p`) is **fundamentally different** from interactive mode:

- **Stateless execution:** No conversation history, each invocation is independent
- **Structured output:** Designed for parsing by scripts (not human reading)
- **Permission model:** Requires explicit `--allow-tool` or `--allow-all-tools` flags
- **Exit codes:** Success (0) or failure (non-zero) for automation workflows

```bash
# Interactive mode: maintains context
$ copilot
> "What's in logs?"
> "Check config too"
> "Now analyze both"

# Programmatic mode: one-shot execution
$ copilot -p "Analyze logs and config, suggest fixes" --allow-tools
```

**Key Takeaway:** Don't use interactive mode in CI/CD (builds break when it prompts for input). Don't use programmatic mode for iterative debugging (loses context each time).

### Context Auto-Compaction Algorithm

At 95% token limit: compressible segments (verbose outputs, repetitive exchanges) are identified and replaced with a dense summary; key decisions and facts are preserved. Sessions can run indefinitely (tested: 200+ exchanges) with no user interruption.

### Repository Memory Storage

Memories are stored in `.copilot/memory/` directory (local to repository):

```
.copilot/
└── memory/
    ├── conventions.json      # Coding standards
    ├── architecture.json     # System patterns
    └── workflows.json        # Common procedures
```

**Privacy model:** Memories never leave your local machine except when explicitly referenced in prompts (then sent to GitHub API like any other context). You can review/edit memory files anytime. Delete `.copilot/memory/` to reset learned knowledge.

---

**Terminal-native AI for developers building new software and DevOps engineers managing infrastructure**
