---
name: quality-and-test-map
description: Map tests, CI quality gates, utilities, error/logging conventions, and design-system assets for Android and Kotlin projects.
---

# Quality, tests, utilities, and design system

Apply `codebase-study-conventions`. Inventory test source sets/frameworks, unit/integration/UI/screenshot/device/contract tests, fakes/fixtures, and exact run commands. Link tests to modules/features. Read CI to distinguish tests present from tests automatically run; a test directory is not evidence of coverage. Record configured gates only.

Map cross-cutting utilities that aid code understanding: logging, errors/results, dispatcher/threading helpers, serialization/configuration, permissions/platform abstractions. For UI apps, map themes, tokens, components, resources, previews/catalog and usage. For libraries/plugins, substitute reusable utilities, samples, and plugin test harnesses. Mark non-app topics not applicable with a reason.

Write focused docs under `study/architecture/testing.md`, `study/utilities/`, and applicable design-system topic. Avoid unsupported claims such as “well tested.” Do not run expensive tests unless asked; record command and environment if run.
