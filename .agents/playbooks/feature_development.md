---
trigger: model_decision
description: Load when implementing new features, fixing bugs, refactoring approved components, or extending existing functionality. This playbook defines the mandatory engineering workflow from understanding requirements through implementation and completion.
---

# Feature Development Playbook

## Purpose

This playbook defines the engineering workflow for implementing software changes.

Its purpose is to ensure every implementation is:

- well understood
- properly planned
- architecturally consistent
- minimally invasive
- maintainable
- reviewed before completion

Implementation should never begin immediately after receiving a request.

---

# Workflow

Every implementation should follow this workflow.

```
Understand Request
        │
        ▼
Inspect Repository
        │
        ▼
Analyze Existing Implementation
        │
        ▼
Identify Impact
        │
        ▼
Create Implementation Plan
        │
        ▼
Present Plan
        │
        ▼
WAIT FOR APPROVAL
        │
        ▼
Implement
        │
        ▼
Self Review
        │
        ▼
Summarize Changes
```

Do not skip phases.

---

# Phase 1 — Understand the Request

Determine:

- objective
- expected behaviour
- business requirements
- technical requirements
- constraints
- success criteria

If requirements are ambiguous:

Ask questions before continuing.

Never assume missing requirements.

---

# Phase 2 — Repository Analysis

Inspect only the repository areas relevant to the request.

Identify:

- affected modules
- related services
- existing APIs
- existing components
- existing utilities
- existing abstractions
- configuration
- dependencies

Understand the current implementation before proposing changes.

---

# Phase 3 — Pattern Discovery

Search for similar implementations.

Identify existing:

- features
- workflows
- services
- components
- utilities
- helpers
- middleware

Prefer extending existing implementations rather than creating parallel solutions.

---

# Phase 4 — Impact Analysis

Determine:

## Files to Modify

List all files expected to change.

---

## Files to Create

List any new files required.

---

## Dependencies

Identify:

- internal dependencies
- external dependencies
- configuration changes

---

## Risks

Identify:

- regression risk
- compatibility risk
- architectural impact
- deployment impact

---

## Breaking Changes

Determine whether the implementation introduces breaking changes.

If none exist, explicitly state so.

---

# Phase 5 — Implementation Plan

Present a concise implementation plan.

Include:

## Objective

## Proposed Solution

## Architectural Fit

Explain why the implementation aligns with the existing architecture.

## Files

List:

- files to modify
- files to create

## Risks

Summarize implementation risks.

## Validation Strategy

Describe how the implementation should be verified.

---

# Phase 6 — Alternative Solutions

If multiple valid implementations exist:

Present no more than two options.

For each option provide:

- overview
- advantages
- disadvantages
- complexity
- architectural impact
- long-term maintenance considerations

Recommend one option.

Do not implement either option until approval has been received.

---

# Phase 7 — Approval Gate

After presenting the implementation plan:

Stop.

Wait for explicit approval.

Do not:

- write code
- generate files
- modify implementation

Approval must be explicit.

---

# Phase 8 — Implementation

Implement only the approved solution.

Do not:

- introduce unrelated improvements
- refactor unrelated modules
- reorganize folders
- change architecture

If implementation reveals unexpected repository constraints:

Pause.

Explain the issue.

Update the implementation plan.

Obtain approval before continuing.

---

# Phase 9 — Self Review

Before completion verify:

- requirements satisfied
- architecture preserved
- repository conventions followed
- existing behaviour preserved
- no duplicate logic introduced
- implementation remains within scope
- no unnecessary files modified

Correct issues before presenting the final result.

---

# Phase 10 — Completion Summary

Every completed implementation should include:

## Summary

Describe what was implemented.

---

## Files Modified

List modified files.

---

## Files Created

List newly created files.

---

## Architectural Impact

Explain how the implementation integrates with the existing system.

---

## Breaking Changes

List any breaking changes.

If none exist, explicitly state:

"No breaking changes."

---

## Validation

Describe:

- manual validation
- automated testing
- build verification
- deployment verification (when applicable)

---

## Remaining Risks

Document any known limitations or future considerations.

---

## Documentation Review

Before considering the task complete, determine whether the implementation changes repository knowledge.

Examples include:

- architecture
- technology stack
- API contracts
- coding conventions
- project structure

If repository knowledge has changed:

Recommend updating the corresponding document in `.agents/project/`.

If no documentation changes are required, explicitly state:

"No project documentation updates required."

---
# Engineering Principles

Throughout implementation:

- preserve architecture
- preserve existing behaviour
- reuse existing implementations
- minimize code changes
- avoid duplication
- avoid unnecessary complexity
- remain consistent with repository conventions

---

# Completion Criteria

A feature is complete only when:

- requirements have been satisfied
- repository conventions have been followed
- architecture has been preserved
- implementation has been reviewed
- changes have been summarized
- validation has been completed
- remaining risks have been documented

Implementation is not complete simply because the code compiles.