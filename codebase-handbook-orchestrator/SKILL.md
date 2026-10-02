---
name: codebase-handbook-orchestrator
description: Coordinate specialist skills to create or update an evidence-backed Android/Kotlin project handbook inside the repository and track its source baseline.
---

# Codebase handbook orchestration

Use for whole-repository understanding or handbook refresh. Specialists remain independently invocable. Apply `codebase-study-conventions` and `repository-recon` first, then select relevant specialists. Read `references/repo-types.md` only as needed for unusual or compound repo types.

## Initial generation
1. Inspect repo instructions and existing docs. Never replace root `AGENTS.md`. Default to tracked `docs/codebase/`, adapting to established conventions and avoiding conflicts.
2. Capture source SHA, timestamp, branch, and clean/dirty status before analysis. Record changed/untracked paths when dirty.
3. Recon repo kind, scope/exclusions, targets and coverage budget.
4. Create minimal landing docs: `START-HERE.md`, `APP-MAP.md` or `PROJECT-MAP.md`, `STUDY-STATE.md`.
5. Tier 1: build/release, modules/architecture, entry paths. Then one representative feature or public API. Add navigation, KMP/CMP, data/background, testing/quality, library/publishing, plugin/sample docs only when applicable.
6. Keep first pass useful, not exhaustive. For collections, create a root index and scoped child studies. Adapt or omit irrelevant app sections.
7. Check evidence, confidence, placeholders, scope limits, open questions, freshness and one next action. Report exactly what changed and which commands ran.

## Refresh
Compare documented evidence with the saved source baseline. Revisit only changed/stale evidence plus requested scope; preserve valid findings, update the new source snapshot/state, and keep the docs commit separate. Do not regenerate blindly or modify app/build code during a documentation pass.
