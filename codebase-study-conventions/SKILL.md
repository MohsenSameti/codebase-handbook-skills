---
name: codebase-study-conventions
description: Apply evidence, confidence, freshness, scope, and output-location rules whenever documenting or updating an Android, Kotlin Multiplatform, library, or tooling repository.
---

# Shared study rules

Use these rules for every handbook. Inspect existing repo guidance first. Default output to `docs/codebase/`; adapt to established conventions and avoid overwriting existing content or root `AGENTS.md`.

- Capture source commit SHA, timestamp, branch, and clean/dirty status before analysis. If dirty, record relevant modified/untracked paths and distinguish those findings from committed code. The source baseline and later docs commit are separate facts.
- Cite file paths plus line ranges or symbols. Mark claims `Confirmed` only with direct evidence, `Inferred` with basis and a confirming check, or `Open`. Distinguish `TODO(study)`, checked `none found` (say where checked), and `n/a` (give reason). Remove all unfilled placeholders from finished docs.
- Describe what exists, not what should exist, unless asked for a review. Declare scope, exclusions, platform/module coverage, and a budget for large repos. Never imply exhaustive coverage after a sample.
- Documentation-only by default. Do not modify application/build code, run publish/deploy/signing commands, or expose secrets. Record commands actually executed and their environment.

Suggested landing files: `START-HERE.md`, `APP-MAP.md` (or `PROJECT-MAP.md` for non-apps), `STUDY-STATE.md`, plus topic docs under `study/`. Adapt, omit, or add sections based on repo type.
