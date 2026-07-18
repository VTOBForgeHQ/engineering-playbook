# PDF-001 — VTOBForge Product Development Framework

Status: Approved

Version: 1.0

Owner: VTOBForge

---

# Purpose

This document defines the standard process used to build every VTOBForge product.

It ensures that products are built intentionally, consistently, and can continue evolving without losing direction.

Every product should follow this framework unless there is a documented reason not to.

---

# Core Philosophy

We do not build software by accident.

We build software through documented decisions.

Code is only one part of the product.

A complete product also includes:

- Vision
- Product thinking
- Design
- Engineering
- Documentation
- Reflection
- Continuous improvement

---

# Three-Layer Model

Every VTOBForge product exists within three layers.

## Layer 1 — Institution

Repository:

Engineering Playbook

Purpose:

Defines how VTOBForge builds software.

Owns:

- Engineering standards
- Development workflow
- Architecture principles
- ADRs
- Engineering audits
- Product Development Framework

---

## Layer 2 — Product

Repository:

The product repository (e.g. DailyCurio)

Purpose:

Defines what is being built.

Owns:

- Product vision
- Product roadmap
- Product architecture
- Design system
- Feature specifications
- Product documentation

---

## Layer 3 — Implementation

Purpose:

Transforms documented decisions into working software.

Owns:

- Flutter code
- Assets
- Tests
- Configuration
- Product implementation

---

# Repository Ownership Rule

Every document must have exactly one canonical home.

Engineering knowledge belongs in the Engineering Playbook.

Product knowledge belongs in the product repository.

Avoid duplication.

Reference instead of copying.

---

# Product Lifecycle

Every product follows the same lifecycle.

1. Vision
2. Product Definition
3. Architecture
4. Design System
5. Engineering Handoff
6. Implementation
7. Verification
8. Documentation
9. Release
10. Reflection
11. Continuous Improvement

---

# Milestone Workflow

Every milestone follows the same rhythm.

1. Discuss
2. Refine
3. Decide
4. Document
5. Build
6. Verify
7. Commit
8. Reflect
9. Continue

No milestone skips documentation.

No implementation skips verification.

---

# Documentation Principles

Documentation exists to preserve knowledge.

Every important decision should answer:

- What was decided?
- Why was it decided?
- Where is it implemented?
- What is affected if it changes?

---

# Engineering Principles

Engineering should:

- Prefer simplicity.
- Avoid unnecessary complexity.
- Reuse established patterns.
- Centralize shared decisions.
- Keep repositories organized.
- Document architectural decisions.

---

# Product Principles

Products should:

- Solve real problems.
- Prioritize user experience.
- Maintain consistency.
- Grow through small verified milestones.
- Preserve continuity.

---

# Design–Engineering Relationship

Design defines:

"What experience should exist?"

Engineering defines:

"How should that experience be implemented?"

Neither replaces the other.

They collaborate through documented handoffs.

---

# Single Source of Truth

Every piece of knowledge has one owner.

Examples:

Engineering Playbook

- Flutter Standards
- Git Standards
- ADRs
- Engineering Audits
- Product Development Framework

Product Repository

- Product Vision
- Design System
- Architecture
- Roadmap
- Features

---

# Definition of Success

A VTOBForge product is successful when:

- Its purpose is documented.
- Its decisions are understandable.
- Its implementation is maintainable.
- Another engineer can continue the work without relying on tribal knowledge.

---

# Closing Principle

We build intentionally.

We document consistently.

We verify continuously.

We improve forever.

Software is not only what runs.

Software is also the knowledge that allows it to continue evolving.