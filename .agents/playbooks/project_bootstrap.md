---
trigger: model_decision
description: Load when creating a new software project, bootstrapping an empty repository, or generating a new application scaffold before any implementation begins.
---

# Project Bootstrap Playbook

## Purpose

The purpose of project bootstrapping is to establish a production-ready foundation for a new software project.

The objective is to gather the required project context, select the appropriate framework, generate the initial project scaffold, validate the generated application, and transition the repository into the standard engineering workflow.

Project bootstrapping is a project creation activity.

It should only be used for new projects and empty repositories.

---

# Objective

Create a complete, production-ready project foundation that can immediately transition into normal development.

The generated project should:

- follow the selected framework architecture
- follow the engineering standards
- be immediately runnable
- require minimal manual setup
- serve as the foundation for all future development

---

# When To Use

Use this playbook when:

- the repository is empty
- a new project is requested
- a new application scaffold is requested
- a new boilerplate is requested
- no existing application architecture exists

Do not use this playbook for existing repositories.

---

# Bootstrap Workflow

Always complete the following phases in order.

## Phase 1 — Project Discovery

Understand the project before generating code.

Determine:

- Project purpose
- Technology stack
- Backend framework
- Frontend framework (if applicable)
- Database
- Deployment target
- Initial functional requirements

Do not make assumptions.

Ask for clarification when required.

---

## Phase 2 — Architecture Selection

Select the appropriate project architecture.

Examples include:

- FastAPI
- Next.js
- Express
- NestJS

Load the framework knowledge for the selected technology.

Do not mix multiple framework architectures.

---

## Phase 3 — Generate Boilerplate

Generate the project using the selected framework's boilerplate.

The generated project must:

- Follow the framework architecture.
- Be production-ready.
- Be immediately runnable.
- Follow the project's engineering rules.
- Include only the components required by the developer.

Do not generate unnecessary features.

---

## Phase 4 — Validate

Verify that:

- The project structure is correct.
- The application starts successfully.
- Configuration is complete.
- Required dependencies are configured.
- The generated project follows the framework architecture.

Resolve any issues before continuing.

---

## Phase 5 — Transition

Once the project has been successfully scaffolded:

- Consider the project bootstrapped.
- Stop using this playbook.
- Transition to the standard engineering workflow.

From this point onward, use:

- Repository Indexing
- Architecture Analysis
- Feature Development
- Documentation Sync
- Code Review

The project should now be treated as an existing repository.

---

# Decision Rules

When creating a new project:

- Prefer simplicity.
- Follow the selected framework architecture.
- Generate only what is required.
- Avoid unnecessary abstractions.
- Avoid optional infrastructure unless explicitly requested.

---

# Success Criteria

The project bootstrap is complete when:

- The repository contains a complete project scaffold.
- The application starts successfully.
- The architecture follows the selected framework.
- The project is ready for feature development.
- The project can transition to the normal engineering workflow.