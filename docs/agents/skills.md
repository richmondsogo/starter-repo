# Skills Reference

This document describes the skills available in this project.

Skills are task-specific instruction sets that guide agent behaviour for recurring workflows.

---

## Environment-level skills

These are provided by the Antigravity environment. They are available in every project without any local configuration.

Do not copy these into this repository. Do not try to recreate them locally.

| Skill | Purpose |
|---|---|
| **Antigravity built-in skills** | Core capabilities: browser automation, environment checks, verification tooling, and a growing library of domain-specific skills. |
| **Matt Pocock engineering skills** | TypeScript, JavaScript, and general software engineering patterns and best practices. |
| **Anthropic frontend-design skill** | Frontend design technique, component composition, and general UI implementation guidance. |

---

## Project-local skills

These live in `.agents/skills/` and are specific to this project.

A local skill exists only when there is a recurring project-specific workflow that existing skills do not adequately cover.

| Skill | Location | Purpose |
|---|---|---|
| `design-system` | `.agents/skills/design-system/SKILL.md` | Keep UI implementation aligned with the project design system. Complements Anthropic's frontend-design skill with project-specific grounding. |
| `browser-verification` | `.agents/skills/browser-verification/SKILL.md` | Repeatable workflow for verifying visual and interactive changes in a real browser. |
| `project-bootstrap` | `.agents/skills/project-bootstrap/SKILL.md` | Structured process for initializing a real project from this starter. |

---

## When to create a new local skill

Create a local skill when:
- The same multi-step workflow recurs across multiple sessions or steps.
- The workflow is specific enough to this project that a general skill would not apply.
- The workflow is not already covered by an available environment skill.

Do not create a local skill:
- As a convenience copy of an environment skill.
- Speculatively, before the workflow has actually recurred.
- To document simple conventions that belong in `AGENTS.md` or `CONTEXT.md`.

---

## How skills should work together

Skills should complement, not duplicate, each other.

Example: for a UI task, use both the `design-system` skill (project-specific token and component grounding) and the Anthropic frontend-design skill (general technique). They operate at different levels of specificity and reinforce each other.

If two skills give contradictory instructions, the more specific one takes precedence. Project-local skills take precedence over general environment skills for project-specific concerns.
