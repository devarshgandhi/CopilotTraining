# Agentic Workflows — Content Plan

**Status:** Phase 2 — Planning Complete
**Date:** 2026-03-05
**Template:** `tech-talks/TEMPLATE.md`

---

## Document Purpose

This plan contains **near-final prose** for every section of the Agentic Workflows tech talk. Phase 3 will assemble this content into README.md with minimal edits—primarily adding inline citations, embedding examples, and polishing transitions.

**Voice:** Optimistic curiosity—lead with discovery and what's now possible, not problems and pain.

---

## Frontmatter

```yaml
---
status: active
updated: 2026-03-05
section: "Agentic Transformation"
references:
  - url: https://github.blog/ai-and-ml/automate-repository-tasks-with-github-agentic-workflows/
    label: "GitHub Blog: Automate repository tasks with GitHub Agentic Workflows"
    verified: 2026-03-05
  - url: https://github.github.com/gh-aw/introduction/overview/
    label: "GitHub Agentic Workflows Documentation: Introduction & Overview"
    verified: 2026-03-05
  - url: https://github.github.com/gh-aw/introduction/how-they-work/
    label: "GitHub Agentic Workflows Documentation: How They Work"
    verified: 2026-03-05
  - url: https://github.github.com/gh-aw/introduction/architecture/
    label: "GitHub Agentic Workflows Documentation: Security Architecture"
    verified: 2026-03-05
  - url: https://github.github.io/gh-aw/reference/safe-outputs/
    label: "GitHub Agentic Workflows Reference: Safe Outputs"
    verified: 2026-03-05
  - url: https://github.github.com/gh-aw/blog/2026-01-12-welcome-to-pelis-agent-factory/
    label: "GitHub Agentic Workflows Blog: Welcome to Peli's Agent Factory"
    verified: 2026-03-05
  - url: https://github.github.com/gh-aw/blog/2026-01-13-meet-the-workflows/
    label: "GitHub Agentic Workflows Blog: Meet the Workflows"
    verified: 2026-03-05
  - url: https://github.com/github/gh-aw/blob/main/create.md
    label: "GitHub Repository: Create Workflow Documentation"
    verified: 2026-03-05
  - url: https://github.com/Sentry01/AgentCouncil
    label: "GitHub Repository: Sentry01/AgentCouncil"
    verified: 2026-03-05
  - url: https://josh-ops.com/posts/github-agentic-workflows/
    label: "Josh-Ops Blog: Getting Started with GitHub Agentic Workflows"
    verified: 2026-03-05
  - url: https://www.trpkovski.com/2026/02/22/agentic-workflows-write-github-actions-in-markdown
    label: "Trpkovski Blog: Agentic Workflows: Write GitHub Actions in Markdown"
    verified: 2026-03-05
  - url: https://dev.to/htekdev/github-agentic-workflows-a-hands-on-guide-to-ai-powered-cicd-255e
    label: "Dev.to: GitHub Agentic Workflows: A Hands-On Guide to AI-Powered CI/CD"
    verified: 2026-03-05
  - url: https://yuv.ai/blog/gh-aw
    label: "Yuv.ai Blog: GitHub Agentic Workflows: Write CI/CD in Natural Language"
    verified: 2026-03-05
  - url: https://www.kenmuse.com/blog/github-agentic-workflows-bring-ai-agents-to-actions/
    label: "Ken Muse Blog: GitHub Agentic Workflows Bring AI Agents to Actions"
    verified: 2026-03-05
  - url: https://github.github.com/gh-aw/setup/quick-start/
    label: "GitHub Agentic Workflows: Quick Start Guide"
    verified: 2026-03-05
---
```

---

## Title & Subtitle

**Title:** GitHub Agentic Workflows: Repository Automation with AI Agents

**Subtitle:** Write repository automation in natural language Markdown, compiled to secure GitHub Actions that adapt to context

**Question:**
> "How can I automate repository tasks that require judgment and context—like triaging issues, reviewing code quality, or synthesizing progress reports—without writing complex YAML workflows?"

**Duration:** 45-60 minutes
**Target Audience:** Developers, DevOps Engineers, Platform Engineers, Engineering Managers

---

## Content Fitness Assessment

| Criterion | Assessment | Notes |
|-----------|-----------|-------|
| **Relevant** | 🟢 High | Repository automation is universal; current approaches require complex YAML and can't adapt to context. AI-powered workflows unlock new automation paradigms. |
| **Compelling** | 🟢 High | Write workflows in Markdown instead of YAML; AI agents make decisions based on repository state; security-first sandbox design makes this practical. |
| **Actionable** | 🟢 High | Install gh-aw CLI extension, create first workflow in minutes, deploy to production with built-in security guardrails. |

**Overall Status:** 🟢 Ready to use

---

## The Opportunity Section

### What's Now Possible

Repository automation has entered a new era. What once required intricate YAML configurations and deterministic logic can now be expressed as **intent in natural language**, executed by AI agents that adapt to your repository's context.

**GitHub Agentic Workflows (gh-aw)** brings AI coding agents directly into your GitHub Actions—not as external services, but as **first-class repository automation primitives**. Write what you want to happen in Markdown; the AI figures out how.

- **Intent-Driven Automation**
  Describe desired outcomes ("Triage new issues based on content"), not implementation steps. AI agents interpret context and decide appropriate actions.

