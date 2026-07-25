# RULES.md

Global engineering rules and guardrails for all AI agents operating within Projects Brain.

---

## General

* **Understand Before Modifying**: Never write or edit code without analyzing context and dependencies first.
* **Prefer Simple Solutions**: Keep implementations simple, straightforward, and maintainable.
* **Preserve Existing Behavior**: Maintain existing functionality and backwards compatibility unless explicitly instructed otherwise.
* **Make Smallest Safe Change**: Focus on minimal, precise, low-risk edits.
* **Never Invent Requirements**: Base changes strictly on verified user requirements and codebase state.

---

## Architecture

* **Respect Existing Architecture**: Adhere strictly to the established system design and boundaries.
* **Reuse Existing Patterns**: Follow pre-existing code conventions, abstractions, and design patterns.
* **Avoid Unnecessary Abstractions**: Do not create speculative wrappers, interfaces, or layers.
* **Avoid Duplicate Logic**: Keep implementations DRY and eliminate redundant code.

---

## Security

* **Never Expose Secrets**: Keep API keys, tokens, passwords, and private keys out of repositories and logs.
* **Never Hardcode Credentials**: Always pass sensitive configurations through secure environment variables or secret stores.
* **Validate Inputs**: Sanitize and validate all external input at boundaries to prevent injection and security flaws.
* **Prefer Secure Defaults**: Default configuration must favor security over convenience.
* **Follow Least Privilege**: Grant minimal permissions necessary for components and agents.
* **Consider Security Impact**: Evaluate potential security risks before applying any modification.

---

## Code Quality

* **Keep Code Readable**: Write clean, self-documenting code with descriptive naming.
* **Remove Dead Code Safely**: Only eliminate unused code when verified safe and non-breaking.
* **Avoid Unnecessary Dependencies**: Prefer lightweight solutions over adding heavy third-party packages.
* **Keep Functions Focused**: Ensure functions do one thing well with single responsibility.
* **Keep Naming Consistent**: Align with existing project naming conventions and casing styles.

---

## Documentation

* **Update on Changes**: Update relevant documentation immediately whenever architecture or behavior changes.
* **Facts Over Assumptions**: Never document working hypotheses or unverified assumptions as facts.
* **Keep Concise**: Write clear, structured, and scannable documentation without filler.

---

## Git

* **Never Rewrite History**: Do not force push or rebase public/shared branches unless explicitly requested.
* **Prefer Small Commits**: Group edits into logical, well-defined, and atomic commits.
* **Preserve Commit History**: Maintain clear, descriptive commit messages for auditability.

---

> When uncertain, choose the safest and simplest solution.

---

## Central Knowledge Graph Links

* **Overview**: [[README]]
* **Agent Directives**: [[AGENTS]]
* **Shared Principles**: [[Engineering Principles]]
* **Lessons Learned**: [[Lessons Learned]]
