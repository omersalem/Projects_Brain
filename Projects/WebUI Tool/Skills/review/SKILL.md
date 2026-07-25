---
name: review
description: Perform a comprehensive engineering review of architecture, code quality, security, performance, maintainability, dependencies, documentation, technical debt, and project structure.
---

# Engineering Review Skill

## Purpose

Perform a complete, objective engineering review of a project without modifying code unless explicitly requested.

---

## Workflow

1. **Read Project Context**: Read the project's `README.md`.
2. **Read Agent Directives**: Read `AGENTS.md`.
3. **Read Engineering Rules**: Read `RULES.md`.
4. **Understand Context**: Understand the project domain and architecture before making assumptions.
5. **Establish Source of Truth (Code)**: Treat the GitHub repository as the single source of truth for source code.
6. **Establish Source of Truth (Knowledge)**: Treat Projects Brain as the single source of truth for project knowledge.
7. **Perform Multi-Dimensional Audit**: Evaluate the project across the following core dimensions:
   * **Architecture**: Structural integrity, modularity, boundary separation, component coupling.
   * **Code Quality**: Readability, complexity, naming consistency, function focus, adherence to clean code rules.
   * **Security**: Secrets exposure, input validation, authentication, authorization, least privilege, dependency vulnerabilities.
   * **Performance**: Bottlenecks, query efficiency, resource lifecycle management, caching opportunities.
   * **Maintainability**: Test coverage, code organization, ease of extension.
   * **Dependencies**: Heavy/outdated packages, unnecessary libraries, licensing risks.
   * **Documentation**: Accuracy, scannability, completeness, documentation-to-code alignment.
   * **Technical Debt**: Legacy workarounds, dead code, anti-patterns, temporary fixes.
   * **Project Structure**: Folder organization, file naming, separation of concerns.

---

## Rules

* **Read-Only Standard**: Never modify source code during a review unless explicitly requested by the user.
* **Empirical Analysis**: Ground all findings in specific file references, line numbers, and verified codebase evidence.

---

## Expected Output

Produce a structured review report containing:

1. **Findings**: Clear summary of observations categorized by review dimension.
2. **Risks**: Security vulnerabilities, performance bottlenecks, or high-risk architectural debt.
3. **Recommendations**: Concrete, prioritized actionable fixes.
4. **Suggested Improvements**: Non-critical enhancement suggestions and maintainability refactorings.
