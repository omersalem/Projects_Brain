# Engineering Principles

This file stores long-term, reusable engineering knowledge, design patterns, and quality standards applicable across all software projects managed within Projects Brain.

---

## Architecture Principles

* **Decoupled System Boundaries**: Design components with clear boundaries, minimal direct dependencies, and explicit API contracts.
* **Single Responsibility**: Every module, class, or service should have one focused purpose and one reason to change.
* **High Cohesion & Low Coupling**: Group related capabilities together while minimizing inter-module dependencies.
* **Interface-Driven Design**: Rely on abstractions and stable interface contracts rather than concrete implementations.
* **Statelessness Where Feasible**: Prefer stateless services and components to simplify scaling, testing, and deployment.

---

## Coding & Implementation Standards

* **Readability Over Cleverness**: Write clear, simple code that is easy for humans and AI agents to comprehend.
* **Defensive Boundary Validation**: Validate all inputs, parameters, and external payload schemas at system boundaries.
* **Explicit Error Handling**: Handle errors explicitly at appropriate levels; avoid swallowing exceptions silently or returning ambiguous fallback states.
* **Consistent Naming**: Adhere strictly to project domain terminology and consistent casing conventions across codebases.
* **Minimal Dependencies**: Prefer lean native capabilities or lightweight libraries over adding large, unverified third-party packages.

---

## Security Principles

* **Secure Defaults**: All configurations, endpoints, and credentials must default to the most restrictive secure setting.
* **Least Privilege**: Grant components, service accounts, and users only the minimal permissions needed to perform their tasks.
* **Secrets Isolation**: Never hardcode credentials, API keys, or tokens; manage them strictly through environment variables or secret vaults.
* **Defense in Depth**: Layer security controls across input validation, authentication, authorization, and data encryption.

---

## Performance & Resource Management

* **Measure Before Optimizing**: Base performance tuning on empirical profiling metrics rather than premature assumptions.
* **Resource Cleanup**: Ensure open connections, file handles, memory allocations, and worker threads are deterministically closed.
* **Database Efficiency**: Prevent N+1 queries, index frequently queried fields, and fetch only required columns.

---

## Documentation & Knowledge Transfer

* **Single Source of Truth**: Store every technical fact in one authoritative location to prevent drift.
* **Factual & Scannable**: Document empirical state and concrete decisions cleanly using Markdown bullet points and headers.
* **Keep Docs Synchronized**: Update documentation concurrently whenever system behavior or architecture evolves.
