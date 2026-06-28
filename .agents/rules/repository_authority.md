---
trigger: model_decision
description: Apply when analyzing, modifying, extending, or reviewing an existing repository to ensure repository evidence and architecture always take precedence over assumptions or redesigns.
---

# Repository Authority

## Purpose

The current repository is the authoritative source of truth.

All engineering decisions should be based on repository evidence before relying on external knowledge, assumptions, or prior experience.

The goal is to preserve architectural consistency and evolve the existing system rather than redesign it.

---

# Rule 1 — Repository First

Always treat the current repository as the primary source of truth.

Before making recommendations:

- inspect the repository
- understand the existing implementation
- identify existing patterns
- identify existing architecture

Do not assume how the project should be structured.

Determine how it is actually structured.

---

# Rule 2 — Architecture Preservation

Assume the existing architecture is intentional.

Do not redesign:

- project structure
- application layers
- module boundaries
- dependency direction
- package organization

Architectural changes require explicit approval.

---

# Rule 3 — Existing Patterns Take Priority

When implementing new functionality:

Search for similar implementations already present in the repository.

Reuse existing patterns whenever appropriate.

Prefer extending existing implementations over introducing new ones.

---

# Rule 4 — Repository Evidence

Every recommendation should be supported by repository evidence whenever possible.

Examples include:

- existing code
- documentation
- configuration
- tests
- naming conventions
- implementation patterns

Repository evidence takes precedence over general best practices.

---

# Rule 5 — No Assumptions

Never invent:

- APIs
- services
- utilities
- modules
- abstractions
- configuration
- folder structures

If repository evidence is insufficient:

- state what is known
- state what is unknown
- request additional evidence if necessary

Do not guess.

---

# Rule 6 — Respect Existing Decisions

Assume previous engineering decisions were made intentionally.

Do not recommend replacing technologies, frameworks, or architectural patterns simply because alternatives exist.

Recommend changes only when there is clear technical justification.

---

# Rule 7 — Repository Consistency

Every implementation should remain consistent with the repository.

Maintain consistency in:

- folder structure
- naming
- imports
- exports
- typing
- logging
- validation
- error handling
- documentation

New code should appear native to the repository.

---

# Rule 8 — Repository Evolution

The goal is to evolve the repository.

Not reinvent it.

Every implementation should integrate naturally into the existing codebase.

Avoid introducing parallel implementations.

Avoid unnecessary abstractions.

Avoid unnecessary restructuring.

---

# Rule 9 — Repository Context

Maintain an internal understanding of:

- repository structure
- architecture
- module boundaries
- implementation patterns
- coding conventions

Reuse this understanding throughout the session.

Avoid repeatedly re-analyzing unchanged repository areas.

---

# Rule 10 — Repository Over Prior Knowledge

If prior knowledge conflicts with repository implementation:

Follow the repository.

The current repository always has higher authority than prior knowledge or generalized best practices unless explicitly instructed otherwise.

---

# Rule 11 — Preserve Existing Behaviour

Do not modify existing behaviour unless explicitly requested.

Preserve backwards compatibility whenever reasonably possible.

Avoid introducing unintended behavioural changes.

---

# Rule 12 — Repository Before Recommendation

Before recommending:

- new libraries
- new frameworks
- new abstractions
- new services
- new utilities
- architectural changes

Verify that an equivalent solution does not already exist within the repository.

Prefer reuse over replacement.

---

# Rule 13 — Scope Awareness

Limit repository modifications to the approved task.

Do not:

- refactor unrelated modules
- reorganize folders
- rename files
- replace existing patterns
- modernize unrelated code

Stay within the approved scope.

---

# Rule 14 — Repository Integrity

Every change should improve or extend the repository without reducing:

- consistency
- readability
- maintainability
- architectural integrity

The repository should remain internally coherent after every implementation.