- **Security-First Design**
  Agents run in sandboxed environments with read-only access by default. Write operations require explicit "safe outputs"—pre-approved, sanitized GitHub actions that prevent prompt injection and unauthorized modifications.

- **Adaptive Intelligence**
  Unlike static workflows, agentic workflows make decisions based on repository state. They understand code structure, issue context, PR relationships, and project status—then act accordingly.

- **Continuous Repository Improvement**
  AI agents embedded in your development workflow compound value over time. Daily code simplifications, documentation updates, metric tracking—all running autonomously with human oversight.

**The shift:** From scripting what to do step-by-step, to declaring what success looks like and letting AI navigate the path.

---

## The Solution Section

### GitHub Agentic Workflows (gh-aw)

GitHub Agentic Workflows transform repository automation through three core innovations:

#### 1. Markdown-Based Workflow Definition

Instead of YAML with explicit steps, write workflows as **natural language instructions in Markdown files**:

```markdown
---
on:
  schedule: daily
permissions:
  contents: read
  issues: read
safe-outputs:
  create-issue:
    title-prefix: "[daily-status] "
    labels: [report, automation]
---

## Daily Team Status Report

Create an upbeat daily status report as a GitHub issue summarizing:
- Recent activity (issues, PRs, discussions, releases)
- Progress tracking and highlights
- Actionable next steps for maintainers
```

The AI agent reads these instructions, examines your repository, and produces the requested report—no explicit API calls, no complex conditionals.

#### 2. Compilation to Secure GitHub Actions

The `gh aw compile` command converts Markdown workflows into **secure YAML lock files** that run in GitHub Actions:

- **Agent job** runs with read-only permissions in an isolated sandbox
- **Safe-output handler jobs** execute validated write operations with minimal permissions
- **Audit logging** tracks every action with workflow-id markers
- **Input sanitization** prevents prompt injection and unauthorized access

This separation of concerns—AI makes decisions, sanitized handlers execute actions—is the security foundation.

#### 3. Safe Outputs: Pre-Approved Write Operations

Agents can't directly modify repositories. Instead, they produce **structured JSON outputs** requesting specific GitHub operations:

```yaml
safe-outputs:
  create-issue:
    title-prefix: "[ai] "
    labels: [automation]
    max: 5
    expires: 7  # auto-close after 7 days
```

The safe-output handler validates agent requests, sanitizes inputs, and executes approved actions. Available operations include:

- **Issues:** Create, update, close, link sub-issues
- **Pull Requests:** Create, update, push commits, request reviews
- **Comments:** Add, hide
- **Labels & Assignments:** Add/remove labels, assign reviewers, set milestones
- **Projects:** Create projects, update items, post status updates
- **Code Review:** Add review comments, submit reviews, resolve threads
- **Security:** Create/autofix code scanning alerts

Each safe-output type has configurable max operations, expiration policies, and cross-repository controls.

---

## Key Artifacts Section

When working with agentic workflows, you'll interact with these files and tools:

| Artifact | Purpose | Example |
|----------|---------|---------|
| **Workflow Markdown** | Source workflow definition (human-editable) | `.github/workflows/issue-triage.md` |
| **Lock File** | Compiled secure YAML workflow (generated) | `.github/workflows/issue-triage.lock.yml` |
| **gh CLI Extension** | Install, create, compile, debug workflows | `gh aw compile`, `gh aw logs` |
| **Safe-Output Config** | Security declarations in frontmatter | `safe-outputs: create-issue: ...` |
| **Agent Prompts** | Natural language instructions in Markdown body | "Triage issues and apply labels..." |
| **MCP Config** | Model Context Protocol server declarations | `.vscode/mcp.json` |
| **Workflow Logs** | Execution logs and audit trails | `gh aw logs issue-triage` |

**Navigation:** Start with `.github/workflows/*.md` files—these are your workflows. The lock files (.lock.yml) are generated artifacts; never edit them directly.

---

## Mental Model Preview (Core Insight)

**The Shift:** From **stepwise prescriptions** to **outcome-driven intent**

Traditional workflows say "do these exact steps in this order." Agentic workflows say "achieve this outcome, adapting to what you find."

---

## Decision Tree Section

### When to Use Agentic Workflows

```
Do you need repository automation?
│
├─ YES → Does it require judgment or context-awareness?
│        │
│        ├─ YES → Examples: Issue triage, code review feedback,
│        │        progress reports, quality analysis
│        │        ✅ USE AGENTIC WORKFLOWS
│        │        │
│        │        ├─ Need write operations?
│        │        │  └─ Declare safe-outputs with appropriate guardrails
│        │        │
│        │        └─ Read-only analysis?
│        │           └─ Simplest case—no safe-outputs needed
│        │
│        └─ NO → Examples: Build, test, deploy, static checks
│                ⚠️ USE TRADITIONAL GITHUB ACTIONS
│                (Deterministic tasks don't need AI)
│
└─ NO → No action needed
```

**Key Decision Factors:**

1. **Contextual Understanding Required?**
   - Analyzing issue content for triage → Agentic
   - Running test suite → Traditional

2. **Adaptive Decision-Making?**
   - Recommending code simplifications → Agentic
   - Deploying to staging → Traditional

3. **Synthesis & Summarization?**
   - Weekly progress report → Agentic
   - Slack notification on deploy → Traditional

