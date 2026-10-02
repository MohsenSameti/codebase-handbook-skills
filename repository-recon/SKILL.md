---
name: repository-recon
description: Classify a Kotlin/Android repository, establish its exact snapshot and scope, and inventory roots, modules, targets, and special cases before deeper study.
---

# Repository reconnaissance

Inspect repository instructions/docs and identify root and checkout. Apply `codebase-study-conventions`.

1. Capture source SHA, timestamp, branch, and clean/dirty state before reading deeply.
2. Inventory `settings.gradle[.kts]` roots, modules, version catalogs, convention plugins, `buildSrc`/`build-logic`, submodules, worktrees, CI, and relevant source roots. Exclude generated/vendor/cache trees and duplicate worktrees from counts. Check whether the root project itself is an app.
3. Classify from evidence; types can compound: Android app (Compose or legacy Views/Java), KMP shared-logic app, CMP app, Android/Kotlin library, KMP library, Gradle/lint plugin, tutorial/sample collection, multi-app monorepo, multiple independent Gradle roots, native-engine shell, fork/submodule-heavy repo, docs-only repo, or another Kotlin target.
4. Do not call a repo Android-less based on one grep. Inspect plugin aliases/catalogs, convention plugins, Groovy and Kotlin DSL, root and module build files. Separate configured targets from buildable/released targets.
5. Declare scope/exclusions and coverage budget. For collections, index independent roots and select scoped children rather than inventing a global module graph.
6. Write/update reconnaissance in `docs/codebase/` or the established docs location.

Report repo kind (including qualifiers), scope, source baseline, root/module/target inventory, scale budget, constraints, evidence, and one recommended next study phase. Do not write detailed feature or architecture docs in this pass.
