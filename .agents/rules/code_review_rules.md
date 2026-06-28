---
trigger: model_decision
description: Apply when reviewing code, pull requests, implementations, architectural changes, or release readiness to ensure reviews are objective, evidence-based, repository-aware, and actionable.
---

# Code Review Rules

## Purpose

These rules define how implementations should be reviewed.

Reviews should improve quality while preserving repository consistency and architectural integrity.

The goal of a review is to identify real issues, not rewrite the implementation.

---

# Rule 1 — Understand Before Reviewing

Before reviewing:

- understand the objective
- understand the requested change
- identify the intended behaviour

Review the implementation against its intended purpose.

---

# Rule 2 — Review Against the Repository

Evaluate the implementation against:

- repository architecture
- existing patterns
- coding conventions
- project structure

Do not compare implementations against personal preferences.

The repository is the reference.

---

# Rule 3 — Be Evidence Based

Every finding should be supported by evidence.

Examples include:

- implementation
- architecture
- configuration
- documentation
- tests
- behaviour

Avoid speculative criticism.

---

# Rule 4 — Review Scope

Determine whether the implementation remained within the approved scope.

Identify:

- unrelated refactoring
- unrelated cleanup
- unnecessary architectural changes
- unnecessary optimizations

Only review work that actually changed.

---

# Rule 5 — Functional Correctness

Verify that:

- requirements are satisfied
- behaviour is correct
- edge cases are handled
- failures are handled appropriately

Identify incomplete implementations.

---

# Rule 6 — Architectural Consistency

Review whether the implementation:

- respects module boundaries
- follows dependency direction
- integrates naturally
- preserves architectural consistency

Recommend architectural changes only when technically justified.

---

# Rule 7 — Reuse

Determine whether existing functionality could have been reused.

Identify duplicated:

- logic
- utilities
- services
- components
- abstractions

Prefer extension over duplication.

---

# Rule 8 — Maintainability

Review whether the implementation is:

- readable
- understandable
- maintainable
- testable

Avoid recommending unnecessary complexity.

---

# Rule 9 — Performance

Identify obvious performance issues.

Examples:

- repeated work
- unnecessary allocations
- unnecessary queries
- inefficient algorithms

Do not speculate about performance problems without evidence.

---

# Rule 10 — Security

Review for obvious security concerns.

Examples include:

- unsafe input handling
- missing validation
- hardcoded secrets
- excessive permissions
- sensitive data exposure

Only report issues supported by evidence.

---

# Rule 11 — Backwards Compatibility

Determine whether existing behaviour has changed.

Identify:

- breaking APIs
- changed contracts
- migration requirements

If none exist, explicitly state:

"No breaking changes detected."

---

# Rule 12 — Testing

Review available validation.

Consider:

- manual verification
- automated tests
- integration testing
- edge case coverage

If testing cannot be evaluated, state that explicitly.

---

# Rule 13 — Categorize Findings

Every finding should be categorized.

Use:

## Critical

Must be fixed before merge.

---

## High

Should be fixed before merge.

---

## Medium

Should be addressed soon.

---

## Low

Optional improvements.

Do not exaggerate issue severity.

---

# Rule 14 — Recognize Good Engineering

A review should identify strengths as well as weaknesses.

Highlight positive aspects such as:

- good architectural fit
- effective reuse
- consistency
- clean implementation
- maintainability
- simplicity

Reviews should be balanced and objective.

---

# Rule 15 — Actionable Feedback

Every issue should include:

- what the issue is
- why it matters
- evidence supporting the finding
- a practical recommendation

Avoid vague feedback.

---

# Rule 16 — Final Recommendation

Conclude every review with one recommendation.

Choose one:

- Approve
- Approve with Minor Changes
- Request Changes
- Reject

Provide a concise justification for the recommendation.

---

# Rule 17 — Review Mindset

The objective of a review is to improve the software.

Do not:

- rewrite code unnecessarily
- redesign the system
- recommend changes based solely on preference
- expand the implementation scope

Provide feedback that is objective, constructive, and aligned with the repository.