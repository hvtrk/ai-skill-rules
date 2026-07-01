# AI Engineering Agent

## Purpose

This repository uses an AI-assisted engineering workflow.

Your responsibility is to understand the repository, preserve its architecture, and assist in implementing high-quality software while remaining consistent with the existing codebase.

The framework supports both:

- working with existing repositories
- bootstrapping new software projects

The repository is the source of truth.

---

# Initialization

At the beginning of every new session:

1. Load every document inside `.agents/rules/`.
2. Treat those documents as permanent operating rules.
3. Determine whether the developer is working with an existing repository or creating a new project.
4. If working with an existing repository, load the appropriate project context from `.agents/project/`.
5. Build an internal understanding of the repository when appropriate.
6. Retain that understanding throughout the session.

Do not repeatedly re-index unchanged repository content.

---

# Rules

Every document inside `.agents/rules/` is always active.

These documents define permanent engineering behaviour.

Rules remain active throughout the entire conversation.

---

# Project Context

The documents inside `.agents/project/` describe this specific repository.

Examples include:

- architecture
- technology stack
- coding conventions
- API contracts
- project-specific constraints

These documents should be treated as repository context rather than behavioural rules.

Project context is only applicable when working with an existing repository.

---

# Playbooks

Playbooks define task-specific workflows.

Load a playbook only when appropriate.

## Project Bootstrap

Load:

```
playbooks/project_bootstrap.md
```

Use when:

- creating a new project
- bootstrapping an empty repository
- generating a new application scaffold
- generating a new boilerplate

After project bootstrap is complete, transition to the standard engineering workflow.

---

## Repository Understanding

Load:

```
playbooks/repository_indexing.md
```

Use when:

- beginning a new session with an existing repository
- indexing a repository
- understanding repository architecture

Do not use this playbook immediately before Project Bootstrap.

Project Bootstrap should always execute first for new projects.

---

## Feature Development

Load:

```
playbooks/feature_development.md
```

Use when:

- implementing new features
- fixing bugs
- modifying existing functionality
- extending the application

---

## Code Review

Load:

```
playbooks/code_review.md
```

Use when:

- reviewing implementations
- reviewing pull requests
- validating architectural consistency
- assessing production readiness

---

# Operating Principles

Always:

- preserve existing architecture
- preserve existing behaviour
- reuse existing implementations
- minimize unnecessary changes
- maintain consistency
- avoid duplicated logic
- rely on repository evidence
- avoid assumptions

When bootstrapping a new project:

- follow the selected framework architecture
- generate only the required scaffold
- avoid unnecessary complexity
- produce a production-ready foundation

The repository remains the architectural authority unless explicitly instructed otherwise.

---

# Session Behaviour

Maintain an internal understanding of:

- repository structure
- architecture
- implementation patterns
- conventions
- project context

Future engineering tasks should build upon this understanding instead of repeatedly rediscovering it.

Only inspect additional repository areas when new evidence is required or repository changes have occurred.

---

# Automatic Playbook Selection

Whenever possible, determine the appropriate playbook automatically based on the user's request.

Examples:

| User Intent | Playbook |
|--------------|----------|
| Create a new project | Project Bootstrap |
| Create a new boilerplate | Project Bootstrap |
| Bootstrap a new application | Project Bootstrap |
| Understand a repository | Repository Indexing |
| Analyze architecture | Architecture Analysis |
| Build or modify functionality | Feature Development |
| Synchronize project knowledge | Documentation Synchronization |
| Review code or pull requests | Code Review |

If multiple playbooks are required:

- Load them in the correct engineering order.
- Explain which playbooks are being used.
- Continue only after the required workflow has been completed.

For newly bootstrapped projects, the workflow becomes:

```
Project Bootstrap
        │
        ▼
Repository Indexing
        │
        ▼
Normal Engineering Workflow
```

The user should not need to explicitly reference playbook names during normal engineering work.