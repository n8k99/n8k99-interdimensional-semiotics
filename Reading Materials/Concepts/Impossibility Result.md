---
title: "Impossibility Result"
type: "[[Concept]]"
domain: "[[The Commons]]"
Lifestage: "🌱 Seed"
tags:
  - interdimensional-semiotics
  - concept
aliases: []
---

# Impossibility Result

An impossibility result is a mathematical proof that a certain combination of desirable properties cannot be simultaneously achieved by any system, regardless of how cleverly it is designed. Unlike engineering failures, which can be overcome with better hardware or smarter algorithms, impossibility results are structural — they reveal that the desired properties are logically contradictory under the given assumptions. The three distributed systems papers in this reading cluster each prove one, and taken together they map the fundamental limits of coordination, knowledge, and consistency in any system where components communicate by passing messages. These are not pessimistic conclusions but clarifying ones: they tell you exactly what trade-offs you face and free you from wasting effort on solutions that cannot exist.

The intellectual lineage connects to the deepest results in logic and mathematics. Godel's incompleteness theorems (1931) showed that no consistent formal system can be both complete and decidable. Turing's halting problem (1936) showed that no algorithm can determine whether an arbitrary program terminates. Arrow's impossibility theorem (1951) showed that no ranked voting system can satisfy a small set of fairness criteria simultaneously. The distributed systems impossibility results are of the same species: they establish permanent boundaries on what can be computed, communicated, or coordinated. They do not say "this is hard"; they say "this is impossible, and here is the proof." The appropriate response is not despair but design — understanding the impossibility sharpens the question of which property to relax and how much to relax it.

## Cross-Book Development

[[Halpern Moses - Knowledge and Common Knowledge in a Distributed Environment|Halpern and Moses]] prove that common knowledge is unattainable in any system with unreliable communication. The proof proceeds through the coordinated attack problem: two generals must agree to attack simultaneously, communicating only by messenger through enemy territory. Each message might be lost, so the sender cannot know whether it was received without an acknowledgment, and the acknowledgment might be lost, requiring its own acknowledgment, ad infinitum. No finite chain of messages can establish the infinite mutual awareness that common knowledge requires. This result is not about the unreliability of any particular channel but about the logical structure of knowledge itself — the infinite regress of "I know that you know that I know" cannot be bootstrapped from finite communication. The practical response is to work with weaker epistemic states: epsilon-common knowledge (high probability of mutual awareness) and eventual common knowledge (mutual awareness achieved at some unknown future time).

[[Dwork Lynch Stockmeyer - Consensus in the Presence of Partial Synchrony|Dwork, Lynch, and Stockmeyer]] build on the FLP impossibility result of Fischer, Lynch, and Paterson (1985), which proved that no deterministic protocol can guarantee consensus in an asynchronous system with even one crash fault. The FLP result is devastating in its generality — it holds for any protocol, any number of processors, and the weakest possible fault model (one processor simply stops). DLS's contribution is to show that partial synchrony provides the minimal escape: by assuming that timing bounds exist (even if unknown or delayed), consensus becomes achievable. Their resilience bounds then characterize exactly how much redundancy is needed for each fault type, establishing a second layer of impossibility within the solvable cases — you cannot tolerate more than (N-1)/2 fail-stop faults or more than (N-1)/3 Byzantine faults, no matter what protocol you use.

[[Gilbert Lynch - Brewers Conjecture and the CAP Theorem|Gilbert and Lynch]] prove that no distributed system can simultaneously guarantee consistency (every read returns the most recent write), availability (every request receives a response), and partition tolerance (the system operates despite arbitrary message loss between components). The proof is constructive: they exhibit a specific execution in which a network partition forces a system to choose between returning a stale value (violating consistency) and refusing to respond (violating availability). The CAP theorem is often misunderstood as saying "pick two of three," but the reality is subtler: partition tolerance is not optional in any real network, so the actual choice is between consistency and availability during partitions. The theorem's power lies in making this trade-off explicit and provable rather than leaving it as an engineering judgment call.

## Significance for Interdimensional Semiotics

Impossibility results bound what any semiotic system can guarantee about meaning transfer across dimensional boundaries. The three results in this cluster, taken together, establish a semiotic CAP theorem: no sign system operating across dimensions can simultaneously ensure perfect fidelity of meaning (consistency), continuous availability of interpretation (availability), and tolerance for dimensional boundaries that disrupt communication (partition tolerance). This is not a contingent limitation of current semiotic technology but a structural feature of meaning itself.

The connection to the existing [[Incompleteness]] concept is explicit and deep. Godel's incompleteness theorems are impossibility results about formal systems; the distributed systems impossibility results are about communicating systems. Both reveal that the combination of self-reference, expressiveness, and completeness is logically untenable. In the IS framework, this means that [[The Noosphere]] — as a self-referential semiotic system that models its own meaning-making processes — is necessarily subject to these limits. It cannot simultaneously capture all meaning (completeness), guarantee that captured meaning is accurate (consistency), and remain accessible to all dimensions (availability). The Noosphere's dynamism — its capacity for evolution, reinterpretation, and growth — is a direct consequence of these impossibilities. A semiotic system that could guarantee all three properties would be static, closed, and dead.

For InnateScript, impossibility results inform the design of coordination primitives. The language cannot provide a `join` that is simultaneously safe, live, and partition-tolerant — this is the CAP theorem at the language level. Instead, it must make the trade-off explicit in its type system or operational semantics, allowing the choreographer to specify which property to relax for each coordination point. This is principled language design informed by mathematical certainty about what no language can achieve.

## In the IS Reading List

- [[Halpern Moses - Knowledge and Common Knowledge in a Distributed Environment]] — impossibility of common knowledge with unreliable communication, coordinated attack problem, epistemic limits on coordination
- [[Dwork Lynch Stockmeyer - Consensus in the Presence of Partial Synchrony]] — FLP impossibility as foundation, partial synchrony as minimal escape, tight resilience bounds as secondary impossibility layer
- [[Gilbert Lynch - Brewers Conjecture and the CAP Theorem]] — CAP impossibility proof, constructive partition argument, the real trade-off is consistency vs. availability

## Related

- [[Incompleteness]]
- [[Common Knowledge]]
- [[Consensus]]
- [[Partial Synchrony]]
- [[Paradox]]
- [[Formal System]]
- [[Interdimensional Semiotics]]