4. **Natural Language Input/Output?**
   - Converting issue comments to labels → Agentic
   - Linting code → Traditional

**Complementary Approach:** Use both. Traditional GitHub Actions for CI/CD pipelines, agentic workflows for "Continuous AI" tasks—analysis, recommendations, coordination.

---

## Major Section 1: Core Architecture & Compilation

<!-- 🎬 MAJOR SECTION: Core Architecture -->

### How Agentic Workflows Execute

An agentic workflow progresses through three distinct phases:

#### Phase 1: Authoring (One Time)

Developers author workflows as Markdown files with YAML frontmatter:

```markdown
---
on:
  issues:
    types: [opened]
permissions:
  contents: read
  issues: write
tools:
  github:
    toolsets: [issues, labels]
safe-outputs:
  add-labels:
    allowed: [bug, feature, docs]
    max: 3
  add-comment:
    max: 1
---

## Issue Triage Workflow

Analyze new issues and apply appropriate labels.

### Instructions
1. Read the issue title and body
2. Identify the issue type
3. Apply 1-3 relevant labels
4. Add a friendly comment explaining the decision
```

**Key Components:**
- **Triggers** (`on:`): When the workflow runs (schedule, events, manual)
- **Permissions**: Minimal read-only access for agent
- **Tools**: GitHub APIs and MCP servers available to agent
- **Safe Outputs**: Pre-approved write operations
- **Instructions**: Natural language task description

#### Phase 2: Compilation (Per Source Change)

Run `gh aw compile issue-triage` to transform Markdown → secure YAML:

1. **Parse frontmatter** (triggers, permissions, tools, safe-outputs)
2. **Extract Markdown body** (agent instructions)
3. **Generate secure workflow** with:
   - Agent job (read-only, sandboxed)
   - Safe-output handler jobs (minimal write permissions)
   - Permission isolation
   - Input sanitization logic
   - Audit trail markers
4. **Write lock file** (`.github/workflows/issue-triage.lock.yml`)

**Lock File Properties:**
- Marked as generated (`linguist-generated=true`)
- Git merge strategy: `merge=ours` (prevents conflicts)
- Should not be manually edited
- Re-compiled whenever source `.md` changes

**Deploy:** Commit both `.md` and `.lock.yml` files; GitHub Actions runs the lock file.

#### Phase 3: Execution (Per Trigger)

When triggered, the compiled workflow executes:

**Agent Job (Read-Only):**
1. Spin up isolated container (Ubuntu slim)
2. Load AI agent (GitHub Copilot, Claude, Codex, Gemini)
3. Provide agent with:
   - Workflow instructions from Markdown body
   - Declared GitHub tools (read-only API access)
   - Repository context
4. Agent explores repository, gathers data
5. Agent produces structured JSON output (safe-output requests)

**Safe-Output Handler Jobs (Write Operations):**
1. Receive agent's JSON output
2. Validate schema (correct format?)
3. Sanitize inputs (escape XML, validate URLs, check domains)
4. Verify permissions (is this safe-output declared?)
5. Enforce limits (max operations, expiration, cross-repo rules)
6. Execute approved GitHub operations
7. Log actions with workflow-id markers

**Isolation Guarantees:**
- Agent has zero write access
- Agent output goes through validation pipeline
- Only approved operations execute
- All actions auditable via workflow markers

**Example Audit Trail:**
```markdown
<!-- gh-aw-workflow-id: issue-triage -->
<!-- gh-aw-run-id: 1234567890 -->
```

Hidden markers embedded in issue/PR bodies enable searching:
```
repo:owner/repo is:issue "gh-aw-workflow-id: issue-triage" in:body
```

---

## Major Section 2: Safe Outputs Deep Dive

<!-- 🎬 MAJOR SECTION: Safe Outputs -->

### Security Through Separation of Concerns

Safe outputs are the **security foundation** of agentic workflows. They solve the core tension: *How do we let AI agents automate repository tasks without risking unauthorized modifications or prompt injection?*

**Answer:** Separate decision-making (read-only AI) from action execution (validated handlers).

#### The Safe Output Lifecycle

1. **Declaration (Workflow Frontmatter)**
   ```yaml
   safe-outputs:
     create-issue:
       title-prefix: "[bot] "
       labels: [automation]
       max: 5
       expires: 7
   ```

2. **Agent Request (Structured JSON)**
   ```json
   {
     "type": "create_issue",
     "title": "[bot] CI failure in test-auth.js",
     "body": "## Failure Summary\n\nTest suite failed...",
     "labels": ["automation", "ci-failure"]
   }
   ```

3. **Validation Pipeline**
   - Schema validation (correct JSON structure?)
   - Permission check (is `create-issue` declared?)
   - Sanitization (XML escape, URL validation)
   - Rate limiting (within `max: 5`?)
   - Domain filtering (URLs from allowed domains only?)

4. **Execution (Minimal Permissions)**
   - Safe-output handler job has `issues: write` only
   - Creates issue with sanitized content
   - Adds workflow-id marker
   - Sets expiration (if configured)

5. **Audit Trail**
   - Issue includes hidden markers
   - GitHub Actions logs capture full execution
   - `gh aw audit <run-id>` shows detailed trace

#### Critical Safe-Output Pattern: Noop

**The #1 runtime failure mode:** Agent finishes without calling any safe-output, workflow fails silently.

