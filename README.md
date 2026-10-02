# Codebase Handbook Skills

A modular set of agent skills for understanding and documenting Android, Kotlin, Kotlin Multiplatform (KMP), Compose Multiplatform (CMP), and related repositories.

The skills turn a codebase into an evidence-backed handbook **inside that codebase**. Use the orchestrator for a complete first-pass handbook or refresh, or call any specialist on its own for a focused study. Repo-specific guidance is loaded only when it applies, so library, tooling, sample-collection, and mixed repositories do not get forced into an app-shaped template.

## What the skills produce

A compact, tracked documentation area, normally `docs/codebase/`, adapted to the repository's existing conventions. It typically contains:

- `START-HERE.md`: repository type, scope, included/excluded areas, and the exact source snapshot studied.
- `APP-MAP.md` or `PROJECT-MAP.md`: quick orientation, entry points, and links to deeper notes.
- `STUDY-STATE.md`: coverage, unresolved questions, freshness, and the next study action.
- Focused studies under `study/`: build and release, modules and architecture, navigation, feature/API traces, data and background work, KMP/CMP platform boundaries, library APIs, tests, utilities, or design system details as applicable.

These are not prescriptive architecture documents or code reviews. They describe what the repository actually contains, cite evidence, distinguish confirmed facts from inferences, and say what was not studied.

## Skills in this collection

| Skill | Use it to... |
|---|---|
| [`codebase-handbook-orchestrator`](codebase-handbook-orchestrator/SKILL.md) | Generate or refresh a whole repository handbook and coordinate the relevant specialists. |
| [`codebase-study-conventions`](codebase-study-conventions/SKILL.md) | Apply shared evidence, confidence, scope, freshness, and output-location rules to any study. |
| [`repository-recon`](repository-recon/SKILL.md) | Identify repository type, source snapshot, Gradle roots, modules, targets, and study scope. |
| [`build-and-release-map`](build-and-release-map/SKILL.md) | Document toolchains, build/test/package commands, CI, variants, publishing, and release paths. |
| [`architecture-and-modules`](architecture-and-modules/SKILL.md) | Map modules, startup or consumer paths, architecture boundaries, dependency injection, and call direction. |
| [`navigation-map`](navigation-map/SKILL.md) | Trace app destinations, routes, deep links, and platform-specific navigation. |
| [`feature-trace`](feature-trace/SKILL.md) | Follow one feature from its entry point through UI/state and data dependencies. |
| [`data-and-background-work`](data-and-background-work/SKILL.md) | Map persistence, networking, repositories, concurrency, jobs, services, and push/background work. |
| [`kmp-cmp-platform-map`](kmp-cmp-platform-map/SKILL.md) | Explain targets, source sets, shared UI/logic, platform entry points, and iOS interop. |
| [`library-api-surface`](library-api-surface/SKILL.md) | Document library/plugin APIs, consumer integration, compatibility evidence, targets, and publishing. |
| [`quality-and-test-map`](quality-and-test-map/SKILL.md) | Map tests, CI quality gates, utilities, logging/error patterns, and applicable UI design resources. |

Each specialist is independently usable. When available in the agent, the orchestrator loads the shared conventions and repository reconnaissance first, then chooses only the relevant specialists. The orchestrator's [repo-type reference](codebase-handbook-orchestrator/references/repo-types.md) covers Android/legacy apps, KMP/CMP apps and libraries, Gradle/lint plugins, tutorials, multi-app and multi-root repositories, native-engine shells, forks, and non-Gradle projects.

## Quick start

1. Install the skill directories in a skill location supported by your coding agent. For example, some agents discover project skills under `.agents/skills/` or `.claude/skills/`; confirm the correct path for your agent and version.
2. Open the project repository you want to study in that agent.
3. Ask: **â€œUse `codebase-handbook-orchestrator` to create a first-pass handbook for this repository.â€**
4. Review the generated docs and commit them with your normal project workflow.

For a focused task, ask for a single skill, for example: **â€œUse `feature-trace` to document the sign-in flowâ€** or **â€œUse `library-api-surface` to map this library's public API and publication setup.â€**

## Source snapshot and later updates

Before studying, the skills record the **source** commit SHA, branch, timestamp, and whether the working tree is clean. If it is dirty, relevant modified and untracked paths are recorded so the handbook does not imply those changes were part of the commit.

That source baseline is different from the later commit that adds or updates the handbook. On refresh, the agent compares the current source with the recorded baseline, rechecks claims whose evidence may have changed, preserves still-valid findings, and updates the baseline. This makes the docs maintainable without blindly regenerating them.

## Safety and scope

The default workflow writes documentation only. It does not change application or build code, publish artifacts, sign releases, deploy, or run destructive commands. Builds and tests are run only when appropriate and available; the result is reported honestly as executed, failed, or not attempted, including relevant environment limits. Publishing, signing, deployment, or other side-effecting actions require explicit authorization.

For large repositories, the handbook declares a coverage budget and explicitly marks areas that were not studied. A checked absence is distinguished from an unknown or not-yet-studied area. The output is an orientation map with evidence, not a claim of exhaustive coverage.

## Portability

Each skill is a directory with a `SKILL.md` file and standard YAML frontmatter. The bundle avoids agent-specific tool names and assumes the coding agent can inspect and write files in the open repository. Installation paths, automatic invocation, and reference-loading behavior vary by agent, so check its documentation if a skill is not discovered or loaded.

## License
MIT. See [LICENSE](./LICENSE).
