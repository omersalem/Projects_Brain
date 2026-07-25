# Projects Brain

Projects Brain is a lightweight, platform-independent AI knowledge system designed to understand, document, and manage software projects. It serves as an architectural memory bank and operational guide for AI coding agents, enabling seamless context sharing, rapid project onboarding, and safe, consistent code modifications.

This knowledge base works across all major AI coding tools—including ChatGPT, Codex, Claude Code, OpenCode, Antigravity, and future AI agents—without vendor lock-in or dependency on any single provider ecosystem.

---

## Core Philosophy

* **Maximum Simplicity**: Keep structure clean and minimal. Avoid unnecessary nested directories or excessive hierarchy.
* **Zero Duplication**: Ensure every piece of information lives in one place with a clear target purpose.
* **No Over-Engineering**: Avoid complex custom tooling or overhead; focus on lean, human-readable, and machine-actionable Markdown files.
* **Platform Independence**: The knowledge structure remains entirely decoupled from any specific AI platform or vendor toolchain.
* **Long-Term Maintainability**: Built to endure and remain effortless to maintain across many years and changing agent models.

---

## Design Goals

Projects Brain helps AI coding agents:
1. **Understand Projects Quickly**: Get instant context on project goals, domain rules, and system state.
2. **Navigate Repositories**: Easily locate key modules, entry points, and component boundaries.
3. **Understand Architecture & Tech Stack**: Grasp structural design, dependencies, and framework choices.
4. **Understand Project Status**: Clear insight into current milestones, active tasks, and recent updates.
5. **Understand Engineering Decisions**: Access architectural decision records (ADRs) and rationale behind technical choices.
6. **Modify Code Safely**: Understand constraints, guardrails, and testing expectations before touching code.
7. **Reduce Repeated Explanations**: Stop re-explaining background context, conventions, and business logic to AI agents.

---

## Structure & Folder Descriptions

The structure of Projects Brain is deliberately constrained to the following root layout:

* **`README.md`**: Overview of the Projects Brain system, core philosophy, structure, and operational rules.
* **`AGENTS.md`**: Operational guidelines, capabilities, and workflows for AI agents operating within the system.
* **`RULES.md`**: Global engineering standards, design constraints, and quality guardrails.
* **`Projects/`**: Dedicated subdirectories containing knowledge bases, architecture maps, and state records for individual software projects.
* **`Shared/`**: Common technical specifications, reusable domain patterns, cross-cutting architectural standards, and shared protocols.
* **`Skills/`**: Modular, reusable procedural capabilities and workflows that AI agents can execute across projects.

---

## Relationship with GitHub Repositories

* **Source Code**: GitHub repositories remain the single source of truth for all application source code, configuration files, and implementation details.
* **Project Knowledge**: Projects Brain is the single source of truth for project context, architectural decisions, domain concepts, and project-level knowledge.
* **Zero Code Duplication**: Source code is **never copied** into Projects Brain. Instead, high-level knowledge, architectural summaries, component interfaces, and decision rationales are extracted from repositories and systematically organized within the Brain.

---

## Central Knowledge Graph

* **Operational Directives**: [[AGENTS]]
* **Global Guardrails**: [[RULES]]
* **Reusable Knowledge**: [[Engineering Principles]] | [[Lessons Learned]]
* **Global Sync Skill**: [[Skills/github-project-sync/SKILL]]
