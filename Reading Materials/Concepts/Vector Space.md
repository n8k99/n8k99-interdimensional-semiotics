---
title: "Vector Space"
type: "[[Concept]]"
icon: "→"
domain: "[[The Commons]]"
Lifestage: "🌱 Seed"
aliases:
  - vector space
  - vector spaces
  - linear space
tags:
  - interdimensional-semiotics
  - concept
  - mathematics
source_concepts: []
related:
  - "[[Manifold]]"
  - "[[Jacobian Matrix]]"
  - "[[Symplectic Geometry]]"
  - "[[Orthonormal Tangent Vectors]]"
  - "[[Quantum Mechanics]]"
---

# → Vector Space

## Definition

A **vector space** over a field $F$ is a nonempty set $V$ equipped with two operations — **addition** $+ : V \times V \to V$ and **scalar multiplication** $\cdot : F \times V \to V$ — satisfying the following axioms for all $u, v, w \in V$ and $a, b \in F$:

$$
\begin{aligned}
&(1)\;u+v = v+u \quad\text{(commutativity)}\\
&(2)\;(u+v)+w = u+(v+w)\quad\text{(associativity)}\\
&(3)\;\exists\,0_V\in V:\;u+0_V = u\quad\text{(additive identity)}\\
&(4)\;\forall u\,\exists\,(-u)\in V:\;u+(-u)=0_V\quad\text{(additive inverse)}\\
&(5)\;a\,u\in V\quad\text{(closure under scalars)}\\
&(6)\;a\,(u+v)=a\,u + a\,v\quad\text{(distributivity over vector addition)}\\
&(7)\;(a+b)\,u = a\,u + b\,u\quad\text{(distributivity over field addition)}\\
&(8)\;(ab)\,u = a\,(b\,u)\quad\text{(compatibility of scalar multiplication)}\\
&(9)\;1_F\,u = u\quad\text{(unit property).}
\end{aligned}
$$

In plain terms: you have a collection of "vectors" (these can be arrows, number tuples, functions, matrices — anything that behaves the right way) and a field of "scalars" (for example $\mathbb{R}$ or $\mathbb{C}$). You can add two vectors and get a vector; you can scale a vector by a scalar and get a vector; and both operations play nicely together (commutativity, associativity, distributivity, a zero, inverses, and a unit).

## Properties

- **Dimension.** Every vector space has a well-defined dimension — the cardinality of a basis. Finite-dimensional spaces behave much more tamely than infinite-dimensional ones.
- **Linear transformations.** Maps between vector spaces that preserve addition and scalar multiplication are the natural morphisms. The set of linear maps $V \to V$ forms the algebra $\text{End}(V)$; the invertible ones form the general linear group $GL(V)$.
- **Inner products.** Adding an inner product gives angles, lengths, and orthogonality — turning a vector space into an inner-product space. See [[Orthonormal Tangent Vectors]].
- **Tensor products and duals.** Vector spaces combine: $V \otimes W$, $V^*$, $\text{Hom}(V, W)$. The whole apparatus of linear algebra is the theory of these combinations.

## Why It Matters

Vector spaces guarantee that vectors "add like arrows" and "scale like stretching," letting you do geometry and algebra in a very wide variety of settings. Almost every computation in physics, engineering, and applied mathematics reduces to a problem in vector spaces — because linearisation (see [[Jacobian Matrix]]) turns local questions about smooth functions into linear ones.

## In the IS Reading List

- [[Penrose - Road to Reality]] — Vector spaces as the foundation of differential geometry and physics (Ch 11-13); tangent spaces at a point of a manifold are vector spaces
- [[Lee - Introduction to Topological Manifolds]] — Tangent spaces as the canonical vector spaces associated to smooth manifolds
- [[Hofstadter - Godel Escher Bach]] — Formal systems and their models; vector spaces appear as semantic models in certain formalisations

## Significance for Interdimensional Semiotics

The state space of [[HEMM Space]] is defined on the complex vector space $\mathbb{C}^{3 \times 2}$: three spatial dimensions × two columns (coordinate and spin), with entries in $\mathbb{C}$. Every [[Monodromy|monodromy transformation]] is an element of $GL(3 \times 2, \mathbb{C})$ — an invertible linear map on this vector space. The [[Topological Invariant|topological invariants]] of the manifold are precisely the functions on the state vector space that are fixed by the monodromy group's action.

At a higher level of abstraction, vector spaces are the canonical example of a structure where the same abstract object ($V$) can be realised in countless concrete forms (arrows, tuples, polynomials, function spaces). This is itself an IS lesson: the concept of vector-space-as-such is a semiotic invariant across enormously different realisations. [[Quantum Mechanics]] relies on this: the Hilbert space of a quantum system is a vector space, and the state vector $|\psi\rangle$ lives in it regardless of whether we are describing electrons, photons, or qubits.

## Related

- [[Manifold]]
- [[Jacobian Matrix]]
- [[Symplectic Geometry]]
- [[Orthonormal Tangent Vectors]]
- [[Quantum Mechanics]]
- [[Hamiltonian Systems]]
- [[HEMM Space]]
- [[Interdimensional Semiotics]]
