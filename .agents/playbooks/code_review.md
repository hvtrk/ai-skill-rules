---
trigger: model_decision
description: Load when reviewing code, pull requests, feature implementations, architectural changes, release readiness, or production deployments. This playbook defines the review workflow and reporting structure.
---

# Code Review Playbook

## Purpose

This playbook defines the workflow for reviewing software changes.

The objective is to evaluate implementations for correctness, architectural consistency, maintainability, and production readiness.

A review should validate whether the implementation successfully solves the intended problem while remaining consistent with the existing repository.

Reviews should remain objective, evidence-based, and actionable.

---

# Review Workflow

Every review should follow this workflow.

```
Understand the Change
        │
        ▼
Inspect the Affected Area
        │
        ▼
Review Correctness
        │
        ▼
Review Architecture
        │
        ▼
Review Consistency
        │
        ▼
Review Risks
        │
        ▼
Categorize Findings
        │
        ▼
Provide Recommendation
```

Do not skip phases.

---

# Phase 1 — Understand the Change

Determine:

- purpose of the change
- intended behaviour
- requested scope
- expected outcome

If the purpose cannot be determined, state this before continuing.

---

# Phase 2 — Inspect the Implementation

Identify:

- modified files
- newly created files
- deleted files
- configuration changes
- dependency changes

Determine whether the implementation matches the requested scope.

---

# Phase 3 — Functional Review

Evaluate whether:

- requirements are satisfied
- implementation behaves correctly
- edge cases have been considered
- failure scenarios have been handled
- existing behaviour has been preserved

Identify any incomplete implementation.

---

# Phase 4 — Architectural Review

Determine whether the implementation:

- fits the existing architecture
- follows repository conventions
- respects module boundaries
- integrates naturally
- avoids unnecessary abstractions

Review against the repository, not personal preference.

---

# Phase 5 — Code Quality Review

Evaluate:

- readability
- maintainability
- consistency
- simplicity
- reuse of existing functionality
- duplication
- separation of responsibilities

Identify opportunities to simplify while preserving behaviour.

---

# Phase 6 — Risk Assessment

Review for:

## Functional Risk

Possible regressions.

---

## Architectural Risk

Long-term maintainability concerns.

---

## Performance Risk

Obvious performance issues supported by evidence.

---

## Security Risk

Potential security concerns supported by evidence.

---

## Operational Risk

Deployment, configuration, migration, or runtime concerns.

---

# Phase 7 — Testing Review

Determine whether the implementation has been appropriately validated.

Consider:

- manual testing
- automated testing
- integration testing
- edge-case verification
- deployment validation (when applicable)

If testing information is unavailable, explicitly state that.

---

# Phase 8 — Findings

Categorize findings using the following severity levels.

## Critical

Must be resolved before merge.

Examples:

- broken functionality
- security vulnerabilities
- data corruption
- deployment failure

---

## High

Should be resolved before merge.

Examples:

- significant bugs
- architectural violations
- major maintainability concerns

---

## Medium

Should be addressed soon.

Examples:

- inconsistencies
- readability improvements
- minor maintainability concerns

---

## Low

Optional improvements.

Examples:

- documentation
- naming
- formatting
- minor simplifications

Do not overstate issue severity.

---

# Phase 9 — Positive Findings

Identify strengths of the implementation.

Examples include:

- effective reuse
- clean architecture
- consistent implementation
- good readability
- maintainable design
- minimal scope changes

A review should recognize good engineering as well as issues.

---

# Phase 10 — Final Recommendation

Conclude the review with one recommendation.

Choose exactly one.

## Approve

Ready to merge.

---

## Approve with Minor Changes

Small improvements recommended before merge.

---

## Request Changes

Additional work required before merge.

---

## Reject

Implementation is unsuitable for merge due to critical issues.

Provide a concise explanation supporting the recommendation.

---

# Review Report Structure

Structure review reports using the following sections.

## Summary

Brief overview of the implementation.

---

## Scope

What changed.

---

## Strengths

Positive observations.

---

## Findings

Grouped by severity.

---

## Risks

Remaining concerns.

---

## Recommendation

Final review outcome.

---

# Completion Criteria

A review is complete when:

- implementation has been understood
- scope has been verified
- correctness has been evaluated
- architecture has been reviewed
- risks have been identified
- findings have been categorized
- a final recommendation has been provided

The objective is to improve software quality while preserving architectural integrity.
