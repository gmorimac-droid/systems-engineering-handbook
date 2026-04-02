# Allocation of Functions to Elements

## Purpose

This page defines how logical system functions are allocated to architectural elements. Allocation is one of the key engineering activities that transforms requirements and logical architecture into an implementable system structure.

## Context

In the current project baseline, the Autonomous Infrastructure Inspection Drone System has already been described in terms of logical functions and high-level physical elements. This page connects those two views by assigning functional responsibilities to the elements that will realize them.

## Why Allocation Matters

Function allocation is essential because it:

- turns abstract capability into design responsibility
- clarifies what each system element is expected to do
- reveals overloaded or weakly defined components
- supports interface definition
- enables verification planning at element and integration levels
- provides the basis for trade studies and architecture refinement

## Allocation Principles

The allocation process follows these principles:

1. Every critical logical function shall be assigned to at least one responsible element.
2. Allocation shall preserve traceability to requirements.
3. Allocation shall not obscure interface dependencies.
4. Safety-related functions shall be explicitly allocated.
5. Human responsibilities shall be represented where the operator remains part of the operational system.

## Main Architectural Elements

At the current level of maturity, the main architectural elements are:

- Flight Control System
- Navigation Subsystem
- Payload System
- Communication System
- Power System
- Ground Control Station
- Operator
- Safety Management Logic
- Data Storage and Processing Environment

## Allocation Matrix

| Logical Function ID | Logical Function | Allocated Element(s) | Allocation Rationale |
|---|---|---|---|
| LF-01 | Mission Planning and Initialization | Ground Control Station, Operator | Mission definition and initialization require human intent and ground-based planning capability. |
| LF-02 | System Readiness and Health Management | Flight Control System, Power System, Payload System, Communication System | Readiness depends on distributed subsystem status and centralized health evaluation. |
| LF-03 | Flight Control and Stabilization | Flight Control System | Stable autonomous flight requires a dedicated control authority. |
| LF-04 | Navigation and Position Management | Navigation Subsystem, Flight Control System | Navigation requires sensing, estimation, and execution coordination. |
| LF-05 | Payload Operation and Inspection Data Acquisition | Payload System | Mission inspection effectiveness depends on a dedicated payload responsibility. |
| LF-06 | Communications and Data Exchange | Communication System, Ground Control Station | Uplink and downlink functions are shared across airborne and ground segments. |
| LF-07 | Operator Interaction and Mission Supervision | Ground Control Station, Operator | Human supervision is executed through the ground interface and operational oversight. |
| LF-08 | Safety Management and Contingency Response | Safety Management Logic, Flight Control System, Operator | Safe response requires embedded autonomy with operator visibility and intervention capability. |
| LF-09 | Mission Data Management and Post-Mission Availability | Payload System, Communication System, Data Storage and Processing Environment | Data must be captured, transferred, and preserved across multiple elements. |

## Allocation Interpretation

The matrix shows that some functions map cleanly to single elements, while others require shared realization across the system. This is normal in complex systems. Allocation should not be misread as a claim that each function belongs exclusively to one component; rather, it identifies the primary realization responsibility and the supporting actors.

## Relationship to Requirements

Allocation directly supports requirement realization. Examples include:

- `FR-001` is primarily realized by the Flight Control System and supported by Navigation and Safety functions
- `FR-002` is primarily realized by the Payload System
- `FR-003` is primarily realized by the Communication System and Ground Control Station
- `PR-001` depends strongly on the Power System and efficient behavior of mission functions
- `IR-001` is realized through the Ground Control Station and communications interfaces

## Allocation Review Criteria

A sound allocation review should confirm that:

- every mission-critical logical function has an identified implementing element
- safety responsibilities are explicit
- human and machine roles are appropriately balanced
- no architectural element exists without meaningful responsibility
- shared allocations are supported by identifiable interfaces

## Common Failure Modes

Frequent allocation weaknesses include:

- assigning functions to components too early without logical justification
- omitting the operator from the system view
- allocating safety responsibilities only implicitly
- creating elements with vague or overlapping roles
- failing to revisit allocation after requirement changes

## Engineering Implications

Function allocation is not the end of architecture work. It drives the next layer of engineering detail, including:

- interface definition
- physical architecture refinement
- subsystem responsibilities
- verification decomposition
- integration planning

## Related Pages

- `architecture/logical-architecture.md`
- `architecture/physical-architecture.md`
- `architecture/interface-architecture.md`
- `requirements/requirements-allocation.md`
- `case-study/architecture-baseline.md`
- `case-study/requirements-baseline.md`
