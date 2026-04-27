---
title: "Phase Portraits"
type: "[[Concept]]"
icon: "⇝"
domain: "[[The Commons]]"
Lifestage: "🌱 Seed"
aliases:
  - phase portrait
  - phase portraits
  - phase plane
  - phase space diagram
tags:
  - interdimensional-semiotics
  - concept
  - mathematics
  - dynamical-systems
source_concepts:
  - "[[Vector Space]]"
  - "[[Manifold]]"
related:
  - "[[Hamiltonian Systems]]"
  - "[[Symplectic Geometry]]"
  - "[[Chaos Theory]]"
  - "[[Strange Attractors]]"
  - "[[Jacobian Matrix]]"
---

# ⇝ Phase Portraits

## Definition

A **phase portrait** is a graphical tool for visualising how a dynamical system evolves over time in its **state space** (or "phase space"). Instead of plotting individual variables against time, you plot one state variable along the horizontal axis and another along the vertical, then draw:

- **Vector arrows** at a grid of points showing the instantaneous direction and speed of motion (the *flow field*)
- **Sample trajectories** — curves that follow those arrows — starting from different initial points

Every point in this plane (for a two-variable system) represents a complete *state* of the system: position vs. velocity, predator population vs. prey population, voltage vs. current.

## Key Features

### Equilibria & Stability

**Fixed points** are locations where the flow vanishes — equilibrium states. By inspecting how nearby arrows point (toward, away, or past), you classify the equilibrium:

- **Stable fixed point (attractor)** — nearby trajectories spiral or settle in
- **Unstable fixed point (repellor)** — nearby trajectories flee outward
- **Saddle** — attracts in one direction, repels in another

The classification is determined by the eigenvalues of the [[Jacobian Matrix|Jacobian]] evaluated at the fixed point.

### Trajectories

If you pick an initial point and follow the arrows, you trace out the solution curve. Overlaying many such trajectories gives the portrait of all possible behaviours the system can exhibit.

### Attractors and Limit Cycles

Repeating or bounded behaviour shows up as **closed loops** (limit cycles) or **strange-shaped regions** (see [[Strange Attractors]]). Unbounded motion runs off to infinity in the portrait.

## Why It Is Useful

- **Qualitative insight.** You see all possible motions at once — who moves toward equilibrium, who oscillates, who diverges — without solving the equations in closed form.
- **Stability analysis.** You classify fixed points by local arrow patterns, avoiding the algebra.
- **Chaos visualisation.** For three-dimensional or higher systems, you project onto 2D slices or render 3D plots to reveal fractal strange attractors (e.g. the Lorenz butterfly).

In practice: choose your state variables $(x, y)$, compute the vector field $(\dot x, \dot y)$, then let software or hand-sketching produce the plot. The resulting phase portrait is the **fingerprint** of your system's dynamics.

## In the IS Reading List

- [[Penrose - Road to Reality]] — Phase-space reasoning as a tool across classical and quantum mechanics (Ch 20-21)
- [[Lee - Introduction to Topological Manifolds]] — The topological context in which phase portraits live: flows on manifolds

## Significance for Interdimensional Semiotics

Phase portraits are the canonical picture of a **dynamical landscape** — the set of all possible behaviours of a system rendered in a single geometric object. For IS, this is the visual template for thinking about semiotic dynamics: *which interpretations are attractors? Which are saddles that tip context one way or the other? Where are the limit cycles of interpretation — the readings a text keeps falling back into no matter where the reader starts?*

More technically, a phase portrait makes the distinction between **local** and **global** structure operational: local structure is what the [[Jacobian Matrix|Jacobian]] eigenvalues tell you at a single point; global structure is the overall topology of the flow (how attractor basins tile the space, where saddle connections run). IS invariants live at both levels — some preserved pointwise, some only globally — and phase portraits are the most direct picture of the difference.

## Related

- [[Hamiltonian Systems]]
- [[Symplectic Geometry]]
- [[Chaos Theory]]
- [[Strange Attractors]]
- [[Jacobian Matrix]]
- [[Orthonormal Tangent Vectors]]
- [[Manifold]]
- [[Interdimensional Semiotics]]
