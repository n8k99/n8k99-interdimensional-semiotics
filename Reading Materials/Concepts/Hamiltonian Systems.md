---
title: "Hamiltonian Systems"
type: "[[Concept]]"
icon: "H"
domain: "[[The Commons]]"
Lifestage: "🌱 Seed"
aliases:
  - Hamiltonian system
  - Hamiltonian systems
  - Hamiltonian mechanics
  - Hamilton's equations
tags:
  - interdimensional-semiotics
  - concept
  - mathematics
  - physics
source_concepts:
  - "[[Symplectic Geometry]]"
  - "[[Vector Space]]"
  - "[[Manifold]]"
related:
  - "[[Symplectic Geometry]]"
  - "[[Phase Portraits]]"
  - "[[Chaos Theory]]"
  - "[[Strange Attractors]]"
  - "[[Quantum Mechanics]]"
---

# H Hamiltonian Systems

## Definition

Let $(M, \omega)$ be a $2n$-dimensional [[Symplectic Geometry|symplectic manifold]] and $H : M \to \mathbb{R}$ a smooth function (the **Hamiltonian**). The **Hamiltonian vector field** $X_H$ is uniquely defined by:

$$
i_{X_H}\,\omega \;=\; dH
$$

In canonical coordinates $(q_1, \dots, q_n, p_1, \dots, p_n)$, this produces **Hamilton's equations**:

$$
\dot q_i = \frac{\partial H}{\partial p_i}, \qquad \dot p_i = -\,\frac{\partial H}{\partial q_i}, \qquad i = 1, \dots, n
$$

with two fundamental properties:

$$
\begin{aligned}
\frac{d}{dt}H\bigl(q(t), p(t)\bigr) &= 0 \quad\text{(energy conserved)} \\[4pt]
\mathcal{L}_{X_H}\,\omega &= 0 \quad\text{(symplectic flow, volume-preserving)}
\end{aligned}
$$

## Intuition

A Hamiltonian system is the canonical, energy-conserving way to describe physical processes — from a swinging pendulum to planets orbiting a star — by encoding "where you are" and "how fast you're moving" into a single framework.

### Phase Space as Your Stage

Instead of tracking only position, you track both positions $q_i$ and momenta $p_i$. All these $(q, p)$ pairs live in a $2n$-dimensional space called **phase space**.

### The Hamiltonian $H(q, p)$

This is your energy function — usually kinetic plus potential energy. It assigns a real number (the total energy) to every point in phase space.

### Hamilton's Equations: Nature's Rulebook

The system flows through phase space following two simple rules: velocity comes from how energy changes when you tweak momentum; force (rate of change of momentum) comes from how energy changes when you tweak position.

### Built-in Conservation and Structure

- Energy is automatically conserved: $H(q(t), p(t))$ stays constant along trajectories.
- Volumes in phase space never shrink or expand (**Liouville's theorem**) — the flow is volume-preserving.
- More deeply, the equations preserve the symplectic form $\omega$ — an oriented "area" in each $(q_i, p_i)$ plane that survives the motion unchanged.

## Why It Matters

- It unifies virtually all of classical mechanics under one roof.
- It reveals hidden constants of motion via symmetries (Noether's theorem).
- It provides the starting point for [[Quantum Mechanics]] through canonical quantisation: the classical Hamiltonian becomes the quantum Hamiltonian operator.
- It gives powerful geometric tools — [[Symplectic Geometry]] — to analyse stability, resonances, and chaotic behaviour.

## In the IS Reading List

- [[Penrose - Road to Reality]] — Hamiltonian mechanics, symplectic structure, and the transition to quantum theory (Ch 20, Ch 21)
- [[Lee - Introduction to Topological Manifolds]] — Smooth manifolds and vector fields as the topological substrate of Hamiltonian flows

## Significance for Interdimensional Semiotics

Hamiltonian systems are the archetypal case of a dynamical law that is **deterministic, reversible, and structure-preserving** — exactly the behaviour [[Interdimensional Semiotics]] wants to understand for transformations of meaning. The symplectic form $\omega$ is an [[Topological Invariant|invariant]] of the flow: it is preserved no matter how far the trajectory travels. In IS terms, $\omega$ is what survives [[Monodromy|monodromy]] under energy-conserving dynamics — the template for what a preserved semiotic invariant looks like when the substrate itself is in motion.

More specifically: every symmetry of a Hamiltonian system yields a conserved quantity (Noether's theorem). This is the mathematical version of the IS principle that **invariants emerge from symmetries of the transformation group**. The invariant ring of a [[Monodromy|monodromy group]] is exactly analogous to the Noether-charges of a Hamiltonian symmetry group.

## Related

- [[Symplectic Geometry]]
- [[Phase Portraits]]
- [[Chaos Theory]]
- [[Strange Attractors]]
- [[Quantum Mechanics]]
- [[Manifold]]
- [[Topological Invariant]]
- [[Monodromy]]
- [[Interdimensional Semiotics]]
