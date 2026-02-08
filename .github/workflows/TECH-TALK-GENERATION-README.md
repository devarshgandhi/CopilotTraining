# Tech Talk Generation Workflow

Automated 4-phase workflow for creating tech talks using GitHub Issues and Copilot CLI.
Each phase commits artifacts to a shared feature branch so subsequent phases read real files.

## How It Works

```
Issue opened ─► Phase 1 (Research) ─► Phase 2 (Plan) ─► /approve-plan ─► Phase 3 (Build) ─► Phase 4 (Slides)
                  │                      │                                   │                    │
                  ▼                      ▼                                   ▼                    ▼
              Creates branch         Commits              Creates PR +    Commits slides
          tech-talk/{topic}-{#}      plan.md              commits README   to PR branch
          Commits research.md,
          images/, examples/
```

## Branch & Artifact Strategy

All phases operate on a **deterministic branch**: `tech-talk/{topic}-{issue_number}`

| Phase | Artifacts Committed | Where |
|-------|-------------------|-------|
| 1. Research | `research.md`, `images/*.png`, `examples/*` | `tech-talks/{topic}/` on branch |
| 2. Plan | `plan.md` | `tech-talks/{topic}/` on branch |
| 3. Build | `README.md` | `tech-talks/{topic}/` on branch (creates PR) |
| 4. Slides | `{topic}.md` | `slides/tech-talks/` on branch |

Phases 2-4 discover the branch via `git ls-remote --exit-code origin tech-talk/{topic}-{#}` and check it out before reading artifacts.

## Phase Details

| Phase | Trigger | What Happens | Output |
|-------|---------|-------------|--------|
| 1. Research | Issue opened with `tech-talk:intake` | Copilot CLI researches URLs, downloads images, extracts code examples | `research.md` + `images/` + `examples/` committed to branch |
| 2. Plan | `tech-talk:planned` label (auto-added) | Copilot CLI reads research artifacts, creates content outline | `plan.md` committed to branch; preview posted as comment |
| 3. Build | `/approve-plan` comment (human) | Copilot CLI reads research + plan + examples, generates README | `README.md` committed; PR created |
| 4. Slides | `tech-talk:slides` label (manual) | Copilot CLI reads README + images, generates Slidev slides | Slides committed to PR branch |

## Labels

| Label | Meaning |
|-------|---------|
| `tech-talk` | Base label for all tech talk issues |
| `tech-talk:intake` | Phase 1 trigger (set by issue template) |
| `tech-talk:planned` | Phase 2 trigger (auto-set after Phase 1) |
| `tech-talk:ready` | Content generated (auto-set after Phase 3) |
| `tech-talk:slides` | Phase 4 trigger (manually added) |
| `tech-talk:complete` | All phases done (auto-set after Phase 4) |

## Human Checkpoints

- **After Phase 2**: Review `plan.md` on the branch (link in issue comment). Comment `/approve-plan` to proceed.
- **After Phase 3**: Review the PR with `README.md`. Add `tech-talk:slides` label when ready.
- **After Phase 4**: Review slides in PR, merge when satisfied.

## Files

### Workflows
- `tech-talk-1-research.yml` — Phase 1: Research, images, examples
- `tech-talk-2-plan.yml` — Phase 2: Content plan
- `tech-talk-3-build.yml` — Phase 3: README generation + PR
- `tech-talk-4-slides.yml` — Phase 4: Slidev slide generation

### Prompt Templates
- `.github/prompts/tech-talk/research-instructions.md`
- `.github/prompts/tech-talk/planning-instructions.md`
- `.github/prompts/tech-talk/build-instructions.md`
- `.github/prompts/tech-talk/slides-instructions.md`

### Supporting Scripts
- `scripts/download-images.py` — Extracts and downloads images from source URLs

## Requirements

- **Secret**: `COPILOT_GITHUB_TOKEN` — PAT with Copilot CLI access
- **Copilot CLI**: Installed via `npm install -g @github/copilot` in workflow
- **Python 3.12+**: Used in Phase 1 for image download (`requests` package)
