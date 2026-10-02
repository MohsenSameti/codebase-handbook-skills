# Conditional repository profiles

Load only the profile relevant to the repo scope; profiles may compound. Do not generate every section by default.

## Product apps
Map entry points, variants, navigation, UI/state, data, background work, permissions, tests and design resources. Legacy Java/XML uses Activities/Fragments, layouts, intents and its actual state mechanism, not Compose assumptions.

## KMP/CMP apps
Establish targets and source-set graph. For logic-sharing apps map shared logic and native UIs. For CMP map shared UI plus Android/iOS/desktop/web bootstraps, target-specific behavior/resources and actual tested/running targets.

## Android/Kotlin libraries and SDKs
Replace screen map with public API and consumer journey; include coordinates, visibility/API checks, compatibility/versioning evidence, platform/target support, publishing, samples and tests. Omit app lifecycle sections unless a sample app is in scope.

## Multiplatform libraries
Add common/intermediate/platform API split, source-set hierarchy, framework/export settings and target-specific behavior. Separate configured targets from published artifacts.

## Gradle/build/lint plugins
Map plugin IDs, extension DSL, conventions, registered tasks/rules, lifecycle hooks, inputs/outputs, fixtures and sample consumers. No screen/data docs unless a separate app exists.

## Tutorials and sample collections
Create a root index of independent examples and their purpose. Study selected demos individually; do not imply they share one architecture if examples intentionally differ.

## Multi-app and multi-root repos
Distinguish one Gradle build with several apps from many independent Gradle roots. Map shared code and app deltas for the former; index roots and scope a child project for the latter. Never invent one global module graph across separate builds.

## Bundled native engine/shell
Focus on Kotlin-to-engine boundaries (JNI/CLI/IPC), bundled artifacts, lifecycle, configuration and exposed APIs. Treat unrelated shell UI as out of scope unless requested.

## Forks, submodules, generated/vendor code
Record upstream/fork point and delta only with evidence. State whether submodules are initialized/in scope. Exclude generated/vendor code from normal counts; study only if it defines the product boundary.

## Docs-only/non-Gradle repo
Do not force Android/Gradle sections. Identify actual executable/API entry surface, tooling, content structure and missing evidence; stop if the template assumptions do not fit.
