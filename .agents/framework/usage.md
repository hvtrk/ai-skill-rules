# AI Engineering Framework Usage Guide

Version: 1.1.0

Status: Stable

---

# Purpose

This guide explains how to use the AI Engineering Framework during everyday software development.

The framework is designed to support both new project creation and engineering within existing repositories while minimizing repeated repository analysis and ensuring the AI works consistently with the selected architecture.

In most situations the AI should automatically determine the appropriate playbook based on the requested task.

---

# Engineering Workflows

The framework supports two engineering workflows.

## Existing Repository

Use this workflow when the repository already contains an application.

```
Initialize Framework
        │
        ▼
Load Repository Knowledge
        │
        ▼
Perform Engineering Task
        │
        ▼
Synchronize Documentation (if required)
        │
        ▼
Review Implementation
```

Repository indexing and architecture analysis should only occur when necessary.

---

## New Project

Use this workflow when creating a brand-new application.

```
Initialize Framework
        │
        ▼
Project Bootstrap
        │
        ▼
Select Framework
        │
        ▼
Generate Project Scaffold
        │
        ▼
Repository Ready
        │
        ▼
Normal Engineering Workflow
```

Once the project has been generated, it should be treated as an existing repository.
---

# Bootstrap a New Project

Use this when creating a brand-new application or bootstrapping an empty repository.

### Prompt

```text
Initialize yourself using the AI Engineering Framework.

Load the framework and rules.

Execute the Project Bootstrap playbook.

Determine the required technology stack.

Load the appropriate framework knowledge.

Generate a production-ready project scaffold.

Summarize the generated project and wait for further instructions.
```

---

# First-Time Existing Repository Setup

Use this only once after copying the framework into an existing repository.

### Prompt

```text
Initialize yourself using the AI Engineering Framework contained in this repository.

Load the framework, rules and playbooks.

Execute the Repository Indexing playbook.

Execute the Architecture Analysis playbook.

Generate every missing document inside .agents/knowledge.

Do not modify application source code.

Summarize the generated knowledge and wait for further instructions.
```

---

# Daily Development Session

Use this after a project has been bootstrapped or when working with an existing repository that already contains project knowledge.

### Prompt

```text
Initialize yourself using the AI Engineering Framework.

Load the framework.

Load the repository knowledge.

Do not perform repository indexing unless repository knowledge is missing or outdated.

Wait for my first engineering task.
```

---

# Implement a New Feature

### Prompt

```text
Implement a new feature.

Follow the appropriate playbook.

Produce an implementation plan.

Wait for approval before writing code.
```

---

# Fix a Bug

### Prompt

```text
Investigate the reported issue.

Determine the root cause.

Produce an implementation plan.

Wait for approval before making changes.
```

---

# Review an Implementation

### Prompt

```text
Review this implementation.

Evaluate:

- correctness
- architectural fit
- maintainability
- repository consistency

Categorize findings and provide a final recommendation.
```

---

# Refresh Repository Knowledge

Use this when the repository structure has changed significantly.

### Prompt

```text
Repository structure has changed.

Re-execute the Repository Indexing playbook.

Update the repository knowledge.

Do not modify application source code.
```

---

# Refresh Architecture Documentation

Use this after major architectural changes.

### Prompt

```text
The repository architecture has changed.

Re-execute the Architecture Analysis playbook.

Update only the affected knowledge documents.

Do not modify application source code.
```

---

# Synchronize Documentation

Use this after completing significant engineering work.

### Prompt

```text
Review the completed implementation.

Determine whether repository knowledge has changed.

Update only the affected knowledge documents.

If no updates are required, explicitly state so.
```

---

# Perform a Release Review

### Prompt

```text
Perform a release readiness review.

Review:

- architecture
- deployment
- maintainability
- documentation
- security

Identify any remaining risks before release.
```

---

# Upgrade the Framework

When a newer version of the framework becomes available.

### Prompt

```text
Upgrade this repository to the latest version of the AI Engineering Framework.

Compare the current framework version.

Identify required framework changes.

Do not modify repository knowledge unless necessary.

Summarize the upgrade plan before making changes.
```

---

# Common Commands

| Goal                         | Suggested Prompt                                             |
| ---------------------------- | ------------------------------------------------------------ |
| Bootstrap new project        | Bootstrap a new project using the AI Engineering Framework.  |
| Create FastAPI backend       | Create a new FastAPI backend.                                |
| Initialize repository        | Initialize the AI Engineering Framework for this repository. |
| Start a development session  | Load the framework and repository knowledge.                 |
| Build a feature              | Implement a new feature following the framework.             |
| Fix a bug                    | Investigate and fix the reported issue.                      |
| Review code                  | Review this implementation.                                  |
| Refresh repository knowledge | Refresh the repository knowledge.                            |
| Refresh architecture         | Analyze the architecture again.                              |
| Synchronize documentation    | Synchronize the project knowledge.                           |
| Perform release review       | Perform a release readiness review.                          |
| Upgrade framework            | Upgrade the AI Engineering Framework.                        |


---

# Best Practices

* Initialize the framework only once per conversation.
* Avoid re-indexing the repository unless it has changed significantly.
* Keep the knowledge documents synchronized with the repository.
* Review generated documentation before committing it.
* Allow the AI to select the appropriate playbooks automatically whenever possible.
* Use implementation plans before writing code.
* Keep project knowledge concise, accurate, and aligned with the repository.

---

# Framework Philosophy

The framework is designed to behave like a senior software engineer capable of both creating production-ready software projects and evolving existing codebases while preserving architecture, consistency, and engineering quality.

Its purpose is to:

* preserve architecture
* minimize unnecessary changes
* reuse existing implementations
* remain evidence-based
* produce maintainable software
* keep repository knowledge synchronized with the evolving codebase
* Bootstrap new projects using the Project Bootstrap playbook.
* After project creation, treat the project as an existing repository.

The framework should assist engineering teams by providing structured reasoning and repeatable engineering workflows rather than replacing engineering judgment.
