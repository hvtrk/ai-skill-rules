---
trigger: always_on
description: Defines the architecture, philosophy, and operating model of the AI Engineering Framework. This document explains how the framework is organized and how its components interact.
---

# AI Engineering Framework

Version: 1.1

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

The framework supports both:

- creating new software projects
- working with existing repositories

The framework separates behaviour, process, framework knowledge, and project knowledge into independent layers.

---

# Framework Philosophy

The framework follows four principles.

1. Repository First
2. Evidence Before Assumption
3. Incremental Evolution
4. Separation of Responsibilities

The objective is not to redesign software.

The objective is to help engineers safely bootstrap new projects and evolve existing systems.

---

# Framework Layers

The framework is organized into five independent layers.

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

## Layer 3 — Framework Knowledge

Location

```
.agents/knowledge/frameworks/
```

Purpose

Framework-specific engineering knowledge.

These documents describe supported application frameworks, recommended architectures, project structures, and implementation patterns.

Framework knowledge is loaded only when creating a new project or when framework-specific guidance is required.

---

## Layer 4 — Project

Location

```
.agents/project/
```

Purpose

Repository-specific knowledge.

These documents describe the current repository.

Unlike Rules, Playbooks, and Framework Knowledge, these documents are unique for every project.

---

## Layer 5 — Repository

The repository itself.

The repository remains the authoritative source of evidence.

Project documentation summarizes repository knowledge.

It never replaces repository evidence.

---

# Engineering Workflows

The framework supports two engineering workflows.

## Existing Repository

```
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
```

---

## New Project

```
Empty Repository

↓

Project Bootstrap

↓

Framework Selection

↓

Project Scaffolding

↓

Repository Indexing

↓

Standard Engineering Workflow
```

After a project has been bootstrapped, it is treated as an existing repository.

---

# Responsibilities

## Rules

Own behaviour.

## Playbooks

Own engineering workflows.

## Framework Knowledge

Own framework-specific engineering knowledge.

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

Framework-specific knowledge should remain isolated from the core engineering framework.

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

The framework governs engineering behaviour and engineering workflows.

It does not dictate:

- programming languages
- application frameworks
- infrastructure
- architecture styles

Those belong to the selected framework or the repository being analyzed.

---

# Goal

The objective of the framework is to make AI behave like an experienced software engineer that can either:

- bootstrap a new software project using an approved framework
- work safely within an existing codebase while preserving its architecture and conventions