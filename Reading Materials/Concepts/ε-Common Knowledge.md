---
title: "ε-Common Knowledge"
type: "[[Concept]]"
domain: "[[The Commons]]"
Lifestage: "🌱 Seed"
tags:
  - interdimensional-semiotics
  - concept
aliases:
  - Epsilon-Common Knowledge
  - Approximate Common Knowledge
---

ε-Common knowledge is a practical weakening of common knowledge introduced in [[Halpern Moses - Knowledge and Common Knowledge in a Distributed Environment|Halpern and Moses §11]]. Where true common knowledge requires that everyone knows φ, everyone knows that everyone knows φ, and so on to infinite depth with absolute certainty, ε-common knowledge requires only that at each level of the knowledge hierarchy, the probability of knowledge holding is at least 1 - ε. Everyone knows φ with high probability; everyone knows that everyone knows with high probability; the chain continues but each link is probabilistic rather than certain. This relaxation is not merely a mathematical convenience — it represents the boundary between the theoretically impossible and the practically achievable. True common knowledge cannot be attained in systems with any possibility of message loss; ε-common knowledge can be attained whenever communication is reliable with sufficiently high probability.

## Cross-Book Development

Halpern and Moses develop ε-common knowledge as the resolution to the impossibility results that dominate their paper. Having proven that common knowledge is unachievable in asynchronous systems with unreliable communication (the coordinated attack), and that simultaneous coordinated action requires common knowledge, they show that ε-common knowledge is sufficient for approximate coordination. If agents share ε-common knowledge of an attack plan, they can coordinate with failure probability bounded by ε — not perfect, but arbitrarily close to perfect as ε approaches zero. They also introduce the related notion of eventual common knowledge: at some future time, common knowledge will hold, even if the exact time is unknown. This connects directly to [[Dwork Lynch Stockmeyer - Consensus in the Presence of Partial Synchrony|Dwork, Lynch, and Stockmeyer's]] temporal model. Their Global Stabilization Time (GST) is the point after which communication becomes reliable, and consensus becomes achievable — the point after which ε-common knowledge can converge toward true common knowledge. DLS protocols do not require knowing when GST occurs; they guarantee that after it passes, agreement will eventually be reached. The ε in ε-common knowledge maps onto the DLS failure probability: the probability that synchrony has not yet been reached, that the system is still in its partitioned phase. [[Gilbert Lynch - Brewers Conjecture and the CAP Theorem|Gilbert and Lynch's]] Delayed-t consistency model is another instantiation of the same idea — consistency is not atomic but holds within a time bound t, trading the absolute guarantee of linearizability for a probabilistic, temporally bounded approximation.

## Significance for Interdimensional Semiotics

ε-Common knowledge is the realistic model for shared meaning in any semiotic system. No sign system achieves perfect common knowledge of what a sign means — the infinite regress of "I know that you know that I know what this word means" never terminates with certainty in practice. But in a functioning semiotic community, meaning is shared with high enough probability, at sufficient depth of mutual understanding, to enable coordination. When two speakers of the same language use the word "justice," they do not hold identical concepts — but their concepts overlap with probability high enough, and their mutual awareness of this overlap runs deep enough, that productive discourse occurs. The Noosphere operates on ε-common knowledge, not common knowledge. It is a system where meaning converges probabilistically across substrates and agents rather than being fixed atomically. Narrative drift — the gradual divergence of a story's meaning as it passes through retellings, translations, adaptations — is the gap between ε and 1. The smaller the gap, the more stable the meaning; the larger the gap, the more the sign evolves. Semiotic gravitational mass determines how quickly ε approaches zero for a given sign: high-mass signs (archetypes, mathematical truths, deeply embodied metaphors) achieve near-common-knowledge rapidly across communities. Low-mass signs (slang, inside jokes, context-dependent references) may never achieve ε-common knowledge beyond a small group. InnateScript's temporal operators — `until`, `since`, `always` — implicitly work with ε-common knowledge by specifying time bounds within which convergence is expected, not instants at which identity is guaranteed.

## In the IS Reading List

- Halpern/Moses §11: formal definition and properties of ε-common knowledge
- Halpern/Moses §4: the impossibility that motivates the weakening (coordinated attack)
- Halpern/Moses §5-6: knowledge hierarchies and the infinite depth that ε-CK approximates
- DLS §2: GST as the temporal condition under which ε converges toward zero
- Gilbert/Lynch §4: Delayed-t consistency as an applied instance of approximate agreement

## Related

- [[Common Knowledge]]
- [[Coordinated Attack Problem]]
- [[Partial Synchrony]]
- [[Delayed-t Consistency]]
- [[Narrative Drift]]
