---
name: data-and-background-work
description: Map network and persistence flows, repositories, caches, errors, concurrency, jobs, services, push, and work outside the UI.
---

# Data and background work

Apply `codebase-study-conventions`. Trace implemented paths: clients/endpoints, serialization, repository/data-source boundaries, databases/preferences/files, cache behavior, data mapping, error handling, concurrency/dispatchers, and ownership/lifecycle. Cite symbols/configuration; do not expose secrets.

For Android, search WorkManager, services, receivers, alarms, foreground work, push, notifications, widgets, and startup scheduling. Record trigger, constraints, retry/persistence, unique work IDs, cancellation, and manifest/permission wiring only when evidenced. For KMP, separate common abstractions from platform implementations.

Write representative path diagrams/tables and topic docs such as `study/architecture/data-layer.md` and `background-work.md`; cross-link feature studies. Confirmed absence must name inspected locations/terms; otherwise use TODO/Open. Do not turn this into a security review or redesign unless asked.
