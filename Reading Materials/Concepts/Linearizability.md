---
title: "Linearizability"
type: "[[Concept]]"
domain: "[[The Commons]]"
Lifestage: "🌱 Seed"
tags:
  - interdimensional-semiotics
  - concept
aliases:
  - Atomic Consistency
---

Linearizability, also called atomic consistency, is the strongest standard consistency condition for distributed data. As defined in [[Gilbert Lynch - Brewers Conjecture and the CAP Theorem|Gilbert and Lynch §2.1]], it requires that all operations on a distributed object appear to execute instantaneously at some point between their invocation and response, and that these execution points form a total order consistent with real time. A read that begins after a write completes must return that write's value or a later one — never a stale value. The system behaves as if there is a single copy of the data, updated atomically, even though the data is physically replicated across nodes. Linearizability is the gold standard that the CAP theorem proves cannot be maintained simultaneously with availability under network partitions.

## Cross-Book Development

Gilbert and Lynch use linearizability as the precise definition of "consistency" in the CAP theorem. Their proof constructs a partitioned network in which an available system must respond to both sides of the partition, but cannot propagate writes between them — so a read on one side must either return a stale value (violating linearizability) or the system must refuse to respond (violating availability). The impossibility is tight: linearizability is exactly the consistency model that cannot coexist with availability and partition tolerance. They then introduce Delayed-t consistency as a weakened alternative — linearizability holds except within a window of t time units around a partition, giving systems a practical escape at the cost of temporary staleness. [[Dwork Lynch Stockmeyer - Consensus in the Presence of Partial Synchrony|Dwork, Lynch, and Stockmeyer's]] consensus protocols aim to establish linearizable agreement on a decision value among distributed processes. Their consensus problem requires agreement (all correct processes decide the same value), validity (the decided value was proposed by some process), and termination (all correct processes eventually decide). This is linearizability applied to a single decision: the system must behave as if all processes decided at a single instant, in a single total order. The DLS resilience bounds quantify the cost of this guarantee — how many faulty processes can be tolerated while still achieving linearizable consensus. [[Halpern Moses - Knowledge and Common Knowledge in a Distributed Environment|Halpern and Moses]] reveal the epistemic foundation beneath linearizability: for a system to be linearizable, all participants must effectively share knowledge of the current state. A linearizable read requires that the reader knows the result of all prior writes — which, in the epistemic framework, requires a form of common knowledge about the system's history. The impossibility of common knowledge under unreliable communication is thus the deep reason why linearizability is incompatible with partitions.

## Significance for Interdimensional Semiotics

Linearizability is the condition where all observers agree on the same sequence of semiotic events — the same meaning, in the same order, at the same time. It is the ideal that substrate independence aspires to: a poem should mean the same thing whether read in English or Japanese, whether processed by a human mind or a machine, whether encountered in 1924 or 2024. If the semiotic system were linearizable, every agent observing a sign would derive the same interpretation, and the order of semiotic events (this metaphor was coined before that allusion, this text influenced that text) would be universally agreed upon. The CAP theorem tells us this ideal cannot be maintained across partitions — across dimensional boundaries, substrate transitions, cultural divides. When meaning crosses a partition, linearizability breaks. Two communities separated by language, by time, by medium will develop divergent readings of the same source text, and these readings cannot be atomically reconciled without halting interpretation (sacrificing availability) or ignoring the partition (pretending it does not exist). The IS framework therefore works with weaker consistency models. Meaning persistence is not linearizability — it is eventual convergence, the guarantee that meaning will stabilize across substrates given sufficient time and communication, not that it is identical at every instant. Semiotic gravitational mass determines the convergence rate: high-mass signs approach linearizable consistency rapidly (mathematical notation, musical scales, archetypal narratives), while low-mass signs may permanently exhibit the staleness that linearizability forbids. The Noosphere is not a linearizable system. It is an eventually consistent one, and the IS framework's power comes from accepting this and building interpretive tools — InnateScript among them — that operate correctly under eventual consistency rather than demanding the atomic agreement that the theorems prove impossible.

## In the IS Reading List

- Gilbert/Lynch §2.1: formal definition of linearizability (atomic consistency)
- Gilbert/Lynch §3: proof that linearizability is incompatible with availability under partitions
- Gilbert/Lynch §4: Delayed-t consistency as a weakened linearizability
- DLS §3: consensus as linearizable agreement on a single value
- Halpern/Moses §5-6: epistemic conditions (common knowledge) underlying linearizable coordination

## Related

- [[CAP Theorem]]
- [[Partition Tolerance]]
- [[Delayed-t Consistency]]
- [[Common Knowledge]]
- [[Consensus]]
