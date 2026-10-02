---
name: feature-trace
description: Trace one Android/Kotlin app feature end to end from entry point through UI/state, domain, repository, and data source with evidence.
---

# Feature trace

Apply `codebase-study-conventions`. Trace only the selected feature: real entry/route → UI or API surface → state/controller → domain/use case if present → repository → data source, stopping about one layer past the repository when the pattern is clear. Search symbols first; inspect focused windows.

Document purpose/trigger, files/symbols, route, state/events and transformations, data dependencies, verified loading/error/empty behavior, navigation/system interactions, tests, and gaps. Do not invent a use-case layer or infer product intent from names. For each factual claim cite evidence and certainty.

Create one file per feature under `study/features/`; update the index and state. Do not study multiple features unless asked. After two or three traces, capture shared patterns separately. For a library/plugin, trace one representative public API call from consumer entry to implementation.