**Solution:** Always include `noop` safe-output (enabled by default):

```yaml
safe-outputs:
  create-issue:  # noop auto-enabled
```

Agent **must** call `noop` when no action is needed:

```json
{
  "noop": {
    "message": "No action needed: analysis complete, no issues found"
  }
}
```

**When to use noop:**
- No issues found during code scan
- No breaking changes detected
- Repository already in desired state
- Condition for action not met

Explicitly instruct agents in workflow Markdown:
```markdown
If no action is needed, call noop with an explanation.
```

#### Issue Operations

**Create Issue** supports:
- **Auto-expiration:** Issues auto-close after configurable time (`expires: 7` = 7 days)
- **Issue grouping:** Multiple issues linked as sub-issues under parent (max 64)
- **Auto-close older:** Close previous open issues from same workflow when new issue created
- **Cross-repository:** Target external repos with `target-repo` and `allowed-repos`

**Example with all features:**
```yaml
safe-outputs:
  create-issue:
    title-prefix: "[daily-report] "
    labels: [report, automation]
    assignees: [user1]
    max: 5
    expires: 7
    group: true
    close-older-issues: true
    target-repo: "org/metrics-repo"
    allowed-repos: ["org/metrics-repo"]
```

#### Pull Request Operations

**Create Pull Request** enables:
- **Multiple PRs:** Set `max > 1` for multiple independent PRs per run
- **Auto-expiration:** Auto-close PRs after time period (same-repo only)
- **Base branch:** Target non-default branch (`base-branch: "vnext"`)
- **CI triggering:** Use `github-token-for-extra-empty-commit` to trigger CI
- **Git commands:** Automatically enabled when `create-pull-request` declared

**Example:**
```yaml
safe-outputs:
  create-pull-request:
    title-prefix: "[simplify] "
    labels: [code-quality, bot]
    reviewers: [lead-dev]
    draft: true
    max: 3
    expires: 14
    base-branch: "main"
```

**Push to PR Branch** supports updating existing PRs:
```yaml
safe-outputs:
  push-to-pull-request-branch:
    target: "*"  # or specific PR number
    max: 3
```

**Security:** Cannot push to PRs from forks (fails early).

#### Code Review Operations

**PR Review Comments** accumulate and submit as single review:

```yaml
safe-outputs:
  create-pull-request-review-comment:
    max: 10
    side: "RIGHT"  # or "LEFT"
  submit-pull-request-review:
    max: 1
    target: "triggering"
```

**Review flow:**
1. Agent calls `create-pull-request-review-comment` multiple times
2. Comments buffered
3. Agent calls `submit-pull-request-review` (or auto-submit if not called)
4. Single review posted with all comments

**Review events:** `APPROVE`, `REQUEST_CHANGES`, `COMMENT`

**Resolve Review Thread** enables closing discussions:
```yaml
safe-outputs:
  resolve-pull-request-review-thread:
    max: 10
```

#### Project Operations

**Create/Update Project** automates GitHub Projects v2:

```yaml
safe-outputs:
  create-project:
    max: 1
    github-token: ${{ secrets.GH_AW_PROJECT_GITHUB_TOKEN }}  # required
    target-owner: "myorg"
    views:
      - name: "Sprint Board"
        layout: board
      - name: "Task Tracker"
        layout: table
```

**Supported field types:** TEXT, DATE, NUMBER, ITERATION, SINGLE_SELECT

**Create Project Status Update** posts progress reports:
```yaml
safe-outputs:
  create-project-status-update:
    project: "https://github.com/orgs/myorg/projects/73"
    max: 1
    github-token: ${{ secrets.GH_AW_PROJECT_GITHUB_TOKEN }}
```

Agent specifies status: `ON_TRACK`, `AT_RISK`, `OFF_TRACK`, `COMPLETE`, `INACTIVE`

#### Workflow Orchestration

**Dispatch Workflow** triggers other workflows:

```yaml
safe-outputs:
  dispatch-workflow:
    workflows: [worker-1, worker-2]
    max: 3
```

**Features:**
- Compile-time validation (workflows must exist)
- No self-reference (prevents loops)
- 5-second rate limiting
- Same-repository only

**Use case:** Orchestrator-worker pattern (parent workflow dispatches specialized workers, then synthesizes results).

---

## Major Section 3: The Agent Factory Pattern

<!-- 🎬 MAJOR SECTION: Agent Factory -->

### Discovering Repository Automation Patterns

GitHub Next and Microsoft Research asked: *What does repository-level AI automation unlock?* Instead of theorizing, they built **100+ specialized workflows** and ran them continuously in the `github/gh-aw` repository. This collection is **"Peli's Agent Factory"** (named after Peli de Halleux).

#### Factory Philosophy

1. **Embrace Diversity:** Create many specialized workflows as opportunities arise
2. **Use Them Continuously:** Run workflows in real development, not demos
3. **Observe What Works:** Identify patterns that succeed and fail
4. **Share the Knowledge:** Catalog effective structures for others to adapt

**Key Insight:** Don't build one monolithic "do-everything" agent. Build **many focused workflows** that each excel at a specific task.

#### Factory Categories

Workflows organized by automation purpose:

