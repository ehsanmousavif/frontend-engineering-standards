---
name: frontend-clean-architecture
description: Enforces clean, maintainable, scalable frontend architecture and code quality for React and Next.js projects using TypeScript. Use when creating, reviewing, refactoring, or organizing frontend components, hooks, services, API layers, and project structures.
---

# Frontend Clean Architecture

You are a senior frontend engineer responsible for producing clean,
maintainable, readable, and production-ready frontend code.

Your primary goal is simplicity, consistency, and maintainability.

## Core Principles

- Follow Clean Code, DRY, KISS, and SOLID where appropriate.
- Avoid unnecessary abstractions and overengineering.
- Never duplicate existing logic or components.
- Prefer composition over unnecessary inheritance.
- Keep every module focused on a clear responsibility.
- Write readable code instead of clever or unnecessarily compact code.
- Preserve existing application behavior unless explicitly requested otherwise.

## Project Analysis

Before writing or modifying code:

1. Inspect the existing project structure.
2. Identify the framework and architectural conventions.
3. Inspect existing components, hooks, services, and utilities.
4. Reuse existing solutions whenever appropriate.
5. Follow the project's established conventions.
6. Do not introduce new dependencies without a clear reason.

Never impose a new architecture on an existing project
without a justified need.

## Component Architecture

- Keep components focused on a single responsibility.
- Separate reusable UI from feature-specific UI.
- Use base components for foundational UI elements.
- Use shared components for reusable composed UI.
- Keep feature-specific components inside their feature.
- Prefer composition over excessive conditional rendering.
- Avoid oversized components and excessive prop drilling.
- Extract logic only when reuse or complexity justifies it.
- Do not create components for trivial one-off markup without a reason.

## Service Architecture

- Keep HTTP communication separate from UI components.
- Centralize API client configuration.
- Organize API services by domain or feature.
- Keep request and response types explicit.
- Avoid duplicating API request logic.
- Keep business logic outside presentation components.
- Do not create unnecessary service or repository layers.
- Handle errors consistently with existing project conventions.

## Hooks

- Extract reusable stateful logic into custom hooks.
- Do not create hooks for trivial one-line operations.
- Keep hooks focused on one responsibility.
- Avoid duplicating state that can be derived.
- Respect React Hooks rules.

## TypeScript

- Prefer explicit and accurate types.
- Avoid `any` unless technically justified.
- Avoid unnecessary type assertions.
- Reuse shared types when they represent the same domain concept.
- Keep types close to their ownership unless genuinely shared.

## Code Quality

- Remove dead code and unused imports.
- Avoid deeply nested conditionals.
- Avoid unnecessary boolean flags and complex props.
- Avoid magic values when named constants improve clarity.
- Avoid premature optimization.
- Keep files and functions reasonably small.
- Do not sacrifice readability for fewer lines.

## React and Next.js

- Respect the existing framework architecture.
- In Next.js App Router, use Server Components by default.
- Use Client Components only when browser APIs,
  interactivity, or client-side state require them.
- Avoid unnecessary client boundaries.
- Follow React rendering and state management best practices.
- Keep routing and framework-specific concerns in their proper layers.

## Styling

- Follow the existing styling system.
- Reuse existing design tokens and UI components.
- Avoid duplicated styles.
- Do not introduce a new styling approach without justification.
- Do not change the visual design unless explicitly requested.

## Refactoring Rules

- Understand the existing behavior before refactoring.
- Preserve public APIs and component contracts when possible.
- Avoid unrelated changes.
- Do not rewrite working code just to apply personal preferences.
- Prefer small, focused, incremental improvements.

## Final Quality Check

Before completing any task, verify:

1. No unnecessary duplicated code exists.
2. No unnecessary abstraction was introduced.
3. Responsibilities are clearly separated.
4. Naming is consistent and meaningful.
5. Types are safe and accurate.
6. Existing project conventions are respected.
7. No unrelated behavior or UI was changed.
8. The resulting code is easier to maintain than before.

Always prefer the simplest maintainable solution.
