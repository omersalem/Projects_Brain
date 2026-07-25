# AGENTS.md

Welcome to Projects Brain. This document is the primary entry point for any AI coding agent operating within this knowledge base.

---

## Purpose

Projects Brain exists to provide AI agents with immediate, reliable project context, architectural maps, and engineering background before any code is modified.

* **Projects Brain** is the single source of truth for **project knowledge, context, and decisions**.
* **GitHub Repositories** are the single source of truth for **source code, configuration, and implementation**.
* **Separation of Concerns**: Never confuse these two responsibilities. Source code must never be copied into Projects Brain, and non-code knowledge should reside here.

---

## Agent Responsibilities

When interacting with any project governed by Projects Brain, every AI agent must:

1. **Understand Before Modifying**: Fully read and analyze relevant documentation and codebase context prior to making changes.
2. **Read Existing Documentation**: Consult existing records first rather than making unverified assumptions.
3. **Prefer Existing Patterns**: Follow pre-existing architectural conventions, coding styles, and project patterns.
4. **Preserve Architectural Consistency**: Maintain system integrity and structural design across all modifications.
5. **Keep Documentation Synchronized**: Update Projects Brain whenever meaningful engineering decisions, architectural changes, or state updates occur.
6. **Prefer Small, Safe, Incremental Changes**: Implement concise, well-scoped, and low-risk edits.
7. **Avoid Unnecessary Complexity**: Keep solutions as simple as possible without over-engineering.
8. **Protect Existing Functionality**: Verify that new edits do not break existing features or introduce regressions.
9. **Improve Maintainability**: Strive to enhance readability, structure, and long-term maintainability whenever possible.

---

## Working Principles

All AI agents must adhere to the following core operational principles:

* **Never Duplicate Knowledge**: Keep every factual detail in its single designated location.
* **Never Invent Project Facts**: Rely strictly on verified codebase artifacts and documented history.
* **Never Fabricate Missing Documentation**: If context is missing, investigate the codebase or ask for clarification.
* **Distinguish Facts from Assumptions**: Explicitly separate verified codebase state from working hypotheses.
* **Ask for Clarification**: Pause and seek user input whenever requirements or designs are ambiguous.
* **Respect Project Conventions**: Follow project-specific rules, linters, and architectural boundaries.
* **Prioritize Quality Over Speed**: Value security, correctness, and long-term maintainability above rapid implementation.

---

## Project Workflow

For every task across any project, execute the following step-by-step workflow:

1. **Read Project Documentation**: Review the project's knowledge entry in Projects Brain.
2. **Understand the Repository**: Inspect the relevant repository files and structural layout.
3. **Identify the Requested Change**: Clarify the explicit goal and scope of the task.
4. **Evaluate the Impact**: Trace dependencies and assess potential side effects across the system.
5. **Implement Smallest Safe Solution**: Make minimal, precise, and verified changes.
6. **Update Documentation**: Synchronize Projects Brain if the change affects architecture, decisions, or project status.

---

## Knowledge Rules

### What Projects Brain Stores
* High-level project knowledge and domain context
* System architecture maps and component interactions
* Key engineering decisions (ADRs) and design rationale
* Reusable technical standards and patterns
* Active project status, milestones, and state updates

### What Projects Brain Does NOT Store
* Source code files (`.ts`, `.py`, `.go`, `.cs`, etc.)
* Build artifacts and compiled outputs
* Dependency packages (`node_modules`, `vendor`, etc.)
* Generated files, logs, or temporary outputs
* Executables and binary files

---

## Documentation Style

All documentation created or modified within Projects Brain must adhere to the following style:

* **Short & Factual**: Clear, direct statements without filler or speculation.
* **Structured**: Standardized Markdown layouts using clear headings and bullet points.
* **Reusable**: Written so both human engineers and AI agents can digest and reuse information easily.
* **AI- & Human-Friendly**: Scannable, unambiguous, and cleanly formatted.
* **No Long Essays**: Avoid verbose prose; present context efficiently.
* **No Redundancy**: Omit duplicated information and eliminate unnecessary documentation.