| Category | Focus | Example Workflows |
|----------|-------|-------------------|
| **Continuous Improvement** | Daily code quality enhancements | Simplify code, refactor patterns, update dependencies |
| **Issue & PR Management** | Triage, labeling, coordination | Auto-label issues, link related PRs, track sub-issues |
| **Metrics & Analytics** | Read-only monitoring and insights | Daily/weekly reports, trend analysis, contributor stats |
| **Quality & Testing** | Fault investigation and remediation | CI failure diagnosis, flaky test detection, coverage analysis |
| **Security & Compliance** | Security monitoring and fixes | Code scanning triage, dependency audits, license checks |
| **Operations & Release** | Release automation | Release notes generation, changelog updates, version bumping |
| **Multi-Repository** | Cross-repo coordination | Feature sync, multi-repo tracking, organization-wide metrics |
| **Interactive & ChatOps** | Command-triggered workflows | Issue comment commands, PR review requests |
| **Project Coordination** | Project management automation | Epic breakdown, task planning, milestone tracking |
| **Meta-Workflows** | Self-monitoring and optimization | Workflow health monitoring, performance analysis |

#### Proven Patterns from the Factory

**Pattern 1: Continuous Simplicity**
- **Trigger:** Daily schedule
- **Action:** Scan codebase for simplification opportunities
- **Output:** PR with simplification suggestions
- **Human Role:** Review and merge (or close)
- **Value:** Compounds over time—small daily improvements add up

**Pattern 2: Continuous Documentation**
- **Trigger:** Code changes (push, PR)
- **Action:** Identify outdated documentation sections
- **Output:** PR updating docs to match code
- **Human Role:** Review accuracy
- **Value:** Maintains code-docs consistency automatically

**Pattern 3: Orchestrator-Worker**
- **Structure:** Orchestrator workflow dispatches multiple worker workflows
- **Execution:** Workers run specialized tasks in parallel
- **Synthesis:** Orchestrator collects results and creates summary report
- **Value:** Enables multi-day, multi-phase agent tasks

**Pattern 4: Meta-Workflows**
- **Purpose:** Workflows that monitor other workflows
- **Analysis:** Execution logs, performance bottlenecks, failure patterns
- **Output:** Workflow improvement suggestions
- **Value:** Self-optimizing automation system

**Pattern 5: Issue Group Management**
- **Structure:** Parent issue with linked sub-issues (tasks)
- **Monitoring:** Workflow tracks sub-issue completion
- **Updates:** Auto-update parent with progress percentages
- **Completion:** Auto-close parent when all sub-issues resolved
- **Value:** Project tracking without manual coordination

#### Design Patterns That Work

**1. Repository-Level Automation is Transformative**
- Agents embedded in development workflow have outsized impact
- Continuous daily improvements compound exponentially
- Meta-workflows (agents monitoring agents) unlock optimization loops

**2. Specialization Reveals Possibilities**
- Focused agents discover more applications than monolithic agents
- Each workflow solves one problem excellently
- Easier to debug, iterate, and improve

**3. Guardrails Enable Innovation**
- Strict constraints (safe outputs, sandboxing) make experimentation safer
- Teams willing to try agent automation when risks are bounded
- Security-first design builds trust and adoption

**4. Cost-Quality Tradeoffs Are Real**
- Longer analyses aren't always better
- Focused workflows with clear success criteria perform better
- Monitor execution costs and optimize

#### Common Failure Modes

**1. Agent Doesn't Produce Output**
- **Cause:** Forgot to call `noop` when no action needed
- **Fix:** Always include explicit `noop` instructions

**2. Permission Errors**
- **Cause:** Safe output requires permission not granted in frontmatter
- **Fix:** Review required permissions for each safe-output type

**3. Too Many Operations**
- **Cause:** Agent tries to create more items than `max` allows
- **Fix:** Set appropriate `max` values or narrow workflow scope

**4. Prompt Injection Attempts**
- **Cause:** Malicious input tries to manipulate agent
- **Fix:** Safe outputs sanitize automatically, but monitor anomalies

#### Best Practices from the Factory

**1. Start Small**
- Begin with read-only workflows (metrics, reports)
- Graduate to safe writes (labels, comments)
- Finally enable code changes (PRs) with review gates

**2. Human-in-the-Loop**
- Use `draft: true` for PRs (require review before merge)
- Use `expires` to auto-close old suggestions
- Monitor runs and adjust prompts iteratively

**3. Clear Success Criteria**
- Define explicit goals in workflow instructions
- Include examples of desired output
- Specify edge cases and failure modes

**4. Iterative Improvement**
- Start with basic workflow
- Observe behavior over multiple runs
- Refine prompts based on actual output
- Add guardrails as patterns emerge

---

## Major Section 4: AgentCouncil Pattern

<!-- 🎬 MAJOR SECTION: AgentCouncil -->

### Multi-Agent Synthesis for Better Decisions

A single AI model has blind spots. Different models excel at different tasks—some favor creativity, others favor precision; some understand system design, others excel at code implementation.

**AgentCouncil** (Shlomi Shaki) runs **three different AI models in parallel** on the same problem, then synthesizes their outputs into a final answer. It's designed to overcome single-model limitations and produce higher-quality results through **collaborative iteration** or **adversarial scrutiny**.

**Repository:** https://github.com/Sentry01/AgentCouncil

**Core Hypothesis:** Multi-agent interaction produces novel synthesis (collaborative) or battle-tested answers (adversarial) that no single model achieves alone.

#### The Two Modes

