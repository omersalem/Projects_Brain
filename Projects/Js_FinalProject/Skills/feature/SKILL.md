---
name: feature
description: Safely design and implement a new feature while preserving architectural consistency and updating project documentation.
---

# Feature Implementation Skill

## Purpose

Safely implement a new feature in the project while maintaining architectural integrity and project knowledge.

---

## Workflow

1. **Read Project Context**: Read the project's `README.md`.
2. **Read Agent Directives**: Read `AGENTS.md`.
3. **Read Engineering Rules**: Read `RULES.md`.
4. **Understand Context**: Understand the project domain and architecture before making assumptions.
5. **Establish Source of Truth (Code)**: Treat the GitHub repository as the single source of truth for source code.
6. **Establish Source of Truth (Knowledge)**: Treat Projects Brain as the single source of truth for project knowledge.
7. **Analyze Existing Architecture**: Inspect repository entry points, module boundaries, and data flows.
8. **Understand Requested Feature**: Clarify user requirements and feature boundaries.
9. **Reuse Patterns**: Leverage existing code conventions, design patterns, and utility functions.
10. **Design Smallest Safe Implementation**: Formulate a minimal, low-risk implementation plan.
11. **Preserve Consistency**: Ensure architectural boundaries and coding standards are maintained.
12. **Avoid Unnecessary Dependencies**: Use native platform/language features where possible without adding heavy third-party packages.
13. **Implement Feature**: Execute the code edits safely and test functionality.
14. **Update Project Knowledge**: Update the project `README.md` if system architecture or behavior changed.
15. **Update Shared Knowledge**: Update `Shared/Engineering Principles.md` only if a new, reusable engineering pattern was discovered.

---

## Rules

* Never introduce breaking changes without explicit user approval.
* Never copy source code into Projects Brain.
* Keep changes atomic, well-scoped, and verified.

---

## Expected Output

* Clean, working feature implementation in the target codebase.
* Verified tests/build status.
* Updated project `README.md` (if architectural changes occurred).

---

## System Navigation

* **Project Hub**: [[README]]
* **Global Core**: [[AGENTS]] | [[RULES]]
* **Continuous Knowledge**: [[Engineering Principles]] | [[Lessons Learned]]
