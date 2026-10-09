# Step 01: Agent Governance, Branch & PR Workflow, and File Structure Discipline

**Step Branch**: `step/01-agent-governance-and-workflow`  
**Primary Branch**: `main` (or `master`)  
**Pull Request**: `[Pending PR]`  

---

## Objective

Establish repository-wide agent governance by equipping `AGENTS.md` with an exhaustive catalog of all available resources, formalizing a 10-stage Build Protocol with isolated step branches and Pull Requests, and codifying functional directory conventions in `docs/agents/file-structure.md`.

## Scope

**Explicitly included:**
- Comprehensive resource catalog in `AGENTS.md` indexing all rules, documentation, all 12 local skills, scripts, and templates.
- Update `BUILD_PROTOCOL.md` to a 10-stage development loop incorporating branch isolation (`step/NN-<slug>`), primary branch protection (`main` / `master`), and PR merges with standard merge commits (`--no-ff`).
- Update `docs/steps/00-plan-template.md` to track branch metadata, PR link, and commit SHAs (first, last, merge).
- Create `docs/agents/file-structure.md` establishing functional directory conventions (`src/`, `tests/`, `docs/`, `scripts/`, `.agents/`, `.tmp/`).
- Synchronize `docs/agents/skills.md` and `README.md`.

**Explicitly excluded:**
- Rigid PR templates (`.github/PULL_REQUEST_TEMPLATE.md` omitted per user guidance).
- Extra script overhead (`scripts/new-step.ps1` omitted, no branch guards added to `scripts/verify.ps1`).

## Plan

1. Create `docs/agents/file-structure.md` with directory conventions and decision table.
2. Update `docs/steps/00-plan-template.md` with branch metadata and commit SHA tracking.
3. Update `BUILD_PROTOCOL.md` with the 10-stage loop and PR strategy.
4. Update `AGENTS.md` with the full resource catalog, skills index, file structure rules, and branching protocol.
5. Synchronize `docs/agents/skills.md` and `README.md`.
6. Run `scripts/verify.ps1` and verify all document cross-references.

## Implementation

- Created `docs/agents/file-structure.md` establishing functional conventions rather than restrictive root allowlists.
- Updated `00-plan-template.md` with fields for Step Branch, Primary Branch, Pull Request URL, first commit SHA, last commit SHA, and merge commit SHA.
- Evolved `BUILD_PROTOCOL.md` to detail the 10-stage loop and `--no-ff` merge protocol.
- Refactored `AGENTS.md` into an authoritative repository resource index covering all 12 local skills, core markdown files, scripts, and precedence rules.

## Discoveries

- The repository currently defaults to `master`. The strategy dynamically prefers `main` with fallback to `master` across all docs and instructions.
- All 12 local skills in `.agents/skills/` are fully accessible and now indexed with one-click direct links in `AGENTS.md`.

## Verification

- `scripts/verify.ps1` executed cleanly.
- Git status confirmed clean and isolated on branch `step/01-agent-governance-and-workflow`.
- All markdown cross-links verified.

## Diff / Checkpoint

- Pull Request URL: [Pending PR creation]
- First commit SHA: 14fa02e (initial implementation)
- Last commit SHA: 14fa02e
- Merge commit SHA: [Pending merge]
- Merge strategy: Standard merge commit (`--no-ff`)

## Unresolved Issues

None.

## Decisions

- Standard merge commits (`--no-ff`) selected to preserve granular history on the primary branch.
- Primary branch convention set to prefer `main`, fallback to `master`.
