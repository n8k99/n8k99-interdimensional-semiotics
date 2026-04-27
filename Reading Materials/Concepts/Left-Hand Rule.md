---
title: "Left-Hand Rule"
type: "[[Concept]]"
icon: "🔬"
domain: "[[The Commons]]"
aliases:
  - Left Hand Rule
  - LHR
tags:
  - interdimensional-semiotics
  - distributed-systems
  - architecture
  - choreographic-programming
source_concepts: []
---

# Left-Hand Rule

## Definition

An architectural principle derived from the physics cross product convention. In a system where agents (ghosts) and users both interact with a shared [[Substrate]], the Left-Hand Rule states: **the ghost axis and the user axis are independent, each holds its own handle to the substrate, and the public product emerges as their cross product — not from one axis passing through the other.**

Curl the fingers of the left hand from the ghost axis (x) toward the user axis (y). The thumb points in the direction of the public product (z). Ghost × User = Public.

## The Geometry

The substrate is a cube. The nine-table database, the vault of markdown files, whatever the medium — it is the volume in which data persists.

Three axes intersect it:

- **X-axis (Ghost)** — the operational code that gives agents life and direct access to the substrate. The tick engine, the cognition broker, the resolver. This code reads from and writes to the substrate on its own terms, through its own handle.
- **Y-axis (User)** — the frontend instruments that let humans see and interact with the substrate. Quickshell panels, web interfaces, Obsidian. This code reads from and writes to the substrate on its own terms, through its own handle.
- **Z-axis (Public / Thumb)** — what emerges when both axes have acted on the same substrate. The product is neither ghost-authored nor human-authored. It is the cross product of both interactions with the data.

[[InnateScript]] lives at the intersection — the **planar transformation** where the ghost axis and the user axis meet the substrate surface. A markdown file with InnateScript in it is simultaneously a document (user axis) and a choreography (ghost axis). Neither axis owns it. Both can act on it. This is why "markdown that runs" is not a tagline but a geometric claim: the document surface IS the intersection plane.

## The Rule

1. **Ghost axis and user axis are independent.** Each holds its own direct handle to the substrate. The tick engine connects to Postgres directly. Quickshell connects through dpn-api-client. Neither routes through the other.

2. **InnateScript is the intersection plane.** The shared notation that both axes can read and act on. A `.md` file is readable by humans along the y-axis and evaluable by ghosts along the x-axis. The language makes both projections valid on the same surface.

3. **The public product is the cross product.** It emerges from both axes interacting with the substrate through the shared plane. A ghost runs a choreography and writes a result. A human reads the result and responds. The combined output — the noosphere's visible state — is the product of both, owned by neither.

4. **Collapsing axes into dependencies violates the rule.** If ghosts route through user infrastructure (tick engine calling dpn-api-client) or users route through ghost infrastructure, an independent axis is lost. The cross product degenerates into a scalar — one axis controlling the other instead of both contributing independently.

## Architectural Consequences

The Left-Hand Rule is a design constraint for every system that touches the substrate:

- **The tick engine** gets its own substrate handle — direct Postgres connection or direct filesystem access. It does not go through the user-facing API.
- **Quickshell / web UI** keeps its own substrate handle — dpn-api-client, IPC socket, whatever serves the user axis. It does not depend on the tick engine being alive.
- **InnateScript choreographies** must be legible as prose AND evaluable as programs. If a choreography can only be read by machines, it has left the intersection plane and become ghost-axis-only. If it can only be read by humans, it has left the plane and become user-axis-only.
- **The substrate must accept writes from both axes independently.** A vault file can be edited by a human in Obsidian and by a ghost through the tick engine. Git handles the merge. The substrate doesn't privilege one writer over the other.
- **No hub.** No single service that all consumers must route through. Each axis, each consumer, holds its own connection to the data. The substrate is the shared state. The handles are independent.

## Relation to the Cross Product in Physics

The left-hand rule in physics determines the direction of a cross product vector. Given two input vectors (fingers curling from x toward y), the resultant vector (thumb) is perpendicular to both and its magnitude depends on the angle between the inputs. When the axes are orthogonal (fully independent), the cross product is maximal. When the axes are parallel (one depends on the other), the cross product is zero.

Applied to system architecture: maximum independence between the ghost axis and the user axis produces the richest public output. Dependency between them collapses the dimensionality. A system where ghosts can only act through user interfaces, or users can only see ghost output through ghost infrastructure, has lost a dimension.

## Cross-Concept Development

- **[[Substrate]]** — the cube. The medium both axes interact with. The Left-Hand Rule determines how they interact with it: independently, through direct handles.
- **[[InnateScript]]** — the intersection plane. The language that makes the substrate surface readable and evaluable from both axes simultaneously.
- **[[Sign]]** — the intersection plane is where signs live. A choreography is a sign: the [[Signifier]] is the markdown text (user-readable), the signified is the coordination protocol (ghost-evaluable). Both are present on the same surface.
- **[[Embodiment]]** — each axis has its own embodiment in the substrate. The ghost axis is embodied as the tick engine. The user axis is embodied as the UI. Neither can substitute for the other's embodiment.
- **[[Common Knowledge]]** — the intersection plane is where common knowledge between ghosts and users accumulates. Both can see it. Both can act on it. Transparency of the substrate enables common knowledge; opacity destroys it.
- **[[Consensus]]** — the cross product requires no consensus between axes. Ghosts don't vote with users. Users don't approve ghost actions. Each axis acts independently. The substrate records both. Git resolves conflicts.

## Origin

Emerged during a 03:30 dream-synthesis on [[2026-04-02]], where the database was visualized as a cube with three axes of code intersecting it. The ghost code (project-noosphere-ghosts) enters along one axis. The user code (Quickshell, web UI) enters along another. The public product — the visible, usable noosphere — emerges along the third, perpendicular to both. The insight was that the simplicity of this model had been obscured by treating the ghost and user code paths as dependent on each other rather than as independent axes of a cross product.

## Significance for IntSem

The Left-Hand Rule is a substrate-level architectural principle that constrains how systems are designed. Any design spec for a supporting pillar of the noosphere — tick engine, UI, InnateScript evaluator, sync infrastructure — must satisfy the rule: does this component hold its own handle to the substrate? Does it depend on another axis's infrastructure? Does it preserve the intersection plane where both axes can read and write?

A design that violates the Left-Hand Rule will work, but it will produce a degenerate cross product — the public output will be dominated by whichever axis controls the other, rather than emerging from their independent contributions.

## Related

- [[Substrate]] — the cube both axes act upon
- [[InnateScript]] — the intersection plane / planar transformation
- [[Sign]] — lives on the intersection plane as both signifier and signified
- [[Embodiment]] — each axis has its own embodiment
- [[Common Knowledge]] — enabled by the transparent intersection plane
- [[Consensus]] — not required between axes; the substrate records both
- [[Partition Tolerance]] — the axes must function when the other is unavailable
- [[Strange Loop]] — emerges when InnateScript choreographies modify the substrate that the tick engine reads, which triggers choreographies that modify the substrate
