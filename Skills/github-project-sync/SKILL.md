---
name: github-project-sync
description: Scans GitHub repositories to extract, synchronize, and update project knowledge inside Projects Brain without copying source code.
---

# GitHub Project Sync

The `github-project-sync` skill enables AI coding agents to analyze one or more target software repositories and extract structured, factual engineering context into Projects Brain.

---

## Core Operational Principles

1. **Separation of Code and Knowledge**: GitHub repositories remain the sole source of truth for source code. Projects Brain remains the sole source of truth for project knowledge.
2. **Zero Code Duplication**: Source code files (`.ts`, `.py`, `.go`, `.cs`, etc.) must **never** be copied into Projects Brain. Only architectural context, technical stack details, and state metrics are extracted.
3. **Factual Integrity**: Document strictly what is verified from codebase inspection. Mark any unverified or missing detail explicitly as `Unknown`. Never invent facts or make unverified assumptions.

---

## Synchronization Workflow

When executing this skill for a target repository:

### Step 1: Repository Inspection & Discovery
Inspect the repository root, directory structure, configuration files, and manifests (e.g., `package.json`, `pyproject.toml`, `Cargo.toml`, `go.mod`, `pom.xml`, `Dockerfile`, `.github/workflows/`, `docker-compose.yml`) to identify:

* **Project Type**: (e.g., Monorepo, Microservice, Web Application, CLI, Library, API)
* **Main Technologies**: Core languages, frameworks, and runtime environments
* **Programming Languages**: All primary and secondary languages detected
* **Frameworks**: Web, application, or utility frameworks
* **Databases**: Relational, NoSQL, or vector databases (e.g., PostgreSQL, Redis, MongoDB)
* **Cloud Providers**: (e.g., AWS, GCP, Azure, Vercel, Cloudflare)
* **Infrastructure**: (e.g., Terraform, Kubernetes, Helm, Serverless)
* **Deployment Methods**: Containerized, serverless, static hosting, or VM-based
* **Package Managers**: (e.g., npm, pnpm, yarn, pip, poetry, cargo, go modules)
* **Testing Frameworks**: (e.g., Jest, pytest, Vitest, JUnit, Go testing)
* **CI/CD Pipelines**: (e.g., GitHub Actions, GitLab CI, CircleCI)
* **Docker / Containerization**: Multi-stage builds, compose files, container registers
* **Environment Configuration**: `.env.example`, secret manager integrations, config files
* **Authentication Methods**: (e.g., OAuth2, JWT, Session, API Keys, OIDC)
* **Storage Systems**: Object storage, block storage, local caching, or S3 buckets
* **Architecture Patterns**: (e.g., Hexagonal, MVC, Event-Driven, Microservices, Layered)
* **Major External Services**: Third-party APIs, payment gateways, messaging services (e.g., Stripe, Auth0, Twilio)
* **Existing Documentation**: Primary entry points, `README.md`, architectural diagrams, API specs

### Step 2: Knowledge Extraction & Project Initialization
1. Determine the target folder inside `Projects/<Project_Name>/`.
2. If `Projects/<Project_Name>/README.md` does not exist:
   * Copy the template from `Projects/_Project Template/README.md`.
   * Populate the section headers using factual details extracted in Step 1.

### Step 3: Incremental Synchronization & Note Preservation
If `Projects/<Project_Name>/README.md` already exists:
* **Preserve Manual Notes**: Do not overwrite user-written commentary, custom notes, or manually authored decisions under any section.
* **Update Factual Sections**: Update factual fields (Technologies, Repository paths, Dependencies, CI/CD, etc.) based on new repository findings.
* **Append New Discoveries**: Add newly detected frameworks, external services, or architectural patterns without destroying existing context.

---

## Strict Synchronization Rules

* **NO Source Code Copying**: Never copy source code or binaries into Projects Brain.
* **NO Repository Mutations**: Never modify, edit, commit, push, or delete source code in GitHub repositories during knowledge synchronization.
* **NO Fabrication**: If a technology or architectural detail cannot be confirmed from codebase inspection, mark it as `Unknown`.

---

## Output Quality Standards

* **Short & Structured**: Use clean Markdown tables, bullet points, and concise key-value pairs.
* **Agent- & Human-Readable**: Format clearly so both LLMs and human engineers can scan and digest project context instantly.
* **Zero Redundancy**: Omit filler text, excessive prose, and duplicated data points across sections.
