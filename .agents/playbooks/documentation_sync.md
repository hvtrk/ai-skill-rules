---
trigger: model_decision
description: Load after completing an implementation to determine whether long-term project knowledge has changed and whether any project documentation should be created or updated.
---

# Documentation Synchronization Playbook

## Purpose

This playbook determines whether repository knowledge has changed following an implementation.

Its objective is to keep long-lived project documentation synchronized with the repository while avoiding unnecessary documentation updates.

Documentation should evolve alongside the repository.

Documentation should not be updated for cosmetic or implementation-only changes.

---

# Workflow

Every documentation review should follow this workflow.

```
Implementation Complete
        │
        ▼
Determine Knowledge Changes
        │
        ▼
Identify Affected Documentation
        │
        ▼
Determine Update Scope
        │
        ▼
Recommend Documentation Updates
        │
        ▼
Update Documentation (if approved)
```

---

# Phase 1 — Determine Repository Knowledge Changes

Determine whether the implementation changed long-term repository knowledge.

Examples include:

- architecture
- project structure
- technology stack
- coding conventions
- API contracts
- deployment strategy
- design decisions
- extension points

Ignore implementation details that do not affect long-term understanding.

---

# Phase 2 — Determine Documentation Impact

Identify which project documents are affected.

Examples:

| Repository Change | Documentation |
|-------------------|---------------|
| Architecture changes | architecture.md |
| Technology changes | tech_stack.md |
| API additions or modifications | api_contracts.md |
| Coding standard changes | coding_conventions.md |
| Repository structure changes | repository_map.md |
| Project goals or assumptions | project_baseline.md |

Only recommend updates for affected documents.

---

# Phase 3 — Determine Update Type

Classify documentation changes.

## New Document

Repository knowledge now exists that has not previously been documented.

---

## Update Existing Document

Existing documentation no longer accurately reflects the repository.

---

## No Documentation Required

Implementation does not change long-term repository knowledge.

---

# Phase 4 — Validate Necessity

Before recommending documentation updates ask:

- Does this change repository understanding?
- Will future contributors benefit from this documentation?
- Does the repository now differ from the documented architecture?
- Has an API contract changed?
- Has a design decision changed?

If the answer to all questions is "No":

Do not update documentation.

---

# Phase 5 — Documentation Summary

If documentation updates are required:

Provide:

## Documents

List every affected document.

---

## Reason

Explain why each document requires updating.

---

## Summary

Describe what information should be added or modified.

---

# Completion Criteria

Documentation synchronization is complete when one of the following is true:

## Documentation Updated

Repository knowledge has been synchronized.

---

## No Updates Required

Explicitly state:

"No project documentation updates required."

---

# Documentation Principles

Documentation should:

- describe repository knowledge
- remain concise
- remain accurate
- avoid duplication
- evolve with the repository
- preserve historical design decisions

Documentation should never become a changelog.

It should describe the current state of the repository.

---

# Scope

This playbook applies only to long-term project documentation.

Do not recommend documentation updates for:

- bug fixes
- formatting changes
- variable renaming
- internal refactoring
- comments
- implementation details that do not affect repository understanding

Focus only on knowledge that future engineers need in order to understand and extend the repository.