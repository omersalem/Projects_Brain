---
name: fix
description: Safely diagnose, reproduce, and resolve bugs while minimizing side effects and capturing reusable engineering lessons.
---

# Bug Fix Skill

## Purpose

Safely fix bugs in the codebase, preserve existing functionality, and capture reusable lessons.

---

## Workflow

1. **Read Project Context**: Read the project's `README.md`.
2. **Read Agent Directives**: Read `AGENTS.md`.
3. **Read Engineering Rules**: Read `RULES.md`.
4. **Understand Context**: Understand the project domain and architecture before making assumptions.
5. **Establish Source of Truth (Code)**: Treat the GitHub repository as the single source of truth for source code.
6. **Establish Source of Truth (Knowledge)**: Treat Projects Brain as the single source of truth for project knowledge.
7. **Understand the Bug**: Analyze the error report, stack trace, or failing behavior.
8. **Reproduce Bug**: Reproduce the issue using test cases or minimal reproduction steps whenever possible.
9. **Find Root Cause**: Trace data flow and execution path to isolate the underlying root cause.
10. **Fix Root Cause**: Apply a precise fix addressing the core issue rather than masking symptoms.
11. **Preserve Existing Behavior**: Ensure adjacent functionality and existing tests remain unbroken.
12. **Minimize Side Effects**: Keep edits targeted to prevent unintended regressions.
13. **Update Project Documentation**: Update project documentation if behavior or configuration requirements changed.
14. **Update Lessons Learned**: Update `Shared/Lessons Learned.md` only if the lesson or bug pattern is reusable across projects.

---

## Rules

* Never swallow exceptions or mask symptoms with empty fallbacks.
* Base diagnosis strictly on empirical log evidence and root cause analysis.
* Never delete failing tests to claim success.

---

## Expected Output

* Verified bug fix in the codebase.
* Passing tests and build check.
* Updated `Shared/Lessons Learned.md` entry if a generalizable lesson was discovered.
