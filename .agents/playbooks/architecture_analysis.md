---
trigger: model_decision
description: Load when analyzing an existing repository to understand, document, or validate its architecture. This playbook defines the workflow for discovering architectural structure and producing or updating the project's architecture documentation.
---

# Architecture Analysis Playbook

## Purpose

This playbook defines the process for analyzing the architecture of an existing software project.

The objective is to understand how the repository is organized, why it is organized that way, and how future work should integrate into the existing design.

This playbook does not redesign architecture.

Its purpose is to understand and document architecture.

---

# Workflow

Every architectural analysis should follow this workflow.

```
Understand Repository
        │
        ▼
Identify Major Modules
        │
        ▼
Identify Architectural Layers
        │
        ▼
Identify Responsibilities
        │
        ▼
Identify Dependencies
        │
        ▼
Identify Extension Points
        │
        ▼
Identify Constraints
        │
        ▼
Document Architecture
```

---

# Phase 1 — Repository Understanding

Understand:

- project purpose
- application responsibilities
- deployment model
- major technologies

Build enough understanding to reason about the architecture.

---

# Phase 2 — Module Discovery

Identify every major module.

For each module determine:

- purpose
- responsibilities
- public interfaces
- dependencies
- ownership

Do not infer responsibilities without repository evidence.

---

# Phase 3 — Layer Analysis

Determine whether the repository contains architectural layers.

Examples include:

- presentation
- business logic
- domain
- application
- infrastructure
- persistence

Do not force the repository into a predefined architecture.

Describe only what actually exists.

---

# Phase 4 — Responsibility Analysis

Determine what each layer or module is responsible for.

Document:

- responsibilities
- boundaries
- ownership
- collaboration

Avoid overlapping responsibilities.

---

# Phase 5 — Dependency Analysis

Determine dependency direction.

Identify:

- allowed dependencies
- forbidden dependencies
- shared modules
- circular dependencies
- external dependencies

Document architectural dependency rules.

---

# Phase 6 — Extension Points

Identify where future functionality should be added.

Determine:

- reusable abstractions
- extension mechanisms
- existing services
- reusable utilities
- shared models

Future implementations should extend these before introducing new patterns.

---

# Phase 7 — Constraints

Identify architectural constraints.

Examples:

- layering rules
- deployment assumptions
- framework limitations
- technology choices
- performance constraints

Future implementations should respect these constraints.

---

# Phase 8 — Design Decisions

Identify intentional design decisions.

Where repository evidence exists, determine:

- what decision was made
- why it was made
- alternatives that were rejected (if documented)

Do not invent architectural reasoning.

---

# Phase 9 — Architecture Documentation

Produce or update the project architecture document.

The document should include:

- architectural overview
- major modules
- responsibilities
- dependency rules
- extension strategy
- architectural constraints
- important design decisions

Keep the documentation aligned with the repository.

---

# Completion Criteria

Architecture analysis is complete when:

- repository structure is understood
- module responsibilities are documented
- dependency direction is understood
- architectural boundaries are clear
- extension points have been identified
- constraints have been documented
- architecture documentation reflects the current repository

Do not recommend architectural changes unless explicitly requested.

The objective is understanding, not redesign.