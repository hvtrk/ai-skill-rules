---
trigger: always_on
description: Defines the architecture, philosophy, and operating model of the AI Engineering Framework. This document explains how the framework is organized and how its components interact.
---

# AI Engineering Framework

Version: 1.0

Status: Stable

---

# Purpose

The AI Engineering Framework provides a structured methodology for AI-assisted software engineering.

Its purpose is to ensure engineering work remains:

- consistent
- evidence-based
- maintainable
- predictable
- repository-aware

The framework separates behaviour, process, and project knowledge into independent layers.

---

# Framework Philosophy

The framework follows four principles.

1. Repository First
2. Evidence Before Assumption
3. Incremental Evolution
4. Separation of Responsibilities

The objective is not to redesign software.

The objective is to help engineers safely evolve existing systems.

---

# Framework Layers

The framework is organized into four independent layers.

## Layer 1 — Rules

Location

```
.agents/rules/
```

Purpose

Permanent engineering behaviour.

Rules are always active.

Rules define how the AI should think.

---

## Layer 2 — Playbooks

Location

```
.agents/playbooks/
```

Purpose

Engineering workflows.

Playbooks define how engineering activities are performed.

Playbooks are loaded only when required.

---

## Layer 3 — Project

Location

```
.agents/project/
```

Purpose

Repository-specific knowledge.

These documents describe the current repository.

Unlike Rules and Playbooks, these documents are unique for every project.

---

## Layer 4 — Repository

The repository itself.

The repository remains the authoritative source of evidence.

Project documentation summarizes repository knowledge.

It never replaces repository evidence.

---

# Engineering Workflow

The intended engineering workflow is:

Repository

↓

Repository Indexing

↓

Architecture Analysis

↓

Project Documentation

↓

Feature Development

↓

Documentation Synchronization

↓

Code Review

---

# Responsibilities

## Rules

Own behaviour.

## Playbooks

Own engineering workflows.

## Project

Own repository knowledge.

## Repository

Own implementation and evidence.

Each layer has a single responsibility.

---

# Design Principles

The framework is designed to be:

- reusable
- modular
- framework independent
- language independent
- repository independent

Only the Project layer should change between repositories.

---

# Versioning

The framework should evolve over time.

Changes should be versioned.

Breaking changes should increment the major version.

Backward-compatible improvements should increment the minor version.

Bug fixes should increment the patch version.

Example:

- v1.0.0
- v1.1.0
- v1.2.0
- v2.0.0

---

# Scope

The framework governs engineering behaviour.

It does not dictate:

- programming languages
- frameworks
- infrastructure
- architecture styles

Those belong to the repository being analyzed.

---

# Goal

The objective of the framework is to make AI behave like an experienced software engineer working within an existing codebase instead of an autonomous code generator.