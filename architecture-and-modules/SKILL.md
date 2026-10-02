---
name: architecture-and-modules
description: Map a repository’s modules, startup/consumer entry points, actual architecture layers, dependency injection, and call directions with code evidence.
---

# Architecture and modules

Apply `codebase-study-conventions`. Inspect Gradle inclusion/dependencies, plugin aliases/conventions, manifests and entry points, DI registrations, and representative cross-module call sites. Do not impose MVVM, clean architecture, or UI/data/domain layers if the code does not use them.

Deliver a module/component graph with evidenced roles and dependency directions; actual startup or consumer/integration path; real layers and call direction; DI/service-locator/manual construction approach and registrations; shared build logic and notable boundaries. Names alone do not prove purpose.

For a library/plugin, map the consumer path and public boundaries instead of app startup. For multi-root collections, map roots separately. Keep the landing map concise and put detail in `study/architecture/modules.md` and `layers.md` (or equivalent). Report unclear edges as Open Questions, not quality judgments.
