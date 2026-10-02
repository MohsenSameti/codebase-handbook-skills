---
name: build-and-release-map
description: Document how an Android/Kotlin Gradle project is configured, built, tested, packaged, published, and released, including variants and blockers.
---

# Build and release map

Apply `codebase-study-conventions`. Inspect settings/root/module build files, wrapper properties, catalogs, convention plugins, CI, publishing/signing scripts, and project build docs. Search first; inspect focused files.

Record toolchain versions from source, prerequisites, exact build/test/run/package/publish commands, relevant variants/flavors, target constraints, centralized build logic, CI triggers/matrices/artifacts, release/versioning, publication destinations, and signing requirements (never secret values). For libraries, include coordinates and artifact/variant metadata when discoverable. Separate root tasks from module tasks.

State build verdict exactly as `builds`, `does not build`, or `not attempted`, with command/environment/blocker. Missing SDK, network, credentials, or Apple host is a constraint, not proof of a source defect. Do not claim execution if it did not happen.

Write a focused doc such as `study/architecture/build-and-release.md`, link it from the map/state, and list unknowns as Open Questions. Never run publish, release, signing, or deployment tasks without explicit authorization.
