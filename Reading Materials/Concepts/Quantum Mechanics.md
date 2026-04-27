---
title: "Quantum Mechanics"
type: "[[Concept]]"
icon: "ψ"
domain: "[[The Commons]]"
Lifestage: "🌱 Seed"
aliases:
  - quantum mechanics
  - quantum theory
  - QM
  - wavefunction
tags:
  - interdimensional-semiotics
  - concept
  - physics
source_concepts:
  - "[[Vector Space]]"
  - "[[Hamiltonian Systems]]"
related:
  - "[[Hamiltonian Systems]]"
  - "[[Symplectic Geometry]]"
  - "[[Vector Space]]"
  - "[[Speed of Light]]"
  - "[[Incompleteness]]"
  - "[[HEMM Space]]"
---

# ψ Quantum Mechanics

## Definition

**Quantum mechanics** is the framework that replaces classical point-particle mechanics at microscopic scales. A physical system is represented by a state vector $|\psi\rangle$ in a complex Hilbert space $\mathcal{H}$; observables are Hermitian operators; measurement outcomes are operator eigenvalues with probabilities given by the state; evolution between measurements is unitary and deterministic.

$$
\begin{aligned}
&\textbf{1. State Space:}\quad |\psi\rangle \in \mathcal{H}\ (\text{complex Hilbert space}) \\[4pt]
&\textbf{2. Observables:}\quad A = A^\dagger,\quad A|\phi_a\rangle = a\,|\phi_a\rangle,\; \Pr(a)=\langle\psi|P_a|\psi\rangle \\[4pt]
&\textbf{3. Measurement:}\quad |\psi\rangle \;\xrightarrow{\text{measure }A=a}\; \frac{P_a|\psi\rangle}{\sqrt{\langle\psi|P_a|\psi\rangle}} \\[4pt]
&\textbf{4. Time Evolution:}\quad i\hbar\,\frac{d}{dt}|\psi(t)\rangle = H\,|\psi(t)\rangle,\quad U(t)=e^{-iHt/\hbar} \\[4pt]
&\textbf{5. Uncertainty:}\quad \sigma_A\,\sigma_B \;\ge\; \tfrac{1}{2}\bigl|\langle[A,B]\rangle\bigr| \\[4pt]
&\textbf{6. Composite Systems:}\quad |\Psi\rangle \in \mathcal{H}_1\otimes\mathcal{H}_2,\; \rho_i = \mathrm{Tr}_{j\neq i}\bigl(|\Psi\rangle\langle\Psi|\bigr)
\end{aligned}
$$

## Core Principles

### A Wave of Possibilities

Instead of "the particle is here," QM assigns a **wavefunction** $\psi$ (or state vector $|\psi\rangle$) to every system. The wavefunction encodes probabilities — where you are likely to find the particle, how likely it is to have a given energy. The **Born rule** says: probability of outcome = amplitude squared. You apply a **measurement operator** (Hermitian) to the state; each possible result is an eigenvalue; the system collapses into the corresponding eigenstate after measurement. You cannot predict a single outcome with certainty — only the odds.

### Smooth Evolution Between Measurements

When you are not measuring, the wavefunction obeys the **Schrödinger equation**, a deterministic linear rule:

$$
i\hbar\,\frac{\partial}{\partial t}\psi = H\,\psi
$$

where $H$ is the system's [[Hamiltonian Systems|Hamiltonian operator]]. This evolution is perfectly reversible and preserves total probability.

### Uncertainty By Design

Certain pairs of quantities — most famously position and momentum — cannot both be known to arbitrary precision. **Heisenberg's inequality**:

$$
\sigma_x\,\sigma_p \ge \frac{\hbar}{2}
$$

tells you that the more sharply you pin down one, the fuzzier the other becomes. This is not a limitation of instruments — it is built into nature's rules.

### Superposition and Interference

Because the theory is linear, you can **add** wavefunctions. If $\psi_1$ says "particle at A" and $\psi_2$ says "particle at B," then $\psi_1 + \psi_2$ says "particle is in a quantum blend of A and B." When these overlapping possibilities evolve, they **interfere** — producing the rippling patterns of the double-slit experiment.

### Entanglement and Nonlocal Correlations

When two particles interact, they can become **entangled** — you cannot describe one without referencing the other, even across astronomical distances. Measuring one instantly updates your description of the other (Einstein's "spooky action at a distance"). No faster-than-light communication occurs, but the correlations defy any simple classical picture of independent, pre-set properties.

## In the IS Reading List

- [[Penrose - Road to Reality]] — The full apparatus of QM in physical-geometric context (Ch 21-26); Penrose's own views on measurement, consciousness, and quantum gravity
- [[Kaku - Hyperspace]] — Higher-dimensional generalisations of QM and their cosmological implications
- [[Hofstadter - Godel Escher Bach]] — The role of formal undecidability and self-reference, which echoes structurally with QM's measurement problem

## Significance for Interdimensional Semiotics

Quantum mechanics is the canonical example of a physics in which **meaning (outcome) is substrate-dependent**: the same $|\psi\rangle$ yields different results depending on the measurement apparatus, because the apparatus selects the basis in which the state is expressed. For IS, this is the sharpest available illustration of a principle the semiotic reading list circles around: *meaning is not intrinsic to the signified — it is co-determined by the substrate of measurement.* The observer's choice of basis is the substrate; the wavefunction is the signifier; the measurement outcome is the sign extracted from their interaction.

QM also provides the **complex Hilbert space formalism** that [[HEMM Space]] generalises. The 3×2 state matrix over $\mathbb{C}$ is structurally analogous to a quantum state vector — a composite object with coordinate and spin columns, lying in a complex [[Vector Space|vector space]], acted on by a group of unitary-like transformations. The mathematical kinship is not coincidence; both are attempts to describe systems whose identity is not a point but a distribution over possibilities.

Finally, **entanglement** is the clearest natural-world model of what IS calls *non-local invariants*: properties that cannot be attributed to either sub-system alone but persist only in the joint description. The Ghost-across-surfaces phenomenon ([[Ghost]] concept) has this structure — the Ghost exists in the joint system of nexus + surface, not in either alone.

## Related

- [[Hamiltonian Systems]]
- [[Symplectic Geometry]]
- [[Vector Space]]
- [[Speed of Light]]
- [[Incompleteness]]
- [[Self-Reference]]
- [[HEMM Space]]
- [[Interdimensional Semiotics]]
