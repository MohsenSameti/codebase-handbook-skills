---
name: library-api-surface
description: Document a Kotlin/Android library’s public API, consumer path, compatibility surface, publication coordinates, samples, and multiplatform targets.
---

# Library API surface

Apply `codebase-study-conventions`. Identify plugin/module type, public packages/declarations, visibility, API validation files/tasks (for example binary API dumps), annotations/nullability, extension points, generated APIs, and representative consumer entry point. Separate documented public API from implementation and trace one public call.

Record coordinates/versioning, publication repositories/tasks, artifact types, sources/docs, POM/module metadata, signing requirements (no secret values), supported targets/minimum platform versions, and compatibility checks when discoverable. Link samples, demo apps, fixtures, and tests. For KMP, distinguish common and target-specific surfaces and behavior differences.

For Gradle/lint plugins, focus on plugin IDs, configuration DSL, registered tasks/rules, and test fixtures. Avoid claiming compatibility guarantees unless enforced by source or release policy. Do not execute publish/sign/release tasks. Write an API index and integration/publishing map under the codebase docs.
