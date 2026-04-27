---
title: "Orthonormal Tangent Vectors"
type: "[[Concept]]"
icon: "⊥"
domain: "[[The Commons]]"
Lifestage: "🌱 Seed"
aliases:
  - orthonormal tangent vectors
  - orthonormal frame
  - orthonormal basis
  - tangent frame
tags:
  - interdimensional-semiotics
  - concept
  - mathematics
source_concepts:
  - "[[Vector Space]]"
  - "[[Manifold]]"
related:
  - "[[Vector Space]]"
  - "[[Manifold]]"
  - "[[Jacobian Matrix]]"
  - "[[Chaos Theory]]"
  - "[[Phase Portraits]]"
---

# ⊥ Orthonormal Tangent Vectors

## Definition

Let $M$ be a smooth $n$-manifold equipped with a Riemannian metric $\langle\cdot,\cdot\rangle$. At each point $p \in M$, the **tangent space** $T_p M$ is an $n$-dimensional real [[Vector Space|vector space]]. A set of vectors $\{e_1, \dots, e_n\} \subset T_p M$ is **orthonormal** if:

$$
\langle e_i, e_j \rangle = \delta_{ij} \quad\text{for all } i, j = 1, \dots, n
$$

That is: each $e_i$ has unit length, and distinct $e_i, e_j$ are mutually perpendicular. An orthonormal set that spans $T_p M$ is an **orthonormal basis** or **orthonormal frame** at $p$.

Specialising to $M = \mathbb{R}^n$ with the usual dot product, each tangent space is just $\mathbb{R}^n$ itself, and orthonormality reduces to $e_i \cdot e_j = 1$ if $i = j$, $0$ otherwise.

## Intuition

Think of standing on a smooth hilltop and planting little arrows: an orthonormal frame is like planting one arrow due north and another due east, each exactly one unit long and at right angles to each other. You can now decompose any instantaneous step into how much of it is "north" and how much "east" — the frame gives you a coordinate system for infinitesimal motion at that point.

## Properties

- **Local, not global.** An orthonormal frame is defined at a single point. As you move along the manifold, you typically cannot extend it consistently to a global frame (unless the manifold is parallelisable — a strong topological condition).
- **Gram-Schmidt construction.** Given any basis of $T_p M$, the Gram-Schmidt process produces an orthonormal basis. This is how orthonormal frames are produced computationally.
- **Connection to measurement.** Once you have an orthonormal frame, lengths and angles are measured by ordinary Euclidean formulas in the frame coordinates. The frame is the bridge between the manifold's intrinsic geometry and concrete computation.
- **Transport and curvature.** Parallel transporting an orthonormal frame along a loop on a curved manifold does not generally return it to itself — the discrepancy is a measure of curvature. This is the same phenomenon that, on multi-sheeted manifolds, shows up as [[Monodromy|monodromy]].

## Practical Use: Lyapunov Exponents

In dynamical-systems computation, you carry a small set of orthonormal tangent vectors along a trajectory through phase space. Periodically you re-orthonormalise them (using Gram-Schmidt) so they stay perpendicular and unit-length. Tracking how each arrow stretches or shrinks over time gives you the **Lyapunov exponents** $\lambda_i$ — the rates at which the system expands or contracts in each independent direction. A positive Lyapunov exponent is the signature of [[Chaos Theory|chaos]]: trajectories diverge exponentially along that direction.

## In the IS Reading List

- [[Penrose - Road to Reality]] — Tangent spaces, Riemannian metrics, and orthonormal frames as the basic machinery of differential geometry (Ch 14)
- [[Lee - Introduction to Topological Manifolds]] — Smooth frames, their existence conditions, and their relation to manifold topology

## Significance for Interdimensional Semiotics

Orthonormal tangent vectors are the computational machinery that makes [[Monodromy|monodromy]] quantifiable in practice. Where the [[Jacobian Matrix|Jacobian]] is the abstract linearisation of a sheet-crossing transformation, the orthonormal frame is the concrete ruler-and-protractor that lets you measure *by how much* the transformation stretches some directions and compresses others. The Lyapunov spectrum computed from a transported orthonormal frame is, in IS terms, a direct measurement of how much semiotic information survives versus disperses under the action of a given dynamical [[Substrate|substrate]].

## Related

- [[Vector Space]]
- [[Manifold]]
- [[Jacobian Matrix]]
- [[Chaos Theory]]
- [[Phase Portraits]]
- [[Strange Attractors]]
- [[Symplectic Geometry]]
- [[Interdimensional Semiotics]]
