---
title: "Jacobian Matrix"
type: "[[Concept]]"
icon: "∂"
domain: "[[The Commons]]"
Lifestage: "🌱 Seed"
aliases:
  - Jacobian matrix
  - Jacobian
  - Jacobian determinant
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
  - "[[Monodromy]]"
  - "[[Hamiltonian Systems]]"
  - "[[Phase Portraits]]"
---

# ∂ Jacobian Matrix

## Definition

The **Jacobian matrix** of a differentiable function $F : \mathbb{R}^n \to \mathbb{R}^m$ at a point $x$ is the matrix of all first-order partial derivatives:

$$
J_F(x) \;=\; \frac{\partial (f_1,\dots,f_m)}{\partial (x_1,\dots,x_n)} \;=\;
\begin{pmatrix}
\frac{\partial f_1}{\partial x_1} & \cdots & \frac{\partial f_1}{\partial x_n} \\[6pt]
\vdots & \ddots & \vdots \\[6pt]
\frac{\partial f_m}{\partial x_1} & \cdots & \frac{\partial f_m}{\partial x_n}
\end{pmatrix}
$$

It is the **best linear approximation** of $F$ near $x$: in a small neighbourhood, $F(x + \delta) \approx F(x) + J_F(x)\,\delta$. The Jacobian generalises the ordinary derivative from one-dimensional calculus to maps between spaces of arbitrary dimension.

## Properties

- **Linearisation.** Near any point at which $F$ is differentiable, the Jacobian is the linear map that best approximates $F$'s behaviour on infinitesimal displacements.
- **Chain rule.** For composed maps, Jacobians multiply: $J_{G \circ F}(x) = J_G(F(x)) \cdot J_F(x)$.
- **Jacobian determinant.** When $m = n$, $\det J_F(x)$ measures local volume scaling: it is positive for orientation-preserving, negative for orientation-reversing, and zero at singularities where $F$ collapses dimension.
- **Inverse function theorem.** If $\det J_F(x) \neq 0$, then $F$ is locally invertible near $x$, and the inverse's Jacobian is $J_F(x)^{-1}$.
- **Change of variables.** In multivariable integration, $|\det J_F|$ is the factor converting volumes in the source space to volumes in the target.

## In the IS Reading List

- [[Penrose - Road to Reality]] — Derivatives on manifolds, tangent vectors, and Jacobian-like linearisations as foundational tools of differential geometry (Ch 10-12)
- [[Lee - Introduction to Topological Manifolds]] — The Jacobian reappears in the definition of smooth maps between manifolds: a map is smooth iff its coordinate representations have continuous partial derivatives, i.e. well-defined Jacobians

## Significance for Interdimensional Semiotics

The Jacobian is the local-linear skeleton of every [[Monodromy|monodromy transformation]]. Whatever the global topology of the map from one [[Sheet|sheet]] of a manifold to another, at every non-singular point the transformation is approximated by a Jacobian matrix — a concrete, computable linear map telling you exactly how infinitesimal displacements on the source sheet are carried to infinitesimal displacements on the destination sheet. Branch points of the manifold appear as precisely the places where the Jacobian becomes singular ($\det J_F = 0$): the places where the linear approximation fails and the transformation's true multi-valued, sheet-crossing character is forced to show itself.

For [[Phase Portraits|phase-portrait analysis]] and stability theory, the Jacobian evaluated at a fixed point is the eigenvalue problem that classifies the point as attractor, repellor, saddle, or centre. In IS terms, the Jacobian is what lets you *measure* the character of a semiotic equilibrium from local data.

## Related

- [[Vector Space]]
- [[Manifold]]
- [[Monodromy]]
- [[Hamiltonian Systems]]
- [[Phase Portraits]]
- [[Orthonormal Tangent Vectors]]
- [[Symplectic Geometry]]
- [[Interdimensional Semiotics]]
