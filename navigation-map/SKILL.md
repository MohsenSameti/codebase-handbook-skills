---
name: navigation-map
description: Document app destinations, routes, deep links, entry points, and platform-specific navigation paths from implementation evidence.
---

# Navigation map

Apply `codebase-study-conventions`. Locate actual routing via manifests, route declarations, navigation graphs, and call sites; do not assume a particular framework. Trace start destinations, route IDs/arguments, nesting, deep links/external intents, and platform host entry points. Record back behavior only when verified.

Use a compact table: destination/route, how reached, arguments/deep links, owning module, evidence, confidence. Distinguish declared from reachable routes if reachability is not proven. For CMP, separate common route definitions from platform host behavior; for legacy Views, use Activity/Fragment/Intent vocabulary. For non-app repos, mark screen navigation not applicable with reason and map API/CLI entry surface instead.

Write under `study/navigation/`, link from project map, and list unresolved behavior as Open Questions.