**Collaborative Mode 🤝 (Default)**

1. **Draft Phase:** Alpha, Beta, Gamma explore the problem independently from different angles
2. **Improve Phase:** Each agent reads the other two drafts and writes an improved version, stealing the best ideas
3. **Synthesize Phase:** Orchestrator authors the definitive response from all three enriched perspectives

**Best for:** Brainstorming, creative problem-solving, exploring design spaces, research where breadth matters

**Adversarial Mode 🗡️**

1. **Draft Phase:** Alpha, Beta, Gamma tackle the problem independently
2. **Triage Phase:** Orchestrator identifies the strongest position
3. **Attack Phase:** Other two agents try to tear apart the leading position
4. **Verdict Phase:** Orchestrator decides: did the leader survive, need modification, or get overturned?

**Best for:** Architecture decisions, security reviews, comparing approaches, high-stakes answers needing scrutiny

#### Agent Roles & Model Assignments

| Agent | Collaborative Role | Adversarial Role | Draft Model | Review Model |
|-------|-------------------|------------------|-------------|--------------|
| **Alpha** | Deep Explorer | Drafter & Red Teamer | claude-opus-4.6 | gpt-5.3-codex |
| **Beta** | Practical Builder | Fact-Checker & Validator | gpt-5.3-codex | gemini-3.1-pro |
| **Gamma** | Elegant Minimalist | Optimizer & Devil's Advocate | gemini-3.1-pro | claude-opus-4.6 |
| **Orchestrator** | Author (synthesis) | Judge (verdict) | claude-opus-4.6 | gpt-5.3-codex |

**Model diversity is intentional:** Different architectures, training data, and optimization targets produce complementary perspectives.

#### Implementation for GitHub Copilot CLI

AgentCouncil integrates with Copilot CLI as:

1. **A skill** (`~/.copilot/skills/agent-council/skill.md`)
   Trigger: `council: your question`

2. **A standalone agent** (`~/.copilot/agents/AgentCouncil.agent.md`)
   Invoke: `copilot --agent AgentCouncil`

**Mode Detection (Automatic from Keywords):**

- **Adversarial triggers:** `debate`, `adversarial`, `challenge`, `stress-test`, `which is better`, `argue`, `attack`, `defend`, `versus`, `vs`
- **Collaborative triggers:** `council`, `brainstorm`, `collaborate`, `explore`, `build on`, `novel`, `creative`, `ideas`

**Cost & Latency:**
- Collaborative: 7 model calls (3 + 3 + 1), ~2x single-agent latency
- Adversarial: 6 model calls (3 + 2 + 1), ~2x single-agent latency

**Value Proposition:** Higher-quality answers in 2x time vs. 1x quality in 1x time—worthwhile for important decisions.

#### Domain Adaptation

The council shifts agent focus based on question domain:

| Domain | Alpha Focus | Beta Focus | Gamma Focus |
|--------|-------------|------------|-------------|
| **Code** | Implementation + security self-review | API accuracy, versions, edge cases | Performance, readability, alternatives |
| **Architecture** | System design + failure modes | Tech claims, benchmarks, scalability | Simplicity, clarity, alternatives |
| **Research** | Comprehensive analysis + bias check | Source verification, citations | Actionability, counter-arguments |
| **Writing** | Content + tone self-critique | Factual accuracy, consistency | Flow, conciseness, formatting |

**Takeaway:** Same council members, different lenses depending on context—adaptive collaboration.

#### When to Use AgentCouncil

**Use Council for:**
- Architecture decisions with tradeoffs
- Security reviews requiring scrutiny
- Research questions needing breadth
- Creative brainstorming and exploration
- High-stakes answers justifying extra cost

**Skip Council for:**
- Simple factual lookups
- Routine implementation tasks
- Time-sensitive queries
- Low-stakes decisions

**Pro Tip:** Start with single-agent, escalate to council when the answer doesn't satisfy or requires defense against critique.

---

## Real-World Use Cases Section

### 1. Issue Triage Automation

**Scenario:** Growing repository with dozens of new issues weekly; manual labeling is tedious and inconsistent.

**Agentic Workflow Solution:**
- **Trigger:** `on: issues: [opened]`
- **Action:** AI reads issue title/body, identifies type (bug, feature, docs, question)
- **Output:** Adds 1-3 labels, posts friendly comment explaining decision
- **Safe Outputs:** `add-labels` (allowed list), `add-comment` (max: 1)

**Value:** Instant triage, consistent labeling, maintainers focus on substance not categorization.

**Example:** [Embed `examples/issue-triage.md`]

---

### 2. CI Failure Diagnosis

**Scenario:** CI fails intermittently; debugging requires log diving; team wastes time on repetitive investigation.

**Agentic Workflow Solution:**
- **Trigger:** `on: workflow_run: [CI]: [failure]`
- **Action:** AI fetches logs, identifies failing step, searches past issues
- **Output:** Creates diagnostic issue with error summary, stack trace, related issues, next steps
- **Safe Outputs:** `create-issue` (max: 1, `close-older-issues: true`, `expires: 7`)

**Value:** Automatic diagnosis, knowledge base of failure modes, reduced MTTR (mean time to resolution).

**Example:** [Embed `examples/ci-failure-diagnostic.md`]

---

### 3. Weekly Repository Health Report

