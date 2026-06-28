---
trigger: always_on
description: Rules governing feature implementation, planning, scope management, solution evaluation, and engineering execution before code is written.
---

# Implementation Rules

## Purpose

These rules define how engineering tasks should be approached and implemented.

Every implementation should be deliberate, well planned, minimally invasive, and consistent with the existing codebase.

Implementation should never begin before the problem is understood.

---

# Rule 1 — Understand Before Implementing

Before writing code:

- understand the request
- identify the objective
- determine the expected behaviour
- identify constraints

If requirements are ambiguous:

Ask for clarification.

Do not guess.

---

# Rule 2 — Inspect Before Changing

Before modifying code:

- inspect the relevant files
- understand the existing implementation
- identify dependencies
- identify existing patterns

Do not modify code that has not been understood.

---

# Rule 3 — Plan Before Coding

Before implementation:

Create a concise implementation plan.

The plan should include:

- objective
- affected modules
- files to modify
- files to create
- architectural impact
- potential risks

Do not begin implementation until the plan has been approved.

---

# Rule 4 — One Problem at a Time

Solve only the approved problem.

Avoid introducing:

- unrelated improvements
- opportunistic refactoring
- unrelated cleanup
- speculative optimization

Keep implementations focused.

---

# Rule 5 — Two Solutions Maximum

When multiple valid approaches exist:

Present no more than two solutions.

For each solution include:

- summary
- advantages
- disadvantages
- implementation complexity
- architectural impact

Recommend the most appropriate solution.

Wait for approval before implementing.

---

# Rule 6 — Reuse Existing Code

Before introducing new code:

Search for existing:

- utilities
- services
- components
- abstractions
- helpers
- middleware

Prefer extension over duplication.

---

# Rule 7 — Minimize Change

Modify the smallest amount of code necessary.

Avoid touching unrelated files.

Small, focused changes are preferred over large refactors.

---

# Rule 8 — Preserve Existing Behaviour

New implementations should not unintentionally change existing functionality.

Maintain backwards compatibility whenever practical.

Breaking changes require explicit approval.

---

# Rule 9 — Maintain Architectural Consistency

Every implementation should:

- fit the existing architecture
- respect module boundaries
- preserve dependency direction
- follow repository conventions

Avoid introducing parallel implementations.

---

# Rule 10 — Handle Errors Intentionally

Consider:

- invalid input
- missing data
- recoverable failures
- unexpected conditions

Handle failures predictably.

Avoid silent failures.

---

# Rule 11 — Consider Edge Cases

Think beyond the happy path.

Consider:

- empty values
- null values
- duplicate data
- invalid state
- concurrent operations
- missing configuration

Edge cases should be considered during implementation rather than after deployment.

---

# Rule 12 — Keep Implementations Readable

Prefer code that is:

- readable
- understandable
- maintainable

Avoid unnecessary cleverness.

Optimize for future maintenance.

---

# Rule 13 — Respect Existing APIs

Do not modify existing APIs without approval.

If changes are required:

- identify affected consumers
- explain compatibility impact
- propose migration strategy

---

# Rule 14 — Validate Before Completion

Before considering implementation complete:

Verify:

- requirements satisfied
- architecture preserved
- repository conventions followed
- no duplicate logic introduced
- no unrelated files modified
- no obvious regressions introduced

---

# Rule 15 — Summarize the Work

After implementation provide:

## Summary

What was implemented.

## Files Modified

List modified files.

## Files Created

List new files.

## Architectural Impact

Explain how the implementation integrates with the existing system.

## Breaking Changes

List breaking changes.

If none exist, explicitly state:

"No breaking changes."

## Risks

Identify any remaining limitations or risks.

---

# Rule 16 — Know When to Stop

Complete only the approved work.

Do not continue improving the implementation after the requested feature has been completed.

Wait for the next task before making further changes.

---

# Rule 17 — Implementation Quality

Every implementation should strive to be:

- Correct
- Consistent
- Minimal
- Maintainable
- Reliable
- Readable
- Testable

Quality should never be sacrificed for speed.