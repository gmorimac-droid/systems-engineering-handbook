# Conventions and Notation

## Purpose

This page defines the editorial and technical conventions used across the handbook. Consistent notation and terminology improve readability, reduce ambiguity, and support traceability across sections.

## Editorial Conventions

### File and Page Naming

Repository file names use lowercase words separated by hyphens. Page titles use title case. File names are chosen to be descriptive, stable, and semantically aligned with the subject they describe.

### Controlled Vocabulary

The handbook uses selected terms with deliberately constrained meanings. For example:

- **Need** expresses an externally meaningful problem, objective, or expected capability.
- **Requirement** expresses a stated condition, capability, constraint, or performance level that the system must satisfy.
- **Function** expresses what the system does.
- **Component** expresses a structural element of the system.
- **Interface** expresses an interaction boundary between elements.
- **Verification** asks whether the system was built correctly with respect to specified requirements.
- **Validation** asks whether the correct system was built for its intended use.
- **Baseline** expresses an approved technical reference state subject to control.

These terms are used consistently throughout the handbook unless a page explicitly introduces a narrower context.

## Referencing Conventions

Internal references should use repository-relative paths when discussing page relationships in prose. This helps preserve the connection between conceptual descriptions and the project structure.

Artifact names should be written consistently. For example:

- Concept of Operations (ConOps)
- System Requirements Specification (SRS)
- Interface Control Document (ICD)
- Verification Cross-Reference Matrix (VCRM)

## Diagram and Model Conventions

Where diagrams are introduced later in the project, they should aim to distinguish clearly between:

- operational context
- functional decomposition
n- logical architecture
- physical architecture
- interface view
- lifecycle or process flow

A diagram should never attempt to communicate too many viewpoints simultaneously.

## Requirement Identifier Convention

When requirements are added to the case study, identifiers should follow a structured convention such as:

- `AIIDS-SYS-REQ-001`
- `AIIDS-IF-REQ-014`
- `AIIDS-OPS-REQ-003`

The identifier should reveal at least the system context and the requirement class.

## Assumptions and Constraints

Assumptions and constraints should be stated explicitly and not embedded implicitly in prose. If a statement materially affects architecture, verification, cost, safety, or operations, it should be represented in a form that can be reviewed and traced.

## Related Sections

- `reference/glossary.md`
- `requirements/requirements-writing-guidelines.md`
- `artifacts/system-requirements-specification-template.md`
