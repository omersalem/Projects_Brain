# Lessons Learned

This file records important engineering lessons, recurring bug patterns, deployment risks, and operational discoveries across projects.

---

## Recurring Bugs & Anti-Patterns

* **Unhandled Async Promise Rejections**: Unhandled promises or missing `await` statements lead to unhandled rejections and silent failures. *Solution*: Always handle promises with `try/catch` or explicit `.catch()` handlers.
* **Unvalidated External Payloads**: Trusting external API responses without runtime schema validation leads to unexpected runtime null pointer / undefined attribute errors deep in execution paths. *Solution*: Validate all incoming external payloads at the boundary using schema validators.
* **Race Conditions in Concurrent State**: Mutating shared state concurrently without atomic operations or locking causes silent data corruption. *Solution*: Use atomic database operations or explicit concurrency locks.

---

## Security & Configuration Pitfalls

* **Accidental Exposure of Sensitive Defaults**: Default configuration files frequently leak development passwords or API keys if committed to repositories. *Solution*: Use `.env.example` templates with empty placeholders and strictly ignore `.env` files in git.
* **Missing CORS & Security Headers**: Web services deployed without explicit CORS policies or security headers expose applications to cross-origin attacks. *Solution*: Configure strict origin whitelists and mandatory security headers by default.

---

## Performance & Database Discoveries

* **N+1 Query Explosions**: Fetching related entities inside loops causes severe database connection pool exhaustion and slow response times. *Solution*: Use eager loading, join queries, or batching.
* **Missing Indexing on Filtered Columns**: Querying unindexed columns on growing tables degrades database performance linearly over time. *Solution*: Index foreign keys and columns frequently used in `WHERE`, `JOIN`, and `ORDER BY` clauses.

---

## Deployment & Operational Lessons

* **Environment Variable Mismatches**: Discrepancies between local environment variables and production staging environments cause silent runtime startup crashes. *Solution*: Maintain a centralized, validated schema for environment variables required at startup.
* **Unlocked Database Migration Runs**: Running database migrations concurrently across multiple application replicas leads to migration table deadlocks. *Solution*: Run migrations in an isolated pre-deployment job with advisory locking enabled.

---

## Workflow & Agent Guidance

* **Verification Post-Refactoring**: Code changes or refactoring must be empirically verified by running tests and build checks prior to completion. *Solution*: Never assume code correctness based solely on visual inspection.
* **Atomic Commits**: Large, multi-feature commits complicate bisecting and rollback procedures. *Solution*: Break work down into small, single-purpose, atomic commits.

---

## Central Knowledge Graph Links

* **Overview**: [[README]]
* **Directives**: [[AGENTS]]
* **Global Rules**: [[RULES]]
* **Engineering Principles**: [[Engineering Principles]]
