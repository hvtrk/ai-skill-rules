# FastAPI Framework Knowledge

## Purpose

This directory contains the framework knowledge required to bootstrap and maintain FastAPI applications.

These documents describe the recommended architecture, project structure, and implementation patterns for FastAPI projects created using this AI framework.

This knowledge is loaded only when the selected backend framework is FastAPI.

---

# Contents

## architecture.md

Defines the recommended architecture for FastAPI applications.

Includes:

- Design principles
- Project structure
- Layer responsibilities
- Routing strategy
- Dependency flow
- Shared components

---

## boilerplate.md

Defines the standard project scaffold.

Includes:

- Folder structure
- Initial files
- Required tooling
- Configuration
- Development environment
- Project conventions

---

## feature_structure.md

Defines how new features should be implemented.

Includes:

- Feature folder structure
- File responsibilities
- Feature registration
- Router registration
- Service and repository responsibilities
- Feature development workflow

---

# Usage

These documents are reference material.

They are consumed by the **Project Bootstrap Playbook** whenever the selected backend framework is FastAPI.

They should not be interpreted as implementation workflows.

---

# Scope

This knowledge applies only to FastAPI projects.

Framework-specific implementation details should remain inside this directory.

Framework-independent engineering practices belong in the repository's shared knowledge, rules, and playbooks.

---

# Guiding Principles

All FastAPI projects generated using this framework should:

- Follow the documented architecture.
- Maintain a consistent folder structure.
- Use the standard feature layout.
- Keep responsibilities clearly separated.
- Avoid unnecessary complexity.
- Be production-ready from the initial scaffold.

---

# Future Expansion

Additional framework knowledge should follow the same structure.

Example:

```text
knowledge/
└── frameworks/
    ├── fastapi/
    ├── nextjs/
    ├── express/
    ├── nestjs/
    └── django/
```

Each framework directory should remain self-contained and document only framework-specific knowledge.