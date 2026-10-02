---
name: kmp-cmp-platform-map
description: Explain Kotlin Multiplatform and Compose Multiplatform targets, source sets, shared UI, expect/actual, native entry points, and iOS interop.
---

# KMP/CMP platform map

Apply `codebase-study-conventions`. Inspect actual `kotlin {}` targets, source-set dependency graph and source dirs, module edges, platform entry points, and relevant build configuration. Distinguish configured, buildable, tested, and released targets. Identify whether shared code includes logic, UI, or both.

Map `expect`/`actual`, interfaces/factories, DI-based platform services, platform-only dependencies, and target limitations. For CMP, trace Android, iOS, desktop, web/wasm and other configured bootstraps, host UI integration, resources, and platform-specific back/window behavior where relevant.

For iOS, document framework/base name, exported modules/dependencies and visibility, Xcode/SPM/CocoaPods integration, Swift call sites if present, and wrappers such as SKIE only when used. For libraries, record target publication metadata and consumer support.

Create target/source-set and entry-point tables under `study/platform/`. Mark unavailable Apple-host builds `not attempted` with the host constraint. If not KMP, state not applicable and stop.