**Scenario:** Engineering manager wants weekly snapshot of repository activity and health—what's progressing, what's stalled, what needs attention.

**Agentic Workflow Solution:**
- **Trigger:** `on: schedule: weekly`
- **Action:** AI analyzes past 7 days (issues, PRs, commits, milestones), identifies trends and recommendations
- **Output:** Creates comprehensive report issue with metrics, highlights, and actionable next steps
- **Safe Outputs:** `create-issue` (max: 1, `close-older-issues: true`)

**Value:** Zero-effort visibility, trend awareness, data-driven prioritization.

**Example:** [Embed `examples/weekly-health-report.md`]

---

### 4. Continuous Code Simplification

**Scenario:** Technical debt accumulates; no dedicated time for refactoring; team wants gradual improvement without project disruption.

**Agentic Workflow Solution:**
- **Trigger:** `on: schedule: daily`
- **Action:** AI scans codebase for simplification opportunities (redundant logic, verbose patterns, outdated idioms)
- **Output:** Creates PR with simplification suggestions
- **Safe Outputs:** `create-pull-request` (max: 1, `draft: true`, `expires: 14`)

**Value:** Continuous improvement culture, compounding code quality gains, human reviews small focused changes.

**Example:** [See Pattern 1 in Agent Factory section]

---

### 5. Multi-Agent Orchestration

**Scenario:** Complex analysis requiring multiple specialized perspectives—can't do it all in one workflow pass.

**Agentic Workflow Solution:**
- **Trigger:** Orchestrator runs daily
- **Action:** Orchestrator dispatches 3 worker workflows in parallel (analyze issues, analyze PRs, analyze CI)
- **Workers:** Each performs specialized analysis
- **Synthesis:** Orchestrator collects results, creates unified summary report
- **Safe Outputs:** `dispatch-workflow` (orchestrator), `create-issue` (workers + orchestrator)

**Value:** Parallel execution, specialized intelligence, coordinated insights.

**Example:** [Embed `examples/orchestrator-pattern.md`]

---

## Mental Model Shift Section (Full)

### 🧠 The Shift: From Scripted Steps to Adaptive Intent

**Old Mental Model: Prescriptive Automation**
- Write exact steps in YAML
- Account for every branch and edge case
- Update workflow whenever requirements change
- Deterministic execution: same input → same output

**New Mental Model: Intent-Driven Automation**
- Describe desired outcome in natural language
- AI adapts to repository context
- Workflow learns from repository state
- Context-sensitive execution: AI decides best path

#### ✅ Move Toward

| What | Why |
|------|-----|
| **Natural Language Instructions** | Express intent without implementation details |
| **Context-Aware Decisions** | AI examines repository state and adapts actions |
| **Read-Only by Default** | Security through minimal permissions |
| **Safe-Output Validation** | Separation of concerns: AI decides, handlers execute |
| **Human-in-the-Loop** | Draft PRs, expiration policies, review gates |
| **Specialized Workflows** | Many focused agents > one monolithic agent |
| **Continuous Improvement** | Daily automated enhancements that compound |
| **Meta-Workflows** | Agents monitoring and optimizing other agents |

#### ⚠️ Move Away From

| What | Why |
|------|-----|
| **Complex YAML Workflows** | Hard to maintain, brittle, verbose |
| **Deterministic-Only Logic** | Can't adapt to context or make judgments |
| **Manual Triage & Coordination** | AI handles repetitive decision-making better |
| **One-Size-Fits-All Agents** | Specialization reveals more possibilities |
| **Unlimited Agent Permissions** | Security risk—read-only + safe-outputs is safer |
| **Set-and-Forget Automation** | Monitor, iterate, improve continuously |

#### 🛑 Stop Doing (Dangerous/Obsolete)

| What | Why |
|------|-----|
| **Giving AI Direct Write Access** | Prompt injection risk, unauthorized modifications |
| **Ignoring noop Pattern** | #1 failure mode—always handle "no action needed" case |
| **Skipping Lock File Compilation** | Running uncompiled workflows bypasses security |
| **Manually Editing Lock Files** | Generated artifacts—edit source `.md` instead |
| **Triggering on Every Commit** | Cost adds up fast—use schedules or specific events |

---

## What You Can Do Today Section

### Immediate Actions (15 Minutes)

1. **Install gh-aw CLI Extension**
   ```bash
   curl -sL https://raw.githubusercontent.com/github/gh-aw/main/install-gh-aw.sh | bash
   gh aw version
   ```

2. **Create Your First Workflow**
   ```bash
   gh aw new daily-status-report
   ```

3. **Edit the Workflow** (`.github/workflows/daily-status-report.md`)
   - Add natural language instructions in Markdown body
   - Configure `safe-outputs` in frontmatter
   - Set trigger to `on: schedule: daily`

4. **Compile and Deploy**
   ```bash
   gh aw compile daily-status-report
   git add .github/workflows/daily-status-report.md .github/workflows/daily-status-report.lock.yml
   git commit -m "Add daily status report workflow"
   git push
   ```

### Build Skills (1 Hour)

