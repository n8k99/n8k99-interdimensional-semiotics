---
title: "Symplectic Geometry"
type: "[[Concept]]"
icon: "ω"
domain: "[[The Commons]]"
Lifestage: "🌱 Seed"
aliases:
  - symplectic geometry
  - symplectic form
  - symplectic manifold
  - symplectomorphism
tags:
  - interdimensional-semiotics
  - concept
  - mathematics
source_concepts:
  - "[[Manifold]]"
  - "[[Vector Space]]"
related:
  - "[[Manifold]]"
  - "[[Hamiltonian Systems]]"
  - "[[Phase Portraits]]"
  - "[[Topological Invariant]]"
  - "[[Quantum Mechanics]]"
---

# ω Symplectic Geometry

## Definition

**Symplectic geometry** is the mathematical language of "area preservation" and phase space in classical mechanics. Its central object is a **symplectic form** — a closed, non-degenerate 2-form on a manifold — that lets you measure oriented areas in every pair of coordinate directions.

Let $M$ be a smooth $2n$-dimensional [[Manifold|manifold]]. A **symplectic form** $\omega \in \Omega^2(M)$ satisfies:

$$
\begin{aligned}
d\omega &= 0 \quad\text{(closedness)} \\[4pt]
\forall p \in M:\; \iota_v \omega_p = 0 &\implies v = 0 \quad\text{(non-degeneracy)}
\end{aligned}
$$

The pair $(M, \omega)$ is a **symplectic manifold**.

## Key Structures

### The Symplectic Form $\omega$

A 2-form $\omega$ assigns to each point $p \in M$ a bilinear pairing $\omega_p(v, w)$ on tangent vectors. "Closed" means $d\omega = 0$ — no local sources of area. "Non-degenerate" means $\omega_p$ is a perfect area-detector in every 2D slice; no direction is invisible to it.

### Darboux's Theorem & Canonical Coordinates

Locally, you can always find coordinates $(q_1, \dots, q_n, p_1, \dots, p_n)$ so that:

$$
\omega = \sum_{i=1}^n dq_i \wedge dp_i
$$

There are no other local invariants — all symplectic manifolds look the same in small patches. This is a striking contrast to Riemannian geometry, where local curvature is an invariant. Symplectic geometry is **locally rigid but globally free**: everything interesting happens at the level of global topology.

### Symplectomorphisms & Hamiltonian Flows

Maps that preserve $\omega$ ($\varphi^* \omega = \omega$) are **symplectomorphisms** — the area-preserving diffeomorphisms. Given a function $H$ (the [[Hamiltonian Systems|Hamiltonian]]), the vector field $X_H$ defined by $i_{X_H} \omega = dH$ generates the Hamiltonian flow, which preserves both $\omega$ and phase-space volume (Liouville's theorem).

### Lagrangian Submanifolds

A submanifold $L$ of dimension $n$ (half the ambient dimension) is **Lagrangian** if $\omega|_L = 0$. These are the "maximal flat" (zero-area) slices. Classical examples include configuration space $\{p = 0\}$ and the constant-momentum surfaces $\{q = \text{const}\}$.

## Why It Matters

- It underpins classical mechanics, geometric quantisation, and modern symplectic topology (Floer homology, mirror symmetry).
- It provides a rigorous way to talk about conserved areas, action-angle variables, and the geometric heart of integrability and chaos.
- It is the right home for Hamilton's equations, which are exactly the equations of a [[Hamiltonian Systems|Hamiltonian flow]] on a symplectic manifold.

## In the IS Reading List

- [[Penrose - Road to Reality]] — Symplectic structure as the geometric foundation of classical mechanics (Ch 20); transition to quantum theory via geometric quantisation
- [[Lee - Introduction to Topological Manifolds]] — Differential forms and the 2-form machinery that symplectic geometry exploits

## Significance for Interdimensional Semiotics

Symplectic structure is a rich source of [[Topological Invariant|topological invariants]] — Chern classes of tangent bundles, symplectic cohomology, Gromov-Witten invariants — properties of a symplectic manifold that are fixed under every symplectomorphism. For IS, this is concrete: given a flow on a symplectic substrate, you can name in advance which of its features are guaranteed to survive the flow and which are not.

Moreover, the **locally-rigid, globally-free** character of symplectic geometry is itself an IS lesson. Small neighbourhoods of any two symplectic manifolds look identical (Darboux). All the interesting structure lives at global topology. This matches the IS intuition that **meaning survives local substrate translation trivially; what carries the substantive content of semiotic persistence is global topology.**

## Related

- [[Manifold]]
- [[Hamiltonian Systems]]
- [[Phase Portraits]]
- [[Topological Invariant]]
- [[Vector Space]]
- [[Quantum Mechanics]]
- [[Interdimensional Semiotics]]
