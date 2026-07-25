---
name: new
description: Initialize a newly discovered GitHub repository inside Projects Brain by discovering technical metadata, populating README, and creating project skills.
---

# New Project Initialization Skill

## Purpose

Initialize a newly discovered software repository inside Projects Brain by creating its project directory, populating its `README.md`, and provisioning its local `Skills/` structure.

---

## Workflow

1. **Read Project Context**: Read the project's `README.md` (or template if newly created).
2. **Read Agent Directives**: Read `AGENTS.md`.
3. **Read Engineering Rules**: Read `RULES.md`.
4. **Understand Context**: Understand the project domain and architecture before making assumptions.
5. **Establish Source of Truth (Code)**: Treat the GitHub repository as the single source of truth for source code.
6. **Establish Source of Truth (Knowledge)**: Treat Projects Brain as the single source of truth for project knowledge.
7. **Analyze Repository Artifacts**: Inspect root files, package manifests, configs, and directory layout.
8. **Detect Technical Elements**:
   * Detect programming languages and runtimes.
   * Detect frameworks and libraries.
   * Detect architecture patterns and component structures.
   * Detect infrastructure, cloud providers, and containerization.
   * Detect deployment methods and CI/CD pipelines.
   * Detect existing documentation and entry points.
9. **Populate Project Knowledge**: Initialize or update `Projects/<Project_Name>/README.md` using the standard project template.
10. **Provision Project Skills**: Ensure the project has its dedicated `Skills/` folder containing `feature/`, `fix/`, `review/`, and `new/`.

---

## Strict Synchronization Rules

* **Never Copy Source Code**: Source code files must never be copied into Projects Brain.
* **Never Modify Repository**: Never edit, commit, push, or delete files in the source GitHub repository during knowledge initialization.
* **No Code Generation**: Only create knowledge documentation inside Projects Brain.

---

## Expected Output

* Initialized project directory inside `Projects/<Project_Name>/`.
* Fully populated project `README.md` with detected technical stack and repository metadata.
* Provisioned project `Skills/` directory containing `feature/`, `fix/`, `review/`, and `new/` skills.