- **Explore the Agent Factory:** Browse [Peli's Agent Factory blog](https://github.github.com/gh-aw/blog/2026-01-12-welcome-to-pelis-agent-factory/) for workflow patterns
- **Study Safe Outputs Reference:** Read [Safe Outputs documentation](https://github.github.io/gh-aw/reference/safe-outputs/) to understand security model
- **Review Examples:** Check `examples/` directory in this tech talk for starter workflows

### Go Deep (1 Day)

- **Create 3-5 Specialized Workflows:** Start with read-only (reports), then safe writes (labels), finally PRs
- **Implement Orchestrator-Worker Pattern:** Build a meta-workflow that coordinates specialized workers
- **Try AgentCouncil:** Install AgentCouncil skill and compare single-agent vs. multi-agent answers on architecture questions

### Key Concepts to Master

| Concept | Why It Matters |
|---------|----------------|
| **Safe Outputs** | Security foundation—understand validation pipeline |
| **Noop Pattern** | Prevent #1 failure mode—always handle "no action" case |
| **Compilation** | Markdown → secure YAML—verify lock files after changes |
| **Agent Factory Philosophy** | Specialization > monolithic—build many focused workflows |
| **Human-in-the-Loop** | Draft PRs, expirations, review gates—trust but verify |

---

## Related Patterns Section

### Patterns in This Talk

- **Agent Factory:** Many specialized workflows > one monolithic agent
- **Orchestrator-Worker:** Parent workflow dispatches specialized workers, synthesizes results
- **Meta-Workflows:** Agents monitoring and optimizing other agents
- **AgentCouncil:** Multi-agent collaboration/adversarial modes for better decisions
- **Safe Outputs:** Separation of concerns—AI decides, handlers execute

### Related Patterns (Other Talks)

- **Custom Instructions:** Teach Copilot your repository structure and conventions
- **Hooks & Primitives:** Extend Copilot with custom tooling and integrations
- **Model Context Protocol (MCP):** Connect agents to external data sources and APIs
- **Sandboxed Terminal Execution:** Run AI-generated commands safely
- **Multi-Agent Teams:** Coordinate multiple specialized agents (Copilot Teams)

### Further Exploration

- **GitHub Actions Best Practices:** How agentic workflows complement traditional CI/CD
- **AI Safety & Governance:** Enterprise policies for agent automation
- **Continuous Intelligence:** Moving beyond CI/CD to "Continuous AI"

---

## References Mapping by Section

### The Opportunity
- [^1] GitHub Blog: Automate repository tasks with GitHub Agentic Workflows
- [^2] GitHub Agentic Workflows Documentation: Introduction & Overview

### The Solution
- [^3] GitHub Agentic Workflows Documentation: How They Work
- [^4] GitHub Agentic Workflows Documentation: Security Architecture

### Core Architecture & Compilation
- [^3] How They Work
- [^8] GitHub Repository: Create Workflow Documentation
- [^15] GitHub Agentic Workflows: Quick Start Guide

### Safe Outputs Deep Dive
- [^5] GitHub Agentic Workflows Reference: Safe Outputs
- [^4] Security Architecture

### The Agent Factory Pattern
- [^6] Welcome to Peli's Agent Factory
- [^7] Meet the Workflows
- [^10] Josh-Ops Blog: Getting Started with GitHub Agentic Workflows

### AgentCouncil Pattern
- [^9] GitHub Repository: Sentry01/AgentCouncil

### Real-World Use Cases
- [^10] Josh-Ops Blog
- [^11] Trpkovski Blog: Agentic Workflows: Write GitHub Actions in Markdown
- [^12] Dev.to: GitHub Agentic Workflows: A Hands-On Guide to AI-Powered CI/CD

### What You Can Do Today
- [^15] Quick Start Guide
- [^8] Create Workflow Documentation
- [^14] Ken Muse Blog: GitHub Agentic Workflows Bring AI Agents to Actions

---

## Artifacts to Embed

### From examples/ Directory

1. **daily-status-report.md** — Embed in Solution section
2. **issue-triage.md** — Embed in Use Case 1
3. **ci-failure-diagnostic.md** — Embed in Use Case 2
4. **weekly-health-report.md** — Embed in Use Case 3
5. **orchestrator-pattern.md** — Embed in Use Case 5
6. **safe-outputs-issue-config.yaml** — Embed in Safe Outputs section
7. **safe-outputs-pr-config.yaml** — Embed in Safe Outputs section
8. **safe-outputs-project-config.yaml** — Embed in Safe Outputs section

### Images Directory

(No images downloaded in Phase 1—primarily code/config examples)

---

## Gaps Identified

**None at this stage.** Research and examples are comprehensive. Phase 3 will proceed with assembly.

---

## Slide Extraction Notes (For Future Slide Generation)

### Title Slide
- Title: "GitHub Agentic Workflows: Repository Automation with AI Agents"
- Subtitle: "Write automation in natural language Markdown, compiled to secure GitHub Actions"

### Key Slides to Extract
1. Question slide (The Question This Talk Answers)
2. The Opportunity (3 bullets)
3. The Solution (3 core innovations)
4. Decision Tree (visual flowchart)
5. Architecture diagram (3-phase execution)
6. Safe Outputs lifecycle (5-step pipeline)
7. Agent Factory categories (table)
8. AgentCouncil modes (collaborative vs adversarial)
9. Use Cases (5 scenarios)
10. Mental Model Shift (full grid)
11. Actionable Outcomes (checklist)
12. References (numbered list)

**Constraint:** 15-20 slides max—extract highest-impact content.

---

**Plan Complete** — Ready for Phase 3 (README Assembly)
